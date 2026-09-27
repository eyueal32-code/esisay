<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Eyueal Sisay</title>
<meta name="description" content="Eyueal Sisay: computer science student at the University of Maryland, focused on cybersecurity and robotics.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400;12..96,700;12..96,800&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --paper: #EEF1EC;
    --ink: #1A2A26;
    --muted: #56655F;
    --line: #C7D0C9;
    --pond: #2E6B57;
    --amber: #B9772A;
    --panel: #E3E8E1;
    box-sizing: border-box;
    padding-top: env(safe-area-inset-top, 0px);
    padding-bottom: env(safe-area-inset-bottom, 0px);
  }
  @media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) {
      --paper: #14201C; --ink: #E4EBE6; --muted: #9CAEA6;
      --line: #2E3F39; --pond: #7FC1A6; --amber: #E0A95E; --panel: #1B2A25;
    }
  }
  :root[data-theme="dark"] {
    --paper: #14201C; --ink: #E4EBE6; --muted: #9CAEA6;
    --line: #2E3F39; --pond: #7FC1A6; --amber: #E0A95E; --panel: #1B2A25;
  }
  *, *::before, *::after { box-sizing: inherit; }
  html { scroll-padding-top: env(safe-area-inset-top, 0px); scroll-behavior: smooth; }
  @media (prefers-reduced-motion: reduce) { html { scroll-behavior: auto; } * { animation: none !important; } }
  body {
    margin: 0; background: var(--paper); color: var(--ink);
    font: 400 1.0625rem/1.6 "Instrument Sans", system-ui, -apple-system, "Segoe UI", sans-serif;
  }
  a { color: var(--pond); text-underline-offset: 3px; }
  a:focus-visible, button:focus-visible { outline: 3px solid var(--amber); outline-offset: 3px; border-radius: 2px; }
  .wrap { max-width: 68rem; margin: 0 auto; padding: 0 1.5rem; }

  nav { display: flex; justify-content: space-between; align-items: center; padding: 1.5rem 0; gap: 1rem; flex-wrap: wrap; }
  nav .mark { font-family: "Bricolage Grotesque", sans-serif; font-weight: 800; font-size: 1.25rem; text-decoration: none; color: var(--ink); }
  nav ul { list-style: none; display: flex; gap: 1.5rem; margin: 0; padding: 0; }
  nav ul a { color: var(--muted); text-decoration: none; font-weight: 500; }
  nav ul a:hover { color: var(--ink); }

  .hero { display: grid; grid-template-columns: 1.1fr 1fr; gap: 3rem; align-items: center; padding: 3rem 0 4.5rem; }
  h1 {
    font-family: "Bricolage Grotesque", sans-serif; font-weight: 800;
    font-size: clamp(3rem, 8vw, 6rem); line-height: .92; letter-spacing: -.035em; margin: 0 0 1.5rem;
  }
  .hero p { font-size: 1.25rem; max-width: 32rem; color: var(--muted); margin: 0 0 2rem; }
  .actions { display: flex; gap: .75rem; flex-wrap: wrap; }
  .btn {
    display: inline-block; padding: .8rem 1.3rem; border-radius: 999px; font-weight: 600; text-decoration: none;
    border: 2px solid var(--ink); color: var(--ink);
  }
  .btn.primary { background: var(--ink); color: var(--paper); }

  /* The schematic: the one bold element on the page */
  .schematic { position: relative; }
  .schematic svg { width: 100%; height: auto; display: block; }
  .schematic svg .body { fill: var(--panel); stroke: var(--ink); stroke-width: 2.5; }
  .schematic svg .bone { fill: none; stroke: var(--ink); stroke-width: 2.5; stroke-linecap: round; stroke-linejoin: round; }
  .schematic svg .cable { fill: none; stroke: var(--amber); stroke-width: 2; stroke-dasharray: 6 5; }
  .schematic svg .web { fill: var(--pond); opacity: .28; stroke: var(--pond); stroke-width: 1.5; }
  .schematic svg .joint { fill: var(--paper); stroke: var(--ink); stroke-width: 2.5; }
  .schematic svg .servo { fill: var(--amber); }
  .schematic svg text { font: 500 13px "Instrument Sans", sans-serif; fill: var(--muted); }
  .schematic svg .leader { stroke: var(--muted); stroke-width: 1; }
  .schematic figcaption { font-size: .9rem; color: var(--muted); margin-top: .5rem; }
  .sweep { transform-origin: 0 0; animation: sweep 3.2s ease-in-out infinite alternate; }
  .sweep.r { animation-delay: 1.6s; }
  @keyframes sweep { from { transform: rotate(-8deg); } to { transform: rotate(10deg); } }

  section { padding: 4rem 0; border-top: 1px solid var(--line); }
  h2 { font-family: "Bricolage Grotesque", sans-serif; font-weight: 700; font-size: clamp(1.9rem, 4vw, 2.6rem); letter-spacing: -.02em; margin: 0 0 2rem; }
  h3 { font-family: "Bricolage Grotesque", sans-serif; font-weight: 700; font-size: 1.4rem; margin: 0 0 .5rem; }
  .split { display: grid; grid-template-columns: 16rem 1fr; gap: 2rem; }
  .split > h2 { margin: 0; }
  .prose { max-width: 40rem; }
  .prose p { margin: 0 0 1rem; }

  .project { display: grid; grid-template-columns: 1fr 1fr; gap: 2.5rem; background: var(--panel); border-radius: 20px; padding: 2rem; }
  .project .status { color: var(--amber); font-weight: 600; margin: 0 0 1rem; }
  .project dl { margin: 0; display: grid; grid-template-columns: auto 1fr; gap: .6rem 1.25rem; }
  .project dt { color: var(--muted); }
  .project dd { margin: 0; }
  .placeholder { border: 2px dashed var(--line); border-radius: 20px; padding: 2rem; margin-top: 1.5rem; color: var(--muted); }

  .timeline { list-style: none; margin: 0; padding: 0; max-width: 40rem; }
  .timeline li { display: grid; grid-template-columns: 9rem 1fr; gap: 1.5rem; padding: 1.25rem 0; border-bottom: 1px solid var(--line); }
  .timeline li:last-child { border-bottom: 0; }
  .timeline .when { color: var(--muted); font-variant-numeric: tabular-nums; }
  .timeline p { margin: .25rem 0 0; color: var(--muted); }

  .certs { list-style: none; margin: 0; padding: 0; display: grid; gap: .75rem; max-width: 40rem; }
  .certs li { display: flex; justify-content: space-between; gap: 1rem; padding-bottom: .75rem; border-bottom: 1px solid var(--line); }
  .certs li span:last-child { color: var(--muted); white-space: nowrap; }
  .skills { display: flex; flex-wrap: wrap; gap: .5rem; margin-top: 2rem; padding: 0; list-style: none; }
  .skills li { padding: .35rem .9rem; border: 1.5px solid var(--ink); border-radius: 999px; font-weight: 500; font-size: .95rem; }

  .contact p { font-size: 1.25rem; max-width: 36rem; }
  footer { padding: 2rem 0 3rem; color: var(--muted); font-size: .9rem; }

  @media (max-width: 800px) {
    .hero, .project, .split { grid-template-columns: 1fr; }
    .hero { padding-top: 1.5rem; gap: 2rem; }
    .timeline li { grid-template-columns: 1fr; gap: .25rem; }
    nav ul { gap: 1rem; }
  }
</style>
</head>
<body>
<div class="wrap">
  <nav aria-label="Main">
    <a class="mark" href="#top">ES</a>
    <ul>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#certifications">Certifications</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <header class="hero" id="top">
    <div>
      <h1>Eyueal<br>Sisay</h1>
      <p>Computer science student at the University of Maryland, focused on cybersecurity, with a habit of building robots on the side.</p>
      <div class="actions">
        <a class="btn primary" href="#projects">See my projects</a>
        <a class="btn" href="resume.pdf">Download résumé</a>
      </div>
    </div>

    <figure class="schematic">
      <svg viewBox="0 0 420 340" role="img" aria-labelledby="schem-title">
        <title id="schem-title">Top-view schematic of the PIPA-1 toad-inspired underwater robot, showing its body, two servo-driven hind legs, and webbed feet.</title>
        <!-- body -->
        <path class="body" d="M210 40 C 285 40 320 85 322 150 C 324 205 290 245 210 248 C 130 245 96 205 98 150 C 100 85 135 40 210 40 Z"/>
        <!-- spine -->
        <path class="bone" d="M210 62 V 228" opacity=".35"/>
        <!-- front legs (small, static) -->
        <path class="bone" d="M120 110 L 78 92 L 62 70"/>
        <path class="bone" d="M300 110 L 342 92 L 358 70"/>
        <!-- servos -->
        <rect class="servo" x="168" y="200" width="18" height="26" rx="3"/>
        <rect class="servo" x="234" y="200" width="18" height="26" rx="3"/>
        <!-- left hind leg -->
        <g transform="translate(150 232)">
          <g class="sweep">
            <path class="bone" d="M0 0 L -40 30 L -30 72"/>
            <path class="cable" d="M27 -12 L 0 0 L -40 30 L -30 72"/>
            <path class="web" d="M-30 72 L -62 104 L -40 112 L -26 114 L -8 108 Z"/>
            <path class="bone" d="M-30 72 L -62 104 M -30 72 L -40 112 M -30 72 L -26 114 M -30 72 L -8 108" stroke-width="1.8"/>
            <circle class="joint" r="5"/><circle class="joint" cx="-40" cy="30" r="5"/><circle class="joint" cx="-30" cy="72" r="5"/>
          </g>
        </g>
        <!-- right hind leg -->
        <g transform="translate(270 232)">
          <g class="sweep r">
            <path class="bone" d="M0 0 L 40 30 L 30 72"/>
            <path class="cable" d="M-27 -12 L 0 0 L 40 30 L 30 72"/>
            <path class="web" d="M30 72 L 62 104 L 40 112 L 26 114 L 8 108 Z"/>
            <path class="bone" d="M30 72 L 62 104 M 30 72 L 40 112 M 30 72 L 26 114 M 30 72 L 8 108" stroke-width="1.8"/>
            <circle class="joint" r="5"/><circle class="joint" cx="40" cy="30" r="5"/><circle class="joint" cx="30" cy="72" r="5"/>
          </g>
        </g>
        <!-- callouts -->
        <line class="leader" x1="322" y1="120" x2="372" y2="140"/><text x="336" y="158">silicone skin</text>
        <line class="leader" x1="252" y1="212" x2="330" y2="212"/><text x="336" y="216">servo</text>
        <line class="leader" x1="96" y1="190" x2="40" y2="190"/><text x="4" y="182">PETG</text><text x="4" y="197">skeleton</text>
      </svg>
      <figcaption>PIPA-1, my current build: a robot modeled on the Surinam toad.</figcaption>
    </figure>
  </header>

  <section id="about" class="split">
    <h2>About</h2>
    <div class="prose">
      <p>I'm a second-year computer science student at the University of Maryland, College Park, on the cybersecurity track. I hold the CompTIA Security+ certification and several Cisco cybersecurity certificates.</p>
      <p>Before UMD, I spent four years as a computer technician and data entry specialist, and volunteered as a math tutor. I'm looking for internships in security and software, and I like projects where code meets physical hardware.</p>
    </div>
  </section>

  <section id="projects">
    <h2>Projects</h2>
    <article class="project">
      <div>
        <h3>PIPA-1: a toad-inspired underwater crawler</h3>
        <p class="status">In progress</p>
        <p>A bio-inspired robot modeled on the Surinam toad (<i>Pipa pipa</i>). Two servos pull fishing-line tendons through each hind leg to sweep it, and the toe webbing opens and closes from water pressure alone, with no extra motors.</p>
      </div>
      <dl>
        <dt>Size</dt><dd>25 × 15 × 5 cm</dd>
        <dt>Frame</dt><dd>3D-printed PETG skeleton</dd>
        <dt>Skin</dt><dd>Silicone jacket</dd>
        <dt>Actuation</dt><dd>2 servos, tendon-cable hind legs</dd>
        <dt>Joints</dt><dd>Pin hinges at knee and ankle</dd>
        <dt>Feet</dt><dd>Passive webbed toe fans</dd>
      </dl>
    </article>
    <div class="placeholder">
      <!-- Replace this box with another project: a security lab, a Python tool, a class project. -->
      Add your next project here: what it does, what you built it with, and a link to its GitHub repo.
    </div>
  </section>

  <section id="experience">
    <h2>Experience</h2>
    <ol class="timeline">
      <li>
        <span class="when">2025 – present</span>
        <div><h3>University of Maryland, College Park</h3><p>B.S. Computer Science, cybersecurity track</p></div>
      </li>
      <li>
        <span class="when">2020 – 2024</span>
        <div><h3>Computer technician &amp; data entry</h3><p>Amazon Consulting, Silver Spring, MD. Supported the IT needs of an accounting and airline ticketing firm.</p></div>
      </li>
      <li>
        <span class="when">2022 – 2024</span>
        <div><h3>Volunteer math tutor</h3><p>Learn To Be</p></div>
      </li>
    </ol>
  </section>

  <section id="certifications">
    <h2>Certifications &amp; skills</h2>
    <ul class="certs">
      <li><span>CompTIA Security+</span><span>April 2025</span></li>
      <li><span>Cisco Junior Cybersecurity Analyst career path</span><span>Cisco</span></li>
      <li><span>Cisco Cyber Threat Management</span><span>Cisco</span></li>
      <li><span>Cisco Introduction to Cybersecurity</span><span>Cisco</span></li>
    </ul>
    <ul class="skills" aria-label="Skills">
      <li>Python</li><li>Java</li><li>Network security</li><li>Threat management</li><li>3D printing</li><li>Servo control</li>
    </ul>
  </section>

  <section id="contact" class="contact">
    <h2>Get in touch</h2>
    <p>I'm open to internships and research roles in cybersecurity and robotics.</p>
    <div class="actions">
      <!-- Replace these three links with your real ones -->
      <a class="btn primary" href="mailto:you@umd.edu">Email me</a>
      <a class="btn" href="https://github.com/YOUR-USERNAME">GitHub</a>
      <a class="btn" href="https://www.linkedin.com/in/YOUR-PROFILE">LinkedIn</a>
    </div>
  </section>

  <footer>© 2026 Eyueal Sisay. Hosted on GitHub Pages.</footer>
</div>
</body>
</html>
