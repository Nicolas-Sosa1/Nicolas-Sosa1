<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Nicolás Esteban Sosa | Portfolio</title>
  <meta name="description" content="Portfolio of Nicolás Esteban Sosa: C#, ASP.NET, relational databases, frontend and more.">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg: #0b0e15;
      --bg-soft: #101521;
      --card: #0e1420;
      --text: #e8edf7;
      --text-dim: #b7c1d9;
      --accent: #7c3aed; /* violeta */
      --accent-2: #06b6d4; /* cian */
      --ring: 0 0 0 2px rgba(124,58,237,.35);
      --radius: 16px;
      --shadow: 0 10px 30px rgba(0,0,0,.35), inset 0 1px 0 rgba(255,255,255,.02);
      --glass: rgba(255,255,255,.06);
      --border: 1px solid rgba(255,255,255,.08);
    }
    *{ box-sizing: border-box }
    html,body{ height:100% }
    body{
      margin:0; font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial;
      color:var(--text); background: radial-gradient(1200px 600px at 20% -10%, rgba(124,58,237,.18), transparent 60%),
                           radial-gradient(800px 400px at 90% 10%, rgba(6,182,212,.18), transparent 60%),
                           var(--bg);
      line-height:1.6;
    }
    a{ color:inherit; text-decoration:none }
    .container{ max-width:1100px; margin:0 auto; padding:24px 20px 64px }
    header{
      position:sticky; top:0; z-index:20; backdrop-filter:saturate(120%) blur(8px);
      background:linear-gradient(to bottom, rgba(10,12,20,.75), rgba(10,12,20,.35) 60%, transparent);
      border-bottom:var(--border);
    }
    .nav{
      display:flex; align-items:center; gap:16px; padding:14px 20px; max-width:1100px; margin:0 auto;
    }
    .brand{ font-weight:800; letter-spacing:.4px }
    .spacer{ flex:1 }
    .btn{
      display:inline-flex; align-items:center; gap:10px; padding:10px 14px; border-radius:12px; border:var(--border);
      background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
      box-shadow:var(--shadow); transition:.25s transform, .25s box-shadow, .25s background;
      font-weight:600; color:var(--text);
    }
    .btn:hover{ transform:translateY(-1px); box-shadow:0 16px 40px rgba(124,58,237,.18); }
    .btn.primary{ background:linear-gradient(180deg, var(--accent), #5b21b6); border:none }
    .btn.ghost{ background:transparent }

    .hero{
      display:grid; grid-template-columns:1.1fr .9fr; gap:28px; align-items:center; padding:32px 0 8px;
    }
    @media (max-width: 900px){ .hero{ grid-template-columns:1fr } }
    .card{
      background:linear-gradient(180deg, var(--glass), rgba(255,255,255,.03));
      border:var(--border); border-radius:var(--radius); box-shadow:var(--shadow);
    }
    .hero-card{ padding:28px }
    h1{ margin:0 0 10px; font-size:clamp(28px, 5vw, 44px); line-height:1.1 }
    .subtitle{ color:var(--text-dim); font-size:clamp(14px, 2.2vw, 18px) }
    .tags{ margin-top:18px; display:flex; flex-wrap:wrap; gap:10px }
    .tag{
      border:var(--border); border-radius:999px; padding:6px 10px; font-size:13px;
      background:rgba(124,58,237,.10); color:#d9d3ff;
    }
    .glass{
      padding:18px; border-radius:var(--radius); background:linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02)); border:var(--border)
    }
    .grid{
      display:grid; grid-template-columns:repeat(12,1fr); gap:16px; margin-top:26px;
    }
    .col-6{ grid-column:span 6 }
    .col-12{ grid-column:span 12 }
    @media (max-width: 900px){
      .col-6{ grid-column:span 12 }
    }
    h2{ font-size:22px; margin:0 0 10px }
    .section{ margin-top:34px }
    .pill{
      display:inline-flex; align-items:center; gap:8px; padding:8px 12px; border-radius:12px; border:var(--border);
      background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03)); font-weight:600; font-size:14px;
    }

    /* Icon rows */
    .icons{ display:flex; flex-wrap:wrap; gap:10px; align-items:center }
    .icons img{ height:38px; filter: drop-shadow(0 4px 10px rgba(0,0,0,.35)); transition: transform .2s }
    .icons img:hover{ transform: translateY(-2px) }

    /* Section cards */
    .tech-card{ padding:18px }
    .muted{ color:var(--text-dim) }

    /* Footer */
    footer{ margin-top:48px; padding-top:24px; border-top:var(--border); color:var(--text-dim); font-size:14px }

    /* Simple fade */
    [data-reveal]{ opacity:0; transform: translateY(10px); transition: .6s ease }
    [data-reveal].visible{ opacity:1; transform:none }
  </style>
</head>
<body>
  <header>
    <nav class="nav">
      <div class="brand">Nicolás Esteban Sosa</div>
      <div class="spacer"></div>
      <a class="btn ghost" href="https://github.com/Nicolas-Sosa1" target="_blank" rel="noreferrer">GitHub</a>
      <a class="btn" href="#contact">Contact</a>
      <button id="theme" class="btn primary" aria-label="Toggle theme">Toggle Theme</button>
    </nav>
  </header>

  <main class="container">
    <!-- HERO -->
    <section class="hero">
      <div class="card hero-card" data-reveal>
        <h1>Software Development Student</h1>
        <p class="subtitle">
          Focused on <strong>C#</strong> and <strong>ASP.NET</strong>, with a strong interest in <strong>relational databases</strong> and clean, accessible front-end.
          Currently improving my English and building real projects to sharpen my skills.
        </p>
        <div class="tags">
          <span class="tag">C#</span>
          <span class="tag">ASP.NET</span>
          <span class="tag">SQL Server</span>
          <span class="tag">HTML</span>
          <span class="tag">CSS</span>
          <span class="tag">JavaScript</span>
        </div>

        <div style="display:flex; gap:12px; margin-top:20px; flex-wrap:wrap">
          <a class="btn" href="mailto:youremail@example.com">Email</a>
          <a class="btn" href="https://www.linkedin.com/" target="_blank" rel="noreferrer">LinkedIn</a>
          <a class="btn ghost" href="https://Nicolas-Sosa1.github.io" target="_blank" rel="noreferrer">View Site</a>
        </div>
      </div>

      <div class="card hero-card" data-reveal>
        <div class="glass">
          <div class="pill">Quick Profile</div>
          <ul class="muted" style="margin:12px 0 0 18px">
            <li>Technicature in Programming (in progress)</li>
            <li>Back-end leaning; strong interest in C# / ASP.NET</li>
            <li>Relational DBs and clean domain models</li>
            <li>Learning English for professional growth</li>
          </ul>
        </div>

        <div class="grid">
          <div class="col-6 card tech-card" data-reveal>
            <h2>Frameworks</h2>
            <div class="icons">
              <!-- ASP.NET badge -->
              <img alt="ASP.NET" src="https://img.shields.io/badge/ASP.NET-5C2D91?style=for-the-badge&logo=dotnet&logoColor=white">
            </div>
            <p class="muted">Building web apps with the .NET ecosystem.</p>
          </div>

          <div class="col-6 card tech-card" data-reveal>
            <h2>Databases</h2>
            <div class="icons">
              <img alt="SQL Server" src="https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white">
            </div>
            <p class="muted">Relational schemas, stored procedures, and T-SQL.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- STACK -->
    <section class="section" data-reveal>
      <div class="pill">Tech Stack</div>
      <div class="grid">
        <div class="col-6 card tech-card">
          <h2>Frontend</h2>
          <div class="icons">
            <img alt="HTML" src="https://skillicons.dev/icons?i=html">
            <img alt="CSS" src="https://skillicons.dev/icons?i=css">
            <img alt="JavaScript" src="https://skillicons.dev/icons?i=js">
          </div>
          <p class="muted">Semantic HTML, modern CSS, basic components, and DOM manipulation.</p>
        </div>

        <div class="col-6 card tech-card">
          <h2>Technologies & Tools</h2>
          <div class="icons">
            <img alt="Git" src="https://skillicons.dev/icons?i=git">
            <img alt="GitHub" src="https://skillicons.dev/icons?i=github">
          </div>
          <p class="muted">Version control, branching, and collaborative workflows.</p>
        </div>

        <div class="col-12 card tech-card">
          <h2>Programming Languages</h2>
          <div class="icons">
            <img alt="C#" src="https://skillicons.dev/icons?i=cs">
            <img alt="C++" src="https://skillicons.dev/icons?i=cpp">
            <img alt="Java" src="https://skillicons.dev/icons?i=java">
          </div>
          <p class="muted">Strong focus on C#; exploring patterns and clean code practices.</p>
        </div>
      </div>
    </section>

    <!-- GITHUB STATS -->
    <section class="section card tech-card" data-reveal>
      <h2>GitHub Stats</h2>
      <p class="muted" style="margin-top:-6px">These charts reflect languages by code size (frameworks like ASP.NET count under C#).</p>
      <div style="display:flex; gap:16px; flex-wrap:wrap; align-items:center; justify-content:center; margin-top:8px">
        <img src="https://github-readme-stats.vercel.app/api?username=Nicolas-Sosa1&show_icons=true&theme=radical" alt="GitHub stats" height="180">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Nicolas-Sosa1&layout=compact&theme=radical" alt="Top languages" height="180">
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="section card tech-card" data-reveal>
      <h2>Contact</h2>
      <p class="muted">Open to internships, junior roles, and collaborative projects.</p>
      <div style="display:flex; gap:12px; flex-wrap:wrap; margin-top:8px">
        <a class="btn" href="mailto:youremail@example.com">youremail@example.com</a>
        <a class="btn ghost" href="https://github.com/Nicolas-Sosa1" target="_blank" rel="noreferrer">GitHub Profile</a>
        <a class="btn ghost" href="https://www.linkedin.com/" target="_blank" rel="noreferrer">LinkedIn</a>
      </div>
    </section>

    <footer class="container">
      <div>© <span id="year"></span> Nicolás Esteban Sosa · Built with HTML/CSS/JS</div>
    </footer>
  </main>

  <script>
    // Year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Theme toggle: swaps accent colors + background depth for a "wow" effect
    const btn = document.getElementById('theme');
    let dark = true;
    btn.addEventListener('click', () => {
      dark = !dark;
      document.documentElement.style.setProperty('--bg', dark ? '#0b0e15' : '#f7f8fc');
      document.documentElement.style.setProperty('--bg-soft', dark ? '#101521' : '#ffffff');
      document.documentElement.style.setProperty('--card', dark ? '#0e1420' : '#ffffff');
      document.documentElement.style.setProperty('--text', dark ? '#0f1220' : '#10121a');
      document.documentElement.style.setProperty('--text', dark ? '#e8edf7' : '#0f1220');
      document.documentElement.style.setProperty('--text-dim', dark ? '#b7c1d9' : '#4b5563');
      document.body.style.background = dark
        ? 'radial-gradient(1200px 600px at 20% -10%, rgba(124,58,237,.18), transparent 60%), radial-gradient(800px 400px at 90% 10%, rgba(6,182,212,.18), transparent 60%), #0b0e15'
        : 'radial-gradient(1000px 500px at 10% -10%, rgba(124,58,237,.10), transparent 60%), radial-gradient(700px 350px at 100% 10%, rgba(6,182,212,.10), transparent 60%), #f7f8fc';
    });

    // Simple reveal on scroll
    const reveal = () => {
      const els = document.querySelectorAll('[data-reveal]');
      const h = window.innerHeight;
      els.forEach(el => {
        const rect = el.getBoundingClientRect();
        if (rect.top < h - 60) el.classList.add('visible');
      });
    };
    reveal();
    document.addEventListener('scroll', reveal);
  </script>
</body>
</html>


