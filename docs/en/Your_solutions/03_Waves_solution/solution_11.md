# Section 3 — Problem 11: Young's Two-Slit Interference

##  Conceptual Introduction

Young's double-slit experiment (1801) was the first convincing demonstration
that light behaves as a wave. Two narrow slits act as **coherent point sources**
— they emit waves with a fixed phase relationship (here, in phase).

The total displacement at any field point $\vec{r}$ is the **sum of the two
partial waves**:

$$u(\vec{r}, t) = \frac{A}{|\vec{r}-\vec{r}_1|}\sin\!\left(k|\vec{r}-\vec{r}_1| - \omega t\right) + \frac{A}{|\vec{r}-\vec{r}_2|}\sin\!\left(k|\vec{r}-\vec{r}_2| - \omega t\right)$$

where $\vec{r}_1$ and $\vec{r}_2$ are the positions of the two slits.

| Symbol | Meaning |
|--------|---------|
| $d = |\vec{r}_1 - \vec{r}_2|$ | Slit separation |
| $\lambda = 2\pi/k$ | Wavelength |
| $A$ | Amplitude of each source |
| $r_1, r_2$ | Distances from slits 1 and 2 to field point |

---

## The Interference Condition

At a distant screen, the path difference between the two waves determines
whether interference is constructive or destructive:

**Path difference:** $\Delta r = r_1 - r_2 \approx d\sin\theta$
(for a screen far from the slits, small angle approximation)

**Constructive interference** (bright fringe):

$$\Delta r = n\lambda, \quad n = 0, \pm1, \pm2, \ldots$$

$$\Rightarrow d\sin\theta_n = n\lambda \Rightarrow \theta_n = \arcsin\!\left(\frac{n\lambda}{d}\right)$$

**Destructive interference** (dark fringe):

$$\Delta r = \left(n + \frac{1}{2}\right)\lambda$$

The **fringe spacing** on a screen at distance $L$:

$$\Delta y = \frac{\lambda L}{d}$$

Increasing $\lambda$ (longer wavelength) widens the fringes.
Increasing $d$ (wider slit separation) narrows them.

---

## Mathematical Setup for Simulation

### Step 1 — Slit positions

Place both slits at $x = 0$ (left edge of canvas), symmetrically about the
centre:

$$\vec{r}_1 = (0,\; H/2 - d/2), \qquad \vec{r}_2 = (0,\; H/2 + d/2)$$

where $H$ is the canvas height and $d$ is the slit separation.

### Step 2 — Precompute distances

For every pixel $(p_x, p_y)$:

$$r_1 = \sqrt{p_x^2 + (p_y - y_1)^2} + \varepsilon, \qquad r_2 = \sqrt{p_x^2 + (p_y - y_2)^2} + \varepsilon$$

($\varepsilon = 0.5$ to prevent division by zero at the slit positions.)

These are recomputed only when $d$ changes.

### Step 3 — Field at each frame

$$u(p_x, p_y, t) = \frac{A}{r_1}\sin(kr_1 - \omega t) + \frac{A}{r_2}\sin(kr_2 - \omega t)$$

### Step 4 — Time-averaged intensity

The instantaneous field oscillates too quickly to see the fringe pattern clearly.
The **time-averaged intensity** at each point is:

$$I \propto \langle u^2 \rangle$$

In practice, update a running average using an exponential moving average (EMA):

$$I_{n+1} = (1-\alpha_{\text{EMA}})\,I_n + \alpha_{\text{EMA}}\,u^2$$

With $\alpha_{\text{EMA}} \approx 0.05$, the intensity profile builds up over
roughly 20 frames, showing the steady-state fringe pattern.

---

## HTML Implementation

Save the following as `two_slit.html` and open in any browser.
Use the sliders to change slit separation and wavelength in real time.
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Two-Slit Interference</title>
<style>
  body { font-family:sans-serif; background:#07070e; color:#ccc; padding:12px; }
  .ctrl{ background:#0e0e1c; border:1px solid #1a1a2c; border-radius:8px;
         padding:12px; margin-bottom:10px; }
  .row { display:flex; align-items:center; gap:8px; margin:4px 0; }
  .row label{ font-size:11px; color:#777; width:120px; }
  .row span { font-size:11px; color:#bbb; width:50px; text-align:right; }
  canvas{ display:block; border-radius:8px; width:100%; }
  button{ background:#161628; border:1px solid #262640; color:#888;
          padding:4px 12px; border-radius:6px; cursor:pointer; font-size:11px; }
  .eq   { font-size:11px; font-family:monospace; color:#555; margin-bottom:8px; }
  #meta { font-size:11px; color:#444; margin-top:8px; display:flex;
          flex-wrap:wrap; gap:12px; }
</style>
</head>
<body>
<h2 style="font-size:14px;font-weight:500;color:#eee;margin-bottom:4px">
  Young's Double-Slit Interference
</h2>
<div class="eq">u = A·sin(k·r₁−ωt)/r₁ + A·sin(k·r₂−ωt)/r₂</div>

<div class="ctrl">
  <div class="row">
    <label>Slit sep. d</label>
    <input type="range" id="sd" min="10" max="160" step="1" value="60" style="flex:1">
    <span id="vd">60 px</span>
  </div>
  <div class="row">
    <label>Wavelength λ</label>
    <input type="range" id="sl" min="20" max="120" step="1" value="50" style="flex:1">
    <span id="vl">50 px</span>
  </div>
  <div class="row">
    <label>ω (speed)</label>
    <input type="range" id="sw" min="0.3" max="6" step="0.1" value="2" style="flex:1">
    <span id="vw">2.0</span>
  </div>
  <div style="margin-top:8px;display:flex;gap:8px">
    <button id="pause">Pause</button>
  </div>
  <div id="meta"></div>
</div>

<canvas id="cv" height="360"></canvas>
<canvas id="ci" height="44" style="margin-top:4px"></canvas>
<p style="font-size:10px;color:#333;margin-top:3px">
  ↑ Wave field (blue = crest, red = trough) &nbsp;|&nbsp;
  ↓ Time-averaged intensity at screen
</p>

<script>
const CW=540,CH=360;
const cv=document.getElementById('cv'); cv.width=CW; cv.height=CH;
const ctx=cv.getContext('2d');
const IMG=ctx.createImageData(CW,CH); const PIX=IMG.data;
const ci=document.getElementById('ci'); ci.width=CW; ci.height=44;
const cti=ci.getContext('2d');
const N=CW*CH;
const r1a=new Float32Array(N),r2a=new Float32Array(N);
const kr1=new Float32Array(N),kr2=new Float32Array(N);
const FLD=new Float32Array(N);
const INT=new Float32Array(CH);   // intensity profile

// LUT
const LN=8192,SL=new Float32Array(LN);
for(let i=0;i<LN;i++) SL[i]=Math.sin(2*Math.PI*i/LN);
const LS=LN/(2*Math.PI);
function fs(x){return SL[((x*LS)|0)&(LN-1)];}

let cD=-1,cK=-1,t=0,paused=false;

function preD(d){
  const y1=CH/2-d/2, y2=CH/2+d/2;
  for(let py=0;py<CH;py++)
    for(let px=0;px<CW;px++){
      const i=py*CW+px;
      r1a[i]=Math.sqrt(px*px+(py-y1)**2)+0.5;
      r2a[i]=Math.sqrt(px*px+(py-y2)**2)+0.5;
    }
  cD=d;
}

function preK(k){
  for(let i=0;i<N;i++){kr1[i]=k*r1a[i];kr2[i]=k*r2a[i];}
  cK=k;
}

function P(id){return parseFloat(document.getElementById(id).value);}

function updateMeta(d,lam,k){
  const ratio=lam/d;
  const t1=ratio<=1?`${(Math.asin(ratio)*180/Math.PI).toFixed(1)}°`:'N/A';
  document.getElementById('meta').innerHTML=
    `<span>λ/d = ${ratio.toFixed(2)}</span>` +
    `<span>k = ${k.toFixed(4)} px⁻¹</span>` +
    `<span>1st fringe: θ₁ ≈ ${t1}</span>` +
    (d<lam?`<span style="color:#a04040">⚠ d < λ — no fringes</span>`:'');
}

function colorize(v){
  const u=Math.max(-1,Math.min(1,v));
  return u>=0?[8+u*32,10+u*70,18+u*192]:[10-u*190,8-u*22,18-u*30];
}

function frame(){
  if(!paused) t+=0.04;
  const d=P('sd'),lam=P('sl'),k=2*Math.PI/lam,om=P('sw'),A=2;
  if(d!==cD) preD(d);
  if(k!==cK) preK(k);
  const ph=om*t;
  for(let i=0;i<N;i++)
    FLD[i]=A/r1a[i]*fs(kr1[i]-ph)+A/r2a[i]*fs(kr2[i]-ph);
  let mx=1e-8;
  for(let i=0;i<N;i++){const a=Math.abs(FLD[i]);if(a>mx)mx=a;}
  const inv=1/mx;
  for(let i=0;i<N;i++){
    const [r,g,b]=colorize(FLD[i]*inv),p=i<<2;
    PIX[p]=r;PIX[p+1]=g;PIX[p+2]=b;PIX[p+3]=255;
  }
  ctx.putImageData(IMG,0,0);
  // Draw slits
  const y1=CH/2-d/2, y2=CH/2+d/2;
  [[y1,'S₁'],[y2,'S₂']].forEach(([y,l])=>{
    ctx.fillStyle='#fff';ctx.fillRect(0,y-3,5,6);
    ctx.fillStyle='rgba(255,255,255,0.4)';
    ctx.font='10px sans-serif';ctx.fillText(l,7,y+4);
  });
  // Update intensity profile (EMA)
  for(let y=0;y<CH;y++){
    const u=FLD[y*CW+(CW-1)];
    INT[y]=INT[y]*0.95+(u*u)*0.05;
  }
  // Draw intensity
  cti.fillStyle='#0c0c18';cti.fillRect(0,0,CW,44);
  const mx2=Math.max(...INT)+1e-8;
  cti.beginPath();cti.strokeStyle='#5090d0';cti.lineWidth=1.5;
  for(let y=0;y<CH;y++){
    const xp=(INT[y]/mx2)*(CW-4)+2, yp=y*44/CH;
    y===0?cti.moveTo(xp,yp):cti.lineTo(xp,yp);
  }
  cti.stroke();
  cti.fillStyle='#333';cti.font='9px sans-serif';
  cti.fillText('Intensity →',4,10);
  updateMeta(d,lam,k);
  requestAnimationFrame(frame);
}

document.getElementById('pause').onclick=function(){
  paused=!paused;this.textContent=paused?'Resume':'Pause';
};
[['sd','vd',v=>Math.round(v)+' px'],
 ['sl','vl',v=>Math.round(v)+' px'],
 ['sw','vw',v=>parseFloat(v).toFixed(1)]]
.forEach(([s,v,f])=>document.getElementById(s).addEventListener('input',()=>{
  document.getElementById(v).textContent=f(document.getElementById(s).value);
  cD=-1;cK=-1;INT.fill(0);
}));

preD(60);preK(2*Math.PI/50);
frame();
</script>
</body>
</html>
```

---

## Key Physics to Observe in the Simulation

| Action | What you see | Why |
|--------|-------------|-----|
| Increase $\lambda$ (larger wavelength) | Fringe spacing **widens** | $\Delta y = \lambda L/d$ — spacing proportional to $\lambda$ |
| Increase $d$ (wider slits) | Fringe spacing **narrows** | More slits per wavelength → tighter pattern |
| Set $d < \lambda$ | Fringes **disappear** | Path difference cannot reach $\lambda$ — constructive condition never met |
| Add more wavelengths | More fringes across screen | Higher-order maxima become visible |

---

## Analytical Fringe Positions

For a screen at distance $L$ from the slits, the $n$-th bright fringe
appears at:

$$y_n = \frac{n\lambda L}{d}, \quad n = 0, \pm1, \pm2, \ldots$$

The central fringe ($n = 0$) always falls on the axis of symmetry regardless
of $\lambda$ or $d$.

The intensity envelope at the screen (ignoring single-slit diffraction) is:

$$I(\theta) = 4A^2\cos^2\!\left(\frac{\pi d \sin\theta}{\lambda}\right)$$

Maximum intensity $4A^2$ occurs at constructive interference — exactly
four times the single-source intensity $A^2$, not twice. This is because
amplitude doubles at a constructive point, and intensity scales as amplitude squared.

---

##  Common Mistakes

- ❌ **Using $I = 2A^2$ for constructive interference** — amplitude doubles
  ($2A$), so intensity is $(2A)^2 = 4A^2$, not $2A^2$
- ❌ **Forgetting the $1/r$ amplitude factor** — each partial wave decays with
  distance; the two sources don't contribute equal amplitudes unless the
  field point is equidistant from both slits
- ❌ **Confusing path difference with phase difference** — path difference
  $\Delta r$ and phase difference $\Delta\phi = k\Delta r = 2\pi\Delta r/\lambda$
  are related by the factor $k$. Constructive interference occurs when
  $\Delta\phi = 2\pi n$, which is equivalent to $\Delta r = n\lambda$
