# TierOneX
This is a text repository just created for assignment purpose. I am one of the member of Tier1X group. My team consists of 5 members: Yam, Ashish, Yogesh, Diya and Abhi.
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>TierOneX — AR Plant Parts Learning</title>
  <meta name="description" content="TierOneX: An AR project that helps elementary school students learn the parts of plants in a fun, interactive way." />
  <style>
    :root{
      --bg: #0b1020;
      --panel: #111735;
      --panel-2: #0f1530;
      --text: #eef2ff;
      --muted: #c9d2ff;
      --accent: #66e3a3; /* mint */
      --accent-2: #8aa9ff; /* soft blue */
      --warning: #ffd166;
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 18px;
    }
    *{ box-sizing: border-box; }
    html, body{ height: 100%; }
    body{
      margin:0; font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, "Helvetica Neue", Arial, "Apple Color Emoji", "Segoe UI Emoji";
      background: radial-gradient(1200px 800px at 80% -10%, #1b2b6a 0%, var(--bg) 50%),
                  radial-gradient(1000px 600px at -10% 20%, #133042 0%, var(--bg) 70%);
      color: var(--text);
    }
    a{ color: var(--accent); text-decoration: none; }
    a:hover{ text-decoration: underline; }

    /* Header */
    header{
      position: sticky; top:0; z-index: 20; backdrop-filter: blur(8px);
      background: color-mix(in srgb, var(--bg) 75%, transparent);
      border-bottom: 1px solid rgba(255,255,255,.08);
    }
    .wrap{ max-width: 1100px; margin: 0 auto; padding: 16px 20px; }
    .row{ display:flex; align-items:center; justify-content: space-between; gap: 16px; }
    .brand{ display:flex; align-items:center; gap: 12px; font-weight: 800; letter-spacing: .3px; }
    .brand .logo{ width: 40px; height: 40px; border-radius: 50%; background: conic-gradient(from 210deg, #74f0bc, #7aa2ff, #74f0bc);
      box-shadow: 0 0 0 3px rgba(255,255,255,.06), inset 0 6px 18px rgba(0,0,0,.35);
      display:grid; place-items:center; font-weight:900; color:#0b1020; }
    nav a{ padding: 10px 12px; border-radius: 10px; color: var(--muted); font-weight: 600; }
    nav a:hover{ background: rgba(255,255,255,.06); color: var(--text); }
    .cta-btn{
      padding: 10px 14px; border-radius: 12px; background: linear-gradient(180deg, var(--accent), #47d089);
      color:#0b1020; font-weight:800; border: none; box-shadow: var(--shadow); cursor:pointer;
    }
    .cta-btn:focus{ outline: 3px solid #fff4; outline-offset:2px; }

    /* Hero */
    .hero{ padding: 64px 20px 28px; }
    .hero-grid{ display:grid; grid-template-columns: 1.1fr .9fr; gap: 28px; align-items:center; }
    h1{ font-size: clamp(28px, 3.4vw, 44px); line-height: 1.05; margin: 6px 0 10px; }
    .lead{ color: var(--muted); font-size: clamp(16px, 1.6vw, 19px); max-width: 56ch; }
    .hero-card{ background: linear-gradient(180deg, color-mix(in srgb, var(--panel) 80%, transparent), var(--panel-2));
      border: 1px solid rgba(255,255,255,.08); border-radius: var(--radius); padding: 20px; box-shadow: var(--shadow);
    }
    .badges{ display:flex; gap: 10px; flex-wrap: wrap; margin: 14px 0 8px; }
    .badge{ background: rgba(255,255,255,.08); padding: 8px 12px; border-radius: 999px; font-weight:700; font-size: 13px; }
    .hero-actions{ display:flex; gap: 12px; flex-wrap: wrap; margin-top: 18px; }
    .btn-ghost{ padding: 10px 14px; border-radius: 12px; border:1px solid rgba(255,255,255,.14); color: var(--text); background: transparent; font-weight:700; cursor:pointer; }
    .btn-ghost:hover{ background: rgba(255,255,255,.06); }

    /* Explorer + Info */
    .section{ padding: 48px 20px; }
    .panel{ background: linear-gradient(180deg, color-mix(in srgb, var(--panel) 82%, transparent), var(--panel-2)); border: 1px solid rgba(255,255,255,.08); border-radius: var(--radius); box-shadow: var(--shadow); }
    .grid-2{ display:grid; grid-template-columns: 1fr 1fr; gap: 24px; }

    /* Plant Explorer */
    .explorer{ padding: 18px; }
    .svg-wrap{ background: radial-gradient(300px 200px at 30% 20%, #1d2a54, transparent 70%); border-radius: 16px; padding: 16px; }
    svg{ width: 100%; height: auto; display:block; }
    .hotspots button{
      position: absolute; width: 30px; height: 30px; border-radius: 50%; border: 2px solid white; background: var(--accent-2);
      transform: translate(-50%, -50%); box-shadow: var(--shadow); cursor: pointer; color:#021; font-weight:800;
    }
    .hotspots button:focus{ outline: 3px solid #fff7; }
    .svg-stage{ position: relative; }

    /* Info card */
    .info{ padding: 18px; display:flex; flex-direction: column; gap: 14px; }
    .info h2{ margin: 0; font-size: 22px; }
    .info .desc{ color: var(--muted); line-height: 1.5; }
    .info .chiprow{ display:flex; gap:8px; flex-wrap:wrap; }
    .chip{ background: rgba(255,255,255,.08); padding: 6px 10px; border-radius: 999px; font-size: 12px; font-weight: 700; }
    .controls{ display:flex; gap: 10px; flex-wrap: wrap; margin-top: 8px; }
    .controls button{ padding: 10px 12px; border-radius: 12px; border:1px solid rgba(255,255,255,.14); background: transparent; color: var(--text); font-weight:700; cursor:pointer; }
    .controls button.primary{ background: linear-gradient(180deg, var(--accent), #47d089); color:#051; border: none; }

    /* Features */
    .features{ margin-top: 20px; display:grid; grid-template-columns: repeat(3, 1fr); gap: 16px; }
    .card{ background: linear-gradient(180deg, color-mix(in srgb, var(--panel) 84%, transparent), var(--panel-2)); border: 1px solid rgba(255,255,255,.08); border-radius: 16px; padding: 16px; }
    .card h3{ margin: 0 0 6px; font-size: 18px; }
    .card p{ margin: 0; color: var(--muted); }

    /* How it works */
    .how{ display:grid; grid-template-columns: repeat(3, 1fr); gap: 16px; margin-top: 16px; }
    .step{ padding: 16px; border-radius: 14px; background: rgba(255,255,255,.06); border: 1px solid rgba(255,255,255,.08); }
    .step .num{ font-weight: 900; color: var(--warning); }

    /* Footer */
    footer{ border-top: 1px solid rgba(255,255,255,.08); margin-top: 48px; }
    .foot{ display:flex; flex-wrap: wrap; justify-content: space-between; gap: 12px; color: var(--muted); padding: 22px 0; }

    /* Responsive */
    @media (max-width: 960px){
      .hero-grid{ grid-template-columns: 1fr; }
      .grid-2{ grid-template-columns: 1fr; }
      .features{ grid-template-columns: 1fr; }
      .how{ grid-template-columns: 1fr; }
      nav{ display:none; }
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header aria-label="Top navigation">
    <div class="wrap">
      <div class="row">
        <div class="brand" aria-label="TierOneX brand">
          <div class="logo" aria-hidden="true">TX</div>
          <div>
            <div style="font-size:18px">TierOneX</div>
            <div style="font-size:12px; color:var(--muted); font-weight:700">AR Plant Learning</div>
          </div>
        </div>
        <nav aria-label="Main">
          <a href="#learn">Learn</a>
          <a href="#demo">AR Demo</a>
          <a href="#teachers">Teacher Kit</a>
          <a href="#about">About</a>
        </nav>
        <button class="cta-btn" onclick="document.getElementById('demo').scrollIntoView({behavior:'smooth'})">Try the AR Demo</button>
      </div>
    </div>
  </header>

  <!-- Hero -->
  <section class="hero wrap">
    <div class="hero-grid">
      <div>
        <span class="badge">Made by Team TierOneX</span>
        <h1>Learn Plant Parts with <span style="background:linear-gradient(90deg,#74f0bc,#8aa9ff); -webkit-background-clip:text; background-clip:text; color:transparent">Augmented Reality</span></h1>
        <p class="lead">We turn any classroom into a science lab. Point a device, explore a 3D plant, and tap hotspots to hear kid‑friendly explanations of <strong>roots, stem, leaves, and flowers</strong>.</p>
        <div class="hero-actions">
          <button class="cta-btn" onclick="document.getElementById('learn').scrollIntoView({behavior:'smooth'})">Start Learning</button>
          <button class="btn-ghost" onclick="document.getElementById('teachers').scrollIntoView({behavior:'smooth'})">Teacher Resources</button>
          <a class="btn-ghost" href="#about" role="button" style="display:inline-block">About TierOneX</a>
        </div>
        <div class="badges" aria-hidden="true">
          <span class="badge">K–5 Friendly</span>
          <span class="badge">No Signup Needed</span>
          <span class="badge">Works Offline*</span>
        </div>
      </div>
      <div class="hero-card" id="demo">
        <h2 style="margin:0 0 10px">AR Demo (placeholder)</h2>
        <p class="lead" style="font-size:15px">Scan a classroom QR or open this on a phone to place a plant in AR. <em>Hook up your actual demo link here.</em></p>
        <div class="controls">
          <button class="primary" onclick="alert('Connect this button to your AR demo URL or WebXR page.')">Open AR</button>
          <button onclick="navigator.clipboard?.writeText(location.href).then(()=>alert('Link copied!'))">Copy Link</button>
        </div>
      </div>
    </div>
  </section>

  <!-- Learn Section: Plant Parts Explorer -->
  <section id="learn" class="section">
    <div class="wrap grid-2">
      <div class="panel explorer">
        <h2 style="margin:0 0 8px">Plant Parts Explorer</h2>
        <p class="lead" style="font-size:14px">Tap the glowing dots to learn what each part does. Toggle narration for audio.
        </p>
        <div class="svg-stage">
          <div class="svg-wrap">
            <!-- Simple SVG plant drawing -->
            <svg viewBox="0 0 400 500" role="img" aria-label="Simple illustration of a plant with roots, stem, leaves, and a flower">
              <defs>
                <filter id="glow"><feGaussianBlur stdDeviation="3.5" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
              </defs>
              <!-- soil -->
              <rect x="0" y="360" width="400" height="140" fill="#3c2d1a" opacity=".7"/>
              <!-- roots -->
              <path id="roots-shape" d="M200 360c-30 40-50 60-80 80 30-10 45-15 70-35-10 20-20 30-25 45 25-10 45-20 60-40 10 18 18 28 35 45-6-22-12-33-18-52 20 16 36 24 60 34-30-18-50-42-80-76z" fill="#d4a373"/>
              <!-- stem -->
              <rect id="stem-shape" x="193" y="160" width="14" height="200" rx="7" fill="#48b26b"/>
              <!-- leaves -->
              <path id="leaf-left" d="M190 250c-70-10-110-40-130-80 50 5 95 10 140 30-10 18-6 34-10 50z" fill="#3dbb78"/>
              <path id="leaf-right" d="M210 230c64-6 108-26 138-64-36-2-78 4-130 22 8 14-3 28-8 42z" fill="#33a86a"/>
              <!-- flower -->
              <circle id="flower-center" cx="200" cy="145" r="16" fill="#ffd166"/>
              <g id="petals" fill="#ff7aa2">
                <ellipse cx="200" cy="120" rx="12" ry="20"/>
                <ellipse cx="200" cy="170" rx="12" ry="20"/>
                <ellipse cx="175" cy="145" rx="20" ry="12"/>
                <ellipse cx="225" cy="145" rx="20" ry="12"/>
              </g>
            </svg>
          </div>
          <!-- Hotspots positioned over the SVG (absolute within .svg-stage) -->
          <div class="hotspots" aria-hidden="false" aria-label="Clickable plant hotspots">
            <button class="hot" data-part="roots" style="left: 200px; top: 390px" aria-label="Roots">R</button>
            <button class="hot" data-part="stem" style="left: 200px; top: 270px" aria-label="Stem">S</button>
            <button class="hot" data-part="leaves" style="left: 125px; top: 250px" aria-label="Leaves">L</button>
            <button class="hot" data-part="flower" style="left: 200px; top: 140px" aria-label="Flower">F</button>
          </div>
        </div>
      </div>

      <aside class="panel info" aria-live="polite" aria-atomic="true">
        <h2 id="part-title">Meet the Plant 🌱</h2>
        <p id="part-desc" class="desc">Tap a dot on the plant to learn what that part does. You can turn on narration to hear it out loud!</p>
        <div class="chiprow">
          <span class="chip">Roots</span>
          <span class="chip">Stem</span>
          <span class="chip">Leaves</span>
          <span class="chip">Flower</span>
        </div>
        <div class="controls">
          <button id="narrate-toggle" aria-pressed="false">🔊 Narration: Off</button>
          <button class="primary" onclick="document.getElementById('teachers').scrollIntoView({behavior:'smooth'})">Teacher Kit</button>
        </div>
      </aside>
    </div>

    <div class="wrap features">
      <div class="card"><h3>Kid‑Friendly</h3><p>Short, colorful explanations made for grades K–5.</p></div>
      <div class="card"><h3>Hands‑On</h3><p>Tap hotspots, get instant feedback, and hear narration.</p></div>
      <div class="card"><h3>AR Ready</h3><p>Place a 3D plant in your classroom for immersive learning.</p></div>
    </div>
  </section>

  <!-- How it works -->
  <section class="section" id="teachers">
    <div class="wrap">
      <h2>How it Works (Teachers)</h2>
      <div class="how">
        <div class="step"><div class="num">1.</div><strong>Open the demo</strong><br/>Use a tablet/phone to open the AR page (link above).</div>
        <div class="step"><div class="num">2.</div><strong>Place the plant</strong><br/>Move your device to detect a surface and tap to place.</div>
        <div class="step"><div class="num">3.</div><strong>Explore together</strong><br/>Students tap hotspots and explain what each part does.</div>
      </div>
      <p class="lead" style="margin-top:12px">Download printable worksheets and a quick lesson plan:</p>
      <div class="controls">
        <button onclick="alert('Hook this up to your PDF handout.')">📄 Worksheet (PDF)</button>
        <button onclick="alert('Hook this up to your slide deck.')">🖥️ Slides</button>
      </div>
    </div>
  </section>

  <!-- About -->
  <section class="section" id="about">
    <div class="wrap grid-2">
      <div class="panel" style="padding:18px">
        <h2>About TierOneX</h2>
        <p class="lead" style="font-size:15px">TierOneX is building playful AR experiences that make science stick. Our first module helps elementary students learn plant parts through exploration, narration, and hands‑on discovery.</p>
        <ul>
          <li>Focus: Elementary science (K–5)</li>
          <li>Tech: Web, WebXR/AR, accessible by design</li>
          <li>Mission: Turn curiosity into understanding</li>
        </ul>
      </div>
      <div class="panel" style="padding:18px">
        <h2>Team</h2>
        <p class="lead" style="font-size:15px">Team <strong>TierOneX</strong> — passionate about education, design, and emerging tech.</p>
        <div class="card" style="margin-top:8px">
          <h3 style="margin:0 0 4px">What we’re building next</h3>
          <p style="margin:0; color:var(--muted)">Fruit vs. seed; photosynthesis visualizer; bilingual narration.</p>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <div class="wrap foot">
      <div>© <span id="year"></span> TierOneX — AR Plant Learning</div>
      <div>
        <a href="#">Privacy</a> · <a href="#">Contact</a> · <a href="#">GitHub</a>
      </div>
    </div>
  </footer>

  <script>
    const ui = {
      title: document.getElementById('part-title'),
      desc: document.getElementById('part-desc'),
      narrateBtn: document.getElementById('narrate-toggle')
    };
    const parts = {
      roots: {
        name: 'Roots',
        description: 'Roots hold the plant in the ground and sip up water and minerals from the soil. Think of them like tiny straws!',
        highlight: ['roots-shape']
      },
      stem: {
        name: 'Stem',
        description: 'The stem is the plant’s elevator. It moves water and food up and down and helps the plant stand tall.',
        highlight: ['stem-shape']
      },
      leaves: {
        name: 'Leaves',
        description: 'Leaves are the chefs! Using sunlight, air, and water, they make food for the plant. This is called photosynthesis.',
        highlight: ['leaf-left','leaf-right']
      },
      flower: {
        name: 'Flower',
        description: 'Flowers help the plant make seeds so new plants can grow. Bright colors invite pollinators like bees.',
        highlight: ['flower-center','petals']
      }
    };

    let narrationOn = false;
    const originalFills = new Map();

    function speak(text){
      if(!narrationOn) return;
      try{
        const utter = new SpeechSynthesisUtterance(text);
        utter.rate = 1.05; utter.pitch = 1.0; utter.lang = 'en-US';
        window.speechSynthesis.cancel();
        window.speechSynthesis.speak(utter);
      }catch(e){
        console.warn('Speech not available', e);
      }
    }

    function highlight(ids){
      // reset previous
      document.querySelectorAll('#roots-shape,#stem-shape,#leaf-left,#leaf-right,#flower-center,#petals')
        .forEach(node=>{
          const key = node.id;
          if(originalFills.has(key)) node.setAttribute('fill', originalFills.get(key));
          node.style.filter = 'none';
          node.style.transition = 'filter .25s ease, transform .25s ease';
          node.style.transform = 'none';
        });
      // apply
      ids.forEach(id=>{
        const el = document.getElementById(id);
        if(!el) return;
        if(!originalFills.has(id)) originalFills.set(id, el.getAttribute('fill'));
        el.style.filter = 'url(#glow)';
        el.style.transform = 'scale(1.03)';
        el.setAttribute('fill', '#9af7c6');
      });
    }

    function showPart(key){
      const p = parts[key];
      if(!p) return;
      ui.title.textContent = p.name + ' 🌿';
      ui.desc.textContent = p.description;
      highlight(p.highlight);
      speak(p.name + '. ' + p.description);
    }

    // Wire hotspots
    document.querySelectorAll('.hot').forEach(btn=>{
      btn.addEventListener('click', ()=> showPart(btn.dataset.part));
      btn.addEventListener('keypress', (e)=>{ if(e.key==='Enter' || e.key===' '){ e.preventDefault(); showPart(btn.dataset.part); }});
    });

    // Narration toggle
    ui.narrateBtn.addEventListener('click', ()=>{
      narrationOn = !narrationOn;
      ui.narrateBtn.setAttribute('aria-pressed', narrationOn ? 'true' : 'false');
      ui.narrateBtn.textContent = narrationOn ? '🔊 Narration: On' : '🔇 Narration: Off';
      if(!narrationOn){ window.speechSynthesis?.cancel(); }
    });

    // Footer year
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
