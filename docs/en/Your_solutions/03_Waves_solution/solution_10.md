# Section 3 — Problem 10: Superposition of Wave Sources

##  Conceptual Introduction

A point source located at position $\vec{r}_0$ emits circular (or spherical)
waves that spread outward in all directions. The displacement at any
field point $\vec{r}$ due to that single source is:

$$u(\vec{r}, t) = \frac{A}{|\vec{r} - \vec{r}_0|^\alpha}\sin\!\left(k|\vec{r}-\vec{r}_0| - \omega t\right)$$

| Symbol | Meaning |
|--------|---------|
| $|\vec{r} - \vec{r}_0|$ | Distance from the source to the field point |
| $A$ | Source amplitude |
| $\alpha \in [0, 2]$ | Spatial decay exponent — controls how fast amplitude falls with distance |
| $k = 2\pi/\lambda$ | Wavenumber |
| $\omega$ | Angular frequency |

When $\alpha = 0$: amplitude is constant everywhere (plane wave approximation).
When $\alpha = 1$: amplitude falls as $1/r$ (correct for 2D circular waves, e.g. ripples on water).
When $\alpha = 2$: amplitude falls as $1/r^2$ (3D spherical wave intensity law).

When multiple sources are present, the **superposition principle** gives:

$$u_{total}(\vec{r}, t) = \sum_{i} \frac{A}{|\vec{r} - \vec{r}_i|^\alpha}\sin\!\left(k|\vec{r}-\vec{r}_i| - \omega t\right)$$

The resulting pattern of constructive and destructive interference
depends on the positions of the sources, the wavelength, and $\alpha$.

---

## Mathematical Setup for Simulation

### Step 1 — Discretize the field

Divide the simulation canvas into a grid of pixels. Each pixel at position
$(p_x, p_y)$ is a field point $\vec{r}$.

### Step 2 — Precompute distances

For each source at $(s_x, s_y)$, precompute the distance to every pixel:

$$r_i(p_x, p_y) = \sqrt{(p_x - s_x)^2 + (p_y - s_y)^2}$$

This is done once when a source is added, not every frame. The distance
does not change over time — only the time argument $\omega t$ advances.

### Step 3 — Evaluate field at each frame

At time $t$, the field value at pixel $(p_x, p_y)$ is:

$$u(p_x, p_y, t) = \sum_{i=1}^{N} \frac{A}{r_i^{\,\alpha}} \cdot \sin(k\, r_i - \omega t)$$

### Step 4 — Normalize and colorize

Normalize $u$ by its maximum absolute value so the color scale always
uses the full dynamic range regardless of the number of sources:

$$u_{norm} = \frac{u}{\max|u|}$$

Map $u_{norm} \in [-1, 1]$ to a diverging color map
(e.g. blue for positive / crests, red for negative / troughs, black for zero).

### Step 5 — Performance: sin lookup table

Calling `Math.sin()` per pixel per frame is too slow for real-time rendering.
Instead, precompute a table of $N_{LUT}$ sine values:

$$\text{LUT}[i] = \sin\!\left(\frac{2\pi i}{N_{LUT}}\right), \quad i = 0, 1, \ldots, N_{LUT}-1$$

Then approximate $\sin(\theta)$ as:

$$\sin(\theta) \approx \text{LUT}\!\left[\left\lfloor\frac{\theta \cdot N_{LUT}}{2\pi}\right\rfloor \bmod N_{LUT}\right]$$

With $N_{LUT} = 8192$ this gives excellent accuracy at $\sim 5\times$ the
speed of the native function.

---

## HTML Implementation

Save the following as `wave_sources.html` and open in any browser.
Click anywhere on the canvas to place a wave source.
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Wave Sources — Superposition</title>
<style>
  body { font-family: sans-serif; background:#07070e; color:#ccc; padding:12px; }
  .ctrl { background:#0e0e1c; border:1px solid #1a1a2c; border-radius:8px;
          padding:12px; margin-bottom:10px; }
  .row  { display:flex; align-items:center; gap:8px; margin:4px 0; }
  .row label { font-size:11px; color:#777; width:120px; }
  .row span  { font-size:11px; color:#bbb; width:40px; text-align:right; }
  canvas { display:block; border-radius:8px; width:100%; cursor:crosshair; }
  button { background:#161628; border:1px solid #262640; color:#888;
           padding:4px 12px; border-radius:6px; cursor:pointer; font-size:11px; }
  .eq    { font-size:11px; font-family:monospace; color:#555; margin-bottom:8px; }
</style>
</head>
<body>
<h2 style="font-size:14px;font-weight:500;color:#eee;margin-bottom:4px">
  Wave Sources — Interactive Superposition
</h2>
<div class="eq">u(r,t) = Σ A · |r−r₀|⁻ᵅ · sin(k·|r−r₀| − ω·t)</div>

<div class="ctrl">
  <div class="row">
    <label>α (spatial decay)</label>
    <input type="range" id="sa" min="0" max="2" step="0.05" value="0.5" style="flex:1">
    <span id="va">0.50</span>
  </div>
  <div class="row">
    <label>k (wavenumber)</label>
    <input type="range" id="sk" min="0.01" max="0.18" step="0.005" value="0.055" style="flex:1">
    <span id="vk">0.055</span>
  </div>
  <div class="row">
    <label>ω (angular freq.)</label>
    <input type="range" id="sw" min="0.3" max="6" step="0.1" value="2.0" style="flex:1">
    <span id="vw">2.0</span>
  </div>
  <div class="row">
    <label>A (amplitude)</label>
    <input type="range" id="sA" min="0.2" max="5" step="0.1" value="1.5" style="flex:1">
    <span id="vA">1.5</span>
  </div>
  <div style="display:flex;gap:8px;margin-top:8px;align-items:center">
    <button id="clr">Clear Sources</button>
    <button id="pause">Pause</button>
    <span id="cnt" style="font-size:11px;color:#444">Click canvas to add sources</span>
  </div>
</div>

<canvas id="cv"></canvas>
<p style="font-size:10px;color:#333;margin-top:4px">
  Click to place sources. Each source emits circular waves; the canvas shows
  their superposition in real time. White dots mark source positions.
</p>

<script>
const CW=480, CH=300;
const cv=document.getElementById('cv');
cv.width=CW; cv.height=CH;
const ctx=cv.getContext('2d');
const IMG=ctx.createImageData(CW,CH);
const PIX=IMG.data;
const N=CW*CH;
const FIELD=new Float32Array(N);

// Sin lookup table
const LN=8192, SLUT=new Float32Array(LN);
for(let i=0;i<LN;i++) SLUT[i]=Math.sin(2*Math.PI*i/LN);
const LS=LN/(2*Math.PI);
function fs(x){return SLUT[((x*LS)|0)&(LN-1)];}

const sources=[];

function addSrc(sx,sy){
  const d=new Float32Array(N), kd=new Float32Array(N), dec=new Float32Array(N);
  for(let py=0;py<CH;py++)
    for(let px=0;px<CW;px++){
      const dx=px-sx,dy=py-sy;
      d[py*CW+px]=Math.sqrt(dx*dx+dy*dy)+0.5;
    }
  sources.push({x:sx,y:sy,d,kd,dec,ck:-1,ca:-1});
  document.getElementById('cnt').textContent=
    sources.length+' source'+(sources.length>1?'s':'')+' active';
}

function prep(s,k,a){
  if(s.ck!==k){s.ck=k; for(let i=0;i<N;i++) s.kd[i]=k*s.d[i];}
  if(s.ca!==a){s.ca=a; for(let i=0;i<N;i++) s.dec[i]=Math.pow(s.d[i],a);}
}

function clr(v){
  const u=Math.max(-1,Math.min(1,v));
  return u>=0?[8+u*32,10+u*70,18+u*192]:[10-u*190,8-u*22,18-u*30];
}

let t=0,paused=false;

function P(id){return parseFloat(document.getElementById(id).value);}

function frame(){
  if(!paused) t+=0.045;
  const a=P('sa'),k=P('sk'),om=P('sw'),A=P('sA'),ph=om*t;
  FIELD.fill(0);
  for(const s of sources){
    prep(s,k,a);
    for(let i=0;i<N;i++) FIELD[i]+=A/s.dec[i]*fs(s.kd[i]-ph);
  }
  let mx=1e-8;
  for(let i=0;i<N;i++){const a=Math.abs(FIELD[i]);if(a>mx)mx=a;}
  const inv=1/mx;
  for(let i=0;i<N;i++){
    const [r,g,b]=clr(FIELD[i]*inv), p=i<<2;
    PIX[p]=r;PIX[p+1]=g;PIX[p+2]=b;PIX[p+3]=255;
  }
  ctx.putImageData(IMG,0,0);
  for(const s of sources){
    ctx.beginPath();ctx.arc(s.x,s.y,4,0,6.283);
    ctx.fillStyle='rgba(255,255,255,0.9)';ctx.fill();
  }
  requestAnimationFrame(frame);
}

cv.addEventListener('click',e=>{
  const r=cv.getBoundingClientRect();
  addSrc(Math.round((e.clientX-r.left)*CW/r.width),
         Math.round((e.clientY-r.top)*CH/r.height));
});
document.getElementById('clr').onclick=()=>{
  sources.length=0;FIELD.fill(0);
  document.getElementById('cnt').textContent='Click canvas to add sources';
};
document.getElementById('pause').onclick=function(){
  paused=!paused;this.textContent=paused?'Resume':'Pause';
};
[['sa','va',v=>v.toFixed(2)],['sk','vk',v=>v.toFixed(3)],
 ['sw','vw',v=>v.toFixed(1)],['sA','vA',v=>v.toFixed(1)]]
.forEach(([s,v,f])=>document.getElementById(s).addEventListener('input',()=>
  document.getElementById(v).textContent=f(+document.getElementById(s).value)));

frame();
</script>
</body>
</html>
```

---

## Key Physics to Observe

| $\alpha$ value | Amplitude behaviour | Pattern type |
|----------------|---------------------|--------------|
| $\alpha = 0$ | Constant everywhere | Uniform amplitude interference |
| $\alpha = 1$ | Falls as $1/r$ | 2D circular wave (water ripple) |
| $\alpha = 2$ | Falls as $1/r^2$ | 3D spherical wave cross-section |

With two sources, concentric rings of constructive interference (bright bands)
and destructive interference (dark bands) appear — this is the same physics
as Young's double-slit experiment. With more sources arranged in a line,
a **phased array** pattern emerges — the basis of radar, sonar, and 5G antennas.

---

##  Common Mistakes

- ❌ **Dividing by zero at the source position** — always add a small offset
  (e.g. $+0.5$) to distances to avoid `Infinity` values at $r = 0$
- ❌ **Recomputing distances every frame** — distances are fixed by geometry;
  only the phase $\omega t$ changes each frame. Precompute and cache.
- ❌ **Not normalizing the field before colorizing** — without normalization,
  adding more sources makes all previous colors saturate and the pattern
  becomes unreadable
