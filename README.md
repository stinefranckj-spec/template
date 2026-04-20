<!DOCTYPE html>
<html lang="da">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GoLearn — Customer Marketing Manager</title>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --bg:#d6e8f5;--white:#ffffff;--s2:#eaf3fb;--border:#c2d8ed;--navy:#1a2b6b;
  --blue:#4a6cf7;--teal:#4db8e8;--yellow:#f5a623;--green:#16a34a;--green2:#22c55e;
  --red:#dc2626;--red2:#ef4444;--orange:#ea580c;--orange2:#f97316;--purple:#7c3aed;--muted:#6b7db3;
  --ph1:#4a6cf7;--ph2:#0891b2;--ph3:#ea580c;--ph4:#16a34a;
}
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Plus Jakarta Sans',sans-serif;background:var(--bg);color:var(--navy);min-height:100vh;font-size:14px}
nav{background:var(--white);border-bottom:1px solid var(--border);height:62px;display:flex;align-items:center;justify-content:space-between;padding:0 28px;position:sticky;top:0;z-index:300;box-shadow:0 2px 16px rgba(26,43,107,.08)}
.logo{display:flex;align-items:center;gap:10px}
.bulb{width:36px;height:36px;background:var(--yellow);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.05rem}
.lname{font-size:1.15rem;font-weight:800;letter-spacing:-.02em;color:var(--navy)}
.lsub{font-size:.58rem;color:var(--muted);font-weight:400}
.nav-r{display:flex;align-items:center;gap:9px}
.src{display:flex;align-items:center;gap:5px;font-size:.65rem;font-weight:700;padding:4px 10px;border-radius:20px}
.shs{background:rgba(255,122,0,.1);color:#ff7a00}.sga{background:rgba(74,108,247,.1);color:var(--blue)}
.dot{width:6px;height:6px;border-radius:50%;animation:blink 2s ease-in-out infinite}
.shs .dot{background:#ff7a00}.sga .dot{background:var(--blue)}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}
.page{max-width:1440px;margin:0 auto;padding:26px 24px 52px}
.hero{display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:24px;gap:20px}
.hero h1{font-size:1.5rem;font-weight:800;letter-spacing:-.025em}
.hero h1 span{color:var(--blue)}
.hero p{font-size:.79rem;color:var(--muted);margin-top:5px;line-height:1.55}
.hkpis{display:flex;gap:12px;flex-shrink:0}
.hkpi{background:var(--white);border:1px solid var(--border);border-radius:12px;padding:14px 18px;text-align:center;min-width:88px;box-shadow:0 2px 8px rgba(26,43,107,.05)}
.hkv{font-size:1.55rem;font-weight:800;letter-spacing:-.03em;line-height:1}
.hkl{font-size:.63rem;color:var(--muted);margin-top:3px}
.hkd{font-size:.67rem;font-weight:600;margin-top:3px}
.lcbar{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-bottom:22px}
.lc{border-radius:12px;padding:14px 18px;border:1px solid transparent;position:relative;overflow:hidden}
.lc::before{content:'';position:absolute;left:0;top:0;bottom:0;width:4px;border-radius:12px 0 0 12px}
.lc.p1{background:rgba(74,108,247,.08);border-color:rgba(74,108,247,.2)}.lc.p1::before{background:var(--ph1)}
.lc.p2{background:rgba(8,145,178,.07);border-color:rgba(8,145,178,.2)}.lc.p2::before{background:var(--ph2)}
.lc.p3{background:rgba(234,88,12,.07);border-color:rgba(234,88,12,.2)}.lc.p3::before{background:var(--ph3)}
.lc.p4{background:rgba(22,163,74,.07);border-color:rgba(22,163,74,.2)}.lc.p4::before{background:var(--ph4)}
.lclbl{font-size:.61rem;font-weight:800;text-transform:uppercase;letter-spacing:.1em;margin-bottom:3px}
.lc.p1 .lclbl{color:var(--ph1)}.lc.p2 .lclbl{color:var(--ph2)}.lc.p3 .lclbl{color:var(--ph3)}.lc.p4 .lclbl{color:var(--ph4)}
.lct{font-size:.79rem;font-weight:700;color:var(--navy);margin-bottom:7px}
.lcst{display:flex;gap:14px}
.lcsv{font-size:1.35rem;font-weight:800;letter-spacing:-.02em;line-height:1}
.lc.p1 .lcsv{color:var(--ph1)}.lc.p2 .lcsv{color:var(--ph2)}.lc.p3 .lcsv{color:var(--ph3)}.lc.p4 .lcsv{color:var(--ph4)}
.lcsl{font-size:.62rem;color:var(--muted);margin-top:1px}
.sec{font-size:.61rem;font-weight:800;text-transform:uppercase;letter-spacing:.12em;margin-bottom:10px;display:flex;align-items:center;gap:8px}
.sec::after{content:'';flex:1;height:1px;background:var(--border)}
.s1{color:var(--ph1)}.s2{color:var(--ph2)}.s3{color:var(--ph3)}.s4{color:var(--ph4)}.sg{color:var(--muted)}
.card{background:var(--white);border-radius:14px;border:1px solid var(--border);padding:20px 22px;box-shadow:0 2px 8px rgba(26,43,107,.05);transition:box-shadow .2s,transform .2s;animation:fu .4s ease both}
.card:hover{box-shadow:0 6px 22px rgba(26,43,107,.1);transform:translateY(-1px)}
.ch{display:flex;align-items:center;justify-content:space-between;margin-bottom:15px}
.ct{font-size:.86rem;font-weight:700;color:var(--navy)}
.tags{display:flex;gap:5px}
.tag{font-size:.59rem;font-weight:700;text-transform:uppercase;letter-spacing:.07em;padding:3px 9px;border-radius:20px;white-space:nowrap}
.t1{background:rgba(74,108,247,.1);color:var(--ph1)}.t2{background:rgba(8,145,178,.1);color:var(--ph2)}
.t3{background:rgba(234,88,12,.1);color:var(--ph3)}.t4{background:rgba(22,163,74,.1);color:var(--ph4)}
.ths{background:rgba(255,122,0,.1);color:#ff7a00}.tga{background:rgba(74,108,247,.1);color:var(--blue)}
.tg{background:rgba(22,163,74,.1);color:var(--green)}.tr{background:rgba(220,38,38,.1);color:var(--red)}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:16px}
.g3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;margin-bottom:16px}
.g32{display:grid;grid-template-columns:3fr 2fr;gap:16px;margin-bottom:16px}
.mb{margin-bottom:16px}
.ob-funnel{display:flex;flex-direction:column;gap:8px}
.ob-step{display:flex;align-items:center;gap:12px}
.ob-lbl{width:155px;font-size:.74rem;color:var(--muted);text-align:right;flex-shrink:0}
.ob-track{flex:1;background:var(--s2);border-radius:7px;height:34px;overflow:hidden}
.ob-fill{height:100%;border-radius:7px;display:flex;align-items:center;padding-left:13px;font-size:.73rem;font-weight:700;color:white}
.ob-val{width:40px;font-size:.78rem;font-weight:800;text-align:right;flex-shrink:0}
.ttfv{display:grid;grid-template-columns:repeat(3,1fr);gap:9px;margin-bottom:13px}
.ttfv-item{background:var(--s2);border-radius:10px;padding:11px 13px;text-align:center}
.ttfvv{font-size:1.35rem;font-weight:800;letter-spacing:-.02em;color:var(--navy)}
.ttfvl{font-size:.64rem;color:var(--muted);margin-top:2px}
.adopt-grid{display:grid;grid-template-columns:1fr 1fr;gap:9px}
.ai-item{background:var(--s2);border-radius:10px;padding:11px 13px}
.ain{font-size:.72rem;font-weight:700;margin-bottom:5px;color:var(--navy)}
.aib{background:var(--border);border-radius:4px;height:6px;overflow:hidden;margin-bottom:4px}
.aif{height:100%;border-radius:4px}
.aim{display:flex;justify-content:space-between;font-size:.66rem;color:var(--muted)}
.bars{display:flex;flex-direction:column;gap:9px}
.brow{display:grid;grid-template-columns:128px 1fr 40px;align-items:center;gap:10px}
.bl{font-size:.73rem;color:var(--muted);text-align:right}
.bt{background:var(--s2);border-radius:5px;height:8px;overflow:hidden}
.bf{height:100%;border-radius:5px}
.bv{font-size:.73rem;font-weight:700;color:var(--navy);text-align:right}
.trig-list{display:flex;flex-direction:column;gap:8px}
.trig{display:flex;align-items:center;gap:11px;background:var(--s2);border-radius:10px;padding:10px 13px}
.trico{width:30px;height:30px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:.88rem;flex-shrink:0}
.trib{flex:1}
.trin{font-size:.77rem;font-weight:700;color:var(--navy)}
.trid{font-size:.66rem;color:var(--muted);margin-top:1px}
.tris{display:flex;gap:12px;flex-shrink:0;text-align:right}
.trisv{font-size:.86rem;font-weight:800;color:var(--navy)}
.trisl{font-size:.61rem;color:var(--muted)}
.rt{width:100%;border-collapse:collapse}
.rt th{font-size:.6rem;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--muted);text-align:left;padding:0 10px 10px 0;border-bottom:2px solid var(--border)}
.rt td{padding:10px 10px 10px 0;border-bottom:1px solid var(--border);vertical-align:middle;font-size:.76rem;color:var(--navy)}
.rt tr:last-child td{border-bottom:none}
.cn{font-weight:700;font-size:.79rem}.cs{font-size:.65rem;color:var(--muted);margin-top:1px}
.pill{display:inline-block;font-size:.6rem;font-weight:700;text-transform:uppercase;letter-spacing:.05em;padding:2px 9px;border-radius:20px}
.pr{background:rgba(220,38,38,.1);color:var(--red)}.po{background:rgba(234,88,12,.1);color:var(--orange)}
.pg{background:rgba(22,163,74,.1);color:var(--green)}.pb{background:rgba(74,108,247,.1);color:var(--blue)}
.pp{background:rgba(124,58,237,.1);color:var(--purple)}.pm{background:rgba(107,125,179,.1);color:var(--muted)}
.db{display:inline-block;font-size:.68rem;font-weight:700;padding:2px 8px;border-radius:7px}
.dr{background:rgba(220,38,38,.1);color:var(--red)}.do{background:rgba(234,88,12,.1);color:var(--orange)}.dg{background:rgba(22,163,74,.1);color:var(--green)}
.doc{display:flex;align-items:center;gap:5px;font-size:.73rem}
.dd{width:7px;height:7px;border-radius:50%;flex-shrink:0}
.dsg{background:var(--green2)}.dso{background:var(--orange2)}.dst{background:var(--teal)}.dsn{background:#cbd5e1}
.hb{display:flex;align-items:center;gap:6px}
.hbt{flex:1;height:5px;background:var(--s2);border-radius:3px;overflow:hidden}
.hbf{height:100%;border-radius:3px}
.hbn{font-size:.69rem;font-weight:700;width:22px;text-align:right}
.up{color:var(--green)}.down{color:var(--red)}
.churn-list{display:flex;flex-direction:column;gap:7px}
.ci{display:flex;align-items:center;gap:10px;padding:9px 12px;background:var(--s2);border-radius:9px}
.cirk{width:22px;height:22px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:.67rem;font-weight:800;flex-shrink:0;color:white}
.cib{flex:1}
.cin{font-size:.77rem;font-weight:700;color:var(--navy)}
.cid{font-size:.66rem;color:var(--muted);margin-top:1px}
.cip{font-size:.86rem;font-weight:800;flex-shrink:0}
.nps-big{font-size:3.7rem;font-weight:800;color:var(--blue);letter-spacing:-.04em;line-height:1}
.nw{display:flex;align-items:center;gap:20px;margin-bottom:12px}
.nr{flex:1;display:flex;flex-direction:column;gap:6px}
.nrow{display:flex;align-items:center;gap:8px;font-size:.72rem}
.nl{width:72px;color:var(--muted)}.ntr{flex:1;height:6px;background:var(--s2);border-radius:3px;overflow:hidden}
.nf{height:100%;border-radius:3px}.np{width:32px;text-align:right;font-weight:700}
.mini2{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.ms{background:var(--s2);border-radius:9px;padding:10px 13px}
.msl{font-size:.65rem;color:var(--muted)}.msv{font-size:1.2rem;font-weight:800;color:var(--navy)}
.sig-item{display:flex;align-items:center;justify-content:space-between;background:var(--s2);border-radius:9px;padding:9px 13px;margin-bottom:7px}
.sig-item:last-child{margin-bottom:0}
.signame{font-size:.76rem;font-weight:700;color:var(--navy)}
.sigmeta{font-size:.66rem;color:var(--muted);margin-top:1px}
.sigsc{font-size:.98rem;font-weight:800}
.expt{width:100%;border-collapse:collapse}
.expt th{font-size:.6rem;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--muted);text-align:left;padding:0 10px 10px 0;border-bottom:2px solid var(--border)}
.expt td{padding:9px 10px 9px 0;border-bottom:1px solid var(--border);vertical-align:middle;font-size:.76rem}
.expt tr:last-child td{border-bottom:none}
.wi{display:flex;align-items:center;justify-content:space-between;background:var(--s2);border-radius:9px;padding:9px 13px;margin-bottom:7px}
.wi:last-child{margin-bottom:0}
.wn{font-size:.76rem;font-weight:600;color:var(--navy)}.wm{font-size:.65rem;color:var(--muted);margin-top:1px}
.wr{font-size:.93rem;font-weight:800}.wl{font-size:.62rem;color:var(--muted)}
.af{display:flex;flex-direction:column}
.aitem{display:flex;gap:10px;padding:9px 0;border-bottom:1px solid var(--border)}
.aitem:last-child{border-bottom:none}
.aico{width:29px;height:29px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:.83rem;flex-shrink:0;margin-top:1px}
.atitle{font-size:.76rem;font-weight:600;color:var(--navy)}
.ameta{font-size:.67rem;color:var(--muted);margin-top:2px}
.asrc{font-size:.57rem;font-weight:700;text-transform:uppercase;color:var(--muted);margin-top:2px}
@keyframes fu{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}
@media(max-width:1100px){.g3,.g32{grid-template-columns:1fr 1fr}.g2{grid-template-columns:1fr}.lcbar{grid-template-columns:1fr 1fr}}
@media(max-width:680px){.g3,.g32,.g2,.lcbar{grid-template-columns:1fr}.hkpis{display:none}}
</style>
</head>
<body>
<nav>
  <div class="logo">
    <div class="bulb">💡</div>
    <div><div class="lname">GoLearn</div><div class="lsub">part of eduhouse</div></div>
  </div>
  <div style="font-size:.76rem;color:var(--muted);font-weight:500">Customer Marketing Manager · Q2 2026</div>
  <div class="nav-r">
    <span class="src shs"><span class="dot"></span>HubSpot</span>
    <span class="src sga"><span class="dot"></span>GetAccept</span>
  </div>
</nav>
<div class="page">

  <!-- HERO -->
  <div class="hero">
    <div>
      <h1>Customer Marketing <span>Command Center</span></h1>
      <p>Struktureret efter de 4 livscyklusfaser i din rolle — Onboarding · Adoption · Renewal · Expansion<br>Data fra HubSpot CRM, HubSpot Email, HubSpot Events & GetAccept</p>
    </div>
    <div class="hkpis">
      <div class="hkpi"><div class="hkv" style="color:var(--blue)">112%</div><div class="hkl">Net Rev. Retention</div><div class="hkd up">↑ +4% vs Q1</div></div>
      <div class="hkpi"><div class="hkv" style="color:var(--green)">€48k</div><div class="hkl">Expansion Revenue</div><div class="hkd up">↑ +12% vs Q1</div></div>
      <div class="hkpi"><div class="hkv" style="color:var(--orange)">3,2%</div><div class="hkl">Churn Rate</div><div class="hkd down">↑ +0,4% vs Q1</div></div>
      <div class="hkpi"><div class="hkv" style="color:var(--blue)">+61</div><div class="hkl">NPS Score</div><div class="hkd up">↑ +5 vs Q1</div></div>
    </div>
  </div>

  <!-- LIFECYCLE BAR -->
  <div class="lcbar">
    <div class="lc p1"><div class="lclbl">Fase 1 · 0–90 dage</div><div class="lct">Onboarding</div><div class="lcst"><div><div class="lcsv">78%</div><div class="lcsl">Completion rate</div></div><div><div class="lcsv">14d</div><div class="lcsl">Tid til 1. kursus</div></div></div></div>
    <div class="lc p2"><div class="lclbl">Fase 2 · Løbende</div><div class="lct">Adoption & Værdi</div><div class="lcst"><div><div class="lcsv">62%</div><div class="lcsl">Aktive lærere/md</div></div><div><div class="lcsv">3,4</div><div class="lcsl">Kurser/bruger</div></div></div></div>
    <div class="lc p3"><div class="lclbl">Fase 3 · –90 til 0 dage</div><div class="lct">Renewal Forberedelse</div><div class="lcst"><div><div class="lcsv">6</div><div class="lcsl">I pipeline</div></div><div><div class="lcsv">68%</div><div class="lcsl">Underskrevet</div></div></div></div>
    <div class="lc p4"><div class="lclbl">Fase 4 · Løbende</div><div class="lct">Expansion</div><div class="lcst"><div><div class="lcsv">59</div><div class="lcsl">Udvidede konti</div></div><div><div class="lcsv">108</div><div class="lcsl">Klar til upsell</div></div></div></div>
  </div>

  <!-- FASE 1: ONBOARDING -->
  <div class="sec s1">① Onboarding — 0–90 dage</div>
  <div class="g32 mb">
    <div class="card">
      <div class="ch"><div class="ct">Onboarding completion funnel</div><span class="tag t1">HubSpot Lifecycle</span></div>
      <div class="ob-funnel">
        <div class="ob-step"><div class="ob-lbl">Konto oprettet</div><div class="ob-track"><div class="ob-fill" style="width:100%;background:var(--ph1)">284 kunder</div></div><div class="ob-val" style="color:var(--ph1)">100%</div></div>
        <div class="ob-step"><div class="ob-lbl">Onboarding mail åbnet</div><div class="ob-track"><div class="ob-fill" style="width:91%;background:#5b7cf9">258 kunder</div></div><div class="ob-val" style="color:#5b7cf9">91%</div></div>
        <div class="ob-step"><div class="ob-lbl">Første login &lt; 7 dage</div><div class="ob-track"><div class="ob-fill" style="width:84%;background:var(--ph2)">239 kunder</div></div><div class="ob-val" style="color:var(--ph2)">84%</div></div>
        <div class="ob-step"><div class="ob-lbl">Første kursus gennemført</div><div class="ob-track"><div class="ob-fill" style="width:78%;background:#0e9fba">221 kunder</div></div><div class="ob-val" style="color:#0e9fba">78%</div></div>
        <div class="ob-step"><div class="ob-lbl">Onboarding 100% done</div><div class="ob-track"><div class="ob-fill" style="width:61%;background:var(--yellow)">173 kunder</div></div><div class="ob-val" style="color:#c47d00">61%</div></div>
      </div>
    </div>
    <div class="card">
      <div class="ch"><div class="ct">Time to First Value</div><span class="tag t1">HubSpot + LMS</span></div>
      <p style="font-size:.72rem;color:var(--muted);margin-bottom:12px;line-height:1.5">Tid fra kontraktstart til første kursus gennemført. Kortere TTFV = lavere churn.</p>
      <div class="ttfv">
        <div class="ttfv-item"><div class="ttfvv" style="color:var(--green)">14d</div><div class="ttfvl">Median TTFV</div></div>
        <div class="ttfv-item"><div class="ttfvv" style="color:var(--blue)">7d</div><div class="ttfvl">Top 25%</div></div>
        <div class="ttfv-item"><div class="ttfvv" style="color:var(--red)">38d</div><div class="ttfvl">Bund 25%</div></div>
      </div>
      <div style="font-size:.65rem;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--muted);margin-bottom:8px">Onboarding email åbningsrate</div>
      <div style="display:flex;flex-direction:column;gap:6px">
        <div style="display:flex;justify-content:space-between;align-items:center;background:var(--s2);border-radius:7px;padding:7px 11px"><span style="font-size:.73rem;font-weight:600">Velkomst (dag 0)</span><span style="font-size:.79rem;font-weight:800;color:var(--green)">88%</span></div>
        <div style="display:flex;justify-content:space-between;align-items:center;background:var(--s2);border-radius:7px;padding:7px 11px"><span style="font-size:.73rem;font-weight:600">Aktiverings-nudge (dag 3)</span><span style="font-size:.79rem;font-weight:800;color:var(--blue)">71%</span></div>
        <div style="display:flex;justify-content:space-between;align-items:center;background:var(--s2);border-radius:7px;padding:7px 11px"><span style="font-size:.73rem;font-weight:600">Check-in (dag 14)</span><span style="font-size:.79rem;font-weight:800;color:var(--orange)">54%</span></div>
        <div style="display:flex;justify-content:space-between;align-items:center;background:var(--s2);border-radius:7px;padding:7px 11px"><span style="font-size:.73rem;font-weight:600">30-dages review</span><span style="font-size:.79rem;font-weight:800;color:var(--muted)">41%</span></div>
      </div>
    </div>
  </div>

  <!-- FASE 2: ADOPTION -->
  <div class="sec s2">② Adoption & Værdiforankring</div>
  <div class="g3 mb">
    <div class="card">
      <div class="ch"><div class="ct">Seat utilization — top konti</div><span class="tag t2">LMS + HubSpot</span></div>
      <div class="adopt-grid">
        <div class="ai-item"><div class="ain">Norlys</div><div class="aib"><div class="aif" style="width:91%;background:var(--green2)"></div></div><div class="aim"><span style="color:var(--green);font-weight:700">91%</span><span>237/260</span></div></div>
        <div class="ai-item"><div class="ain">Bankdata</div><div class="aib"><div class="aif" style="width:84%;background:var(--green2)"></div></div><div class="aim"><span style="color:var(--green);font-weight:700">84%</span><span>151/180</span></div></div>
        <div class="ai-item"><div class="ain">DSB</div><div class="aib"><div class="aif" style="width:71%;background:var(--teal)"></div></div><div class="aim"><span style="color:var(--ph2);font-weight:700">71%</span><span>241/340</span></div></div>
        <div class="ai-item"><div class="ain">Aarhus Kommune</div><div class="aib"><div class="aif" style="width:38%;background:var(--orange2)"></div></div><div class="aim"><span style="color:var(--orange);font-weight:700">38%</span><span>312/820</span></div></div>
        <div class="ai-item"><div class="ain">Techstep A/S</div><div class="aib"><div class="aif" style="width:29%;background:var(--red2)"></div></div><div class="aim"><span style="color:var(--red);font-weight:700">29%</span><span>35/120</span></div></div>
        <div class="ai-item"><div class="ain">Reg. Midtjylland</div><div class="aib"><div class="aif" style="width:22%;background:var(--red2)"></div></div><div class="aim"><span style="color:var(--red);font-weight:700">22%</span><span>308/1400</span></div></div>
      </div>
    </div>
    <div class="card">
      <div class="ch"><div class="ct">Kursusengagement per kategori</div><span class="tag t2">LMS data</span></div>
      <div class="bars">
        <div class="brow"><div class="bl">AI & Machine Learning</div><div class="bt"><div class="bf" style="width:88%;background:var(--blue)"></div></div><div class="bv">88%</div></div>
        <div class="brow"><div class="bl">Cybersikkerhed</div><div class="bt"><div class="bf" style="width:74%;background:var(--teal)"></div></div><div class="bv">74%</div></div>
        <div class="brow"><div class="bl">Ledelse</div><div class="bt"><div class="bf" style="width:61%;background:var(--yellow)"></div></div><div class="bv">61%</div></div>
        <div class="brow"><div class="bl">Compliance & GDPR</div><div class="bt"><div class="bf" style="width:55%;background:var(--purple)"></div></div><div class="bv">55%</div></div>
        <div class="brow"><div class="bl">Digitale færdigheder</div><div class="bt"><div class="bf" style="width:43%;background:var(--muted)"></div></div><div class="bv">43%</div></div>
        <div class="brow"><div class="bl">Projektledelse</div><div class="bt"><div class="bf" style="width:38%;background:#b2bfd8"></div></div><div class="bv">38%</div></div>
      </div>
    </div>
    <div class="card">
      <div class="ch"><div class="ct">Trigger-baserede kampagner</div><span class="tag ths">HubSpot Automation</span></div>
      <div class="trig-list">
        <div class="trig"><div class="trico" style="background:rgba(22,163,74,.1)">🟢</div><div class="trib"><div class="trin">Low engagement alert</div><div class="trid">Udløser ved &lt;30% utilization i 30 dage</div></div><div class="tris"><div><div class="trisv" style="color:var(--green)">68%</div><div class="trisl">Åbningsrate</div></div><div><div class="trisv">14</div><div class="trisl">Aktive nu</div></div></div></div>
        <div class="trig"><div class="trico" style="background:rgba(74,108,247,.1)">📘</div><div class="trib"><div class="trin">Kursusanbefaling</div><div class="trid">Sendt efter 2 gennemførte kurser</div></div><div class="tris"><div><div class="trisv" style="color:var(--blue)">54%</div><div class="trisl">Klikrate</div></div><div><div class="trisv">89</div><div class="trisl">Sendt i dag</div></div></div></div>
        <div class="trig"><div class="trico" style="background:rgba(245,166,35,.12)">🎓</div><div class="trib"><div class="trin">Milestone celebration</div><div class="trid">10 kurser gennemført af organisation</div></div><div class="tris"><div><div class="trisv" style="color:var(--yellow)">71%</div><div class="trisl">Åbningsrate</div></div><div><div class="trisv">6</div><div class="trisl">Denne uge</div></div></div></div>
        <div class="trig"><div class="trico" style="background:rgba(8,145,178,.1)">📣</div><div class="trib"><div class="trin">Webinar invitation</div><div class="trid">Segmenteret på kursuskategori</div></div><div class="tris"><div><div class="trisv" style="color:var(--ph2)">48%</div><div class="trisl">Åbningsrate</div></div><div><div class="trisv">84</div><div class="trisl">Tilmeldte</div></div></div></div>
      </div>
    </div>
  </div>

  <!-- FASE 3: RENEWAL -->
  <div class="sec s3">③ Renewal Forberedelse — GetAccept + HubSpot</div>
  <div class="mb">
    <div class="card">
      <div class="ch"><div class="ct">Renewal pipeline — næste 90 dage</div><div class="tags"><span class="tag ths">HubSpot CRM</span><span class="tag tga">GetAccept</span></div></div>
      <table class="rt">
        <thead><tr><th>Kunde</th><th>Renewal dato</th><th>Dage tilbage</th><th>ARR</th><th>GetAccept status</th><th>Sidst kontaktet</th><th>Seat util.</th><th>Health</th><th>Handling</th></tr></thead>
        <tbody>
          <tr><td><div class="cn">Region Midtjylland</div><div class="cs">Offentlig · 1.400 seats</div></td><td style="color:var(--muted);font-size:.73rem">28. apr 2026</td><td><span class="db dr">12 dage</span></td><td><b>€42.000</b></td><td><div class="doc"><span class="dd dst"></span>Sendt · ikke åbnet</div></td><td style="color:var(--red);font-weight:600;font-size:.73rem">41 dage siden</td><td style="color:var(--red);font-weight:700">22%</td><td><div class="hb"><div class="hbt"><div class="hbf" style="width:22%;background:var(--red2)"></div></div><span class="hbn" style="color:var(--red)">22</span></div></td><td><span class="pill pr">Ring nu</span></td></tr>
          <tr><td><div class="cn">Aarhus Kommune</div><div class="cs">Offentlig · 820 seats</div></td><td style="color:var(--muted);font-size:.73rem">5. maj 2026</td><td><span class="db dr">19 dage</span></td><td><b>€28.000</b></td><td><div class="doc"><span class="dd dso"></span>Åbnet 3 gange</div></td><td style="color:var(--orange);font-weight:600;font-size:.73rem">32 dage siden</td><td style="color:var(--orange);font-weight:700">38%</td><td><div class="hb"><div class="hbt"><div class="hbf" style="width:28%;background:var(--red2)"></div></div><span class="hbn" style="color:var(--red)">28</span></div></td><td><span class="pill po">Book møde</span></td></tr>
          <tr><td><div class="cn">Techstep A/S</div><div class="cs">Privat · 120 seats</div></td><td style="color:var(--muted);font-size:.73rem">18. maj 2026</td><td><span class="db do">32 dage</span></td><td><b>€8.400</b></td><td><div class="doc"><span class="dd dst"></span>Sendt · ikke åbnet</div></td><td style="color:var(--muted);font-size:.73rem">18 dage siden</td><td style="color:var(--orange);font-weight:700">29%</td><td><div class="hb"><div class="hbt"><div class="hbf" style="width:45%;background:var(--orange2)"></div></div><span class="hbn" style="color:var(--orange)">45</span></div></td><td><span class="pill po">Send case</span></td></tr>
          <tr><td><div class="cn">DSB</div><div class="cs">Offentlig · 340 seats</div></td><td style="color:var(--muted);font-size:.73rem">2. jun 2026</td><td><span class="db do">47 dage</span></td><td><b>€14.200</b></td><td><div class="doc"><span class="dd dso"></span>Åbnet · ikke underskrevet</div></td><td style="color:var(--muted);font-size:.73rem">7 dage siden</td><td style="color:var(--ph2);font-weight:700">71%</td><td><div class="hb"><div class="hbt"><div class="hbf" style="width:63%;background:var(--teal)"></div></div><span class="hbn" style="color:var(--ph2)">63</span></div></td><td><span class="pill pb">Follow up</span></td></tr>
          <tr><td><div class="cn">Norlys</div><div class="cs">Privat · 260 seats</div></td><td style="color:var(--muted);font-size:.73rem">15. jun 2026</td><td><span class="db dg">60 dage</span></td><td><b>€11.800</b></td><td><div class="doc"><span class="dd dsg"></span>Underskrevet ✓</div></td><td style="color:var(--muted);font-size:.73rem">5 dage siden</td><td style="color:var(--green);font-weight:700">91%</td><td><div class="hb"><div class="hbt"><div class="hbf" style="width:78%;background:var(--green2)"></div></div><span class="hbn" style="color:var(--green)">78</span></div></td><td><span class="pill pg">Upsell</span></td></tr>
          <tr><td><div class="cn">Bankdata</div><div class="cs">Privat · 180 seats</div></td><td style="color:var(--muted);font-size:.73rem">22. jun 2026</td><td><span class="db dg">67 dage</span></td><td><b>€9.600</b></td><td><div class="doc"><span class="dd dsn"></span>Ikke sendt endnu</div></td><td style="color:var(--muted);font-size:.73rem">3 dage siden</td><td style="color:var(--green);font-weight:700">84%</td><td><div class="hb"><div class="hbt"><div class="hbf" style="width:82%;background:var(--green2)"></div></div><span class="hbn" style="color:var(--green)">82</span></div></td><td><span class="pill pb">Send dok.</span></td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="g2 mb">
    <div class="card">
      <div class="ch"><div class="ct">Top churn-drivere</div><span class="tag t3">HubSpot + CS data</span></div>
      <div class="churn-list">
        <div class="ci"><div class="cirk" style="background:var(--red)">#1</div><div class="cib"><div class="cin">Lav seat utilization (&lt;30%)</div><div class="cid">Platformen ikke forankret i daglig drift</div></div><div class="cip" style="color:var(--red)">38%</div></div>
        <div class="ci"><div class="cirk" style="background:var(--orange)">#2</div><div class="cib"><div class="cin">Ingen kontakt seneste 45+ dage</div><div class="cid">Manglende relation til beslutningstagere</div></div><div class="cip" style="color:var(--orange)">24%</div></div>
        <div class="ci"><div class="cirk" style="background:var(--yellow)">#3</div><div class="cib"><div class="cin">Onboarding ikke gennemført</div><div class="cid">Kom aldrig rigtig i gang</div></div><div class="cip" style="color:#c47d00">18%</div></div>
        <div class="ci"><div class="cirk" style="background:var(--blue)">#4</div><div class="cib"><div class="cin">Budget/prioritering internt</div><div class="cid">Skift i ledelse eller strategi hos kunden</div></div><div class="cip" style="color:var(--blue)">12%</div></div>
        <div class="ci"><div class="cirk" style="background:var(--muted)">#5</div><div class="cib"><div class="cin">Konkurrent overtog</div><div class="cid">Pris eller indholdsoverlap</div></div><div class="cip" style="color:var(--muted)">8%</div></div>
      </div>
    </div>
    <div class="card">
      <div class="ch"><div class="ct">NPS & Kundeloyalitet</div><span class="tag ths">HubSpot Survey</span></div>
      <div class="nw">
        <div class="nps-big">+61</div>
        <div class="nr">
          <div class="nrow"><div class="nl">Promoters</div><div class="ntr"><div class="nf" style="width:72%;background:var(--green2)"></div></div><div class="np" style="color:var(--green)">72%</div></div>
          <div class="nrow"><div class="nl">Passives</div><div class="ntr"><div class="nf" style="width:17%;background:var(--orange2)"></div></div><div class="np" style="color:var(--orange)">17%</div></div>
          <div class="nrow"><div class="nl">Detractors</div><div class="ntr"><div class="nf" style="width:11%;background:var(--red2)"></div></div><div class="np" style="color:var(--red)">11%</div></div>
        </div>
      </div>
      <div class="mini2">
        <div class="ms"><div class="msl">Svar i alt</div><div class="msv">147</div></div>
        <div class="ms"><div class="msl">Svarprocent</div><div class="msv">52%</div></div>
        <div class="ms"><div class="msl">SaaS benchmark</div><div class="msv" style="color:var(--muted)">+42</div></div>
        <div class="ms"><div class="msl">Over benchmark</div><div class="msv" style="color:var(--green)">+19 ↑</div></div>
      </div>
    </div>
  </div>

  <!-- FASE 4: EXPANSION -->
  <div class="sec s4">④ Expansion Initiativer</div>
  <div class="g3 mb">
    <div class="card">
      <div class="ch"><div class="ct">Upsell-signaler (PQA score)</div><span class="tag t4">HubSpot + LMS</span></div>
      <p style="font-size:.71rem;color:var(--muted);margin-bottom:11px;line-height:1.5">Konti med høj utilization og aktivt engagement — klar til upsell-samtale.</p>
      <div class="sig-item"><div><div class="signame">Norlys</div><div class="sigmeta">91% utilization · NPS 9 · Renewal underskrevet</div></div><div class="sigsc" style="color:var(--green)">96 🔥</div></div>
      <div class="sig-item"><div><div class="signame">Bankdata</div><div class="sigmeta">84% utilization · NPS 8 · Webinar deltager</div></div><div class="sigsc" style="color:var(--green)">88</div></div>
      <div class="sig-item"><div><div class="signame">DSB</div><div class="sigmeta">71% utilization · 3 kurser seneste md.</div></div><div class="sigsc" style="color:var(--ph2)">74</div></div>
      <div class="sig-item"><div><div class="signame">Vejle Kommune</div><div class="sigmeta">100% AI Basics · Spurgt om mere indhold</div></div><div class="sigsc" style="color:var(--ph2)">71</div></div>
      <div class="sig-item"><div><div class="signame">GLS</div><div class="sigmeta">68% utilization · Compliance kursus afsluttet</div></div><div class="sigsc" style="color:var(--yellow)">62</div></div>
    </div>
    <div class="card">
      <div class="ch"><div class="ct">Expansion pipeline</div><span class="tag t4">HubSpot Pipeline</span></div>
      <table class="expt">
        <thead><tr><th>Konto</th><th>Type</th><th>Værdi</th><th>Status</th></tr></thead>
        <tbody>
          <tr><td><div style="font-weight:700">Norlys</div><div style="font-size:.64rem;color:var(--muted)">+80 seats</div></td><td><span class="pill pg">Seats</span></td><td style="font-weight:700;color:var(--green)">€4.800</td><td><span class="pill pg">Lukket ✓</span></td></tr>
          <tr><td><div style="font-weight:700">Bankdata</div><div style="font-size:.64rem;color:var(--muted)">Cyberpakke</div></td><td><span class="pill pb">Modul</span></td><td style="font-weight:700;color:var(--blue)">€3.200</td><td><span class="pill po">Tilbud sendt</span></td></tr>
          <tr><td><div style="font-weight:700">DSB</div><div style="font-size:.64rem;color:var(--muted)">+60 seats</div></td><td><span class="pill pg">Seats</span></td><td style="font-weight:700;color:var(--green)">€3.600</td><td><span class="pill pb">I dialog</span></td></tr>
          <tr><td><div style="font-weight:700">Vejle Kommune</div><div style="font-size:.64rem;color:var(--muted)">AI Advanced</div></td><td><span class="pill pp">Modul</span></td><td style="font-weight:700;color:var(--purple)">€2.900</td><td><span class="pill pb">Forslag klar</span></td></tr>
          <tr><td><div style="font-weight:700">GLS</div><div style="font-size:.64rem;color:var(--muted)">Ledelsespakke</div></td><td><span class="pill pp">Modul</span></td><td style="font-weight:700;color:var(--muted)">€1.800</td><td><span class="pill pm">Ikke kontaktet</span></td></tr>
        </tbody>
      </table>
      <div style="margin-top:12px;padding-top:11px;border-top:1px solid var(--border);display:flex;justify-content:space-between;align-items:center">
        <span style="font-size:.72rem;color:var(--muted)">Total pipeline værdi</span>
        <span style="font-size:1.05rem;font-weight:800;color:var(--green)">€16.300</span>
      </div>
    </div>
    <div class="card">
      <div class="ch"><div class="ct">Webinarer & Events</div><span class="tag ths">HubSpot Events</span></div>
      <div class="wi"><div><div class="wn">AI Trends 2026</div><div class="wm">14. apr · 84 tilmeldte</div></div><div style="text-align:right"><div class="wr" style="color:var(--green)">76%</div><div class="wl">fremmøde</div></div></div>
      <div class="wi"><div><div class="wn">Cybersikkerhed i praksis</div><div class="wm">28. mar · 61 tilmeldte</div></div><div style="text-align:right"><div class="wr" style="color:var(--green)">68%</div><div class="wl">fremmøde</div></div></div>
      <div class="wi"><div><div class="wn">GDPR & AI-forordningen</div><div class="wm">12. mar · 48 tilmeldte</div></div><div style="text-align:right"><div class="wr" style="color:var(--teal)">54%</div><div class="wl">fremmøde</div></div></div>
      <div class="wi"><div><div class="wn">Nordic L&D Summit</div><div class="wm">18. jan · 112 tilmeldte</div></div><div style="text-align:right"><div class="wr" style="color:var(--green)">82%</div><div class="wl">fremmøde</div></div></div>
      <div style="margin-top:12px;padding-top:11px;border-top:1px solid var(--border)">
        <div style="font-size:.64rem;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--muted);margin-bottom:8px">Seneste aktivitet</div>
        <div class="af">
          <div class="aitem"><div class="aico" style="background:rgba(239,68,68,.08)">🔴</div><div><div class="atitle">Renewal ikke åbnet — Reg. Midtjylland</div><div class="ameta">Sendt for 11 dage siden · €42k i fare</div><div class="asrc">GetAccept</div></div></div>
          <div class="aitem"><div class="aico" style="background:rgba(22,163,74,.1)">✅</div><div><div class="atitle">Renewal underskrevet — Norlys</div><div class="ameta">€11.800 · +80 seats upsell inkl.</div><div class="asrc">GetAccept</div></div></div>
          <div class="aitem"><div class="aico" style="background:rgba(74,108,247,.1)">📋</div><div><div class="atitle">NPS score 9 — Bankdata</div><div class="ameta">"Fremragende indhold og support"</div><div class="asrc">HubSpot Survey</div></div></div>
        </div>
      </div>
    </div>
  </div>

  <div style="text-align:center;margin-top:8px;font-size:.61rem;color:var(--muted)">
    GoLearn Customer Marketing Manager · Demo-data · Baseret på jobprofil: Onboarding · Adoption · Renewal · Expansion · Forbind HubSpot API + GetAccept API for live data
  </div>
</div>
</body>
</html>
