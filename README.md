<!DOCTYPE html>
<html lang="en"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>NEOIMMUNE EVO – Evolution-Aware Therapeutic Stress Testing</title>
<style>
:root{--bg:#0d1520;--p:#142133;--p2:#1a2b42;--ln:#2a3f5c;--tx:#e8eef6;--mu:#93a6bf;--ac:#5fd4c4;--am:#f2b84b;--rd:#ef6b6b;--gn:#7ccf8a}
*{box-sizing:border-box}html,body{margin:0}
body{background:var(--bg);color:var(--tx);font:15px/1.5 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;padding-top:env(safe-area-inset-top)}
h1,h2,h3{font-family:Georgia,"Iowan Old Style",serif;font-weight:600;margin:.2em 0}
h1{font-size:clamp(28px,6vw,52px);letter-spacing:-.5px;line-height:1.05}h2{font-size:21px}h3{font-size:16px}
button,select,input{font:inherit;color:inherit}
button{background:var(--p2);border:1px solid var(--ln);border-radius:6px;padding:8px 12px;cursor:pointer}
button:hover{border-color:var(--ac)}button.pri{background:var(--ac);color:#06201c;border-color:var(--ac);font-weight:700}
:focus-visible{outline:2px solid var(--am);outline-offset:2px}
header{display:flex;flex-wrap:wrap;gap:10px;align-items:center;justify-content:space-between;padding:10px 18px;border-bottom:1px solid var(--ln)}
.badge{display:inline-block;border:1px solid var(--am);color:var(--am);border-radius:4px;padding:1px 7px;font-size:12px;margin:2px}
.badge.off{border-color:var(--rd);color:var(--rd)}.badge.ok{border-color:var(--gn);color:var(--gn)}
.hero{padding:26px 18px;border-bottom:1px solid var(--ln);background:radial-gradient(1200px 300px at 80% -50%,#1d3a52,transparent)}
.hero p.tag{font-family:Georgia,serif;font-style:italic;color:var(--ac);font-size:19px;margin:6px 0 14px}
.story{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:10px;margin:14px 0}
.story div{border-left:3px solid var(--ln);padding:4px 12px;color:var(--mu)}.story b{color:var(--tx);display:block}
.app{display:grid;grid-template-columns:310px 1fr;gap:14px;padding:14px 18px;max-width:1500px;margin:auto}
@media(max-width:900px){.app{grid-template-columns:1fr}}
aside,.panel{background:var(--p);border:1px solid var(--ln);border-radius:8px;padding:14px}
aside label{display:block;margin:9px 0 2px;color:var(--mu);font-size:13px}
aside input[type=text],aside input[type=number],aside select{width:100%;background:var(--bg);border:1px solid var(--ln);border-radius:5px;padding:6px}
aside input[type=range],.w input{width:100%}
.stages{display:flex;flex-wrap:wrap;gap:4px;margin-bottom:10px}
.stages span{font-size:11px;border:1px solid var(--ln);border-radius:4px;padding:2px 6px;color:var(--mu)}
.stages span.on{border-color:var(--ac);color:var(--ac)}
nav[role=tablist]{display:flex;gap:4px;overflow-x:auto;margin-bottom:10px}
nav button{white-space:nowrap}nav button[aria-selected=true]{border-color:var(--ac);color:var(--ac)}
.tab{display:none}.tab.on{display:block}
.grid2{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:12px}
table{border-collapse:collapse;width:100%;font-size:13px}th,td{border:1px solid var(--ln);padding:5px 7px;text-align:center}th{background:var(--p2);font-weight:600}
td.l,th.l{text-align:left}
.S{background:#1f5c4a}.I{background:#7a5f1e}.R{background:#7a2c34}
canvas{width:100%;display:block;background:var(--bg);border:1px solid var(--ln);border-radius:6px}
.chips button{margin:2px;border-width:2px}.chips button[aria-pressed=true]{background:var(--p2)}
details{border:1px dashed var(--ln);border-radius:6px;padding:4px 10px;margin:8px 0;color:var(--mu);font-size:13px}summary{cursor:pointer;color:var(--ac)}
.note{color:var(--mu);font-size:13px}.warn{border:1px solid var(--am);color:var(--am);padding:6px 10px;border-radius:6px;font-size:13px;margin:8px 0}
.big{font-family:Georgia,serif;font-size:22px;color:var(--am);margin:6px 0}
pre{white-space:pre-wrap;background:var(--bg);border:1px solid var(--ln);padding:10px;border-radius:6px;font-size:12.5px;overflow:auto;max-height:420px}
.loop{display:flex;flex-wrap:wrap;gap:6px;align-items:center}.loop span{border:1px solid var(--ac);border-radius:99px;padding:3px 10px;font-size:12px}
.w{display:grid;grid-template-columns:110px 1fr 36px;gap:6px;align-items:center;font-size:13px}
.rs{display:none}body.research .rs{display:block}
footer{padding:18px;color:var(--mu);font-size:12px;text-align:center}
@media(prefers-reduced-motion:no-preference){.stages span{transition:.2s}}
</style></head><body>
<header><div><b style="font-family:Georgia,serif;font-size:18px">NEOIMMUNE EVO</b> <span class="note">v0.1 prototype</span></div>
<div><span class="badge">EDUCATIONAL SIMULATION</span><span class="badge off" id="eng">REAL DOCKING ENGINE: checking…</span><span class="badge">NOT CLINICAL</span></div></header>

<section class="hero">
<h1>Don’t just ask what binds.<br>Ask what survives evolution.</h1>
<p class="tag">Evolution-Aware Therapeutic Stress Testing</p>
<div class="story"><div><b>Traditional approach</b>Find a good candidate against today’s target state.</div><div><b>Proposed approach</b>Stress-test the candidate against tomorrow’s simulated tumor states.</div><div><b>Result</b>Rank candidates by evolutionary robustness, not only baseline performance.</div></div>
<button class="pri" id="load">Load example</button> <button id="start">Start experiment</button> <button id="meth">Method</button>
<div class="warn">Research and educational computational prototype. Uses synthetic, fictional data. It does not diagnose, recommend treatment, or claim efficacy or safety.</div>
</section>

<div class="app">
<aside aria-label="Experiment configuration">
<h2>Experiment configuration</h2>
<label for="mode">Computation mode</label>
<select id="mode"><option>A – Educational simulation (browser)</option><option disabled>B – Real AutoDock Vina (needs backend)</option></select>
<label for="pdb">Target (synthetic OncoTarget-01) – optional PDB ID for provenance lookup</label>
<div style="display:flex;gap:4px"><input type="text" id="pdb" value="1M17" maxlength="4"><button id="fetchpdb">Fetch</button></div>
<div class="note" id="pdbout">Metadata only (RCSB). Not used for docking in this build.</div>
<label for="smi">Ligand (SMILES recorded, not parsed in simulation mode)</label>
<input type="text" id="smi" value="EVO-L1 (synthetic)">
<label for="seed">Random seed</label><input type="number" id="seed" value="847291">
<label for="n">Clones: <output id="nv">5</output></label><input type="range" id="n" min="3" max="10" value="5">
<label for="mu">Mutation pressure: <output id="muv">0.30</output></label><input type="range" id="mu" min="0" max="1" step=".05" value=".3">
<label for="T">Treatment pressure: <output id="Tv">0.70</output></label><input type="range" id="T" min="0" max="1" step=".05" value=".7">
<label for="g">Generations: <output id="gv">12</output></label><input type="range" id="g" min="4" max="20" value="12">
<label><input type="checkbox" id="norm" checked> Normal-cell comparator</label>
<label><input type="checkbox" id="rm"> Research mode (show equations &amp; parameters)</label>
<p><button class="pri" id="run" style="width:100%">Run evolution-aware analysis</button></p>
<button id="repro" style="width:100%">Reproduce this run</button>
</aside>

<main>
<div class="stages" id="stages" aria-live="polite"></div>
<nav role="tablist" id="tabs"></nav>

<section class="tab panel on" id="t-overview"><h2>Overview</h2><div id="ov">Press “Load example” or “Run”.</div></section>

<section class="tab panel" id="t-evo"><h2>Therapeutic evolution map</h2>
<label class="note">Candidate under pressure <select id="ecand"></select></label>
<div class="chips" id="chips"></div>
<div class="grid2"><div><canvas id="cv-freq" height="260" aria-label="Clone frequency over generations"></canvas><button id="png">Export PNG</button></div>
<div><canvas id="cv3d" height="260" aria-label="Schematic structure"></canvas>
<div><button data-v="wt">WT</button> <button data-v="alt">Altered</button> <button data-v="cmp">Compare</button> <span class="note">Drag to rotate</span></div>
<div class="warn" style="margin-top:6px">SIMULATED SCHEMATIC – synthetic points, not a real structure and not a docking pose.</div></div></div>
<div id="cdet"></div>
<h3>Therapy vs evolution</h3><canvas id="cv-eff" height="240" aria-label="Effectiveness over generations"></canvas>
<details><summary>How should I interpret this?</summary>Effectiveness = population-weighted simulated sensitivity. Lines falling over generations mean the simulated tumor is escaping that candidate. Not a clinical prediction.</details></section>

<section class="tab panel" id="t-res"><h2>Resistance</h2><div id="resbody"></div></section>
<section class="tab panel" id="t-red"><h2>Red team the therapy</h2><div id="redbody"></div></section>
<section class="tab panel" id="t-ada"><h2>Adaptive loop</h2><div id="adabody"></div></section>
<section class="tab panel" id="t-rep"><h2>NEOIMMUNE EVO research report</h2><div id="repbody"></div></section>
<section class="tab panel" id="t-met"><h2>Methods &amp; limitations</h2><div id="metbody"></div></section>
</main></div>
<footer>NEOIMMUNE EVO · SIMULATION / COMPUTATIONAL PROTOTYPE · every number on screen comes from user input, deterministic simulation, or a public API response.</footer>

<script>
const $=s=>document.querySelector(s),$$=s=>[...document.querySelectorAll(s)];
const rng=a=>()=>{a|=0;a=a+0x6D2B79F5|0;let t=Math.imul(a^a>>>15,1|a);t=t+Math.imul(t^t>>>7,61|t)^t;return((t^t>>>14)>>>0)/4294967296};
const VER='EVO-SIM 0.1';
const MUT=[{id:'M1',n:'Res118 Thr→Met',i:8,why:'bulky side chain narrows pocket'},{id:'M2',n:'Res142 Gly→Asp',i:15,why:'adds charge near hinge'},{id:'M3',n:'Res176 Leu→Phe',i:22,why:'hydrophobic rearrangement'},{id:'M4',n:'Res203 Ala→Val',i:30,why:'small steric shift'}];
// synthetic candidate library: c[j]=fraction of compatibility retained under mutation Mj
const CANDS=[{id:'A',name:'EVO-L1',base:.95,c:[.2,.9,.3,.5],norm:.35,unc:.30},{id:'B',name:'EVO-L2',base:.78,c:[.8,.75,.85,.7],norm:.2,unc:.2},{id:'C',name:'EVO-L3',base:.7,c:[.6,.8,.9,.85],norm:.25,unc:.25},{id:'D',name:'EVO-L4',base:.85,c:[.5,.4,.8,.6],norm:.45,unc:.35}];
const COL=['#5fd4c4','#f2b84b','#ef6b6b','#a78bfa','#60a5fa','#f472b6','#a3e635','#fb923c','#22d3ee','#e879f9'];
const TABS=[['overview','Overview'],['evo','Evolution & 3D'],['res','Resistance'],['red','Red team'],['ada','Adaptation'],['rep','Report'],['met','Methods']];
const norm=f=>{const s=f.reduce((a,b)=>a+b,0);f.forEach((_,i)=>f[i]/=s)};
const dot=(a,b)=>a.reduce((s,v,i)=>s+v*b[i],0),mean=a=>a.reduce((s,v)=>s+v,0)/a.length;
const sens=(cl,cd)=>cd.base*cl.m.reduce((p,j)=>p*cd.c[j],1);
const lab=s=>s>=.6?['Sensitive','S']:s>=.3?['Intermediate','I']:['Resistant','R'];
const ETR=E=>.6*mean(E)+.4*E[E.length-1];
const f2=x=>x.toFixed(2),pc=x=>(100*x).toFixed(0)+'%';
let S=null,sel=0,view='alt',ang=.6;

function cfg(){return{seed:+$('#seed').value||847291,n:+$('#n').value,mu:+$('#mu').value,T:+$('#T').value,gens:+$('#g').value,normal:$('#norm').checked,pdb:$('#pdb').value,ligand:$('#smi').value}}
function W(){const w={rob:+$('#w1')?.value||40,res:+$('#w2')?.value||25,base:+$('#w3')?.value||15,sel:+$('#w4')?.value||15,conf:+$('#w5')?.value||5};return w}
function clones(c){const r=rng(c.seed),a=[];
for(let i=0;i<c.n;i++){let m=[];if(i>0){m=[Math.floor(r()*4)];if(r()<.4){const j=Math.floor(r()*4);if(!m.includes(j))m.push(j)}}
a.push({id:'C'+(i+1),m,g:1-.06*m.length+(r()-.5)*.02,w:i?r()+.05:0})}
const sw=a.reduce((s,x)=>s+x.w,0);a.forEach((x,i)=>x.f0=i?.55*x.w/sw:.45);return a}
function sim(cl,pick,o){const r=rng(o.seed+7),n=cl.length;let f=cl.map(x=>x.f0);
const ord=cl.map((_,i)=>i).sort((a,b)=>cl[b].m.length-cl[a].m.length||b-a);
for(let k=0;k<(o.boost||0);k++)f[ord[k]]+=.06;norm(f);
const F=[],E=[],U=[];
for(let g=0;g<=o.gens;g++){const cd=pick(f,g);F.push(f.slice());U.push(cd.id);const s=cl.map(x=>sens(x,cd));E.push(dot(f,s));
if(g==o.gens)break;const on=o.sched=='int'?g%4<2:true;
const h=f.map((v,i)=>v*cl[i].g*(1-(on?o.T*.9*(o.ab??1)*s[i]:0))*(1+(r()-.5)*.04));norm(h);
const m=o.mu*.1;f=h.map(v=>v*(1-m)+m/n);norm(f)}
return{F,E,U}}
const resMass=(cl,cd,f)=>f.reduce((s,v,i)=>s+(sens(cl[i],cd)<.45?v:0),0);
function adaptive(cl,start,thr,ev){let cur=start;return(f,g)=>{
if(g>0&&resMass(cl,cur,f)>thr){const here=dot(f,cl.map(x=>sens(x,cur)));
const b=CANDS.filter(c=>c!=cur).map(c=>[c,dot(f,cl.map(x=>sens(x,c)))]).sort((a,b)=>b[1]-a[1])[0];
if(b[1]>here){ev.push({g,from:cur.id,to:b[0].id,rm:resMass(cl,cur,f)});cur=b[0]}}return cur}}
const SCN=[['Low treatment pressure',o=>({T:o.T*.4})],['High treatment pressure',o=>({T:Math.min(1,o.T*1.4)})],['Early resistant clone',o=>({boost:1})],['Dual resistant clones',o=>({boost:2})],['High evolutionary pressure',o=>({mu:Math.min(1,o.mu*2)})],['Intermittent therapy',o=>({sched:'int'})],['Low target abundance',o=>({ab:.6})],['Combined worst case',o=>({T:Math.min(1,o.T*1.4),boost:2,mu:Math.min(1,o.mu*2)})]];
function hash(s){let h=5381;for(const c of s)h=(h*33^c.charCodeAt(0))>>>0;return h.toString(16).toUpperCase().padStart(8,'0').slice(0,4)}

function analyze(c){const cl=clones(c),o={seed:c.seed,gens:c.gens,T:c.T,mu:c.mu};
const res={},rt={};
CANDS.forEach(cd=>{res[cd.id]=sim(cl,()=>cd,o);rt[cd.id]=SCN.map(([n,fn])=>ETR(sim(cl,()=>cd,{...o,...fn(o)}).E))});
const m={};CANDS.forEach(cd=>{const r=res[cd.id],last=r.F[r.F.length-1];
m[cd.id]={etr:ETR(r.E),bar:1-resMass(cl,cd,last),drop:r.E[0]-r.E[r.E.length-1],sel:c.normal?1-cd.norm:.5,worst:Math.min(...rt[cd.id])}});
const arg=(k,f)=>CANDS.reduce((a,b)=>f(b)>f(a)?b:a);
const bw=arg(0,x=>x.base),ew=arg(0,x=>m[x.id].etr);
const ev=[],ad=sim(cl,adaptive(cl,bw,.35,ev),o),inte=sim(cl,()=>bw,{...o,sched:'int'});
const t=new Date(),id=`NEO-EVO-${t.toISOString().slice(0,10).replace(/-/g,'')}-${hash(JSON.stringify(c))}`;
return{c,cl,res,rt,m,bw,ew,ad,ev,inte,id,time:t.toISOString(),
 rob:arg(0,x=>m[x.id].worst),unc:arg(0,x=>x.unc),vul:arg(0,x=>m[x.id].drop),sig:hash(JSON.stringify([res,rt,ad.E]))}}
function score(cd){const w=W(),T=Object.values(w).reduce((a,b)=>a+b,0)||1,m=S.m[cd.id];
return(w.rob*m.etr+w.res*m.bar+w.base*cd.base+w.sel*m.sel+w.conf*(1-cd.unc))/T}
const conf=u=>u<.25?'MODERATE CONFIDENCE':'LOW CONFIDENCE';

/* charts */
function chart(cv,series,o={}){const d=devicePixelRatio||1,w=cv.clientWidth,h=+cv.getAttribute('height');cv.width=w*d;cv.height=h*d;const x=cv.getContext('2d');x.scale(d,d);
const L=36,B=22,N=series[0].data.length,X=i=>L+(w-L-8)*i/(N-1),Y=v=>8+(h-8-B)*(1-v/(o.max||1));
x.strokeStyle='#2a3f5c';x.fillStyle='#93a6bf';x.font='11px system-ui';
for(let k=0;k<=4;k++){const v=(o.max||1)*k/4;x.beginPath();x.moveTo(L,Y(v));x.lineTo(w-8,Y(v));x.stroke();x.fillText(v.toFixed(2),2,Y(v)+4)}
for(let i=0;i<N;i+=Math.ceil(N/8))x.fillText(i,X(i),h-6);x.fillText('generation →',w-80,h-6);
series.forEach(s=>{x.beginPath();x.strokeStyle=s.col;x.lineWidth=s.hl?3.5:1.8;x.globalAlpha=s.dim?.3:1;s.data.forEach((v,i)=>i?x.lineTo(X(i),Y(v)):x.moveTo(X(i),Y(v)));x.stroke()});x.globalAlpha=1}

/* 3D schematic */
const r3=rng(1234),PTS=[...Array(40)].map((_,i)=>{const t=i/40*13.8;return[Math.cos(t)*(1.2+.3*r3()),(i/40-.5)*3.2,Math.sin(t)*(1.2+.3*r3())]});
const POCK=[16,17,18,19,20,21,23,24];
function draw3d(){const cv=$('#cv3d');if(!cv)return;const d=devicePixelRatio||1,w=cv.clientWidth,h=260;cv.width=w*d;cv.height=h*d;const x=cv.getContext('2d');x.scale(d,d);
const cl=S?.cl[sel],mi=cl?cl.m.map(j=>MUT[j].i):[];
const P=(p,alt)=>{let q=[...p];if(alt)q=[q[0]*1.18,q[1]+.12,q[2]*1.18];const c=Math.cos(ang),s=Math.sin(ang),X=q[0]*c+q[2]*s,Z=-q[0]*s+q[2]*c;return[w/2+X*55,h/2-q[1]*55,Z]};
const items=[];PTS.forEach((p,i)=>{const m=mi.includes(i),mark=MUT.some(u=>u.i==i);
 if(view!='alt'||!m)items.push({p:P(p),c:POCK.includes(i)?'#5fd4c4':'#60728b',r:POCK.includes(i)?5:4,ring:m||mark,lab:mark?MUT.find(u=>u.i==i).id:'',i,ghost:0});
 if(m&&view!='wt')items.push({p:P(p,1),c:'#f2b84b',r:7,ring:1,lab:MUT.find(u=>u.i==i).id+'*',i});
 if(m&&view=='cmp')items.push({p:P(p),c:'#60728b',r:5,ring:1,ghost:1,i})});
const cx=[0,.1,0];[[0,0,0],[.35,.2,0],[-.3,.3,.2],[.2,-.3,.3],[-.2,-.2,-.3]].forEach(a=>items.push({p:P([cx[0]+a[0],cx[1]+a[1],cx[2]+a[2]+.1]),c:'#ef6b6b',r:4,lig:1}));
x.strokeStyle='#3b5272';x.beginPath();PTS.forEach((p,i)=>{const q=P(p);i?x.lineTo(q[0],q[1]):x.moveTo(q[0],q[1])});x.stroke();
items.sort((a,b)=>a.p[2]-b.p[2]).forEach(t=>{x.beginPath();x.arc(t.p[0],t.p[1],t.r,0,7);x.fillStyle=t.ghost?'transparent':t.c;if(!t.ghost)x.fill();if(t.ring||t.ghost){x.strokeStyle='#f2b84b';x.lineWidth=1.5;x.stroke()}
 if(t.lab){x.fillStyle='#e8eef6';x.font='11px system-ui';x.fillText(t.lab,t.p[0]+8,t.p[1]-6)}});
x.fillStyle='#93a6bf';x.font='11px system-ui';x.fillText('teal=pocket residues · red=ligand (schematic) · amber=mutated residue',8,h-6)}
{const c=()=>$('#cv3d');let dr=0;document.addEventListener('pointerdown',e=>{if(e.target==c())dr=e.clientX});document.addEventListener('pointermove',e=>{if(dr&&e.target==c()){ang+=(e.clientX-dr)/80;dr=e.clientX;draw3d()}});document.addEventListener('pointerup',()=>dr=0)}

/* rendering */
function cellHtml(s){const[t,k]=lab(s);return`<td class="${k}" title="${t}">${f2(s)}<br><small>${t}</small></td>`}
function renderAll(){renderOv();renderEvoCtl();renderEvo();renderRes();renderRed();renderAda();renderRep();renderMet()}
function renderOv(){const w=W(),rk=[...CANDS].sort((a,b)=>score(b)-score(a)),top=rk[0],m=S.m;
const find=[];
const bwR=S.res[S.bw.id],fl=bwR.F[bwR.F.length-1],di=fl.indexOf(Math.max(...fl));
find.push(S.bw==S.ew?`Baseline winner (${S.bw.name}) was also the most evolutionarily robust under these assumptions.`:`Baseline winner (${S.bw.name}, ${f2(S.bw.base)}) was not the evolutionary winner (${S.ew.name}, ETR ${f2(m[S.ew.id].etr)} vs ${f2(m[S.bw.id].etr)}).`);
find.push(`Under ${S.bw.name}, clone ${S.cl[di].id} reached ${pc(fl[di])} (started ${pc(S.cl[di].f0)})${S.cl[di].f0<.1&&S.cl[di].m.length?' – a low-frequency mutant became dominant':''}.`);
const eg=bwR.F.findIndex(f=>resMass(S.cl,S.bw,f)>.35);find.push(eg>0?`Resistant mass crossed 35% at generation ${eg} for ${S.bw.name}.`:`Resistant mass stayed below 35% for ${S.bw.name} (threshold 0.35).`);
find.push(`Adaptive switching made ${S.ev.length} switch(es); adaptive ETR ${f2(ETR(S.ad.E))} vs continuous ${f2(m[S.bw.id].etr)}.`);
const ws=SCN.map((s,i)=>[s[0],mean(CANDS.map(c=>S.rt[c.id][i]))]).sort((a,b)=>a[1]-b[1])[0];find.push(`Most damaging red-team scenario on average: ${ws[0]} (mean ETR ${f2(ws[1])}).`);
find.push(`Uncertainty is never lower than moderate: states are synthetic and the evolution model is simplified.`);
$('#ov').innerHTML=`<div class="big">${S.bw==S.ew?'Baseline winner = evolutionary winner (this run)':'Baseline winner ≠ evolutionary winner'}</div>
<table><tr><th class="l">Question</th><th>Candidate</th></tr><tr><td class="l">Baseline winner</td><td>${S.bw.name}</td></tr><tr><td class="l">Evolutionary winner (highest ETR)</td><td>${S.ew.name}</td></tr><tr><td class="l">Most robust (best worst-case ETR)</td><td>${S.rob.name}</td></tr><tr><td class="l">Highest uncertainty</td><td>${S.unc.name}</td></tr><tr><td class="l">Most vulnerable (largest drop)</td><td>${S.vul.name}</td></tr></table>
<h3>What did this experiment reveal?</h3><ul>${find.map(x=>`<li>${x}</li>`).join('')}</ul>
<h3>Composite research score <small class="note">(adjust weights)</small></h3>
<div class="grid2"><div>${[['w1','Robustness (ETR)',w.rob],['w2','Resistance barrier',w.res],['w3','Baseline binding',w.base],['w4','Selectivity proxy',w.sel],['w5','Confidence',w.conf]].map(([i,n,v])=>`<div class="w"><label for="${i}">${n}</label><input type="range" id="${i}" min="0" max="100" value="${v}"><output>${v}</output></div>`).join('')}</div>
<div class="note">Score = Σ wᵢ·componentᵢ / Σ wᵢ. Components in [0,1]. Not a validated measure.</div></div>
<table><tr><th>Rank</th><th class="l">Candidate</th><th>Baseline</th><th>ETR</th><th>Res. barrier</th><th>Selectivity proxy${$('#norm').checked?'':' (comparator off → 0.50 neutral)'}</th><th>Uncertainty</th><t
