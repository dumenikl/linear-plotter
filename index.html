<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Koordinaten-Plotter</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Atkinson+Hyperlegible:wght@400;700&family=JetBrains+Mono:wght@400;600&display=swap">
<style>
:root{
  --paper:#F5F8FA; --panel:#FFFFFF; --ink:#16202B; --muted:#5B6B7B; --line:#DCE4EB;
  --grid-major:#C3D1DD; --grid-minor:#E4EBF1; --axis:#2A3643; --canvas:#FBFCFD;
  --pt:#C8372D; --pt-soft:rgba(200,55,45,.12);
  --f1:#1F5FBF; --f2:#0E8A5F; --f3:#8A4FBF; --f4:#B86E00;
  --focus:#1F5FBF; --btn:#EEF3F7; --btn-hover:#E1E9F0;
  --sans:"Atkinson Hyperlegible",system-ui,-apple-system,"Segoe UI",sans-serif;
  --mono:"JetBrains Mono",ui-monospace,"SFMono-Regular",Menlo,Consolas,monospace;
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    color-scheme:dark;
    --paper:#0F151C; --panel:#161F29; --ink:#E4EAF0; --muted:#93A3B3; --line:#26323F;
    --grid-major:#2D3B4A; --grid-minor:#1B2530; --axis:#C9D4DE; --canvas:#121A22;
    --pt:#FF7A6B; --pt-soft:rgba(255,122,107,.16);
    --f1:#6FA2FF; --f2:#3FC99A; --f3:#C39BFF; --f4:#F2B24B;
    --focus:#6FA2FF; --btn:#1F2A36; --btn-hover:#283645;
  }
}
:root[data-theme="dark"]{
  color-scheme:dark;
  --paper:#0F151C; --panel:#161F29; --ink:#E4EAF0; --muted:#93A3B3; --line:#26323F;
  --grid-major:#2D3B4A; --grid-minor:#1B2530; --axis:#C9D4DE; --canvas:#121A22;
  --pt:#FF7A6B; --pt-soft:rgba(255,122,107,.16);
  --f1:#6FA2FF; --f2:#3FC99A; --f3:#C39BFF; --f4:#F2B24B;
  --focus:#6FA2FF; --btn:#1F2A36; --btn-hover:#283645;
}
html,body{height:100%}
body{background:var(--paper);color:var(--ink);font-family:var(--sans);font-size:15px;line-height:1.45}
*{box-sizing:border-box}
.app{display:grid;grid-template-columns:340px 1fr;height:100%;min-height:0}
aside{background:var(--panel);border-right:1px solid var(--line);overflow-y:auto;padding:18px 18px 28px;display:flex;flex-direction:column;gap:22px}
h1{font-size:20px;margin:0;letter-spacing:-.01em}
.sub{margin:2px 0 0;color:var(--muted);font-size:13px}
section{display:flex;flex-direction:column;gap:10px}
h2{margin:0;font-size:11.5px;text-transform:uppercase;letter-spacing:.09em;color:var(--muted);font-weight:700;display:flex;justify-content:space-between;align-items:center}
h2 .count{font-family:var(--mono);letter-spacing:0;text-transform:none;font-weight:400}
input[type=text],input[type=number]{font:inherit;font-family:var(--mono);font-size:14px;color:var(--ink);background:var(--paper);border:1px solid var(--line);border-radius:6px;padding:7px 9px;width:100%;min-width:0}
input:focus-visible,button:focus-visible,select:focus-visible{outline:2px solid var(--focus);outline-offset:1px}
input[type=number]{-moz-appearance:textfield}
input::-webkit-outer-spin-button,input::-webkit-inner-spin-button{-webkit-appearance:none;margin:0}
button,select{font:inherit;font-size:14px;color:var(--ink);background:var(--btn);border:1px solid var(--line);border-radius:6px;padding:7px 11px;cursor:pointer}
button:hover{background:var(--btn-hover)}
button.primary{background:var(--ink);color:var(--panel);border-color:var(--ink);font-weight:700}
button.primary:hover{opacity:.9;background:var(--ink)}
button.ghost{background:transparent;border-color:transparent;color:var(--muted);padding:4px 6px}
button.ghost:hover{color:var(--ink);background:var(--btn)}
.row{display:flex;gap:8px;align-items:center}
.row.wrap{flex-wrap:wrap}
.addpt{display:grid;grid-template-columns:1fr 1fr auto;gap:8px}
.addpt label{position:relative}
.addpt label span{position:absolute;left:9px;top:50%;transform:translateY(-50%);font-family:var(--mono);color:var(--muted);font-size:13px;pointer-events:none}
.addpt label input{padding-left:30px}
table{width:100%;border-collapse:collapse;font-family:var(--mono);font-size:13.5px;font-variant-numeric:tabular-nums}
.tablewrap{max-height:240px;overflow-y:auto;border:1px solid var(--line);border-radius:8px}
th{position:sticky;top:0;background:var(--panel);text-align:left;font-weight:600;color:var(--muted);font-size:12px;padding:6px 8px;border-bottom:1px solid var(--line)}
td{padding:3px 4px;border-bottom:1px solid var(--line)}
tr:last-child td{border-bottom:0}
td.name{color:var(--pt);font-weight:600;padding-left:8px;width:42px}
td input[type=text]{border-color:transparent;background:transparent;padding:4px 6px}
td input[type=text]:hover{border-color:var(--line)}
td.del{width:30px;text-align:right}
.empty{padding:14px;color:var(--muted);font-family:var(--sans);font-size:13px;text-align:center}
.toggle{display:flex;align-items:center;gap:10px;cursor:pointer;user-select:none}
.toggle input{position:absolute;opacity:0;width:1px;height:1px}
.toggle .sw{width:36px;height:20px;border-radius:10px;background:var(--line);position:relative;flex:none;transition:background .15s}
.toggle .sw::after{content:"";position:absolute;left:2px;top:2px;width:16px;height:16px;border-radius:50%;background:var(--panel);box-shadow:0 1px 2px rgba(0,0,0,.25);transition:transform .15s}
.toggle input:checked + .sw{background:var(--pt)}
.toggle input:checked + .sw::after{transform:translateX(16px)}
.toggle input:focus-visible + .sw{outline:2px solid var(--focus);outline-offset:2px}
.toggle.blue input:checked + .sw{background:var(--focus)}
.sub-opt{padding-left:46px;display:flex;gap:8px;align-items:center;color:var(--muted);font-size:13px}
.sub-opt select{padding:4px 8px;font-size:13px}
.fn-form{display:flex;gap:8px}
.fn-list{display:flex;flex-direction:column;gap:6px;margin:0;padding:0;list-style:none}
.fn-list li{display:grid;grid-template-columns:auto auto 1fr auto;align-items:center;gap:8px;padding:6px 6px 6px 8px;border:1px solid var(--line);border-radius:8px}
.fn-list .swatch{width:14px;height:3px;border-radius:2px}
.fn-list .expr{font-family:var(--mono);font-size:13.5px;overflow-wrap:anywhere}
.fn-list .meta{grid-column:3/4;font-size:12px;color:var(--muted);font-family:var(--mono)}
.fn-list input[type=checkbox]{margin:0;accent-color:var(--focus)}
.hint{font-size:12.5px;color:var(--muted);margin:0}
.hint code{font-family:var(--mono);font-size:12px;background:var(--btn);padding:1px 4px;border-radius:4px}
.err{color:var(--pt);font-size:13px;margin:0}
.zoomrow{display:grid;grid-template-columns:62px 1fr 92px;gap:8px;align-items:center;font-size:13px;color:var(--muted)}
.zoomrow output{font-family:var(--mono);font-size:12px;text-align:right;color:var(--ink)}
input[type=range]{width:100%;accent-color:var(--ink)}
.stage{position:relative;min-width:0;min-height:0;background:var(--canvas)}
canvas{display:block;width:100%;height:100%;touch-action:none;cursor:crosshair}
canvas.grab{cursor:grab} canvas.grabbing{cursor:grabbing}
.hud{position:absolute;right:12px;top:12px;display:flex;gap:6px;flex-direction:column}
.hud button{width:38px;height:38px;padding:0;font-size:18px;background:var(--panel);box-shadow:0 1px 3px rgba(0,0,0,.08)}
.hud button.txt{font-size:11px;font-weight:700;letter-spacing:.04em}
.coord{position:absolute;left:12px;bottom:12px;font-family:var(--mono);font-size:12.5px;background:var(--panel);border:1px solid var(--line);border-radius:6px;padding:4px 8px;color:var(--muted);font-variant-numeric:tabular-nums;pointer-events:none}
.coord b{color:var(--ink);font-weight:600}
@media (max-width:760px){
  .app{grid-template-columns:1fr;grid-template-rows:62vh auto;height:auto}
  .stage{order:-1;height:62vh}
  aside{border-right:0;border-top:1px solid var(--line);overflow:visible;padding-inline:16px}
}
@media (prefers-reduced-motion:reduce){*{transition:none!important}}
</style>
<style>body{margin:0}[hidden]{display:none!important}</style>
</head>
<body>

<div class="app">
  <aside>
    <header>
      <h1>Koordinaten-Plotter</h1>
    </header>

    <section aria-labelledby="h-pts">
      <h2 id="h-pts">Wertepaare <span class="count" id="ptCount"></span></h2>
      <form class="addpt" id="ptForm" autocomplete="off">
        <label><span>x</span><input id="inX" type="text" inputmode="decimal" placeholder="0" aria-label="x-Wert"></label>
        <label><span>y</span><input id="inY" type="text" inputmode="decimal" placeholder="0" aria-label="y-Wert"></label>
        <button class="primary" type="submit">Hinzufügen</button>
      </form>
      <p class="err" id="ptErr" hidden></p>
      <div class="tablewrap">
        <table>
          <thead><tr><th></th><th>x</th><th>y</th><th></th></tr></thead>
          <tbody id="ptBody"></tbody>
        </table>
      </div>
      <div class="row wrap">
        <button type="button" id="btnFit">Auf Punkte zoomen</button>
        <button type="button" id="btnClear">Alle löschen</button>
        <button type="button" id="btnClearConfirm" hidden>Ja, alle Punkte löschen</button>
      </div>
    </section>

    <section aria-labelledby="h-disp">
      <h2 id="h-disp">Darstellung</h2>
      <label class="toggle"><input type="checkbox" id="optConnect" checked><span class="sw"></span>Punkte verbinden</label>
      <div class="sub-opt" id="orderWrap"><label for="optOrder">Reihenfolge:</label>
        <select id="optOrder"><option value="x">nach x sortiert</option><option value="entry">wie eingegeben</option></select>
      </div>
      <label class="toggle"><input type="checkbox" id="optLabels" checked><span class="sw"></span>Punkte beschriften</label>
      <label class="toggle blue"><input type="checkbox" id="optClickAdd" checked><span class="sw"></span>Klick ins Gitter setzt Punkt</label>
      <label class="toggle blue"><input type="checkbox" id="optSnap" checked><span class="sw"></span>Am Raster einrasten</label>
    </section>

    <section aria-labelledby="h-fn">
      <h2 id="h-fn">Funktionen</h2>
      <form class="fn-form" id="fnForm" autocomplete="off">
        <input id="inFn" type="text" placeholder="y = 0,5x - 1" aria-label="Funktionsterm">
        <button class="primary" type="submit">Zeichnen</button>
      </form>
      <p class="err" id="fnErr" hidden></p>
      <ul class="fn-list" id="fnList"></ul>
    </section>

    <section aria-labelledby="h-zoom">
      <h2 id="h-zoom">Zoom</h2>
      <label class="toggle blue"><input type="checkbox" id="optLock" checked><span class="sw"></span>Gleiche Skalierung beider Achsen</label>
      <div class="zoomrow"><label for="zx" id="zxLabel">Beide</label><input type="range" id="zx" min="-6" max="7" step="0.01" value="0"><output id="zxOut"></output></div>
      <div class="zoomrow" id="zyRow" hidden><label for="zy">y-Achse</label><input type="range" id="zy" min="-6" max="7" step="0.01" value="0"><output id="zyOut"></output></div>
      <div class="row wrap">
        <button type="button" id="btnReset">Ansicht zurücksetzen</button>
      </div>
    </section>
  </aside>

  <div class="stage" id="stage">
    <canvas id="cv" aria-label="Koordinatensystem"></canvas>
    <div class="hud">
      <button type="button" id="zin" aria-label="Vergrößern">+</button>
      <button type="button" id="zout" aria-label="Verkleinern">−</button>
      <button type="button" class="txt" id="zhome" aria-label="Ansicht zurücksetzen">0|0</button>
    </div>
    <div class="coord" id="coord">x <b>–</b> · y <b>–</b></div>
  </div>
</div>

<script>
(() => {
const BASE = 40; // px per unit at zoom 0
const $ = id => document.getElementById(id);
const cv = $('cv'), ctx = cv.getContext('2d'), stage = $('stage');

// ---------- state (example data) ----------
let points = [
  {x:-4,y:-2.5},{x:-2,y:-1.5},{x:1,y:-0.5},{x:3,y:0.5},{x:5,y:2}
];
let fns = [];
let view = {cx:0, cy:0, zx:0, zy:0};
const opt = {connect:true, order:'x', labels:true, clickAdd:true, snap:true, lock:true};
let hoverIdx = -1, mouseWorld = null;

const sx = () => BASE * Math.pow(2, view.zx);
const sy = () => BASE * Math.pow(2, opt.lock ? view.zx : view.zy);
let W = 0, H = 0, dpr = 1;
const toPx = x => W/2 + (x - view.cx) * sx();
const toPy = y => H/2 - (y - view.cy) * sy();
const toWx = px => (px - W/2) / sx() + view.cx;
const toWy = py => -(py - H/2) / sy() + view.cy;

// ---------- number helpers ----------
const parseNum = s => {
  s = String(s).trim().replace(',', '.');
  if (s === '' ) return NaN;
  if (/^[-+]?\d+(\.\d+)?\s*\/\s*[-+]?\d+(\.\d+)?$/.test(s)) { const [a,b] = s.split('/').map(Number); return a/b; }
  return /^[-+]?(\d+\.?\d*|\.\d+)(e[-+]?\d+)?$/i.test(s) ? Number(s) : NaN;
};
const fmt = (v, d = 4) => {
  if (!isFinite(v)) return '–';
  const r = Math.round(v * 10**d) / 10**d;
  return (Object.is(r,-0) ? 0 : r).toString().replace('.', ',');
};
function niceStep(raw){
  const e = Math.floor(Math.log10(raw)), f = raw / 10**e;
  const m = f <= 1 ? 1 : f <= 2 ? 2 : f <= 5 ? 5 : 10;
  return {step: m * 10**e, mant: m === 10 ? 1 : m};
}
const stepFor = s => niceStep(55 / s);
const minorOf = ({step, mant}) => step / (mant === 2 ? 4 : 5);
function fmtTick(v, step){
  const dec = Math.max(0, -Math.floor(Math.log10(step) + 1e-9));
  return fmt(Number(v.toFixed(Math.min(dec, 10))), 10);
}

// ---------- function parser ----------
function compile(src){
  let s = src.trim().replace(/^\s*(y|[a-z]\s*\(\s*x\s*\))\s*=\s*/i, '').replace(/,/g, '.').replace(/·|×/g, '*').replace(/−/g, '-');
  if (!s) throw new Error('Bitte einen Term eingeben, z. B. 2x + 1');
  const toks = []; let i = 0;
  while (i < s.length){
    const c = s[i];
    if (/\s/.test(c)) { i++; continue; }
    const num = s.slice(i).match(/^(\d+\.?\d*|\.\d+)/);
    if (num){ toks.push({t:'n', v:parseFloat(num[0])}); i += num[0].length; continue; }
    if (c === 'x' || c === 'X'){ toks.push({t:'x'}); i++; continue; }
    if ('+-*/^()'.includes(c)){ toks.push({t:c}); i++; continue; }
    throw new Error(`Unbekanntes Zeichen „${c}“.`);
  }
  let p = 0;
  const peek = () => toks[p], eat = t => { if (peek() && peek().t === t){ p++; return true; } return false; };
  const startsPrimary = tk => tk && (tk.t === 'n' || tk.t === 'x' || tk.t === '(');
  function expr(){ let a = term();
    for(;;){ if (eat('+')){ const l=a, r=term(); a = x => l(x)+r(x); } else if (eat('-')){ const l=a, r=term(); a = x => l(x)-r(x); } else return a; } }
  function term(){ let a = unary();
    for(;;){
      if (eat('*')){ const l=a, r=unary(); a = x => l(x)*r(x); }
      else if (eat('/')){ const l=a, r=unary(); a = x => l(x)/r(x); }
      else if (startsPrimary(peek())){ const l=a, r=power(); a = x => l(x)*r(x); }
      else return a; } }
  function unary(){ if (eat('-')){ const a = unary(); return x => -a(x); } if (eat('+')) return unary(); return power(); }
  function power(){ const b = primary(); if (eat('^')){ const e = unary(); return x => Math.pow(b(x), e(x)); } return b; }
  function primary(){
    const tk = peek();
    if (!tk) throw new Error('Der Term ist unvollständig.');
    if (tk.t === 'n'){ p++; const v = tk.v; return () => v; }
    if (tk.t === 'x'){ p++; return x => x; }
    if (eat('(')){ const a = expr(); if (!eat(')')) throw new Error('Es fehlt eine schließende Klammer.'); return a; }
    throw new Error(`Unerwartetes Zeichen „${tk.t}“.`);
  }
  const f = expr();
  if (p < toks.length) throw new Error(`Unerwartetes Zeichen „${toks[p].t}“.`);
  return {f, clean: s};
}
function linearInfo(f){
  const a = f(0), b = f(1), c = f(2), d = f(-3.7), e = f(5.3);
  const m = b - a;
  const ok = [a,b,c,d,e].every(isFinite) && [[c,2],[d,-3.7],[e,5.3]].every(([v,x]) => Math.abs(v - (a + m*x)) < 1e-9 * (1 + Math.abs(v)));
  return ok ? {m, b:a} : null;
}

// ---------- drawing ----------
function tok(name){ return getComputedStyle(document.documentElement).getPropertyValue(name).trim(); }
const FN_COLORS = ['--f1','--f2','--f3','--f4'];

function resize(){
  const r = stage.getBoundingClientRect();
  dpr = window.devicePixelRatio || 1;
  W = r.width; H = r.height;
  cv.width = Math.round(W * dpr); cv.height = Math.round(H * dpr);
  draw();
}

function drawGrid(C){
  const SX = sx(), SY = sy();
  const gx = stepFor(SX), gy = stepFor(SY);
  const x0 = toWx(0), x1 = toWx(W), y0 = toWy(H), y1 = toWy(0);
  const lines = (step, color, width) => {
    ctx.strokeStyle = color; ctx.lineWidth = width; ctx.beginPath();
    const sxp = step.x, syp = step.y;
    for (let x = Math.ceil(x0/sxp)*sxp; x <= x1; x += sxp){ const p = Math.round(toPx(x)) + .5; ctx.moveTo(p,0); ctx.lineTo(p,H); }
    for (let y = Math.ceil(y0/syp)*syp; y <= y1; y += syp){ const p = Math.round(toPy(y)) + .5; ctx.moveTo(0,p); ctx.lineTo(W,p); }
    ctx.stroke();
  };
  lines({x:minorOf(gx), y:minorOf(gy)}, C.minor, 1);
  lines({x:gx.step, y:gy.step}, C.major, 1);

  // axes
  const ax = Math.round(toPy(0)) + .5, ay = Math.round(toPx(0)) + .5;
  ctx.strokeStyle = C.axis; ctx.lineWidth = 1.5; ctx.beginPath();
  if (ax >= 0 && ax <= H){ ctx.moveTo(0,ax); ctx.lineTo(W,ax); }
  if (ay >= 0 && ay <= W){ ctx.moveTo(ay,0); ctx.lineTo(ay,H); }
  ctx.stroke();
  // arrowheads + axis names
  ctx.fillStyle = C.axis; ctx.font = `600 13px ${tok('--mono')}`;
  if (ax >= 0 && ax <= H){
    ctx.beginPath(); ctx.moveTo(W-2,ax); ctx.lineTo(W-11,ax-5); ctx.lineTo(W-11,ax+5); ctx.fill();
    ctx.textAlign='right'; ctx.textBaseline='bottom'; ctx.fillText('x', W-8, ax-7);
  }
  if (ay >= 0 && ay <= W){
    ctx.beginPath(); ctx.moveTo(ay,2); ctx.lineTo(ay-5,11); ctx.lineTo(ay+5,11); ctx.fill();
    ctx.textAlign='left'; ctx.textBaseline='top'; ctx.fillText('y', ay+9, 4);
  }

  // tick labels (clamped to edges when axis is off-screen)
  ctx.font = `12px ${tok('--mono')}`; ctx.fillStyle = C.muted;
  const labY = Math.min(Math.max(ax + 5, 4), H - 18);
  ctx.textAlign = 'center'; ctx.textBaseline = 'top';
  for (let x = Math.ceil(x0/gx.step)*gx.step; x <= x1; x += gx.step){
    if (Math.abs(x) < gx.step/2) continue;
    const p = toPx(x); if (p < 14 || p > W - 24) continue;
    const t = fmtTick(x, gx.step);
    labelBg(C, p, labY, t, 'center', 'top');
  }
  const labX = Math.min(Math.max(ay - 6, 40), W - 6);
  ctx.textAlign = 'right'; ctx.textBaseline = 'middle';
  for (let y = Math.ceil(y0/gy.step)*gy.step; y <= y1; y += gy.step){
    if (Math.abs(y) < gy.step/2) continue;
    const p = toPy(y); if (p < 24 || p > H - 12) continue;
    labelBg(C, labX, p, fmtTick(y, gy.step), 'right', 'middle');
  }
  if (ax >= 0 && ax <= H && ay >= 0 && ay <= W){
    ctx.textAlign='right'; ctx.textBaseline='top'; labelBg(C, ay-5, ax+5, '0', 'right', 'top');
  }
}
function labelBg(C, x, y, t, align, base){
  const w = ctx.measureText(t).width, h = 14;
  let lx = align === 'center' ? x - w/2 : align === 'right' ? x - w : x;
  let ly = base === 'top' ? y : base === 'middle' ? y - h/2 : y - h;
  ctx.fillStyle = C.bg; ctx.globalAlpha = .85; ctx.fillRect(lx-2, ly, w+4, h); ctx.globalAlpha = 1;
  ctx.fillStyle = C.muted; ctx.textAlign = align; ctx.textBaseline = base; ctx.fillText(t, x, y);
}

function drawFn(fn, color){
  ctx.strokeStyle = color; ctx.lineWidth = 2.25; ctx.lineJoin = 'round'; ctx.beginPath();
  let pen = false, prevPy = null;
  for (let px = -1; px <= W + 1; px += 1){
    const y = fn.f(toWx(px)), py = toPy(y);
    if (!isFinite(py) || Math.abs(py) > 1e6 || (prevPy !== null && Math.abs(py - prevPy) > H * 2)){ pen = false; prevPy = isFinite(py) ? py : null; continue; }
    pen ? ctx.lineTo(px, py) : ctx.moveTo(px, py); pen = true; prevPy = py;
  }
  ctx.stroke();
}

function ordered(){
  const arr = points.map((p,i) => ({...p, i}));
  return opt.order === 'x' ? arr.sort((a,b) => a.x - b.x || a.i - b.i) : arr;
}

function draw(){
  ctx.setTransform(dpr,0,0,dpr,0,0);
  const C = {bg:tok('--canvas'), minor:tok('--grid-minor'), major:tok('--grid-major'), axis:tok('--axis'), muted:tok('--muted'), pt:tok('--pt'), ink:tok('--ink'), panel:tok('--panel')};
  ctx.fillStyle = C.bg; ctx.fillRect(0,0,W,H);
  drawGrid(C);

  fns.forEach(fn => { if (fn.on) drawFn(fn, tok(fn.color)); });

  if (opt.connect && points.length > 1){
    ctx.strokeStyle = C.pt; ctx.lineWidth = 2; ctx.lineJoin = 'round'; ctx.beginPath();
    ordered().forEach((p,k) => k ? ctx.lineTo(toPx(p.x), toPy(p.y)) : ctx.moveTo(toPx(p.x), toPy(p.y)));
    ctx.stroke();
  }

  ctx.font = `600 12px ${tok('--mono')}`;
  points.forEach((p,i) => {
    const X = toPx(p.x), Y = toPy(p.y);
    if (X < -20 || X > W+20 || Y < -20 || Y > H+20) return;
    const hot = i === hoverIdx;
    if (hot){ ctx.fillStyle = tok('--pt-soft'); ctx.beginPath(); ctx.arc(X,Y,12,0,Math.PI*2); ctx.fill(); }
    ctx.fillStyle = C.pt; ctx.strokeStyle = C.bg; ctx.lineWidth = 2;
    ctx.beginPath(); ctx.arc(X, Y, hot ? 6 : 5, 0, Math.PI*2); ctx.fill(); ctx.stroke();
    if (opt.labels || hot){
      const t = `P${i+1}(${fmt(p.x,3)} | ${fmt(p.y,3)})`;
      ctx.textAlign = 'left'; ctx.textBaseline = 'bottom';
      const w = ctx.measureText(t).width;
      let lx = X + 9, ly = Y - 7;
      if (lx + w > W - 4) lx = X - 9 - w;
      ctx.fillStyle = C.bg; ctx.globalAlpha = .85; ctx.fillRect(lx-3, ly-15, w+6, 16); ctx.globalAlpha = 1;
      ctx.fillStyle = C.pt; ctx.fillText(t, lx, ly);
    }
  });
  syncZoomUI();
}

// ---------- UI: points ----------
const ptBody = $('ptBody');
function renderPoints(){
  $('ptCount').textContent = points.length ? `${points.length}` : '';
  if (!points.length){ ptBody.innerHTML = '<tr><td colspan="4" class="empty">Noch keine Punkte.</td></tr>'; return; }
  ptBody.innerHTML = points.map((p,i) => `<tr>
    <td class="name">P${i+1}</td>
    <td><input type="text" inputmode="decimal" id="px${i}" data-i="${i}" data-k="x" value="${fmt(p.x,6)}" aria-label="x von P${i+1}"></td>
    <td><input type="text" inputmode="decimal" id="py${i}" data-i="${i}" data-k="y" value="${fmt(p.y,6)}" aria-label="y von P${i+1}"></td>
    <td class="del"><button type="button" class="ghost" data-del="${i}" aria-label="P${i+1} löschen">✕</button></td></tr>`).join('');
}
ptBody.addEventListener('input', e => {
  const t = e.target; if (!t.dataset.k) return;
  const v = parseNum(t.value);
  if (isFinite(v)){ points[+t.dataset.i][t.dataset.k] = v; t.style.color = ''; draw(); }
  else t.style.color = 'var(--pt)';
});
ptBody.addEventListener('change', () => renderPoints());
ptBody.addEventListener('click', e => {
  const d = e.target.closest('[data-del]'); if (!d) return;
  points.splice(+d.dataset.del, 1); hoverIdx = -1; renderPoints(); draw();
});
$('ptForm').addEventListener('submit', e => {
  e.preventDefault();
  const x = parseNum($('inX').value), y = parseNum($('inY').value), err = $('ptErr');
  if (!isFinite(x) || !isFinite(y)){ err.textContent = 'Bitte für x und y jeweils eine Zahl eingeben.'; err.hidden = false; return; }
  err.hidden = true;
  points.push({x,y}); renderPoints(); draw();
  $('inX').value = ''; $('inY').value = ''; $('inX').focus();
});
$('btnClear').addEventListener('click', () => { if (!points.length) return; $('btnClear').hidden = true; $('btnClearConfirm').hidden = false; setTimeout(() => { $('btnClear').hidden = false; $('btnClearConfirm').hidden = true; }, 4000); });
$('btnClearConfirm').addEventListener('click', () => { points = []; hoverIdx = -1; $('btnClear').hidden = false; $('btnClearConfirm').hidden = true; renderPoints(); draw(); });
$('btnFit').addEventListener('click', fitView);

function fitView(){
  if (!points.length){ resetView(); return; }
  let xs = points.map(p => p.x).concat(0), ys = points.map(p => p.y).concat(0);
  let minX = Math.min(...xs), maxX = Math.max(...xs), minY = Math.min(...ys), maxY = Math.max(...ys);
  const spanX = Math.max(maxX - minX, 1e-6), spanY = Math.max(maxY - minY, 1e-6);
  const pad = 70;
  const needX = (W - 2*pad) / spanX, needY = (H - 2*pad) / spanY;
  view.cx = (minX + maxX) / 2; view.cy = (minY + maxY) / 2;
  const clampZ = z => Math.max(-6, Math.min(7, z));
  if (opt.lock){ view.zx = clampZ(Math.log2(Math.min(needX, needY) / BASE)); view.zy = view.zx; }
  else { view.zx = clampZ(Math.log2(needX / BASE)); view.zy = clampZ(Math.log2(needY / BASE)); }
  draw();
}
function resetView(){ view = {cx:0, cy:0, zx:0, zy:0}; draw(); }

// ---------- UI: functions ----------
let colorIdx = 0;
function addFn(src){
  const {f, clean} = compile(src);
  const lin = linearInfo(f);
  fns.push({src: clean, f, lin, on:true, color: FN_COLORS[colorIdx++ % FN_COLORS.length]});
  renderFns(); draw();
}
function renderFns(){
  $('fnList').innerHTML = fns.map((fn,i) => `<li>
    <input type="checkbox" id="fnOn${i}" data-on="${i}" ${fn.on ? 'checked' : ''} aria-label="f${i+1} anzeigen">
    <span class="swatch" style="background:var(${fn.color})"></span>
    <span class="expr">f${sub(i+1)}(x) = ${esc(pretty(fn.src))}</span>
    <button type="button" class="ghost" data-fdel="${i}" aria-label="Funktion entfernen">✕</button>
    ${fn.lin ? `<span class="meta">m = ${fmt(fn.lin.m)} · b = ${fmt(fn.lin.b)}${fn.lin.m !== 0 ? ` · Nullstelle x = ${fmt(-fn.lin.b/fn.lin.m)}` : ''}</span>` : ''}
  </li>`).join('');
}
const sub = n => String(n).replace(/\d/g, d => '₀₁₂₃₄₅₆₇₈₉'[d]);
const esc = s => s.replace(/[&<>"]/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c]));
const pretty = s => s.replace(/\s+/g,'').replace(/([^\^(*/])([+-])/g,'$1 $2 ').replace(/\*/g,'·').replace(/\./g, ',');
$('fnList').addEventListener('change', e => { const i = e.target.dataset.on; if (i !== undefined){ fns[+i].on = e.target.checked; draw(); } });
$('fnList').addEventListener('click', e => { const d = e.target.closest('[data-fdel]'); if (d){ fns.splice(+d.dataset.fdel,1); renderFns(); draw(); } });
$('fnForm').addEventListener('submit', e => {
  e.preventDefault();
  const err = $('fnErr');
  try { addFn($('inFn').value); err.hidden = true; $('inFn').value = ''; }
  catch (x){ err.textContent = x.message; err.hidden = false; }
});

// ---------- UI: options ----------
const bindToggle = (id, key, after) => { const el = $(id); el.checked = opt[key]; el.addEventListener('change', () => { opt[key] = el.checked; after && after(); draw(); }); };
bindToggle('optConnect', 'connect', () => $('orderWrap').hidden = !opt.connect);
bindToggle('optLabels', 'labels');
bindToggle('optClickAdd', 'clickAdd');
bindToggle('optSnap', 'snap');
bindToggle('optLock', 'lock', () => { if (opt.lock) view.zy = view.zx; });
$('optOrder').addEventListener('change', e => { opt.order = e.target.value; draw(); });

// ---------- zoom ----------
function syncZoomUI(){
  $('zyRow').hidden = opt.lock;
  $('zxLabel').textContent = opt.lock ? 'Beide' : 'x-Achse';
  $('zx').value = view.zx; $('zy').value = opt.lock ? view.zx : view.zy;
  const unitTxt = s => { const g = stepFor(s).step; return `${fmt(g,6)}/Kästchen`; };
  $('zxOut').textContent = unitTxt(sx());
  $('zyOut').textContent = unitTxt(sy());
}
$('zx').addEventListener('input', e => { view.zx = +e.target.value; if (opt.lock) view.zy = view.zx; draw(); });
$('zy').addEventListener('input', e => { view.zy = +e.target.value; draw(); });
function zoomAt(px, py, delta){
  const wx = toWx(px), wy = toWy(py);
  const c = z => Math.max(-6, Math.min(7, z + delta));
  view.zx = c(view.zx); view.zy = opt.lock ? view.zx : c(view.zy);
  view.cx = wx - (px - W/2) / sx(); view.cy = wy + (py - H/2) / sy();
  draw();
}
$('zin').addEventListener('click', () => zoomAt(W/2, H/2, .5));
$('zout').addEventListener('click', () => zoomAt(W/2, H/2, -.5));
$('zhome').addEventListener('click', resetView);
$('btnReset').addEventListener('click', resetView);
cv.addEventListener('wheel', e => { e.preventDefault(); const r = cv.getBoundingClientRect(); zoomAt(e.clientX - r.left, e.clientY - r.top, -e.deltaY * (e.deltaMode ? .05 : .0015)); }, {passive:false});

// ---------- pointer interaction ----------
let drag = null;
function hitPoint(mx, my){
  let best = -1, bd = 12;
  points.forEach((p,i) => { const d = Math.hypot(toPx(p.x)-mx, toPy(p.y)-my); if (d < bd){ bd = d; best = i; } });
  return best;
}
function snapV(v, s){ if (!opt.snap) return Math.round(v*1000)/1000; const m = minorOf(stepFor(s)); return Math.round(v/m)*m; }
const local = e => { const r = cv.getBoundingClientRect(); return [e.clientX - r.left, e.clientY - r.top]; };
cv.addEventListener('pointerdown', e => {
  const [mx,my] = local(e);
  const hit = hitPoint(mx,my);
  cv.setPointerCapture(e.pointerId);
  drag = {mode: hit >= 0 ? 'point' : 'pan', i: hit, sx:mx, sy:my, cx:view.cx, cy:view.cy, moved:false};
  if (drag.mode === 'pan') cv.className = 'grabbing';
});
cv.addEventListener('pointermove', e => {
  const [mx,my] = local(e);
  const wx = toWx(mx), wy = toWy(my);
  $('coord').innerHTML = `x <b>${fmt(snapV(wx,sx()),3)}</b> · y <b>${fmt(snapV(wy,sy()),3)}</b>`;
  if (drag){
    if (Math.hypot(mx-drag.sx, my-drag.sy) > 4) drag.moved = true;
    if (drag.mode === 'pan' && drag.moved){ view.cx = drag.cx - (mx-drag.sx)/sx(); view.cy = drag.cy + (my-drag.sy)/sy(); draw(); }
    if (drag.mode === 'point' && drag.moved){
      points[drag.i].x = snapV(wx, sx()); points[drag.i].y = snapV(wy, sy()); hoverIdx = drag.i; draw();
      const ix = $('px'+drag.i), iy = $('py'+drag.i); if (ix){ ix.value = fmt(points[drag.i].x,6); iy.value = fmt(points[drag.i].y,6); }
    }
    return;
  }
  const h = hitPoint(mx,my);
  cv.className = h >= 0 ? 'grab' : '';
  if (h !== hoverIdx){ hoverIdx = h; draw(); }
});
cv.addEventListener('pointerup', e => {
  if (!drag) return;
  const [mx,my] = local(e);
  if (!drag.moved && drag.mode === 'pan' && opt.clickAdd){
    points.push({x: snapV(toWx(mx), sx()), y: snapV(toWy(my), sy())}); renderPoints(); draw();
  }
  drag = null; cv.className = '';
});
cv.addEventListener('pointerleave', () => { if (!drag && hoverIdx !== -1){ hoverIdx = -1; draw(); } $('coord').innerHTML = 'x <b>–</b> · y <b>–</b>'; });

// ---------- theme + resize ----------
new ResizeObserver(resize).observe(stage);
matchMedia('(prefers-color-scheme: dark)').addEventListener('change', draw);
new MutationObserver(draw).observe(document.documentElement, {attributes:true, attributeFilter:['data-theme']});

// ---------- boot with example ----------
renderPoints();
addFn('y = 0.5x - 1');
resize();
if (document.fonts) document.fonts.ready.then(draw);
})();
</script>
</body>
</html>
