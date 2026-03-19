<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Shubhanalytics — GitHub Profile</title>
  <link rel="preconnect" href="https://fonts.googleapis.com"/>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg-primary: #ffffff;
      --bg-secondary: #f5f5f3;
      --text-primary: #1a1a18;
      --text-secondary: #6b6b67;
      --border-light: rgba(0,0,0,0.1);
      --border-mid: rgba(0,0,0,0.18);
      --accent: #FA9D00;
      --radius-md: 8px;
      --radius-lg: 12px;
    }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg-primary);
      color: var(--text-primary);
      padding: 2.5rem 1.5rem;
      max-width: 880px;
      margin: 0 auto;
    }

    /* ── Hero ── */
    .hero {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 2rem;
      margin-bottom: 2.5rem;
      border-bottom: 0.5px solid var(--border-light);
      padding-bottom: 2.5rem;
    }
    .hero-left { flex: 1; }

    .tag {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--text-secondary);
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 1rem;
    }
    .tag::before {
      content: '';
      display: block;
      width: 24px;
      height: 1px;
      background: var(--accent);
    }

    .headline {
      font-family: 'Syne', sans-serif;
      font-size: 2.2rem;
      font-weight: 700;
      line-height: 1.12;
      color: var(--text-primary);
      margin-bottom: 0.85rem;
    }
    .headline span { color: var(--accent); }

    .sub {
      font-size: 14px;
      color: var(--text-secondary);
      line-height: 1.7;
      max-width: 440px;
    }

    .gif-frame {
      width: 136px;
      height: 136px;
      border-radius: 50%;
      border: 2px solid var(--accent);
      overflow: hidden;
      flex-shrink: 0;
      background: var(--bg-secondary);
    }
    .gif-frame img { width: 100%; height: 100%; object-fit: cover; }

    /* ── Chips ── */
    .chips {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 2.5rem;
    }
    .chip {
      font-size: 12px;
      font-weight: 500;
      padding: 5px 14px;
      border-radius: 999px;
      border: 0.5px solid var(--border-mid);
      color: var(--text-secondary);
      background: var(--bg-primary);
      letter-spacing: 0.02em;
    }
    .chip.accent {
      border-color: var(--accent);
      color: var(--accent);
      background: transparent;
    }

    /* ── Section label ── */
    .section-label {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--text-secondary);
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .section-label::after {
      content: '';
      flex: 1;
      height: 0.5px;
      background: var(--border-light);
    }

    /* ── Cards ── */
    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
      margin-bottom: 2.5rem;
    }
    .card {
      background: var(--bg-secondary);
      border-radius: var(--radius-lg);
      padding: 1rem 1.15rem;
      border: 0.5px solid var(--border-light);
    }
    .card-icon { font-size: 18px; margin-bottom: 8px; }
    .card-title {
      font-size: 11px;
      font-weight: 500;
      color: var(--text-secondary);
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 5px;
    }
    .card-body {
      font-size: 13px;
      color: var(--text-primary);
      line-height: 1.55;
    }

    /* ── Link buttons ── */
    .links-row {
      display: flex;
      gap: 12px;
      margin-bottom: 2.5rem;
      flex-wrap: wrap;
    }
    .link-btn {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 9px 18px;
      border-radius: var(--radius-md);
      border: 0.5px solid var(--border-mid);
      font-size: 13px;
      font-weight: 500;
      color: var(--text-primary);
      text-decoration: none;
      font-family: 'DM Sans', sans-serif;
      transition: border-color 0.2s, background 0.2s;
    }
    .link-btn:hover {
      border-color: var(--accent);
      background: var(--bg-secondary);
    }
    .link-btn .dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--accent);
      flex-shrink: 0;
    }

    /* ── Tools ── */
    .tools-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 2.5rem;
    }
    .tool-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 5px 12px;
      border-radius: var(--radius-md);
      border: 0.5px solid var(--border-light);
      background: var(--bg-primary);
      font-size: 12px;
      color: var(--text-secondary);
    }
    .tool-badge img { width: 16px; height: 16px; object-fit: contain; }

    /* ── Footer ── */
    .footer-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-top: 1.5rem;
      border-top: 0.5px solid var(--border-light);
      flex-wrap: wrap;
      gap: 1rem;
    }
    .social-links { display: flex; gap: 14px; }
    .social-links a {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-size: 13px;
      color: var(--text-secondary);
      text-decoration: none;
      font-family: 'DM Sans', sans-serif;
      transition: color 0.2s;
    }
    .social-links a:hover { color: var(--text-primary); }
    .social-links img { width: 16px; height: 16px; }
    .views-badge img { height: 22px; }

    /* ── Responsive ── */
    @media (max-width: 640px) {
      .cards { grid-template-columns: 1fr 1fr; }
      .hero { flex-direction: column-reverse; align-items: flex-start; }
      .headline { font-size: 1.75rem; }
    }
    @media (max-width: 420px) {
      .cards { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <!-- Hero -->
  <div class="hero">
    <div class="hero-left">
      <div class="tag">Data Scientist &amp; AI Engineer</div>
      <div class="headline">Analytics.<br>Learning.<br><span>Innovation.</span></div>
      <p class="sub">Certified in Data Science &amp; Business Analytics. Turning raw data into impactful insights — with SQL, Python, Tableau, Power BI, and a curiosity that never quits.</p>
    </div>
    <div class="gif-frame">
      <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" alt="Coding GIF"/>
    </div>
  </div>

  <!-- Skill Chips -->
  <div class="chips">
    <span class="chip accent">Data Science</span>
    <span class="chip accent">Machine Learning</span>
    <span class="chip accent">NLP</span>
    <span class="chip accent">GenAI</span>
    <span class="chip accent">LLM Orchestration</span>
    <span class="chip">SQL</span>
    <span class="chip">Python</span>
    <span class="chip">Tableau</span>
    <span class="chip">Power BI</span>
  </div>

  <!-- Currently -->
  <div class="section-label">Currently</div>
  <div class="cards">
    <div class="card">
      <div class="card-icon">⚙️</div>
      <div class="card-title">Building</div>
      <div class="card-body">AI Agents, Autonomous Bots &amp; Agentic Pipelines</div>
    </div>
    <div class="card">
      <div class="card-icon">🧠</div>
      <div class="card-title">Exploring</div>
      <div class="card-body">Agentic AI architectures, LLM fine-tuning &amp; Advanced NLP</div>
    </div>
    <div class="card">
      <div class="card-icon">🎓</div>
      <div class="card-title">Certified</div>
      <div class="card-body">PGPDSBA — Data Science &amp; Business Analytics</div>
    </div>
  </div>

  <!-- Links -->
  <div class="section-label">Links</div>
  <div class="links-row">
    <a class="link-btn" href="https://eportfolio.mygreatlearning.com/shubhank-katarey" target="_blank">
      <span class="dot"></span>PGPDSBA Portfolio
    </a>
    <a class="link-btn" href="https://shubhanalytics.github.io/shubhanalytics-webfolio/" target="_blank">
      <span class="dot"></span>Webfolio — Work &amp; Projects
    </a>
  </div>

  <!-- Languages & Tools -->
  <div class="section-label">Languages &amp; Tools</div>
  <div class="tools-grid">
    <span class="tool-badge"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python"/>Python</span>
    <span class="tool-badge"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg" alt="Pandas"/>Pandas</span>
    <span class="tool-badge"><img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="TensorFlow"/>TensorFlow</span>
    <span class="tool-badge"><img src="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" alt="PyTorch"/>PyTorch</span>
    <span class="tool-badge"><img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="Scikit-learn"/>Scikit-learn</span>
    <span class="tool-badge"><img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="Seaborn"/>Seaborn</span>
    <span class="tool-badge"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL"/>MySQL</span>
    <span class="tool-badge"><img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" alt="SQLite"/>SQLite</span>
    <span class="tool-badge"><img src="https://www.vectorlogo.zone/logos/microsoft_azure/microsoft_azure-icon.svg" alt="Azure"/>Azure</span>
    <span class="tool-badge"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="Docker"/>Docker</span>
    <span class="tool-badge"><img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="Kubernetes"/>Kubernetes</span>
    <span class="tool-badge"><img src="https://www.vectorlogo.zone/logos/rabbitmq/rabbitmq-icon.svg" alt="RabbitMQ"/>RabbitMQ</span>
    <span class="tool-badge"><img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git"/>Git</span>
    <span class="tool-badge"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML5"/>HTML5</span>
    <span class="tool-badge"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3"/>CSS3</span>
  </div>

  <!-- Footer -->
  <div class="footer-row">
    <div class="social-links">
      <a href="https://www.linkedin.com/in/shubhanalytics" target="_blank">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn"/>LinkedIn
      </a>
      <a href="https://x.com/shubhanalytics" target="_blank">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/twitter/twitter-original.svg" alt="Twitter/X"/>Twitter / X
      </a>
    </div>
    <div class="views-badge">
      <img src="https://komarev.com/ghpvc/?username=shubhanalytics&label=Visitors&color=FA9D00&style=flat-square" alt="Profile Views"/>
    </div>
  </div>

</body>
</html>
