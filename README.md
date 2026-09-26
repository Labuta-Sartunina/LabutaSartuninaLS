<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Labuta Saturnina — Agricultura, Construção & Assessoria</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=Outfit:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --green: #0b1f16;
    --green2: #103b26;
    --gold: #d4a843;
    --gold2: #e8c468;
    --sage: #7fae86;
    --white: #f5f7f0;
    --gray: #9fb0a3;
    --light: #e6efe4;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }

  body {
    font-family: 'Outfit', sans-serif;
    background: var(--green);
    color: var(--white);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 18px 6%;
    background: rgba(11,31,22,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(212,168,67,0.15);
  }
  .logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.35rem; font-weight: 900;
    color: var(--white);
    letter-spacing: 1px;
    display: flex; align-items: center; gap: 10px;
  }
  .logo-mark {
    width: 34px; height: 34px; border-radius: 8px;
    background: linear-gradient(135deg, var(--gold), var(--gold2));
    color: var(--green); display: flex; align-items: center; justify-content: center;
    font-weight: 900; font-size: 1rem;
  }
  .logo span { color: var(--gold); font-weight: 400; font-size: 1rem; letter-spacing: 3px; }
  nav ul { list-style: none; display: flex; gap: 32px; }
  nav ul a {
    color: var(--gray); text-decoration: none; font-size: .9rem;
    font-weight: 500; letter-spacing: .5px;
    transition: color .25s;
  }
  nav ul a:hover { color: var(--gold); }
  .nav-cta {
    background: var(--gold); color: var(--green) !important;
    padding: 9px 22px; border-radius: 6px;
    font-weight: 600 !important;
    transition: background .25s !important;
  }
  .nav-cta:hover { background: var(--gold2) !important; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: flex; align-items: center;
    padding: 120px 6% 80px;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 60% 80% at 70% 40%, rgba(212,168,67,0.12) 0%, transparent 65%),
      radial-gradient(ellipse 50% 60% at 20% 70%, rgba(127,174,134,0.10) 0%, transparent 60%);
  }
  .hero-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 60px; align-items: center;
    position: relative; z-index: 1;
    max-width: 1200px; margin: 0 auto; width: 100%;
  }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(212,168,67,0.12);
    border: 1px solid rgba(212,168,67,0.3);
    border-radius: 50px; padding: 6px 16px;
    font-size: .8rem; color: var(--gold);
    letter-spacing: 1.5px; text-transform: uppercase;
    margin-bottom: 24px;
    animation: fadeUp .6s ease both;
  }
  .hero-badge::before { content: '🌿'; font-size: 1rem; }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.6rem, 5vw, 4rem);
    line-height: 1.15; font-weight: 900;
    margin-bottom: 20px;
    animation: fadeUp .6s .1s ease both;
  }
  .hero h1 em { font-style: italic; color: var(--gold); }
  .hero p {
    font-size: 1.1rem; line-height: 1.7;
    color: var(--gray); max-width: 480px;
    margin-bottom: 36px;
    animation: fadeUp .6s .2s ease both;
  }
  .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; animation: fadeUp .6s .3s ease both; }
  .btn-primary {
    background: var(--gold); color: var(--green);
    padding: 14px 30px; border-radius: 8px;
    font-weight: 600; font-size: .95rem;
    text-decoration: none; letter-spacing: .3px;
    transition: transform .2s, box-shadow .2s;
    box-shadow: 0 4px 20px rgba(212,168,67,0.35);
    display: inline-flex; align-items: center; gap: 8px;
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 28px rgba(212,168,67,0.45); }
  .btn-secondary {
    border: 1.5px solid rgba(212,168,67,0.5); color: var(--gold);
    padding: 14px 30px; border-radius: 8px;
    font-weight: 500; font-size: .95rem;
    text-decoration: none; letter-spacing: .3px;
    transition: background .2s;
  }
  .btn-secondary:hover { background: rgba(212,168,67,0.1); }

  .hero-visual { position: relative; animation: fadeRight .8s .2s ease both; }
  .hero-card {
    background: linear-gradient(135deg, var(--green2), #0e2c1e);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 20px; padding: 36px;
    position: relative; overflow: hidden;
    box-shadow: 0 30px 80px rgba(0,0,0,0.5);
  }
  .hero-card::before {
    content: '';
    position: absolute; top: 0; right: 0;
    width: 180px; height: 180px;
    background: radial-gradient(circle, rgba(212,168,67,0.2) 0%, transparent 70%);
  }
  .hero-flag { font-size: 2.5rem; margin-bottom: 16px; }
  .hero-card h3 { font-family: 'Playfair Display', serif; font-size: 1.5rem; margin-bottom: 8px; }
  .hero-card p { font-size: .9rem; color: var(--gray); margin-bottom: 28px; }
  .stat-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 24px; }
  .stat-box { background: rgba(255,255,255,0.05); border-radius: 12px; padding: 16px; text-align: center; }
  .stat-box .num { font-family: 'Playfair Display', serif; font-size: 1.3rem; font-weight: 700; color: var(--gold); }
  .stat-box .lbl { font-size: .75rem; color: var(--gray); text-transform: uppercase; letter-spacing: 1px; margin-top: 4px; }
  .trust-bar {
    display: flex; align-items: center; gap: 10px;
    background: rgba(212,168,67,0.08);
    border: 1px solid rgba(212,168,67,0.2);
    border-radius: 10px; padding: 12px 16px;
    font-size: .85rem; color: var(--gold);
  }
  .trust-bar::before { content: '🛡'; font-size: 1.1rem; }

  /* ── SECTION COMUM ── */
  section { padding: 90px 6%; }
  .section-label { font-size: .78rem; letter-spacing: 3px; text-transform: uppercase; color: var(--gold); margin-bottom: 10px; }
  .section-title { font-family: 'Playfair Display', serif; font-size: clamp(2rem, 3.5vw, 2.8rem); font-weight: 900; line-height: 1.2; margin-bottom: 16px; }
  .section-sub { color: var(--gray); font-size: 1.05rem; line-height: 1.6; max-width: 560px; margin-bottom: 56px; }

  /* ── SERVIÇOS ── */
  #servicos { background: var(--green2); }
  .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 24px; max-width: 1200px; margin: 0 auto; }
  .srv-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.07);
    border-radius: 16px; padding: 32px;
    transition: transform .3s, border-color .3s, box-shadow .3s;
    position: relative; overflow: hidden;
  }
  .srv-card:hover { transform: translateY(-6px); border-color: rgba(212,168,67,0.4); box-shadow: 0 20px 50px rgba(0,0,0,0.35); }
  .srv-card::after {
    content: ''; position: absolute; bottom: 0; left: 0; right: 0; height: 3px;
    background: linear-gradient(90deg, var(--gold), var(--sage));
    transform: scaleX(0); transform-origin: left; transition: transform .35s;
  }
  .srv-card:hover::after { transform: scaleX(1); }
  .srv-icon {
    width: 52px; height: 52px; background: rgba(212,168,67,0.15);
    border-radius: 12px; display: flex; align-items: center; justify-content: center;
    font-size: 1.5rem; margin-bottom: 20px;
  }
  .srv-card h3 { font-size: 1.15rem; font-weight: 600; margin-bottom: 12px; }
  .srv-card p { font-size: .9rem; color: var(--gray); line-height: 1.6; }
  .srv-list { list-style: none; margin-top: 16px; }
  .srv-list li { font-size: .88rem; color: var(--gray); padding: 5px 0; display: flex; align-items: center; gap: 8px; }
  .srv-list li::before { content: '→'; color: var(--gold); font-size: .8rem; }

  /* ── DOCUMENTAÇÃO DESTAQUE ── */
  #documentacao { background: var(--green); position: relative; overflow: hidden; }
  #documentacao::before {
    content: ''; position: absolute; top: -100px; right: -100px;
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(212,168,67,0.08) 0%, transparent 70%);
  }
  .doc-inner { max-width: 1200px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: center; position: relative; z-index: 1; }
  .doc-steps { display: flex; flex-direction: column; gap: 20px; }
  .step {
    display: flex; align-items: flex-start; gap: 18px;
    padding: 20px 24px; background: rgba(255,255,255,0.04);
    border-radius: 12px; border-left: 3px solid var(--gold);
    transition: background .25s;
  }
  .step:hover { background: rgba(255,255,255,0.07); }
  .step-num { font-family: 'Playfair Display', serif; font-size: 1.8rem; font-weight: 900; color: var(--gold); opacity: .5; line-height: 1; flex-shrink: 0; }
  .step h4 { font-size: 1rem; font-weight: 600; margin-bottom: 4px; }
  .step p { font-size: .88rem; color: var(--gray); }
  .doc-highlight {
    background: linear-gradient(135deg, var(--green2), #0e2c1e);
    border: 1px solid rgba(212,168,67,0.2);
    border-radius: 20px; padding: 40px; text-align: center;
    box-shadow: 0 20px 60px rgba(0,0,0,0.4);
  }
  .doc-highlight .big-icon { font-size: 4rem; margin-bottom: 16px; }
  .doc-highlight h3 { font-family: 'Playfair Display', serif; font-size: 1.6rem; margin-bottom: 12px; }
  .doc-highlight p { color: var(--gray); font-size: .95rem; line-height: 1.6; margin-bottom: 28px; }
  .flag-row { font-size: 1.8rem; letter-spacing: 6px; margin-bottom: 24px; }
  .doc-types { display: flex; flex-wrap: wrap; gap: 10px; justify-content: center; }
  .doc-tag {
    background: rgba(212,168,67,0.15); border: 1px solid rgba(212,168,67,0.3);
    border-radius: 50px; padding: 6px 16px; font-size: .82rem; color: var(--gold2); font-weight: 500;
  }

  /* ── DETALHE DOCUMENTAÇÃO ── */
  #legalizacao { background: var(--green2); }
  .legal-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 24px; max-width: 1200px; margin: 0 auto; }
  .legal-card {
    background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.07);
    border-radius: 16px; padding: 30px; transition: transform .25s, border-color .25s;
  }
  .legal-card:hover { transform: translateY(-4px); border-color: rgba(212,168,67,0.3); }
  .legal-card .ico {
    width: 48px; height: 48px; border-radius: 12px;
    background: rgba(212,168,67,0.15); display: flex; align-items: center; justify-content: center;
    font-size: 1.4rem; margin-bottom: 18px;
  }
  .legal-card h4 { font-size: 1.05rem; font-weight: 700; margin-bottom: 4px; }
  .legal-card .sub { font-size: .82rem; color: var(--sage); margin-bottom: 14px; }
  .legal-list { list-style: none; }
  .legal-list li { font-size: .87rem; color: var(--gray); padding: 4px 0; display: flex; gap: 8px; }
  .legal-list li::before { content: '✓'; color: var(--gold); }

  /* ── PORQUE NÓS ── */
  #porque { background: var(--green); }
  .porque-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 30px; max-width: 1200px; margin: 0 auto; }
  .pq-card { padding: 36px 28px; border-radius: 16px; position: relative; overflow: hidden; }
  .pq-card:nth-child(1) { background: linear-gradient(135deg, rgba(212,168,67,0.15), rgba(212,168,67,0.05)); border: 1px solid rgba(212,168,67,0.2); }
  .pq-card:nth-child(2) { background: linear-gradient(135deg, rgba(127,174,134,0.15), rgba(127,174,134,0.05)); border: 1px solid rgba(127,174,134,0.25); }
  .pq-card:nth-child(3) { background: linear-gradient(135deg, rgba(212,168,67,0.1), rgba(127,174,134,0.05)); border: 1px solid rgba(255,255,255,0.1); }
  .pq-card .pq-icon { font-size: 2.2rem; margin-bottom: 20px; }
  .pq-card h3 { font-size: 1.15rem; font-weight: 700; margin-bottom: 12px; }
  .pq-card p { font-size: .9rem; color: var(--gray); line-height: 1.6; }

  /* ── CONTACTO ── */
  #contacto { background: linear-gradient(135deg, var(--green2), var(--green)); text-align: center; }
  .contacto-inner { max-width: 700px; margin: 0 auto; }
  .contacto-inner .section-sub { margin: 0 auto 40px; }
  .contact-options { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; margin-bottom: 48px; }
  .contact-btn {
    display: inline-flex; align-items: center; gap: 10px;
    padding: 14px 28px; border-radius: 10px; font-weight: 600; font-size: .95rem;
    text-decoration: none; transition: transform .2s, box-shadow .2s;
  }
  .contact-btn:hover { transform: translateY(-3px); }
  .contact-btn.wa { background: #25d366; color: #fff; box-shadow: 0 4px 20px rgba(37,211,102,0.3); }
  .contact-btn.wa:hover { box-shadow: 0 8px 30px rgba(37,211,102,0.45); }
  .contact-btn.phone { background: rgba(255,255,255,0.08); border: 1px solid rgba(255,255,255,0.15); color: var(--white); }
  .address-box {
    background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08);
    border-radius: 14px; padding: 24px 32px; display: inline-block;
    font-size: .9rem; color: var(--gray); line-height: 1.8; text-align: left;
  }
  .address-box strong { color: var(--white); }

  /* ── FOOTER ── */
  footer { background: #061109; padding: 40px 6% 28px; border-top: 1px solid rgba(255,255,255,0.06); }
  .footer-inner { max-width: 1200px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 20px; }
  .footer-logo { font-family: 'Playfair Display', serif; font-size: 1.1rem; }
  .footer-logo span { color: var(--gold); }
  .footer-links { display: flex; gap: 24px; }
  .footer-links a { color: var(--gray); text-decoration: none; font-size: .85rem; }
  .footer-links a:hover { color: var(--white); }
  .footer-copy { font-size: .8rem; color: var(--gray); margin-top: 24px; text-align: center; }

  @keyframes fadeUp { from { opacity: 0; transform: translateY(28px); } to { opacity: 1; transform: translateY(0); } }
  @keyframes fadeRight { from { opacity: 0; transform: translateX(40px); } to { opacity: 1; transform: translateX(0); } }

  @media (max-width: 768px) {
    nav ul { display: none; }
    .hero-grid { grid-template-columns: 1fr; gap: 40px; }
    .doc-inner { grid-template-columns: 1fr; gap: 40px; }
    .porque-grid { grid-template-columns: 1fr; }
    .hero { padding-top: 100px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo"><span class="logo-mark">LS</span>LABUTA <span>SATURNINA</span></div>
  <ul>
    <li><a href="#servicos">Serviços</a></li>
    <li><a href="#documentacao">Documentação</a></li>
    <li><a href="#porque">Sobre Nós</a></li>
    <li><a href="#contacto" class="nav-cta">Contactar</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-grid">
    <div class="hero-text">
      <div class="hero-badge">Agricultura · Construção · Assessoria</div>
      <h1>Trabalho sério,<br>do <em>campo</em> à sua casa.</h1>
      <p>Agricultura, construção, imóveis, automóveis, limpeza e assessoria documental — a Labuta Saturnina trata do seu projecto do início ao fim, com equipas próprias e acompanhamento pessoal.</p>
      <div class="hero-btns">
        <a href="#contacto" class="btn-primary">💬 Fale Connosco</a>
        <a href="#servicos" class="btn-secondary">Ver Serviços</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-card">
        <div class="hero-flag">🇧🇷 🇵🇹</div>
        <h3>Labuta Saturnina, Lda</h3>
        <p>Agricultura · Assessoria · Construção · Automóveis · Imóveis · Limpeza</p>
        <div class="stat-row">
          <div class="stat-box">
            <div class="num">Santarém</div>
            <div class="lbl">Sede</div>
          </div>
          <div class="stat-box">
            <div class="num">6 áreas</div>
            <div class="lbl">De atuação</div>
          </div>
        </div>
        <div class="trust-bar">Empresa registada e legalmente constituída</div>
      </div>
    </div>
  </div>
</section>

<!-- SERVIÇOS -->
<section id="servicos">
  <div style="max-width:1200px;margin:0 auto;">
    <p class="section-label">O que fazemos</p>
    <h2 class="section-title">Seis áreas,<br>uma só equipa de confiança</h2>
    <p class="section-sub">Da terra à obra, do imóvel ao carro — a Labuta Saturnina acompanha o seu projecto com equipas próprias e atenção ao detalhe.</p>
  </div>
  <div class="services-grid">
    <div class="srv-card">
      <div class="srv-icon">🌾</div>
      <h3>Agricultura</h3>
      <p>Mão de obra qualificada para diversas atividades agrícolas, com organização e compromisso.</p>
      <ul class="srv-list">
        <li>Apanha de fruta e vindimas</li>
        <li>Podas e plantação</li>
        <li>Manutenção de terrenos</li>
      </ul>
    </div>
    <div class="srv-card">
      <div class="srv-icon">🏗️</div>
      <h3>Construção</h3>
      <p>Do projeto à obra pronta — soluções completas para casa, empresa ou investimento.</p>
      <ul class="srv-list">
        <li>Construção de raiz</li>
        <li>Remodelações e ampliações</li>
        <li>Acabamentos e manutenção</li>
      </ul>
    </div>
    <div class="srv-card">
      <div class="srv-icon">🏠</div>
      <h3>Imóveis</h3>
      <p>Compra, venda e gestão de imóveis próprios e alheios, incluindo alojamento local.</p>
      <ul class="srv-list">
        <li>Compra e venda</li>
        <li>Arrendamento</li>
        <li>Gestão e alojamento local</li>
      </ul>
    </div>
    <div class="srv-card">
      <div class="srv-icon">🚗</div>
      <h3>Aluguer de Automóveis</h3>
      <p>Mais liberdade para o seu dia a dia, com viaturas semi-novas e seguras.</p>
      <ul class="srv-list">
        <li>Aluguer diário, semanal ou mensal</li>
        <li>Económicos, SUV e familiares</li>
        <li>Manutenção incluída</li>
      </ul>
    </div>
    <div class="srv-card">
      <div class="srv-icon">🧹</div>
      <h3>Limpeza</h3>
      <p>Serviços de limpeza para casas, obras e espaços comerciais, com atenção e cuidado.</p>
      <ul class="srv-list">
        <li>Limpeza doméstica</li>
        <li>Limpeza pós-obra</li>
        <li>Espaços comerciais</li>
      </ul>
    </div>
    <div class="srv-card">
      <div class="srv-icon">📋</div>
      <h3>Assessoria & Documentação</h3>
      <p>Apoio a quem quer vir trabalhar em Portugal, do NIF ao visto.</p>
      <ul class="srv-list">
        <li>NIF e NISS</li>
        <li>Vistos e autorização de residência</li>
        <li>Acompanhamento do processo</li>
      </ul>
    </div>
  </div>
</section>

<!-- DOCUMENTAÇÃO -->
<section id="documentacao">
  <div class="doc-inner">
    <div>
      <p class="section-label">Quer vir trabalhar em Portugal?</p>
      <h2 class="section-title">A sua documentação<br>em dia, sem complicações</h2>
      <p class="section-sub" style="margin-bottom:40px;">Ajudamos em todo o processo para que possa trabalhar em Portugal com segurança e legalidade.</p>
      <div class="doc-steps">
        <div class="step">
          <div class="step-num">01</div>
          <div>
            <h4>Orientação Inicial</h4>
            <p>Explicamos que tipo de visto ou documento se aplica ao seu caso.</p>
          </div>
        </div>
        <div class="step">
          <div class="step-num">02</div>
          <div>
            <h4>NIF e NISS</h4>
            <p>Pedido, atualização de morada e apoio na ativação no Portal das Finanças e na Segurança Social Direta.</p>
          </div>
        </div>
        <div class="step">
          <div class="step-num">03</div>
          <div>
            <h4>Preenchimento de Formulários</h4>
            <p>Organizamos a documentação e preparamos os formulários necessários.</p>
          </div>
        </div>
        <div class="step">
          <div class="step-num">04</div>
          <div>
            <h4>Agendamento AIMA / VFS</h4>
            <p>Tratamos do agendamento e acompanhamos o processo até ao fim.</p>
          </div>
        </div>
      </div>
    </div>
    <div class="doc-highlight">
      <div class="big-icon">🛂</div>
      <div class="flag-row">🇧🇷 🇵🇹</div>
      <h3>Apoio Documental Completo</h3>
      <p>Atendimento personalizado para trabalhadores de todas as áreas, com processo simples e seguro.</p>
      <div class="doc-types">
        <span class="doc-tag">🪪 NIF</span>
        <span class="doc-tag">🏛️ NISS</span>
        <span class="doc-tag">🛂 Visto</span>
        <span class="doc-tag">📄 Autorização de Residência</span>
      </div>
      <br>
      <a href="#contacto" class="btn-primary" style="display:inline-flex;margin-top:16px;">Tirar Dúvidas</a>
    </div>
  </div>
</section>

<!-- DETALHE DOCUMENTAÇÃO -->
<section id="legalizacao">
  <div style="max-width:1200px;margin:0 auto;">
    <p class="section-label">Passo a passo</p>
    <h2 class="section-title">O que tratamos<br>por si</h2>
    <p class="section-sub">Três frentes de apoio para quem quer viver e trabalhar em Portugal com segurança.</p>
  </div>
  <div class="legal-grid">
    <div class="legal-card">
      <div class="ico">🪪</div>
      <h4>NIF</h4>
      <p class="sub">Número de Identificação Fiscal</p>
      <ul class="legal-list">
        <li>Pedido do NIF</li>
        <li>Atualização de morada</li>
        <li>Apoio na ativação no Portal das Finanças</li>
        <li>Emissão de certidões</li>
        <li>Representação fiscal (se necessário)</li>
      </ul>
    </div>
    <div class="legal-card">
      <div class="ico">🏛️</div>
      <h4>NISS</h4>
      <p class="sub">Número de Identificação da Segurança Social</p>
      <ul class="legal-list">
        <li>Pedido do NISS</li>
        <li>Regularização de dados</li>
        <li>Apoio no registo na Segurança Social Direta</li>
        <li>Declarações e comprovativos</li>
        <li>Acompanhamento do processo</li>
      </ul>
    </div>
    <div class="legal-card">
      <div class="ico">🛂</div>
      <h4>Visto</h4>
      <p class="sub">Apoio em vistos e autorização de residência</p>
      <ul class="legal-list">
        <li>Orientação sobre o tipo de visto</li>
        <li>Organização da documentação</li>
        <li>Preenchimento de formulários</li>
        <li>Agendamento (AIMA / VFS)</li>
        <li>Acompanhamento do processo</li>
      </ul>
    </div>
  </div>
</section>

<!-- PORQUE NÓS -->
<section id="porque">
  <div style="max-width:1200px;margin:0 auto;">
    <p class="section-label">Porque escolher-nos</p>
    <h2 class="section-title">Equipas próprias,<br>compromisso real</h2>
    <p class="section-sub">Mais do que uma empresa de serviços — somos parceiros no seu projeto, do campo à sua nova vida em Portugal.</p>
  </div>
  <div class="porque-grid">
    <div class="pq-card">
      <div class="pq-icon">🤝</div>
      <h3>Atendimento Personalizado</h3>
      <p>Cada cliente é acompanhado de forma próxima, com respostas claras para as suas dúvidas.</p>
    </div>
    <div class="pq-card">
      <div class="pq-icon">🔒</div>
      <h3>Segurança e Confiança</h3>
      <p>Trabalho seguro e responsável, com processos simples e transparentes do início ao fim.</p>
    </div>
    <div class="pq-card">
      <div class="pq-icon">⚙️</div>
      <h3>Soluções Personalizadas</h3>
      <p>Equipas adaptáveis a pequenas ou grandes operações, para trabalhadores de todas as áreas.</p>
    </div>
  </div>
</section>

<!-- CONTACTO -->
<section id="contacto">
  <div class="contacto-inner">
    <p class="section-label">Fale Connosco</p>
    <h2 class="section-title">Pronto para<br>começar?</h2>
    <p class="section-sub">Solicite um orçamento sem compromisso ou tire as suas dúvidas sobre documentação.</p>
    <div class="contact-options">
      <a href="https://wa.me/351930904943" class="contact-btn wa" target="_blank">💬 WhatsApp</a>
      <a href="tel:+351930904943" class="contact-btn phone">📞 Ligar Agora</a>
    </div>
    <div class="address-box">
      <strong>📍 Labuta Saturnina, Lda</strong><br>
      Rua do Sal, n.º 17<br>
      União de Freguesias da Cidade de Santarém<br>
      2000-598 Ribeira de Santarém, Santarém<br><br>
      <strong>📞 +351 930 904 943</strong>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-logo">LABUTA <span>SATURNINA</span> — Agricultura, Construção & Assessoria</div>
    <div class="footer-links">
      <a href="#servicos">Serviços</a>
      <a href="#documentacao">Documentação</a>
      <a href="#porque">Sobre Nós</a>
      <a href="#contacto">Contacto</a>
    </div>
  </div>
  <p class="footer-copy">© 2025 Labuta Saturnina, Lda · Todos os direitos reservados · <em style="color:#d4a843">Trabalho sério, resultados reais.</em></p>
</footer>

</body>
</html>
