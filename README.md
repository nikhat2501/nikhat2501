
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nikhat | Creative Developer</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Manrope:wght@400;500;600;700;800&display=swap');

:root {
  --bg: #fffaf5;
  --ink: #35283e;
  --muted: #827589;
  --pink: #f1a7c5;
  --purple: #c7b5f5;
  --green: #b9d8c1;
  --peach: #ffd0ad;
  --line: #eadfea;
}

* { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  margin: 0;
  background:
    radial-gradient(ellipse at 10% 5%, #fce4ef 0, transparent 30%),
    radial-gradient(ellipse at 90% 25%, #e9e1ff 0, transparent 28%),
    var(--bg);
  color: var(--ink);
  font-family: 'Manrope', sans-serif;
  overflow-x: hidden;
}

a { color: inherit; text-decoration: none; }

.container {
  width: min(1100px, 90%);
  margin: auto;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 25px 0;
}

.logo {
  font-weight: 800;
  font-size: 22px;
  letter-spacing: -1px;
}

.logo span { color: #bc6d9a; }

.navlinks {
  display: flex;
  gap: 24px;
  color: var(--muted);
  font-size: 13px;
}

.navlinks a { transition: color .25s; }
.navlinks a:hover { color: #b45d91; }

.hero {
  position: relative;
  overflow: hidden;
  margin: 24px 0;
  padding: clamp(35px, 7vw, 80px);
  border: 1px solid #ffffff;
  border-radius: 34px;
  background: linear-gradient(130deg,
    rgba(255,255,255,.92),
    rgba(255,232,242,.88) 45%,
    rgba(225,215,255,.88));
  box-shadow: 0 25px 70px #9b7b9d18;
  min-height: 410px;
}

.hero:before, .hero:after {
  content: "";
  position: absolute;
  border-radius: 50%;
  filter: blur(2px);
  pointer-events: none;
}

.hero:before {
  width: 240px;
  height: 240px;
  background: #f7bad5a0;
  right: -45px;
  top: -55px;
  animation: float 7s ease-in-out infinite;
}

.hero:after {
  width: 160px;
  height: 160px;
  background: #b9d8c180;
  right: 130px;
  bottom: -70px;
  animation: float 8s ease-in-out infinite reverse;
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 720px;
}

.eyebrow, .mono {
  font-family: 'DM Mono', monospace;
  font-size: 12px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}

.eyebrow { color: #a35c89; }

h1 {
  font-size: clamp(43px, 8vw, 86px);
  letter-spacing: -5px;
  line-height: .98;
  margin: 22px 0;
}

.gradient-text {
  background: linear-gradient(100deg, #b45f91, #8468cb, #548e7b);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.intro {
  max-width: 490px;
  color: #71657b;
  font-size: 16px;
  line-height: 1.9;
}

.actions {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin-top: 27px;
}

.btn {
  display: inline-block;
  padding: 13px 19px;
  border-radius: 14px;
  font-size: 13px;
  font-weight: 800;
  transition: transform .25s, box-shadow .25s, background .25s;
}

.btn:hover {
  transform: translateY(-5px) scale(1.03);
  box-shadow: 0 12px 25px #80558a25;
}

.btn-primary { background: var(--ink); color: white; }
.btn-secondary { background: white; border: 1px solid var(--line); }

.sparkle {
  position: absolute;
  z-index: 1;
  font-size: 30px;
  animation: float 4s ease-in-out infinite;
}
.s1 { right: 12%; top: 34%; }
.s2 { right: 27%; top: 12%; animation-delay: -2s; }
.s3 { right: 10%; bottom: 18%; animation-delay: -1s; }

section { padding: 45px 0; }

.section-heading {
  display: flex;
  justify-content: space-between;
  align-items: end;
  gap: 15px;
  margin-bottom: 23px;
}

h2 {
  font-size: clamp(26px, 4vw, 38px);
  letter-spacing: -1.8px;
  margin: 8px 0 0;
}

.sub { color: var(--muted); font-size: 13px; }

.grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}

.card {
  position: relative;
  overflow: hidden;
  border: 1px solid #fff;
  border-radius: 24px;
  padding: 25px;
  min-height: 210px;
  background: #ffffffb8;
  box-shadow: 0 8px 30px #785d8110;
  transition:
    transform .35s cubic-bezier(.2,.8,.2,1),
    box-shadow .35s,
    border-color .35s;
  transform-style: preserve-3d;
}

.card:hover {
  transform: translateY(-12px) rotateX(3deg) rotateY(-3deg) scale(1.02);
  box-shadow: 0 24px 45px #77568a24;
  border-color: #e9b4d2;
}

.card:before {
  content: "";
  position: absolute;
  width: 110px;
  height: 110px;
  right: -40px;
  top: -40px;
  border-radius: 50%;
  background: var(--orb, #f7d7e6);
  opacity: .65;
  transition: transform .4s;
}

.card:hover:before { transform: scale(2.1); }

.card > * { position: relative; }

.card-icon {
  font-size: 29px;
  margin-bottom: 20px;
  display: inline-block;
  transition: transform .35s;
}

.card:hover .card-icon { transform: translateY(-5px) rotate(-9deg) scale(1.15); }

.card h3 { margin: 0 0 10px; font-size: 17px; }
.card p { color: var(--muted); font-size: 13px; line-height: 1.8; }

.tags { display: flex; gap: 7px; flex-wrap: wrap; margin-top: 17px; }

.tag {
  font-family: 'DM Mono', monospace;
  font-size: 10px;
  padding: 6px 9px;
  border-radius: 8px;
  background: #f5eaf5;
  transition: background .2s, transform .2s;
}
.card:hover .tag { background: #f8deea; transform: translateY(-2px); }

.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 11px;
}

.skill {
  border: 1px solid white;
  background: #ffffffb8;
  border-radius: 15px;
  padding: 13px 17px;
  font-size: 13px;
  font-weight: 700;
  box-shadow: 0 5px 18px #8061840c;
  transition: transform .25s, background .25s, box-shadow .25s;
}

.skill:hover {
  transform: translateY(-6px) rotate(-2deg);
  background: #f8e1ed;
  box-shadow: 0 12px 22px #80618420;
}

.graph-card {
  border: 1px solid white;
  background: #ffffffb8;
  border-radius: 24px;
  padding: clamp(18px, 4vw, 32px);
  box-shadow: 0 12px 35px #80618410;
}

.graph {
  display: grid;
  grid-template-rows: repeat(7, 1fr);
  grid-auto-flow: column;
  grid-auto-columns: minmax(5px, 1fr);
  gap: 4px;
  overflow: hidden;
}

.cell {
  width: 100%;
  aspect-ratio: 1;
  min-width: 4px;
  border-radius: 3px;
  background: #eee7f2;
  transition: transform .2s, outline .2s;
}

.cell:hover {
  transform: scale(1.55);
  outline: 2px solid white;
  z-index: 2;
}

.level1 { background: #d9c7f3; }
.level2 { background: #eeb4d0; }
.level3 { background: #a8d7bd; }
.level4 { background: #8c68b7; }

.graph-legend {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: var(--muted);
  font-size: 11px;
  margin-top: 15px;
  gap: 10px;
}

.legend-colors { display: flex; align-items: center; gap: 4px; }

.stats-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
}

.stat {
  padding: 23px 10px;
  text-align: center;
  border-radius: 20px;
  border: 1px solid white;
  background: #ffffffb8;
  transition: transform .3s, box-shadow .3s;
}
.stat:hover { transform: translateY(-7px); box-shadow: 0 16px 30px #8061841c; }
.stat strong { display: block; font-size: 25px; color: #a55f97; }
.stat span { color: var(--muted); font-size: 11px; }

footer {
  text-align: center;
  padding: 45px 0 35px;
  color: var(--muted);
  font-size: 12px;
}

.reveal {
  opacity: 0;
  transform: translateY(22px);
  transition: opacity .7s, transform .7s;
}
.reveal.visible { opacity: 1; transform: translateY(0); }

@keyframes float {
  0%,100% { transform: translateY(0) rotate(0); }
  50% { transform: translateY(-17px) rotate(5deg); }
}

@media (max-width: 760px) {
  .grid { grid-template-columns: 1fr; }
  .hero { border-radius: 24px; }
  h1 { letter-spacing: -2.5px; }
  .navlinks { gap: 12px; font-size: 11px; }
  .stats-grid { grid-template-columns: 1fr; }
  .section-heading { align-items: start; flex-direction: column; }
}
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation: none !important;
    transition: none !important;
    scroll-behavior: auto !important;
  }
}
</style>
</head>

<body>
<div class="container">

<nav>
  <a class="logo" href="#">nikhat<span>.</span>dev</a>
  <div class="navlinks">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#activity">Activity</a>
  </div>
</nav>

<header class="hero" id="about">
  <span class="sparkle s1">✳</span>
  <span class="sparkle s2">✦</span>
  <span class="sparkle s3">♡</span>

  <div class="hero-content">
    <div class="eyebrow">✦ HELLO, INTERNET — I'M NIKHAT</div>
    <h1>Building things<br>for the <span class="gradient-text">web.</span></h1>
    <p class="intro">
      Exploring intelligent systems, creating thoughtful digital experiences,
      and turning curious ideas into something real.
    </p>
    <div class="actions">
      <a class="btn btn-primary" href="https://github.com/nikhat2501?tab=repositories">Explore my work ↗</a>
      <a class="btn btn-secondary" href="https://github.com/nikhat2501">Visit GitHub ↗</a>
    </div>
  </div>
</header>

<section id="skills" class="reveal">
  <div class="section-heading">
    <div>
      <div class="eyebrow">01 / THE TOOLBOX</div>
      <h2>Things I work with.</h2>
    </div>
    <span class="sub">Learning never stops ✿</span>
  </div>

  <div class="skills">
    <span class="skill">⚛️ React</span>
    <span class="skill">🟨 JavaScript</span>
    <span class="skill">🟢 Node.js</span>
    <span class="skill">🍃 MongoDB</span>
    <span class="skill">🎨 Tailwind CSS</span>
    <span class="skill">☕ Java</span>
    <span class="skill">🐍 Python</span>
    <span class="skill">🧩 HTML & CSS</span>
    <span class="skill">🔧 Git & GitHub</span>
  </div>
</section>

<section id="projects" class="reveal">
  <div class="section-heading">
    <div>
      <div class="eyebrow">02 / LITTLE EXPERIMENTS</div>
      <h2>Made with curiosity.</h2>
    </div>
    <span class="sub">Hover over the cards ↗</span>
  </div>

  <div class="grid">
    <a class="card" href="https://github.com/nikhat2501?tab=repositories" style="--orb:#f6c5dc">
      <span class="card-icon">✿</span>
      <h3>Web experiences</h3>
      <p>Responsive interfaces, thoughtful layouts, and delightful details.</p>
      <div class="tags"><span class="tag">React</span><span class="tag">JavaScript</span><span class="tag">UI</span></div>
    </a>

    <a class="card" href="https://github.com/nikhat2501?tab=repositories" style="--orb:#cbbaf4">
      <span class="card-icon">⌘</span>
      <h3>Backend adventures</h3>
      <p>Connecting APIs, databases, and server-side logic into useful apps.</p>
      <div class="tags"><span class="tag">Node.js</span><span class="tag">Express</span><span class="tag">MongoDB</span></div>
    </a>

    <a class="card" href="https://github.com/nikhat2501?tab=repositories" style="--orb:#b9dfc8">
      <span class="card-icon">✧</span>
      <h3>Intelligent systems</h3>
      <p>Exploring data, algorithms, and ways to solve real-world problems.</p>
      <div class="tags"><span class="tag">Python</span><span class="tag">ML</span><span class="tag">Learning</span></div>
    </a>
  </div>
</section>

<section id="activity" class="reveal">
  <div class="section-heading">
    <div>
      <div class="eyebrow">03 / SHOWING UP</div>
      <h2>My little coding garden.</h2>
    </div>
    <span class="sub">A decorative graph — not live GitHub data</span>
  </div>

  <div class="graph-card">
    <div class="graph" id="contributionGraph" aria-label="Decorative contribution-style graph"></div>
    <div class="graph-legend">
      <span>Every little step counts 🌱</span>
      <div class="legend-colors">
        <span>Less</span>
        <i class="cell"></i><i class="cell level1"></i>
        <i class="cell level2"></i><i class="cell level3"></i>
        <i class="cell level4"></i>
        <span>More</span>
      </div>
    </div>
  </div>
</section>

<section class="reveal">
  <div class="section-heading">
    <div>
      <div class="eyebrow">04 / THE PROFILE</div>
      <h2>Little numbers, big journey.</h2>
    </div>
  </div>

  <div class="stats-grid">
    <div class="stat"><strong>01</strong><span>Stay curious</span></div>
    <div class="stat"><strong>∞</strong><span>Things to learn</span></div>
    <div class="stat"><strong>✦</strong><span>Ideas to build</span></div>
  </div>

  <p class="sub" style="margin-top:15px">
    <a href="https://github.com/nikhat2501">See actual repositories, contributions, and stats on GitHub ↗</a>
  </p>
</section>

<footer>
  <div style="font-size:25px;margin-bottom:12px">♡</div>
  <div>Designed with curiosity & a little pastel magic.</div>
  <p>© Nikhat · <a href="https://github.com/nikhat2501">@nikhat2501</a></p>
</footer>

</div>

<script>
// Generate a decorative graph locally so it never appears blank.
const graph = document.getElementById("contributionGraph");
const levels = ["", "", "", "level1", "level1", "level2", "level2", "level3", "level4"];

for (let i = 0; i < 7 * 26; i++) {
  const cell = document.createElement("div");
  const level = levels[Math.floor(Math.random() * levels.length)];
  cell.className = "cell " + level;
  cell.title = "A little step in the coding journey";
  graph.appendChild(cell);
}

// Reveal sections as you scroll.
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.12 });

document.querySelectorAll(".reveal").forEach(el => observer.observe(el));
</script>
</body>
</html>
