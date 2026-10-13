#<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>BAS | Sistemas de Asistencia Biónica</title>
<meta name="description" content="BAS desarrolla tecnologías accesibles para la rehabilitación de la mano: un guante terapéutico y una prótesis biónica. Proyecto ganador en Hecho en Merlo 2025.">
<link rel="icon" type="image/png" href="img/logo-bas-azul.png">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;800&display=swap" rel="stylesheet">
<style>
:root{
  --navy:#020247; --navy-deep:#01012e; --royal:#0b0b8f;
  --paper:#fff; --mist:#eceeff; --ink:#0a0a3a;
  --sky:#8fb0ff; --signal:#5fe3c4;
  --maxw:1120px;
  --font:'Poppins',system-ui,-apple-system,'Segoe UI',Roboto,sans-serif;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;scroll-padding-top:76px}
body{font-family:var(--font);color:var(--ink);background:var(--paper);line-height:1.65;font-size:1.0625rem;-webkit-font-smoothing:antialiased}
img{max-width:100%;display:block}
button{font:inherit;color:inherit;cursor:pointer}
a{color:inherit}
:focus-visible{outline:3px solid var(--signal);outline-offset:3px;border-radius:6px}
.wrap{max-width:var(--maxw);margin:0 auto;padding:0 1.25rem}
h1,h2,h3,h4{font-weight:800;line-height:1.12;letter-spacing:-.02em}
h2{font-size:clamp(2rem,5vw,3rem);margin-bottom:1rem}
h3{font-size:1.5rem;margin-bottom:.6rem}
h4{font-size:1.08rem;font-weight:600;letter-spacing:0;margin-bottom:.3rem}
.lead{font-size:clamp(1.08rem,2.3vw,1.35rem);line-height:1.55;max-width:44rem}
p+p{margin-top:1rem}
.small{font-size:.9rem;opacity:.85}

/* ---------- secciones y olas ---------- */
.sec{position:relative;background:var(--bg);color:var(--fg,#fff);padding:5.5rem 0}
.sec.light{--bg:var(--paper);--fg:var(--ink)}
.sec.mist{--bg:var(--mist);--fg:var(--ink)}
.sec.navy{--bg:var(--navy);--fg:#fff}
.sec.deep{--bg:var(--navy-deep);--fg:#fff}
.sec.royal{--bg:var(--royal);--fg:#fff}
.sec>.wave{position:absolute;left:0;top:-59px;width:100%;height:60px;display:block;pointer-events:none}
.sec>.wave path{fill:var(--bg)}

/* ---------- header ---------- */
header{position:sticky;top:0;z-index:60;background:rgba(2,2,71,.95);backdrop-filter:blur(8px);color:#fff}
.nav{display:flex;align-items:center;justify-content:space-between;height:68px;gap:1rem}
.brand{display:flex;align-items:center;gap:.65rem;text-decoration:none;font-weight:800;font-size:1.6rem;letter-spacing:-.02em;line-height:1}
.brand img{height:36px;width:auto}
.nav ul{list-style:none;display:flex;gap:1.35rem;align-items:center}
.nav ul a{text-decoration:none;font-size:.9rem;font-weight:500;opacity:.88;padding:.4rem 0;border-bottom:2px solid transparent}
.nav ul a:hover{opacity:1;border-bottom-color:var(--sky)}
.nav ul a.pill{background:#fff;color:var(--navy);padding:.45rem 1.1rem;border-radius:999px;border:0;font-weight:600;opacity:1}
.burger{display:none;background:none;border:0;color:#fff;padding:.5rem}
.burger svg{width:28px;height:28px}
@media (max-width:1020px){
  .burger{display:block}
  .nav ul{position:absolute;top:68px;left:0;right:0;flex-direction:column;align-items:stretch;gap:0;background:var(--navy-deep);padding:.5rem 1.25rem 1.25rem;display:none}
  .nav ul.open{display:flex}
  .nav ul a{display:block;padding:.9rem 0;border-bottom:1px solid rgba(255,255,255,.1);font-size:1.05rem}
  .nav ul a.pill{margin-top:.8rem;text-align:center;padding:.8rem}
}

/* ---------- hero ---------- */
.hero{background:var(--navy);color:#fff;padding:4.5rem 0 6.5rem;overflow:hidden}
.hero .wrap{display:grid;grid-template-columns:1.15fr .85fr;gap:2rem;align-items:center}
.lockup{display:flex;align-items:center;gap:clamp(1rem,3vw,2rem)}
.lockup img{width:clamp(90px,15vw,170px);height:auto}
.lockup h1{font-size:clamp(5rem,15vw,9.5rem);line-height:.82;letter-spacing:-.04em}
.hero .sub{font-size:clamp(1.15rem,3vw,1.7rem);font-weight:600;margin:1.2rem 0 1.5rem}
.award{background:#fff;color:var(--navy);border-radius:20px;padding:1.1rem 1.4rem;max-width:34rem;font-size:.97rem;line-height:1.5}
.cta-row{display:flex;flex-wrap:wrap;gap:.8rem;margin-top:1.7rem}
.btn{display:inline-block;padding:.85rem 1.6rem;border-radius:999px;font-weight:600;text-decoration:none;border:2px solid #fff;transition:background .2s,color .2s;background:none}
.btn.solid{background:#fff;color:var(--navy)}
.btn.solid:hover{background:var(--sky);border-color:var(--sky)}
.btn.ghost:hover{background:rgba(255,255,255,.14)}
.hero-art{position:relative;display:grid;place-items:center;min-height:440px}
.hero-art::before{content:"";position:absolute;width:min(420px,92%);aspect-ratio:1;background:var(--royal);border-radius:58% 42% 55% 45%/48% 56% 44% 52%}
.hero-art img{position:relative;max-height:520px;width:auto;filter:drop-shadow(0 22px 30px rgba(0,0,40,.5))}
@media (max-width:860px){
  .hero{padding:3rem 0 5.5rem}
  .hero .wrap{grid-template-columns:1fr}
  .hero-art{min-height:340px;order:-1}
  .hero-art img{max-height:360px}
}

/* ---------- franja de validación ---------- */
.strip{background:var(--royal);color:#fff;padding:2rem 0 4.5rem}
.strip ul{list-style:none;display:grid;grid-template-columns:repeat(4,1fr);gap:1.4rem}
.strip li{border-left:3px solid var(--sky);padding-left:1rem;font-size:.95rem;line-height:1.45}
.strip b{display:block;font-weight:600;font-size:1.02rem}
@media (max-width:860px){.strip ul{grid-template-columns:1fr 1fr}}
@media (max-width:520px){.strip ul{grid-template-columns:1fr}}

/* ---------- proyecto ---------- */
.systems{display:grid;grid-template-columns:1fr 1fr;gap:1.6rem;margin-top:2.6rem}
.syscard{display:grid;grid-template-columns:.9fr 1.1fr;background:var(--navy);color:#fff;border-radius:28px;overflow:hidden;text-decoration:none;transition:transform .2s}
.syscard:hover{transform:translateY(-4px)}
.syscard .im{background:var(--royal);display:grid;place-items:center;padding:1rem}
.syscard .im img{max-height:290px;width:auto;object-fit:contain}
.syscard.photo .im img{border-radius:14px;max-height:290px}
.syscard .tx{padding:1.6rem 1.4rem}
.syscard h3{font-size:1.45rem}
.syscard p{font-size:.95rem;opacity:.92;line-height:1.5}
.syscard .go{display:inline-block;margin-top:1rem;font-weight:600;border-bottom:2px solid var(--sky)}
@media (max-width:900px){.systems{grid-template-columns:1fr}}
@media (max-width:480px){.syscard{grid-template-columns:1fr}.syscard .im img{max-height:240px}}

/* ---------- problema ---------- */
.panel-w{background:#fff;border-radius:28px;padding:clamp(1.4rem,4vw,2.8rem);box-shadow:0 20px 50px -28px rgba(2,2,71,.4);margin-top:2.4rem}
.stats{display:grid;grid-template-columns:auto 1fr 1fr;gap:2.2rem;align-items:center;padding-bottom:2.4rem;border-bottom:2px solid var(--mist)}
.ring{--p:70;width:150px;aspect-ratio:1;border-radius:50%;background:conic-gradient(var(--royal) calc(var(--p)*1%),#d8dbf3 0);display:grid;place-items:center;position:relative}
.ring::before{content:"";position:absolute;inset:20px;background:#fff;border-radius:50%}
.ring b{position:relative;font-size:2rem;font-weight:800;color:var(--royal);letter-spacing:-.03em}
.stat b.big{display:block;font-size:clamp(1.8rem,4vw,2.7rem);font-weight:800;color:var(--royal);line-height:1.05;letter-spacing:-.03em}
.stat span{display:block;margin-top:.5rem;font-size:.97rem;line-height:1.45}
.stat small{display:block;margin-top:.35rem;font-size:.8rem;color:#4a4a7a}
.dots-wrap{display:grid;grid-template-columns:1fr 1fr;gap:2.4rem;align-items:center;padding-top:2.4rem}
.dots{display:grid;grid-template-columns:repeat(20,1fr);gap:5px;max-width:430px}
.dots i{aspect-ratio:1;border-radius:50%;background:#d8dbf3;transition:background .35s}
.dots i.on{background:var(--royal)}
.dots i.range{background:#7b7bd6}
.legend{display:flex;flex-wrap:wrap;gap:.3rem 1.2rem;margin-top:1rem;font-size:.85rem}
.legend span::before{content:"";display:inline-block;width:.8rem;height:.8rem;border-radius:50%;margin-right:.45rem;vertical-align:-1px}
.l1::before{background:var(--royal)}.l2::before{background:#7b7bd6}.l3::before{background:#d8dbf3}
.dots-wrap h3{color:var(--navy);font-size:1.4rem}
@media (max-width:860px){.stats{grid-template-columns:1fr;gap:1.6rem}.dots-wrap{grid-template-columns:1fr}}

/* ---------- órtesis / prótesis ---------- */
.split{display:grid;grid-template-columns:minmax(0,.9fr) minmax(0,1.1fr);gap:3.2rem;align-items:center}
.split.flip>:first-child{order:2}
.for{font-weight:600;color:var(--sky);margin-bottom:.9rem}
.light .for,.mist .for{color:var(--royal)}
.hs-stage{position:relative;background:var(--royal);border-radius:32px;padding:1.2rem;max-width:400px;margin:0 auto}
.hs-stage .box{position:relative}
.hs-stage img.main{width:100%;height:auto}
.hs{position:absolute;width:38px;height:38px;margin:-19px 0 0 -19px;border-radius:50%;border:3px solid #fff;background:rgba(2,2,71,.75);color:#fff;font-weight:800;font-size:.95rem;display:grid;place-items:center;padding:0}
.hs::after{content:"";position:absolute;inset:-8px;border-radius:50%;border:2px solid var(--signal);opacity:.0;animation:ping 2.6s ease-out infinite}
.hs[aria-pressed="true"]{background:var(--signal);color:var(--navy);border-color:#fff}
.hs[aria-pressed="true"]::after{animation:none}
@keyframes ping{0%{transform:scale(.7);opacity:.9}100%{transform:scale(1.5);opacity:0}}
.hs-info{margin-top:1.6rem;background:rgba(255,255,255,.1);border-radius:22px;padding:1.2rem 1.4rem;display:grid;grid-template-columns:90px 1fr;gap:1.1rem;align-items:center;min-height:130px}
.hs-info img{width:90px;height:90px;object-fit:contain;background:#fff;border-radius:16px;padding:6px}
.hs-info.noimg{grid-template-columns:1fr}.hs-info.noimg img{display:none}
.hs-info p{font-size:.97rem;line-height:1.5}
.tiles{display:grid;grid-template-columns:repeat(4,1fr);gap:1rem;margin-top:3.6rem}
.tile{background:var(--royal);border:0;border-radius:22px;padding:1.2rem;text-align:left;color:#fff;display:flex;flex-direction:column;gap:.7rem;min-height:150px;transition:background .2s}
.tile:nth-child(even){background:#12125f}
.tile[aria-expanded="true"]{background:#fff;color:var(--navy)}
.tile svg{width:38px;height:38px;fill:none;stroke:currentColor;stroke-width:2.2;stroke-linecap:round;stroke-linejoin:round}
.tile b{font-weight:600;font-size:1.02rem;line-height:1.3}
.tile p{font-size:.88rem;line-height:1.45;display:none}
.tile[aria-expanded="true"] p{display:block}
.tiles-h{margin-top:3.6rem;font-size:1.7rem}
.tiles-h+.tiles{margin-top:1.2rem}
@media (max-width:900px){.tiles{grid-template-columns:1fr 1fr}.split{grid-template-columns:1fr;gap:2rem}.split.flip>:first-child{order:0}}
.chips{display:flex;flex-wrap:wrap;gap:.5rem;margin-top:1.4rem}
.chip{display:inline-block;border:2px solid currentColor;border-radius:999px;padding:.3rem .9rem;font-size:.88rem;font-weight:500}

/* prótesis */
.photo-frame{background:var(--navy);border-radius:32px;padding:1rem;max-width:400px;margin:0 auto}
.photo-frame img{border-radius:20px;width:100%;height:auto;max-height:620px;object-fit:cover;cursor:zoom-in}
.photo-frame figcaption{color:#fff;font-size:.88rem;padding:.8rem .4rem .2rem}
.chain details{border-bottom:1px solid #c9ccef;padding:.9rem 0}
.chain details:first-child{border-top:1px solid #c9ccef}
.chain summary{cursor:pointer;font-weight:600;list-style:none;display:flex;align-items:center;gap:.9rem}
.chain summary::-webkit-details-marker{display:none}
.chain .n{width:34px;height:34px;flex:none;border-radius:50%;background:var(--navy);color:#fff;display:grid;place-items:center;font-size:.9rem;font-weight:800}
.chain details[open] .n{background:var(--royal);box-shadow:0 0 0 4px rgba(11,11,143,.18)}
.chain summary::after{content:"+";margin-left:auto;font-size:1.5rem;color:var(--royal);transition:transform .2s}
.chain details[open] summary::after{transform:rotate(45deg)}
.chain p{padding:.7rem 0 .2rem 3rem;font-size:.97rem}
.flow{display:flex;flex-wrap:wrap;align-items:center;gap:.5rem;margin-top:1.4rem;font-size:.9rem;font-weight:600}
.flow span{background:var(--navy);color:#fff;border-radius:12px;padding:.5rem .9rem}
.flow span.q{background:var(--royal);border-radius:999px}
.flow i{font-style:normal;color:var(--royal)}
.emg-card{display:flex;gap:1.1rem;align-items:center;background:var(--mist);border-radius:22px;padding:1rem 1.2rem;margin-top:1.8rem}
.emg-card img{width:110px;flex:none}
.emg-card p{font-size:.93rem;line-height:1.5}

/* ---------- probalo ---------- */
.demo{display:grid;grid-template-columns:minmax(0,.9fr) minmax(0,1.1fr);gap:2.6rem;margin-top:2.4rem;align-items:start}
.stage{background:var(--royal);border-radius:32px;padding:1.6rem 1.2rem 1.2rem;position:sticky;top:90px}
.stage svg{width:100%;max-width:300px;height:auto;margin:0 auto;display:block}
.angles{display:grid;grid-template-columns:repeat(5,1fr);gap:.4rem;margin-top:.8rem;text-align:center;font-size:.72rem}
.angles b{display:block;font-size:1.02rem;font-weight:800;font-variant-numeric:tabular-nums}
.angles span{opacity:.85}
.stage .cap{font-size:.82rem;opacity:.85;text-align:center;margin-top:.8rem}
.dtabs{display:inline-flex;background:rgba(255,255,255,.1);border-radius:999px;padding:.3rem;margin-bottom:1.4rem}
.dtab{background:none;border:0;padding:.65rem 1.4rem;border-radius:999px;font-weight:600}
.dtab[aria-selected="true"]{background:#fff;color:var(--navy)}
.dpanel[hidden]{display:none}
.phone{background:#f2f6ff;color:var(--ink);border-radius:30px;border:6px solid #0b0b8f;max-width:380px;overflow:hidden}
.phone-top{background:#3f9cf3;color:#fff;font-weight:600;font-size:.82rem;padding:.55rem 1rem;display:flex;justify-content:space-between}
.pat{padding:.8rem 1rem;background:#dcebfb;display:flex;justify-content:space-between;align-items:center;gap:.6rem;font-size:.78rem}
.pat b{display:block;font-size:.98rem;color:var(--navy);line-height:1.2}
.streak{border:2px solid #f6a21e;border-radius:12px;padding:.2rem .6rem;color:#b36b00;font-weight:600;font-size:.75rem;background:#fff;text-align:center}
.mtabs{display:flex;overflow-x:auto;gap:.3rem;padding:.7rem .8rem 0;scrollbar-width:none}
.mtabs::-webkit-scrollbar{display:none}
.mtab{flex:none;border:0;background:#dde8fa;border-radius:999px;padding:.4rem .85rem;font-size:.8rem;font-weight:600;color:var(--navy)}
.mtab[aria-selected="true"]{background:#0b0b8f;color:#fff}
.mbody{padding:1rem .9rem;display:grid;grid-template-columns:1fr 1fr;gap:.6rem;min-height:210px;align-content:start}
.mbody.off{opacity:.4;pointer-events:none}
.ab{border:0;border-radius:14px;padding:.7rem .4rem;background:#3f9cf3;color:#fff;font-weight:600;font-size:.88rem;box-shadow:0 3px 0 #2b7fd1}
.ab:active,.ab[aria-pressed="true"]{background:#0b0b8f;box-shadow:none;transform:translateY(2px)}
.ab.wide{grid-column:1/-1}
.mbody label{grid-column:1/-1;font-size:.88rem;font-weight:600;color:var(--navy)}
.mbody input[type=range]{grid-column:1/-1;width:100%;accent-color:#0b0b8f}
.mbody .hint{grid-column:1/-1;font-size:.8rem;color:#4a4a7a}
.onoff{display:block;width:calc(100% - 1.8rem);margin:0 .9rem 1rem;border:0;border-radius:14px;padding:.7rem;background:#ff5252;color:#fff;font-weight:600}
.onoff[aria-pressed="false"]{background:#9aa0b8}
.emg-box{background:rgba(255,255,255,.08);border-radius:24px;padding:1.3rem}
canvas#wave{width:100%;height:170px;display:block;background:#01012e;border-radius:14px}
.meter{height:10px;background:rgba(255,255,255,.15);border-radius:99px;margin:.9rem 0 .4rem;overflow:hidden;position:relative}
.meter i{display:block;height:100%;width:0;background:var(--signal);border-radius:99px}
.meter u{position:absolute;top:-3px;bottom:-3px;width:2px;background:#fff;left:45%}
.status{display:flex;flex-wrap:wrap;gap:.4rem;margin:.8rem 0 1.1rem;font-size:.85rem;font-weight:600}
.status span{padding:.35rem .8rem;border-radius:999px;background:rgba(255,255,255,.12);opacity:.55}
.status span.act{background:var(--signal);color:var(--navy);opacity:1}
.hold{width:100%;border:0;border-radius:18px;padding:1.2rem;background:#fff;color:var(--navy);font-weight:800;font-size:1.1rem;touch-action:manipulation;user-select:none;-webkit-user-select:none}
.hold.down{background:var(--signal)}
@media (max-width:900px){.demo{grid-template-columns:minmax(0,1fr)}.stage{position:static}.dtabs,.ctabs{display:flex;width:100%}.dtab,.ctab{flex:1;padding:.65rem .5rem;font-size:.92rem}}
.demo>*{min-width:0}

/* ---------- app ---------- */
.app-split{display:grid;grid-template-columns:auto 1fr;gap:3rem;align-items:center}
.phone-shot{width:min(260px,70vw);border-radius:34px;border:7px solid var(--navy);background:var(--navy);cursor:zoom-in;margin:0 auto}
.phone-shot img{border-radius:26px;width:100%}
.modes-nav{display:flex;flex-wrap:wrap;gap:.5rem;margin:1.4rem 0 1rem}
.mn{border:2px solid var(--royal);background:none;color:var(--royal);border-radius:999px;padding:.45rem 1.1rem;font-weight:600;font-size:.95rem}
.mn[aria-selected="true"]{background:var(--royal);color:#fff}
.mode-desc{background:#fff;border-radius:20px;padding:1.2rem 1.4rem;font-size:1rem;min-height:92px;box-shadow:0 14px 34px -24px rgba(2,2,71,.5)}
.report{display:grid;grid-template-columns:230px 1fr;gap:1.6rem;align-items:center;margin-top:2.2rem}
.report img{border-radius:12px;box-shadow:0 14px 34px -20px rgba(2,2,71,.6);cursor:zoom-in}
@media (max-width:860px){.app-split{grid-template-columns:1fr;gap:2rem}.report{grid-template-columns:1fr}.report img{max-width:260px}}

/* ---------- componentes ---------- */
.filters{display:flex;flex-wrap:wrap;gap:.5rem;margin:1.6rem 0 1.8rem}
.fl{border:2px solid var(--navy);background:none;color:var(--navy);border-radius:999px;padding:.45rem 1.2rem;font-weight:600;font-size:.95rem}
.fl[aria-pressed="true"]{background:var(--navy);color:#fff}
.parts{display:grid;grid-template-columns:repeat(4,1fr);gap:1.2rem}
.part{background:var(--mist);border-radius:22px;overflow:hidden;display:flex;flex-direction:column}
.part[hidden]{display:none}
.part .ph{aspect-ratio:1;display:grid;place-items:center;padding:1.1rem;background:#fff}
.part .ph img{max-height:100%;max-width:100%;object-fit:contain}
.part .tx{padding:1rem 1.1rem 1.2rem}
.part .tag{display:inline-block;font-size:.74rem;font-weight:600;background:var(--navy);color:#fff;border-radius:999px;padding:.1rem .65rem;margin-bottom:.5rem}
.part p{font-size:.9rem;line-height:1.45}
.inside{display:grid;grid-template-columns:1fr 1fr;gap:1.2rem;margin-bottom:3rem}
.inside figure{background:var(--navy);border-radius:24px;overflow:hidden;color:#fff}
.inside img{width:100%;aspect-ratio:4/3;object-fit:cover;object-position:center 35%;cursor:zoom-in}
.inside figcaption{padding:.9rem 1.2rem;font-size:.92rem}
@media (max-width:980px){.parts{grid-template-columns:repeat(3,1fr)}}
@media (max-width:720px){.parts{grid-template-columns:1fr 1fr}.inside{grid-template-columns:1fr}}
@media (max-width:420px){.parts{grid-template-columns:1fr}}

})();
</script>
</body>
</html>


