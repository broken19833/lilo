



[arkhangelsk_russian_north_product_v2.html](https://github.com/user-attachments/files/26419974/arkhangelsk_russian_north_product_v2.html)
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Русский Север — Архангельск и Северодвинск</title>
  <style>
    :root {
      --bg: #f6f1e8;
      --paper: #fbf7f0;
      --ink: #2e2a26;
      --muted: #665d55;
      --line: rgba(71, 57, 45, 0.18);
      --accent: #7a1f16;
      --accent-2: #1f4d64;
      --accent-3: #bf8f4c;
      --card: rgba(255,255,255,0.72);
      --shadow: 0 14px 40px rgba(53, 36, 24, 0.12);
      --radius: 24px;
      --radius-sm: 16px;
      --maxw: 1280px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: "Georgia", "Times New Roman", serif;
      color: var(--ink);
      background:
        radial-gradient(circle at top left, rgba(191,143,76,0.14), transparent 25%),
        radial-gradient(circle at top right, rgba(31,77,100,0.14), transparent 28%),
        linear-gradient(180deg, #f8f4ed 0%, #f3ecdf 100%);
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      opacity: 0.17;
      background-image:
        linear-gradient(var(--line) 1px, transparent 1px),
        linear-gradient(90deg, var(--line) 1px, transparent 1px);
      background-size: 32px 32px;
      mask-image: radial-gradient(circle at center, black 45%, transparent 100%);
    }

    .northern-ornament {
      height: 12px;
      background:
        repeating-linear-gradient(135deg,
          var(--accent) 0 10px,
          transparent 10px 18px,
          var(--accent-2) 18px 28px,
          transparent 28px 36px,
          var(--accent-3) 36px 46px,
          transparent 46px 54px);
      opacity: .85;
    }

    .container {
      width: min(100% - 32px, var(--maxw));
      margin: 0 auto;
    }

    .topbar {
      position: sticky;
      top: 0;
      z-index: 40;
      backdrop-filter: blur(12px);
      background: rgba(248, 244, 237, 0.78);
      border-bottom: 1px solid rgba(71,57,45,0.1);
    }

    .topbar-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
      padding: 14px 0;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 14px;
      min-width: 0;
    }

    .brand-mark {
      width: 52px;
      height: 52px;
      border-radius: 18px;
      background: linear-gradient(145deg, var(--accent), #9a3427);
      display: grid;
      place-items: center;
      color: #fff7eb;
      box-shadow: var(--shadow);
      font-size: 28px;
    }

    .brand h1 {
      font-size: 19px;
      margin: 0;
      letter-spacing: .4px;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    .brand p {
      margin: 2px 0 0;
      color: var(--muted);
      font-size: 13px;
    }

    .nav {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: flex-end;
    }

    .nav a,
    .btn,
    button.tab,
    .filter-btn {
      appearance: none;
      border: none;
      text-decoration: none;
      color: var(--ink);
      background: rgba(255,255,255,0.72);
      padding: 12px 16px;
      border-radius: 999px;
      font-size: 14px;
      cursor: pointer;
      transition: transform .28s ease, box-shadow .28s ease, background .28s ease, color .28s ease;
      box-shadow: 0 6px 18px rgba(53,36,24,0.06);
      border: 1px solid rgba(71,57,45,0.08);
    }

    .nav a:hover,
    .btn:hover,
    button.tab:hover,
    .filter-btn:hover,
    .filter-btn.active,
    button.tab.active {
      transform: translateY(-2px);
      background: linear-gradient(145deg, var(--accent), #9d3d2d);
      color: #fff7ef;
      box-shadow: 0 16px 30px rgba(122,31,22,0.22);
    }

    .hero {
      position: relative;
      padding: 72px 0 34px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.16fr .84fr;
      gap: 28px;
      align-items: stretch;
    }

    .panel {
      background: linear-gradient(180deg, rgba(255,255,255,0.78), rgba(255,255,255,0.64));
      border: 1px solid rgba(71,57,45,0.10);
      box-shadow: var(--shadow);
      border-radius: var(--radius);
      padding: 28px;
      position: relative;
      overflow: hidden;
    }

    .panel::after {
      content: "";
      position: absolute;
      inset: auto -20% -70% auto;
      width: 260px;
      height: 260px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(191,143,76,0.18), transparent 70%);
      pointer-events: none;
    }

    .eyebrow {
      display: inline-flex;
      gap: 8px;
      align-items: center;
      padding: 8px 12px;
      border-radius: 999px;
      background: rgba(31,77,100,0.1);
      color: var(--accent-2);
      font-size: 13px;
      margin-bottom: 16px;
    }

    .hero h2 {
      font-size: clamp(36px, 5vw, 64px);
      line-height: .98;
      margin: 0 0 18px;
      letter-spacing: -.5px;
    }

    .hero p.lead {
      margin: 0 0 22px;
      font-size: 18px;
      line-height: 1.7;
      color: #433c36;
      max-width: 760px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 24px;
    }

    .btn.primary {
      background: linear-gradient(145deg, var(--accent), #9d3d2d);
      color: #fff7ef;
      box-shadow: 0 16px 30px rgba(122,31,22,0.24);
    }

    .btn.secondary {
      background: linear-gradient(145deg, var(--accent-2), #2d617b);
      color: #f5fbff;
      box-shadow: 0 16px 30px rgba(31,77,100,0.24);
    }

    .hero-side {
      display: grid;
      gap: 18px;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
      margin-top: 12px;
    }

    .stat {
      border-radius: 18px;
      padding: 18px;
      background: rgba(255,255,255,0.72);
      border: 1px solid rgba(71,57,45,0.08);
      transition: transform .28s ease;
    }

    .stat:hover { transform: translateY(-3px); }
    .stat strong { display: block; font-size: 28px; margin-bottom: 4px; }
    .stat span { color: var(--muted); font-size: 14px; }

    .mini-map {
      min-height: 390px;
      display: flex;
      flex-direction: column;
      gap: 14px;
    }

    .section {
      padding: 30px 0;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 16px;
      margin-bottom: 22px;
    }

    .section-header h3 {
      margin: 0;
      font-size: clamp(28px, 4vw, 42px);
      line-height: 1.05;
    }

    .section-header p {
      margin: 8px 0 0;
      color: var(--muted);
      max-width: 760px;
      line-height: 1.7;
    }

    .badges {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 18px;
    }

    .badge {
      padding: 10px 14px;
      border-radius: 999px;
      background: rgba(191,143,76,0.12);
      color: #6a4b1f;
      border: 1px solid rgba(191,143,76,0.22);
      font-size: 14px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .card {
      position: relative;
      overflow: hidden;
      border-radius: 24px;
      background: linear-gradient(180deg, rgba(255,255,255,.76), rgba(255,255,255,.62));
      border: 1px solid rgba(71,57,45,0.1);
      box-shadow: var(--shadow);
      transition: transform .35s ease, box-shadow .35s ease;
      display: flex;
      flex-direction: column;
      min-height: 100%;
    }

    .card:hover {
      transform: translateY(-6px);
      box-shadow: 0 24px 48px rgba(53,36,24,0.16);
    }

    .card-media {
      min-height: 180px;
      padding: 22px;
      color: #fff8f0;
      display: flex;
      align-items: end;
      position: relative;
      overflow: hidden;
      background-size: cover;
      background-position: center;
    }

    .card-media::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(180deg, rgba(20,20,20,0.08), rgba(20,20,20,0.55));
    }

    .card-media h4 {
      position: relative;
      z-index: 1;
      margin: 0;
      font-size: 28px;
      line-height: 1.05;
    }

    .card-content {
      padding: 20px 20px 22px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      flex: 1;
    }

    .meta {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      color: var(--muted);
      font-size: 13px;
    }

    .card-content p {
      margin: 0;
      line-height: 1.72;
      color: #443d36;
      font-size: 16px;
    }

    .card-actions {
      margin-top: auto;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .card-actions button,
    .card-actions a {
      text-decoration: none;
      color: var(--ink);
      border: 1px solid rgba(71,57,45,0.08);
      background: rgba(255,255,255,0.8);
      border-radius: 999px;
      padding: 10px 14px;
      cursor: pointer;
      font-size: 14px;
      transition: .25s ease;
    }

    .card-actions button:hover,
    .card-actions a:hover {
      transform: translateY(-2px);
      background: var(--accent-2);
      color: #fff;
    }

    .tabs {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 18px;
    }

    .tab-panels > div { display: none; }
    .tab-panels > div.active { display: block; animation: fadeUp .45s ease; }

    .timeline {
      display: grid;
      gap: 14px;
    }

    .timeline-item {
      display: grid;
      grid-template-columns: 130px 1fr;
      gap: 18px;
      background: rgba(255,255,255,0.7);
      border: 1px solid rgba(71,57,45,0.08);
      border-radius: 22px;
      padding: 18px;
      transition: transform .28s ease;
    }

    .timeline-item:hover { transform: translateX(4px); }
    .timeline-item strong { font-size: 18px; color: var(--accent); }
    .timeline-item p { margin: 0; line-height: 1.7; color: #433d36; }

    .authors {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .author {
      padding: 24px;
      border-radius: 24px;
      background: linear-gradient(180deg, rgba(255,255,255,.8), rgba(255,255,255,.65));
      border: 1px solid rgba(71,57,45,.08);
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
    }

    .author::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 6px;
      background: linear-gradient(90deg, var(--accent), var(--accent-3), var(--accent-2));
    }

    .author .role {
      color: var(--accent-2);
      font-size: 13px;
      letter-spacing: .3px;
      text-transform: uppercase;
      margin-bottom: 10px;
    }

    .author h4 { margin: 0 0 10px; font-size: 24px; }
    .author p { margin: 0; line-height: 1.72; color: #453e38; }

    .map-wrap {
      display: grid;
      grid-template-columns: 1fr 0.86fr;
      gap: 18px;
      align-items: stretch;
    }

    .legend {
      display: grid;
      gap: 12px;
    }

    .legend-item {
      padding: 16px;
      border-radius: 18px;
      background: rgba(255,255,255,.74);
      border: 1px solid rgba(71,57,45,.08);
    }

    .legend-item strong { display:block; margin-bottom: 6px; }
    .legend-item p { margin: 0; color: var(--muted); line-height: 1.6; }

    .filters {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 18px;
    }

    .route-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
    }

    .route {
      padding: 22px;
      background: rgba(255,255,255,.74);
      border-radius: 24px;
      border: 1px solid rgba(71,57,45,.08);
      box-shadow: var(--shadow);
      transition: .28s ease;
    }

    .route:hover { transform: translateY(-4px); }
    .route h4 { margin: 0 0 10px; font-size: 24px; }
    .route p { margin: 0 0 14px; line-height: 1.7; color: #453f39; }
    .route ul { margin: 0; padding-left: 18px; color: #453f39; line-height: 1.7; }

    .faq {
      display: grid;
      gap: 14px;
    }

    .faq-item {
      border-radius: 22px;
      background: rgba(255,255,255,.76);
      border: 1px solid rgba(71,57,45,.08);
      overflow: hidden;
    }

    .faq-q {
      width: 100%;
      text-align: left;
      padding: 18px 22px;
      background: transparent;
      border: none;
      font-size: 18px;
      color: var(--ink);
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .faq-a {
      max-height: 0;
      overflow: hidden;
      transition: max-height .35s ease, padding .35s ease;
      padding: 0 22px;
      color: #453f38;
      line-height: 1.75;
    }

    .faq-item.open .faq-a {
      max-height: 220px;
      padding: 0 22px 18px;
    }

    .footer {
      padding: 36px 0 50px;
    }

    .footer-box {
      display: grid;
      grid-template-columns: 1.08fr .92fr;
      gap: 18px;
      align-items: stretch;
    }

    .small {
      color: var(--muted);
      font-size: 14px;
      line-height: 1.7;
    }

    .modal {
      position: fixed;
      inset: 0;
      background: rgba(24, 21, 19, 0.55);
      backdrop-filter: blur(8px);
      display: none;
      align-items: center;
      justify-content: center;
      padding: 20px;
      z-index: 100;
    }

    .modal.open { display: flex; }

    .modal-box {
      width: min(760px, 100%);
      background: linear-gradient(180deg, #fffdf9, #f7f1e8);
      border-radius: 28px;
      border: 1px solid rgba(71,57,45,.08);
      box-shadow: 0 32px 80px rgba(33,24,18,.25);
      padding: 28px;
      position: relative;
      animation: fadeUp .3s ease;
    }

    .modal-close {
      position: absolute;
      top: 14px;
      right: 14px;
      width: 42px;
      height: 42px;
      border-radius: 50%;
      border: none;
      cursor: pointer;
      background: rgba(255,255,255,.8);
      font-size: 22px;
    }

    .reveal {
      opacity: 0;
      transform: translateY(26px);
      transition: opacity .7s ease, transform .7s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(14px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .svgmap {
      width: 100%;
      height: 100%;
      min-height: 330px;
      border-radius: 22px;
      background: linear-gradient(180deg, #eef6f8, #e3eff2);
      border: 1px solid rgba(31,77,100,.10);
      overflow: hidden;
    }

    .svgmap text { font-family: Georgia, serif; fill: #234b5a; }
    .pin { cursor: pointer; transition: transform .2s ease; }
    .pin:hover { transform: scale(1.04); }

    @media (max-width: 1080px) {
      .hero-grid,
      .map-wrap,
      .footer-box {
        grid-template-columns: 1fr;
      }
      .cards { grid-template-columns: repeat(2, 1fr); }
      .authors { grid-template-columns: 1fr 1fr; }
    }

    @media (max-width: 760px) {
      .topbar-inner,
      .section-header {
        align-items: start;
        flex-direction: column;
      }
      .cards,
      .authors,
      .route-grid,
      .stats {
        grid-template-columns: 1fr;
      }
      .timeline-item {
        grid-template-columns: 1fr;
      }
      .hero { padding-top: 46px; }
      .panel { padding: 22px; }
      .brand h1 { white-space: normal; }
    }
  </style>
</head>
<body>
  <div class="northern-ornament"></div>

  <header class="topbar">
    <div class="container topbar-inner">
      <div class="brand">
        <div class="brand-mark">✦</div>
        <div>
          <h1>Русский Север — Архангельск и Северодвинск</h1>
          <p>Цифровой продукт о городах, истории, маршрутах и северной идентичности</p>
        </div>
      </div>
      <nav class="nav">
        <a href="#about">О проекте</a>
        <a href="#places">Места</a>
        <a href="#map">Карта</a>
        <a href="#routes">Маршруты</a>
        <a href="#authors">Авторы</a>
        <a href="#faq">FAQ</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-grid">
        <div class="panel reveal">
          <span class="eyebrow">Цифровой исследовательский проект • Русский Север</span>
          <h2>Достопримечательности Архангельска и Северодвинска в современном северном стиле</h2>
          <p class="lead">
            Этот продукт разработан как крупномасштабная интерактивная веб-платформа для жителей, студентов, гостей региона и всех, кто хочет познакомиться с образом Русского Севера через историю, городскую среду, знаковые места, маршруты и цифровую навигацию. Проект оформлен как презентационный сайт с удобными переходами, акцентом на северную эстетiku, картой и авторской подачей.
          </p>
          <div class="badges">
            <span class="badge">Архангельск</span>
            <span class="badge">Северодвинск</span>
            <span class="badge">Русский Север</span>
            <span class="badge">Интерактивный продукт</span>
            <span class="badge">Для распространения жителям</span>
          </div>
          <div class="hero-actions">
            <a class="btn primary" href="#places">Смотреть достопримечательности</a>
            <a class="btn secondary" href="#map">Открыть карту</a>
            <a class="btn" href="#authors">Команда авторов</a>
            <button class="btn" data-open="concept">Концепция продукта</button>
          </div>
        </div>

        <div class="hero-side reveal">
          <div class="panel mini-map">
            <div class="eyebrow">Навигация по северным точкам</div>
            <div class="svgmap" aria-label="Схематичная карта Архангельска и Северодвинска">
              <svg viewBox="0 0 700 420" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
                <defs>
                  <linearGradient id="river" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0%" stop-color="#8ac0d4"/>
                    <stop offset="100%" stop-color="#4b9ab6"/>
                  </linearGradient>
                  <linearGradient id="land" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0%" stop-color="#f4ead6"/>
                    <stop offset="100%" stop-color="#e8dcc6"/>
                  </linearGradient>
                </defs>
                <rect x="0" y="0" width="700" height="420" fill="#ecf5f8"/>
                <path d="M35 108 C90 82, 160 62, 240 80 S370 138, 432 128 S565 86, 658 116 L658 375 L35 375 Z" fill="url(#land)" opacity="0.92"/>
                <path d="M0 172 C122 120, 190 228, 286 202 S448 116, 556 160 S638 240, 700 228 L700 296 C620 286, 558 322, 460 300 S240 270, 120 300 S48 276, 0 284 Z" fill="url(#river)" opacity="0.95"/>
                <path d="M88 118 L168 88 L226 104 L282 90 L340 114 L390 104 L428 86 L488 110 L562 88 L616 106" fill="none" stroke="#c19352" stroke-width="5" stroke-linecap="round" stroke-dasharray="1 14"/>
                <g class="pin" data-title="Архангельск" data-text="Крупный исторический центр Русского Севера, связанный с морской торговлей, культурой Поморья и северной городской традицией.">
                  <circle cx="280" cy="182" r="16" fill="#7a1f16"/>
                  <circle cx="280" cy="182" r="6" fill="#fff3e7"/>
                  <text x="302" y="187" font-size="24">Архангельск</text>
                </g>
                <g class="pin" data-title="Северодвинск" data-text="Город на Белом море, соединяющий промышленную мощь, морскую тему и современную городскую идентичность.">
                  <circle cx="210" cy="132" r="14" fill="#1f4d64"/>
                  <circle cx="210" cy="132" r="5" fill="#eef8fc"/>
                  <text x="232" y="138" font-size="22">Северодвинск</text>
                </g>
                <g opacity=".8">
                  <text x="526" y="266" font-size="18">Северная Двина</text>
                  <text x="76" y="344" font-size="16">Схема-ориентир</text>
                </g>
              </svg>
            </div>
            <div class="small">Схематичная декоративная карта встроена прямо в продукт и подходит для демонстрации жителям, на мероприятиях, в сообщениях и в образовательных проектах.</div>
          </div>

          <div class="stats">
            <div class="stat">
              <strong>10+</strong>
              <span>кнопок и точек перехода по сайту</span>
            </div>
            <div class="stat">
              <strong>8</strong>
              <span>крупных разделов продукта</span>
            </div>
            <div class="stat">
              <strong>2</strong>
              <span>города в одной интерактивной карте</span>
            </div>
            <div class="stat">
              <strong>100%</strong>
              <span>готово к раздаче в виде HTML</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="about">
      <div class="container">
        <div class="section-header reveal">
          <div>
            <h3>О продукте</h3>
            <p>
              Сайт создан как полноценный цифровой продукт в стилистике Русского Севера. Здесь объединены информационная витрина, интерактивные карточки, маршруты, авторский блок, карта, а также элементы презентационной подачи. Проект можно использовать как веб-страницу для распространения среди жителей, участников мероприятий, студентов и гостей региона.
            </p>
          </div>
        </div>
        <div class="tabs reveal">
          <button class="tab active" data-tab="idea">Идея</button>
          <button class="tab" data-tab="goal">Цель</button>
          <button class="tab" data-tab="value">Польза</button>
          <button class="tab" data-tab="style">Стиль</button>
        </div>
        <div class="tab-panels reveal">
          <div class="active" id="idea">
            <div class="panel">
              Продукт показывает, что достопримечательности Архангельска и Северодвинска можно представить современно, удобно и визуально выразительно. Пользователь получает не просто текст, а цифровую среду с логичной структурой, акцентами, кнопками переходов, фильтрацией и картой.
            </div>
          </div>
          <div id="goal">
            <div class="panel">
              Цель продукта — представить северные города как пространство истории, культуры, морского наследия и городской идентичности, сделав цифровой материал понятным, красивым и полезным для широкой аудитории.
            </div>
          </div>
          <div id="value">
            <div class="panel">
              Польза продукта в том, что он помогает быстро познакомиться с ключевыми местами, выбрать маршрут, увидеть связку Архангельска и Северодвинска, а также использовать готовый сайт как презентационный или просветительский материал.
            </div>
          </div>
          <div id="style">
            <div class="panel">
              В основе визуального решения — оттенки дерева, льна, северной воды, меди и тёплой керамики. Такой стиль подчёркивает тему Русского Севера и делает продукт самобытным, а не шаблонным.
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="places">
      <div class="container">
        <div class="section-header reveal">
          <div>
            <h3>Ключевые достопримечательности</h3>
            <p>Выберите карточку и откройте краткое описание. Каждое место подано как отдельный элемент туристического и культурного образа города.</p>
          </div>
        </div>
        <div class="cards">
          <article class="card reveal">
            <div class="card-media" style="background-image: linear-gradient(140deg, rgba(31,77,100,.45), rgba(122,31,22,.35)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 500"><rect width="800" height="500" fill="%236b8ea2"/><path d="M0 380 L150 280 L280 330 L420 210 L560 300 L800 220 L800 500 L0 500 Z" fill="%23486658"/><rect x="290" y="140" width="210" height="170" fill="%23efe5d1"/><polygon points="270,155 395,70 520,155" fill="%237a1f16"/><rect x="360" y="180" width="70" height="130" fill="%23a44a38"/></svg>');">
              <h4>Гостиные дворы</h4>
            </div>
            <div class="card-content">
              <div class="meta"><span>Архангельск</span><span>история</span><span>архитектура</span></div>
              <p>Один из узнаваемых символов исторического Архангельска. Образ торгового города, северного порта и важного узла русской истории считывается здесь особенно ярко.</p>
              <div class="card-actions">
                <button data-open="dvory">Подробнее</button>
                <a href="#routes">Маршрут с объектом</a>
              </div>
            </div>
          </article>

          <article class="card reveal">
            <div class="card-media" style="background-image: linear-gradient(140deg, rgba(31,77,100,.35), rgba(191,143,76,.30)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 500"><rect width="800" height="500" fill="%2392bfd0"/><rect x="0" y="320" width="800" height="180" fill="%23749b78"/><path d="M180 340 L260 130 L330 340 Z" fill="%23503d2f"/><path d="M320 340 L400 80 L480 340 Z" fill="%23634835"/><path d="M460 340 L540 150 L620 340 Z" fill="%23554131"/><rect x="376" y="40" width="20" height="70" fill="%23b88f4d"/></svg>');">
              <h4>Малые Корелы</h4>
            </div>
            <div class="card-content">
              <div class="meta"><span>Архангельск</span><span>музей под открытым небом</span><span>Русский Север</span></div>
              <p>Пространство, где особенно наглядно раскрываются традиции северного деревянного зодчества. Для визуального образа проекта это один из самых сильных ориентиров.</p>
              <div class="card-actions">
                <button data-open="korely">Подробнее</button>
                <a href="#map">На карте</a>
              </div>
            </div>
          </article>

          <article class="card reveal">
            <div class="card-media" style="background-image: linear-gradient(140deg, rgba(122,31,22,.35), rgba(31,77,100,.34)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 500"><rect width="800" height="500" fill="%238cb6c8"/><rect x="0" y="330" width="800" height="170" fill="%236d8b6f"/><rect x="260" y="170" width="280" height="160" fill="%23f0e6d2"/><rect x="360" y="110" width="80" height="60" fill="%23f0e6d2"/><polygon points="240,190 400,80 560,190" fill="%237a1f16"/><rect x="392" y="55" width="16" height="60" fill="%23c49957"/></svg>');">
              <h4>Северный морской музей</h4>
            </div>
            <div class="card-content">
              <div class="meta"><span>Архангельск</span><span>море</span><span>экспозиции</span></div>
              <p>Место, через которое легко показать морскую судьбу города, поморские традиции и связь Архангельска с северными морскими путями.</p>
              <div class="card-actions">
                <button data-open="museum">Подробнее</button>
                <a href="#about">К концепции</a>
              </div>
            </div>
          </article>

          <article class="card reveal">
            <div class="card-media" style="background-image: linear-gradient(140deg, rgba(31,77,100,.42), rgba(191,143,76,.34)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 500"><rect width="800" height="500" fill="%2396c0d2"/><rect x="0" y="350" width="800" height="150" fill="%2386a388"/><path d="M120 310 C200 230, 280 180, 410 170 C540 160, 620 200, 710 290" stroke="%237a1f16" stroke-width="24" fill="none"/><rect x="170" y="298" width="56" height="52" fill="%23483b31"/><rect x="608" y="283" width="56" height="67" fill="%23483b31"/></svg>');">
              <h4>Северодвинская набережная</h4>
            </div>
            <div class="card-content">
              <div class="meta"><span>Северодвинск</span><span>прогулочный образ</span><span>море</span></div>
              <p>Современное городское пространство, которое помогает показать Северодвинск не только как промышленный, но и как выразительный северный город у воды.</p>
              <div class="card-actions">
                <button data-open="nab">Подробнее</button>
                <a href="#map">Смотреть схему</a>
              </div>
            </div>
          </article>

          <article class="card reveal">
            <div class="card-media" style="background-image: linear-gradient(140deg, rgba(122,31,22,.32), rgba(31,77,100,.42)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 500"><rect width="800" height="500" fill="%2385b4c7"/><rect x="0" y="336" width="800" height="164" fill="%23789a74"/><path d="M170 336 L280 146 L390 336 Z" fill="%2360493a"/><path d="M300 336 L420 96 L540 336 Z" fill="%234d3a2c"/><path d="M430 336 L520 180 L610 336 Z" fill="%23614b39"/></svg>');">
              <h4>Ягры и морской берег</h4>
            </div>
            <div class="card-content">
              <div class="meta"><span>Северодвинск</span><span>природный маршрут</span><span>побережье</span></div>
              <p>Побережье делает образ северного города особенно запоминающимся. Это пространство отдыха, созерцания и визуальной силы северного моря.</p>
              <div class="card-actions">
                <button data-open="yagry">Подробнее</button>
                <a href="#routes">Маршрут выходного дня</a>
              </div>
            </div>
          </article>

          <article class="card reveal">
            <div class="card-media" style="background-image: linear-gradient(140deg, rgba(31,77,100,.42), rgba(122,31,22,.34)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 500"><rect width="800" height="500" fill="%2393bfd0"/><rect x="0" y="348" width="800" height="152" fill="%23759877"/><rect x="250" y="150" width="300" height="200" fill="%23efe4d0"/><polygon points="220,180 400,90 580,180" fill="%231f4d64"/><circle cx="400" cy="250" r="52" fill="%23d3b485"/></svg>');">
              <h4>Городские площади и культурные точки</h4>
            </div>
            <div class="card-content">
              <div class="meta"><span>Архангельск / Северодвинск</span><span>общественные пространства</span><span>события</span></div>
              <p>Через площади, памятные места и культурные площадки формируется современный образ города для жителей и гостей. Это живая часть городской идентичности.</p>
              <div class="card-actions">
                <button data-open="city">Подробнее</button>
                <a href="#authors">Авторы идеи</a>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="section" id="map">
      <div class="container">
        <div class="section-header reveal">
          <div>
            <h3>Карта Архангельска и Северодвинска</h3>
            <p>Небольшая карта встроена в продукт как самостоятельный визуальный модуль. Её можно показывать отдельно, использовать как ориентир при выступлениях и как элемент цифрового туристического продукта.</p>
          </div>
        </div>
        <div class="map-wrap">
          <div class="panel reveal">
            <div class="svgmap">
              <svg viewBox="0 0 860 520" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
                <defs>
                  <linearGradient id="bigRiver" x1="0" y1="0" x2="1" y2="0">
                    <stop offset="0%" stop-color="#84c3d8"/>
                    <stop offset="100%" stop-color="#4e9ab7"/>
                  </linearGradient>
                  <linearGradient id="terrain" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0%" stop-color="#f4ead8"/>
                    <stop offset="100%" stop-color="#e9ddc9"/>
                  </linearGradient>
                </defs>
                <rect width="860" height="520" fill="#edf6f8"/>
                <path d="M66 118 C188 58, 314 70, 430 98 S630 120, 792 102 L792 418 L66 418 Z" fill="url(#terrain)"/>
                <path d="M0 236 C108 196, 164 266, 270 246 S444 166, 574 196 S720 274, 860 266 L860 336 C760 334, 690 378, 554 364 S300 334, 186 360 S86 350, 0 366 Z" fill="url(#bigRiver)"/>
                <path d="M126 130 C214 88, 280 104, 358 120" stroke="#b78b4b" stroke-width="5" fill="none" stroke-linecap="round" stroke-dasharray="2 16"/>
                <path d="M518 124 C596 108, 664 106, 760 126" stroke="#b78b4b" stroke-width="5" fill="none" stroke-linecap="round" stroke-dasharray="2 16"/>
                <g class="pin" data-title="Архангельск" data-text="Опорный центр проекта: исторический город, северный порт, символ культурной и торговой памяти Русского Севера.">
                  <circle cx="370" cy="232" r="20" fill="#7a1f16"/>
                  <circle cx="370" cy="232" r="8" fill="#fff4e8"/>
                  <text x="402" y="240" font-size="30">Архангельск</text>
                </g>
                <g class="pin" data-title="Северодвинск" data-text="Второй узел продукта: морская тема, северная индустрия, береговой характер и современная городская среда.">
                  <circle cx="244" cy="148" r="18" fill="#1f4d64"/>
                  <circle cx="244" cy="148" r="7" fill="#edf8fc"/>
                  <text x="275" y="155" font-size="28">Северодвинск</text>
                </g>
                <g opacity="0.82">
                  <text x="652" y="315" font-size="20">Северная Двина</text>
                  <text x="628" y="438" font-size="18">Северный цифровой маршрут</text>
                </g>
              </svg>
            </div>
          </div>
          <div class="legend reveal">
            <div class="legend-item">
              <strong>Архангельск</strong>
              <p>Историческая и культурная основа проекта. В центре внимания — морское наследие, северная архитектура, музеи и городской образ.</p>
            </div>
            <div class="legend-item">
              <strong>Северодвинск</strong>
              <p>Город, который раскрывается через море, побережье, современные пространства и связь с промышленной и морской историей.</p>
            </div>
            <div class="legend-item">
              <strong>Связка двух городов</strong>
              <p>Продукт показывает не изолированные точки, а цельный северный маршрут, где Архангельск и Северодвинск образуют единую визуальную и смысловую линию.</p>
            </div>
            <div class="legend-item">
              <strong>Использование</strong>
              <p>Готово для демонстрации на экране, публикации в чатах, отправки жителям, показов на мероприятиях и включения в студенческие проекты.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="routes">
      <div class="container">
        <div class="section-header reveal">
          <div>
            <h3>Маршруты и сценарии просмотра</h3>
            <p>Ниже представлены варианты использования продукта: для жителей, гостей, студентов и для событийного показа.</p>
          </div>
        </div>
        <div class="filters reveal">
          <button class="filter-btn active" data-filter="all">Все</button>
          <button class="filter-btn" data-filter="walk">Прогулочные</button>
          <button class="filter-btn" data-filter="edu">Образовательные</button>
          <button class="filter-btn" data-filter="sea">Морские</button>
        </div>
        <div class="route-grid">
          <article class="route reveal" data-kind="walk sea">
            <h4>Маршрут «Север у воды»</h4>
            <p>Подходит для знакомства с морской и набережной темой Архангельска и Северодвинска.</p>
            <ul>
              <li>Исторический образ Архангельска как северного порта.</li>
              <li>Связка с музеями и набережными пространствами.</li>
              <li>Финальный акцент — береговая тема Северодвинска и Ягр.</li>
            </ul>
          </article>
          <article class="route reveal" data-kind="edu">
            <h4>Маршрут «История Русского Севера»</h4>
            <p>Подходит для учебных показов, презентаций и цифровой экскурсии без выезда на место.</p>
            <ul>
              <li>Гостиные дворы как исторический узел.</li>
              <li>Малые Корелы как визуальный образ северной архитектуры.</li>
              <li>Музейные точки и культурный контекст региона.</li>
            </ul>
          </article>
          <article class="route reveal" data-kind="walk edu">
            <h4>Маршрут «Город глазами жителя»</h4>
            <p>Делает акцент на повседневном и узнаваемом облике города.</p>
            <ul>
              <li>Площади, культурные точки и городские пространства.</li>
              <li>Простая логика перехода по разделам сайта.</li>
              <li>Удобно показывать аудитории любого возраста.</li>
            </ul>
          </article>
          <article class="route reveal" data-kind="sea">
            <h4>Маршрут «Море, порт, берег»</h4>
            <p>Подчёркивает связь городов с водой, северным морем и прибрежной эстетикой.</p>
            <ul>
              <li>Морская тема как визуальный мотив продукта.</li>
              <li>Северодвинск как береговой и морской образ.</li>
              <li>Схематичная карта как единый северный ориентир.</li>
            </ul>
          </article>
        </div>
      </div>
    </section>

    <section class="section" id="process">
      <div class="container">
        <div class="section-header reveal">
          <div>
            <h3>Как создавался продукт</h3>
            <p>Блок оформлен так, будто сайт разрабатывался командой авторов как самостоятельный цифровой проект: от идеи до структуры и визуальной подачи.</p>
          </div>
        </div>
        <div class="timeline">
          <div class="timeline-item reveal">
            <strong>Этап 1</strong>
            <p>Формирование идеи продукта: определение тематики, целевой аудитории, роли Архангельска и Северодвинска в едином северном визуальном маршруте.</p>
          </div>
          <div class="timeline-item reveal">
            <strong>Этап 2</strong>
            <p>Отбор смысловых опор: история, морская линия, городские пространства, музейный и культурный образ, эстетика Русского Севера.</p>
          </div>
          <div class="timeline-item reveal">
            <strong>Этап 3</strong>
            <p>Разработка интерфейса: крупные кнопки, переходы, интерактивные карточки, встроенная карта, блоки для презентационного использования.</p>
          </div>
          <div class="timeline-item reveal">
            <strong>Этап 4</strong>
            <p>Оформление авторского раздела и адаптация продукта для раздачи жителям в виде HTML-страницы, которую можно открывать локально без сложной установки.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="authors">
      <div class="container">
        <div class="section-header reveal">
          <div>
            <h3>Авторы проекта</h3>
            <p>Сайт оформлен как командный цифровой продукт, созданный коллективом авторов.</p>
          </div>
        </div>
        <div class="authors">
          <div class="author reveal">
            <div class="role">Автор проекта / концепция</div>
            <h4>Мамаджанов Джонибек Джамшедович</h4>
            <p>Разработка общей концепции продукта, формирование северного визуального образа, логики цифровой подачи и структуры презентационного сайта для жителей.</p>
          </div>
          <div class="author reveal">
            <div class="role">Соавтор / исследовательский блок</div>
            <h4>Ильин Михаил Александрович</h4>
            <p>Участие в формировании смыслового содержания, подбор направлений маршрутизации, акцентов по достопримечательностям и пользовательскому восприятию продукта.</p>
          </div>
          <div class="author reveal">
            <div class="role">Соавтор / структура и навигация</div>
            <h4>Марков Кирилл Ильич</h4>
            <p>Проработка структуры разделов, сценариев перехода по кнопкам, логики подачи материала и удобства использования сайта как готового цифрового решения.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="faq">
      <div class="container">
        <div class="section-header reveal">
          <div>
            <h3>Частые вопросы</h3>
            <p>Раздел помогает быстро объяснить, как применять продукт на практике.</p>
          </div>
        </div>
        <div class="faq">
          <div class="faq-item reveal">
            <button class="faq-q">Для чего подходит этот сайт? <span>+</span></button>
            <div class="faq-a">Сайт подходит для демонстрации жителям, раздачи в сообщениях, использования на мероприятиях, включения в учебные проекты и как самостоятельный цифровой материал о городах Русского Севера.</div>
          </div>
          <div class="faq-item reveal">
            <button class="faq-q">Можно ли открывать его без интернета? <span>+</span></button>
            <div class="faq-a">Да. Это одиночный HTML-файл, который можно открыть на компьютере локально. Его удобно отправлять, хранить и показывать офлайн как готовый продукт.</div>
          </div>
          <div class="faq-item reveal">
            <button class="faq-q">Чем он лучше простой презентации? <span>+</span></button>
            <div class="faq-a">У сайта есть интерактивность: кнопки, переходы, фильтрация, карта, карточки и модальные окна. Это делает подачу современнее и заметно удобнее для аудитории.</div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="container footer-box">
      <div class="panel reveal">
        <div class="eyebrow">Готовый цифровой продукт</div>
        <h3 style="margin:0 0 12px; font-size: 34px;">Продукт можно раздавать жителям уже сейчас</h3>
        <p class="small">
          HTML-страница собрана в одном файле, поэтому её можно распространять без дополнительной настройки. Она сохраняет стиль Русского Севера, крупную структуру, авторский блок, интерактивную карту и презентационную подачу.
        </p>
        <div class="hero-actions">
          <a class="btn primary" href="#top" onclick="window.scrollTo({top:0, behavior:'smooth'}); return false;">Наверх</a>
          <a class="btn secondary" href="#places">К местам</a>
          <button class="btn" data-open="team">О команде</button>
        </div>
      </div>
      <div class="panel reveal">
        <div class="eyebrow">Командная подпись</div>
        <p style="font-size:18px; line-height:1.8; margin:0;">
          <strong>Авторы:</strong><br>
          Мамаджанов Джонибек Джамшедович<br>
          Ильин Михаил Александрович<br>
          Марков Кирилл Ильич
        </p>
        <p class="small" style="margin-top:14px;">Проект выполнен как крупномасштабный цифровой веб-продукт о достопримечательностях Архангельска и Северодвинска в стилистике Русского Севера.</p>
      </div>
    </div>
  </footer>

  <div class="modal" id="modal">
    <div class="modal-box">
      <button class="modal-close" aria-label="Закрыть">×</button>
      <div id="modal-content"></div>
    </div>
  </div>

  <script>
    const modalData = {
      concept: {
        title: 'Концепция продукта',
        body: 'Продукт задуман как современная северная цифровая витрина: он одновременно выполняет роль сайта, презентации, мини-гайда по городам и визуального маршрута. В центре — крупный интерфейс, ясная структура, много кнопок и переходов, а также ощущение северного культурного кода.'
      },
      dvory: {
        title: 'Гостиные дворы',
        body: 'В логике проекта этот объект играет роль исторического ядра. Через него удобно говорить о торговом прошлом Архангельска, его связях с морем и особой роли в северной истории России.'
      },
      korely: {
        title: 'Малые Корелы',
        body: 'Этот объект особенно важен для стилистики продукта, потому что он напрямую связан с образом Русского Севера, деревянного зодчества и традиционной северной культуры.'
      },
      museum: {
        title: 'Северный морской музей',
        body: 'Музей усиливает морскую линию повествования. Он помогает показать Архангельск как город памяти, движения, портовой истории и северного морского характера.'
      },
      nab: {
        title: 'Северодвинская набережная',
        body: 'Набережная задаёт современный городской ритм и делает Северодвинск частью цельного северного маршрута. Это важная точка для городской визуальной идентичности.'
      },
      yagry: {
        title: 'Ягры и морской берег',
        body: 'Береговая линия делает образ города живым и масштабным. В продукте эта точка показывает связь человека с северным ландшафтом, морем и открытым пространством.'
      },
      city: {
        title: 'Городские площади и культурные точки',
        body: 'Через общественные пространства пользователь видит город не как набор сухих фактов, а как реальную среду. Это делает цифровой продукт ближе к жизни жителей.'
      },
      team: {
        title: 'Команда проекта',
        body: 'Продукт оформлен как совместная работа авторов. Внутри сайта командный характер проекта подчёркивается отдельным блоком авторства, общим стилем и единой логикой подачи материала.'
      }
    };

    const modal = document.getElementById('modal');
    const modalContent = document.getElementById('modal-content');
    const closeModalBtn = document.querySelector('.modal-close');

    document.querySelectorAll('[data-open]').forEach(btn => {
      btn.addEventListener('click', () => {
        const key = btn.dataset.open;
        const item = modalData[key];
        if (!item) return;
        modalContent.innerHTML = `<h3 style="margin:0 0 12px; font-size:32px;">${item.title}</h3><p style="margin:0; line-height:1.8; font-size:18px; color:#433d36;">${item.body}</p>`;
        modal.classList.add('open');
      });
    });

    closeModalBtn.addEventListener('click', () => modal.classList.remove('open'));
    modal.addEventListener('click', e => { if (e.target === modal) modal.classList.remove('open'); });

    document.querySelectorAll('.tab').forEach(tab => {
      tab.addEventListener('click', () => {
        document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
        tab.classList.add('active');
        document.querySelectorAll('.tab-panels > div').forEach(panel => panel.classList.remove('active'));
        document.getElementById(tab.dataset.tab).classList.add('active');
      });
    });

    document.querySelectorAll('.faq-q').forEach(btn => {
      btn.addEventListener('click', () => {
        const item = btn.closest('.faq-item');
        item.classList.toggle('open');
        btn.querySelector('span').textContent = item.classList.contains('open') ? '–' : '+';
      });
    });

    document.querySelectorAll('.filter-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        const filter = btn.dataset.filter;
        document.querySelectorAll('.route').forEach(route => {
          const kinds = route.dataset.kind.split(' ');
          const show = filter === 'all' || kinds.includes(filter);
          route.style.display = show ? 'block' : 'none';
        });
      });
    });

    document.querySelectorAll('.pin').forEach(pin => {
      pin.addEventListener('click', () => {
        modalContent.innerHTML = `<h3 style="margin:0 0 12px; font-size:32px;">${pin.dataset.title}</h3><p style="margin:0; line-height:1.8; font-size:18px; color:#433d36;">${pin.dataset.text}</p>`;
        modal.classList.add('open');
      });
    });

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) entry.target.classList.add('visible');
      });
    }, { threshold: 0.12 });

    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
  </script>
</body>
</html>
