<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Diwali Night at Via Teulié</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Rozha+One&family=Karla:wght@400;500;700&family=Caveat:wght@600&display=swap">
<style>
/* Layout: night-sky single column. Hero splits text left / big diya right; details in 3 columns; flip book centred. Single committed dark look (a Diwali night), so no light theme. */
:root {
  --night: #1b0f2e;
  --night-2: #2a1546;
  --marigold: #ffb627;
  --flame: #ff7a1a;
  --magenta: #e0368a;
  --cream: #fff1d6;
  --muted: #cdb9e6;
  --paper: #fbeccb;
  --ink: #3b1d12;
  --font-display: "Rozha One", "Noto Serif Devanagari", Georgia, serif;
  --font-body: "Karla", system-ui, sans-serif;
  --font-hand: "Caveat", "Segoe Script", cursive;
  color-scheme: dark;
}
* { box-sizing: border-box; }
html { background: var(--night); }
body {
  margin: 0; background: var(--night); color: var(--cream);
  font-family: var(--font-body); font-size: 17px; line-height: 1.55;
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
  padding-block: 0 48px;
  overflow-x: hidden;
  background-image:
    radial-gradient(900px 500px at 80% 8%, rgba(255,122,26,.22), transparent 60%),
    radial-gradient(700px 500px at 5% 40%, rgba(224,54,138,.18), transparent 60%),
    linear-gradient(180deg, var(--night) 0%, var(--night-2) 100%);
  background-attachment: scroll;
}
#sparks { position: fixed; inset: 0; width: 100%; height: 100%; pointer-events: none; z-index: 0; }
#lights { position: absolute; left: 0; top: 0; width: 100%; height: 120px; pointer-events: none; z-index: 2; }
main { position: relative; z-index: 1; max-width: 1040px; margin: 0 auto; }
h1, h2, h3 { font-family: var(--font-display); font-weight: 400; text-wrap: balance; margin: 0; }

/* hero */
.hero { display: grid; grid-template-columns: 1.15fr .85fr; align-items: center; gap: 24px; padding-top: 110px; }
.hero > * { min-width: 0; }
.kicker { font-family: var(--font-hand); font-size: 30px; color: var(--marigold); margin: 0 0 4px; }
h1 { font-size: clamp(44px, 8vw, 84px); line-height: 1.02; color: var(--cream); text-shadow: 0 0 30px rgba(255,182,39,.35); }
h1 span { color: var(--marigold); display: block; }
.lede { max-width: 34ch; color: var(--muted); font-size: 19px; margin: 18px 0 0; }
.when {
  display: inline-flex; flex-wrap: wrap; gap: 4px 14px; align-items: baseline;
  margin-top: 22px; padding: 12px 18px; border: 1.5px solid var(--marigold); border-radius: 999px;
  font-weight: 700; letter-spacing: .02em; color: var(--marigold); background: rgba(255,182,39,.08);
}
.when small { font-weight: 500; color: var(--cream); font-size: 16px; }
.diya-wrap { position: relative; display: grid; place-items: center; }
.diya-wrap::before {
  content: ""; position: absolute; width: 120%; aspect-ratio: 1; border-radius: 50%;
  background: radial-gradient(circle, rgba(255,160,40,.45), rgba(255,122,26,.12) 40%, transparent 68%);
  animation: glow 3.2s ease-in-out infinite;
}
.diya { position: relative; width: min(100%, 320px); height: auto; overflow: visible; }
.flame { transform-origin: 50% 100%; transform-box: fill-box; animation: flicker 1.6s ease-in-out infinite; }
.flame.b { animation-duration: 2.1s; animation-delay: -.7s; }
@keyframes flicker {
  0%,100% { transform: scale(1,1) rotate(-1.5deg); }
  30% { transform: scale(.94,1.08) rotate(2deg); }
  60% { transform: scale(1.04,.96) rotate(-2.5deg); }
}
@keyframes glow { 0%,100% { opacity: .85; transform: scale(1); } 50% { opacity: 1; transform: scale(1.06); } }

/* details */
.rule { display: block; width: 100%; height: 28px; margin: 56px 0 28px; }
.details { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
.details > * { min-width: 0; }
.panel { padding: 26px 24px 28px; background: linear-gradient(180deg, rgba(255,241,214,.09), rgba(255,241,214,.04)); border: 1px solid rgba(255,182,39,.32); border-radius: 6px 6px 40px 6px; }
.panel h2 { font-size: 26px; color: var(--marigold); margin-bottom: 10px; }
.panel p { margin: 0 0 8px; }
.panel .big { font-size: 22px; font-weight: 700; line-height: 1.25; }
.panel .sub { color: var(--muted); }
.btns { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 14px; }
.btn {
  font: inherit; font-weight: 700; font-size: 15px; cursor: pointer; text-decoration: none;
  padding: 9px 16px; border-radius: 999px; border: 1.5px solid var(--marigold);
  background: var(--marigold); color: var(--ink);
}
.btn.ghost { background: transparent; color: var(--marigold); }
.btn:hover { filter: brightness(1.1); }
:focus-visible { outline: 3px solid var(--magenta); outline-offset: 3px; }
.rules { list-style: none; padding: 0; margin: 0; display: grid; gap: 14px; }
.rules li { display: grid; grid-template-columns: 34px 1fr; gap: 12px; align-items: start; }
.rules svg { width: 34px; height: 34px; }
.rules b { display: block; color: var(--cream); }
.rules span { color: var(--muted); font-size: 15.5px; }

footer { margin-top: 64px; text-align: center; color: var(--muted); }
footer .shubh { font-family: var(--font-display); font-size: clamp(30px, 5vw, 44px); color: var(--marigold); margin-bottom: 6px; display: block; }

@media (max-width: 820px) {
  .hero { grid-template-columns: 1fr; padding-top: 96px; }
  .diya-wrap { order: -1; max-width: 240px; margin: 0 auto; }
  .details { grid-template-columns: 1fr; }
}
@media (prefers-reduced-motion: reduce) {
  .flame, .diya-wrap::before { animation: none; }
  .leaf { transition: none; }
}
</style>

<canvas id="sparks" aria-hidden="true"></canvas>
<canvas id="lights" aria-hidden="true"></canvas>

<main>
  <section class="hero">
    <div>
      <p class="kicker">शुभ दीपावली</p>
      <h1>Diwali<span>at my place</span></h1>
      <p class="lede">Come light a diya, eat well and celebrate with me. You are invited.</p>
      <div class="when">Sunday 8 November <small>7:30 pm onwards</small></div>
    </div>
    <div class="diya-wrap">
      <svg class="diya" viewBox="0 0 200 180" role="img" aria-label="A lit diya">
        <defs>
          <linearGradient id="bowl" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0" stop-color="#ffb627"/><stop offset="1" stop-color="#c2410c"/>
          </linearGradient>
          <radialGradient id="fl" cx=".5" cy=".75" r=".7">
            <stop offset="0" stop-color="#fff7c2"/><stop offset=".5" stop-color="#ffb627"/><stop offset="1" stop-color="#ff5a1a"/>
          </radialGradient>
        </defs>
        <g class="flame"><path d="M100 18 C 128 56 122 84 100 96 C 78 84 72 56 100 18 Z" fill="url(#fl)"/></g>
        <g class="flame b" opacity=".9"><path d="M100 46 C 111 64 108 80 100 86 C 92 80 89 64 100 46 Z" fill="#fff7c2"/></g>
        <rect x="97" y="88" width="6" height="14" rx="3" fill="#3b1d12"/>
        <path d="M18 98 C 40 150 160 150 182 98 C 150 112 50 112 18 98 Z" fill="url(#bowl)"/>
        <path d="M18 98 C 50 112 150 112 182 98 C 168 92 32 92 18 98 Z" fill="#7c2d0a"/>
        <path d="M60 128 C 80 138 120 138 140 128" stroke="#ffe08a" stroke-width="3" fill="none" stroke-linecap="round"/>
        <circle cx="100" cy="124" r="4" fill="#ffe08a"/><circle cx="82" cy="123" r="3" fill="#ffe08a"/><circle cx="118" cy="123" r="3" fill="#ffe08a"/>
        <ellipse cx="100" cy="162" rx="60" ry="6" fill="#000" opacity=".25"/>
      </svg>
    </div>
  </section>

  <svg class="rule" viewBox="0 0 600 28" preserveAspectRatio="xMidYMid meet" aria-hidden="true">
    <line x1="0" y1="14" x2="250" y2="14" stroke="#ffb627" stroke-opacity=".5"/>
    <line x1="350" y1="14" x2="600" y2="14" stroke="#ffb627" stroke-opacity=".5"/>
    <g fill="#ffb627">
      <path d="M300 2 L308 14 L300 26 L292 14 Z"/>
      <path d="M278 14 L284 8 L290 14 L284 20 Z" fill="#e0368a"/>
      <path d="M310 14 L316 8 L322 14 L316 20 Z" fill="#e0368a"/>
      <circle cx="262" cy="14" r="3"/><circle cx="338" cy="14" r="3"/>
    </g>
  </svg>

  <section class="details" aria-label="Party details">
    <div class="panel">
      <h2>When</h2>
      <p class="big">Sunday, 8 November</p>
      <p class="sub">Doors open at 7:30 pm. Stay as late as you like.</p>
    </div>
    <div class="panel">
      <h2>Where</h2>
      <p class="big" id="addr">Via Pietro Teulié 12</p>
      <div class="btns">
        <a class="btn" href="https://www.google.com/maps/search/?api=1&amp;query=Via+Pietro+Teuli%C3%A9+12+Milano" target="_blank" rel="noopener">Open in Maps</a>
        <button class="btn ghost" id="copy" type="button">Copy address</button>
      </div>
    </div>
    <div class="panel">
      <h2>The plan</h2>
      <ul class="rules">
        <li>
          <svg viewBox="0 0 40 40" aria-hidden="true"><path d="M13 4h14l-2 12c-.6 3-2 5-5 5s-4.400-2-5-5z" fill="none" stroke="#ffb627" stroke-width="2.4" stroke-linejoin="round"/><path d="M20 21v13M13 36h14" stroke="#ffb627" stroke-width="2.4" stroke-linecap="round"/></svg>
          <div><b>Bring your own liquor</b><span>Pour what you like. I will have glasses and ice.</span></div>
        </li>
        <li>
          <svg viewBox="0 0 40 40" aria-hidden="true"><path d="M5 22h30c0 8-6 13-15 13S5 30 5 22z" fill="none" stroke="#ffb627" stroke-width="2.4" stroke-linejoin="round"/><path d="M13 16c0-3 3-3 3-6M21 16c0-3 3-3 3-6" stroke="#ffb627" stroke-width="2.4" fill="none" stroke-linecap="round"/></svg>
          <div><b>Food is on me</b><span>Come hungry. Dinner and sweets are covered.</span></div>
        </li>
        <li>
          <svg viewBox="0 0 40 40" aria-hidden="true"><path d="M20 4l5 5-5 4-5-4zM15 9l-9 6 5 5 4-3v17h10V17l4 3 5-5-9-6" fill="none" stroke="#ffb627" stroke-width="2.4" stroke-linejoin="round"/></svg>
          <div><b>Wear ethnic clothes</b><span>Kurtas, sarees, lehengas, anything festive and bright.</span></div>
        </li>
      </ul>
    </div>
  </section>

  <footer>
    <span class="shubh">Happy Diwali</span>
    May your home be bright and your plate be full. See you there.
  </footer>
</main>

<script>
(function () {
  var reduce = window.matchMedia("(prefers-reduced-motion: reduce)").matches;

  /* ---------- fairy lights ---------- */
  var lc = document.getElementById("lights"), lx = lc.getContext("2d");
  var colors = ["#ffb627", "#ff7a1a", "#e0368a", "#fff1d6", "#ff4d6d", "#7ee0a0"];
  var bulbs = [];
  function sizeLights() {
    var r = lc.getBoundingClientRect(), d = window.devicePixelRatio || 1;
    lc.width = r.width * d; lc.height = r.height * d; lx.setTransform(d, 0, 0, d, 0, 0);
    bulbs = [];
    var w = r.width, step = 46, n = Math.ceil(w / step) + 1;
    for (var i = 0; i < n; i++) {
      var x = i * step, seg = i % 1 === 0 ? 0 : 0;
      var t = (x % (step * 6)) / (step * 6);
      var y = 12 + Math.sin(t * Math.PI) * 36;
      bulbs.push({ x: x, y: y, c: colors[i % colors.length], p: Math.random() * 6.28, s: 1 + Math.random() * 1.5 });
    }
  }
  function drawLights(time) {
    var w = lc.getBoundingClientRect().width, h = 120;
    lx.clearRect(0, 0, w, h);
    lx.strokeStyle = "#4a3a1e"; lx.lineWidth = 2; lx.beginPath();
    bulbs.forEach(function (b, i) { i ? lx.lineTo(b.x, b.y) : lx.moveTo(b.x, b.y); });
    lx.stroke();
    bulbs.forEach(function (b) {
      var a = reduce ? 1 : 0.65 + 0.35 * Math.sin(time / 1000 * b.s + b.p);
      var g = lx.createRadialGradient(b.x, b.y + 8, 0, b.x, b.y + 8, 22);
      g.addColorStop(0, b.c); g.addColorStop(1, "rgba(0,0,0,0)");
      lx.globalAlpha = a * 0.55; lx.fillStyle = g;
      lx.beginPath(); lx.arc(b.x, b.y + 8, 22, 0, 6.29); lx.fill();
      lx.globalAlpha = a; lx.fillStyle = b.c;
      lx.beginPath(); lx.ellipse(b.x, b.y + 8, 4.5, 7, 0, 0, 6.29); lx.fill();
      lx.fillStyle = "#4a3a1e"; lx.globalAlpha = 1; lx.fillRect(b.x - 2.5, b.y - 1, 5, 4);
    });
  }

  /* ---------- floating sparks ---------- */
  var sc = document.getElementById("sparks"), sx = sc.getContext("2d"), sparks = [];
  function sizeSparks() {
    var d = window.devicePixelRatio || 1;
    sc.width = innerWidth * d; sc.height = innerHeight * d; sx.setTransform(d, 0, 0, d, 0, 0);
    sparks = [];
    var n = Math.min(60, Math.floor(innerWidth / 18));
    for (var i = 0; i < n; i++) sparks.push(spark(true));
  }
  function spark(init) {
    return { x: Math.random() * innerWidth, y: init ? Math.random() * innerHeight : innerHeight + 10,
      r: 0.8 + Math.random() * 1.8, v: 0.15 + Math.random() * 0.5, d: Math.random() * 6.28,
      c: colors[Math.floor(Math.random() * 4)] };
  }
  function drawSparks(time) {
    sx.clearRect(0, 0, innerWidth, innerHeight);
    sparks.forEach(function (p, i) {
      if (!reduce) { p.y -= p.v; p.x += Math.sin(time / 1500 + p.d) * 0.25; }
      if (p.y < -10) sparks[i] = spark(false);
      sx.globalAlpha = 0.35 + 0.35 * Math.sin(time / 600 + p.d);
      sx.fillStyle = p.c; sx.beginPath(); sx.arc(p.x, p.y, p.r, 0, 6.29); sx.fill();
    });
  }
  function loop(t) { drawLights(t); drawSparks(t); if (!reduce) requestAnimationFrame(loop); }
  function resize() { sizeLights(); sizeSparks(); loop(performance.now()); }
  addEventListener("resize", resize);
  resize();
  if (!reduce) requestAnimationFrame(loop);

  /* ---------- copy address ---------- */
  var copyBtn = document.getElementById("copy");
  copyBtn.addEventListener("click", function () {
    var txt = "Via Pietro Teulié 12";
    var done = function () { copyBtn.textContent = "Copied"; setTimeout(function () { copyBtn.textContent = "Copy address"; }, 1800); };
    var fallback = function () {
      var r = document.createRange(); r.selectNodeContents(document.getElementById("addr"));
      var s = getSelection(); s.removeAllRanges(); s.addRange(r);
      copyBtn.textContent = "Selected, now copy"; setTimeout(function () { copyBtn.textContent = "Copy address"; }, 2200);
    };
    if (navigator.clipboard && navigator.clipboard.writeText) navigator.clipboard.writeText(txt).then(done, fallback); else fallback();
  });

})();
</script>

</body></html>
