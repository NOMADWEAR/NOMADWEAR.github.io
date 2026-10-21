<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NOMAD WEAR — Кастомная одежда</title>

<!-- ===== КОД ВЕРИФИКАЦИИ ===== -->
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<!-- Verification: f66d3dcca44a8022 -->

<!-- ===== БИБЛИОТЕКА ДЛЯ ПОДПИСИ (MD5) ===== -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/blueimp-md5/2.19.0/js/md5.min.js"></script>

<style>
  /* ---------- БАЗА ---------- */
  * { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --bg: #0d0d0f;
    --bg-2: #16161a;
    --card: #1c1c22;
    --accent: #c8d0d8;
    --accent-light: #eef2f5;
    --accent-dark: #8a97a3;
    --accent-grad: linear-gradient(135deg, #f2f6f9 0%, #b9c4cf 20%, #e6edf2 40%, #98a5b2 60%, #d8e0e7 80%, #aab6c2 100%);
    --accent-2: #ff4d6d;
    --text: #f5f5f7;
    --muted: #8a8a94;
    --border: #2a2a33;
  }

  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.6;
    overflow-x: hidden;
    position: relative;
  }

  /* ---------- ФОН С КАРТИНКОЙ (БОЛЕЕ ВЫРАЖЕННЫЙ) ---------- */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url('MG_2661.JPG'); /* ИМЯ ВАШЕГО ФАЙЛА */
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    filter: blur(3px) brightness(0.5) contrast(1.08) saturate(1.15);
    transform: scale(1.05);
    z-index: -2;
    pointer-events: none;
  }

  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse at 20% 0%, rgba(200, 208, 216, 0.08) 0%, transparent 55%),
      radial-gradient(ellipse at 80% 100%, rgba(200, 208, 216, 0.06) 0%, transparent 55%),
      repeating-linear-gradient(45deg, rgba(255,255,255,0.012) 0px, rgba(255,255,255,0.012) 1px, transparent 1px, transparent 6px),
      rgba(13, 13, 15, 0.45);
    z-index: -1;
    pointer-events: none;
  }

  a { color: inherit; text-decoration: none; }
  img { max-width: 100%; display: block; }

  /* ---------- HEADER ---------- */
  header {
    position: sticky;
    top: 0;
    z-index: 100;
    background: rgba(13, 13, 15, 0.75);
    backdrop-filter: blur(14px);
    border-bottom: 1px solid var(--border);
    box-shadow: 0 1px 0 rgba(200, 208, 216, 0.08), 0 4px 20px rgba(0,0,0,0.5);
  }

  .nav {
    max-width: 1280px;
    margin: 0 auto;
    padding: 1rem 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1.5rem;
  }

  .logo {
    font-size: 1.4rem;
    font-weight: 900;
    letter-spacing: -0.02em;
    cursor: pointer;
  }
  .logo span {
    background: var(--accent-grad);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
  }

  .nav-links {
    display: flex;
    align-items: center;
    gap: 2rem;
    list-style: none;
  }
  .nav-links li { display: flex; align-items: center; }
  .nav-links a {
    display: inline-flex;
    align-items: center;
    line-height: 1;
    font-size: 0.9rem;
    color: var(--muted);
    transition: color 0.2s;
    cursor: pointer;
  }
  .nav-links a:hover { color: var(--accent-light); }

  .cart-btn {
    background: var(--accent-grad);
    color: #0d0d0f;
    border: 1px solid #e6edf2;
    padding: 0.6rem 1.2rem;
    border-radius: 999px;
    font-weight: 700;
    font-size: 0.9rem;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.6), 0 2px 8px rgba(0,0,0,0.4);
  }
  .cart-btn:hover {
    transform: scale(1.05);
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.8), 0 4px 16px rgba(200,208,216,0.25);
  }

  .cart-count {
    background: #0d0d0f;
    color: var(--accent-light);
    border-radius: 999px;
    padding: 0 0.5rem;
    font-size: 0.75rem;
    min-width: 20px;
    text-align: center;
  }

  /* ---------- HERO ---------- */
  .hero {
    max-width: 1280px;
    margin: 0 auto;
    padding: 5rem 2rem 3rem;
    text-align: center;
  }

  .hero h1 {
    font-size: clamp(2.5rem, 6vw, 5rem);
    font-weight: 900;
    line-height: 1;
    letter-spacing: -0.03em;
    margin-bottom: 1.5rem;
  }
  .hero h1 .accent {
    background: var(--accent-grad);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
    font-style: italic;
    filter: drop-shadow(0 0 12px rgba(200, 208, 216, 0.35));
  }
  .hero p {
    color: var(--muted);
    font-size: 1.1rem;
    max-width: 600px;
    margin: 0 auto 2rem;
  }

  .hero-cta {
    display: inline-block;
    background: var(--accent-grad);
    color: #0d0d0f;
    padding: 1rem 2.5rem;
    border-radius: 999px;
    font-weight: 800;
    font-size: 1rem;
    cursor: pointer;
    border: 1px solid #e6edf2;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.7), 0 4px 14px rgba(0,0,0,0.4);
  }
  .hero-cta:hover {
    transform: translateY(-3px);
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.9), 0 10px 30px rgba(200, 208, 216, 0.28);
  }

  /* ---------- TABS (СТИЛИ) ---------- */
  .styles-section {
    max-width: 1280px;
    margin: 0 auto;
    padding: 2rem;
  }

  .section-title {
    font-size: 1.8rem;
    font-weight: 800;
    margin-bottom: 0.5rem;
  }
  .section-sub {
    color: var(--muted);
    margin-bottom: 2rem;
  }

  .tabs {
    display: flex;
    gap: 0.5rem;
    overflow-x: auto;
    padding-bottom: 0.5rem;
    margin-bottom: 2rem;
    scrollbar-width: thin;
  }
  .tabs::-webkit-scrollbar { height: 4px; }
  .tabs::-webkit-scrollbar-thumb { background: var(--border); border-radius: 4px; }

  .tab {
    background: var(--bg-2);
    border: 1px solid var(--border);
    color: var(--muted);
    padding: 0.7rem 1.4rem;
    border-radius: 999px;
    font-weight: 600;
    font-size: 0.9rem;
    cursor: pointer;
    white-space: nowrap;
    transition: all 0.2s;
  }
  .tab:hover {
    color: var(--text);
    border-color: var(--muted);
  }
  .tab.active {
    background: var(--accent-grad);
    color: #0d0d0f;
    border-color: #e6edf2;
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.7), 0 2px 10px rgba(200,208,216,0.2);
  }

  /* ---------- КАТАЛОГ ---------- */
  .products {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 1.5rem;
  }

  .product-card {
    background: linear-gradient(160deg, rgba(31,31,38,0.92) 0%, rgba(25,25,32,0.92) 50%, rgba(29,29,36,0.92) 100%);
    backdrop-filter: blur(8px);
    border: 1px solid var(--border);
    border-radius: 16px;
    overflow: hidden;
    transition: transform 0.3s, border-color 0.3s, box-shadow 0.3s;
    display: flex;
    flex-direction: column;
    position: relative;
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.04), 0 2px 12px rgba(0,0,0,0.4);
  }
  .product-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, rgba(230,237,242,0.5), transparent);
    pointer-events: none;
  }
  .product-card:hover {
    transform: translateY(-6px);
    border-color: var(--accent);
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.08), 0 12px 32px rgba(200,208,216,0.15);
  }

  .product-img {
    aspect-ratio: 1 / 1;
    background:
      linear-gradient(135deg, #23232b, #2f2f3a),
      repeating-linear-gradient(60deg, rgba(255,255,255,0.03) 0px, rgba(255,255,255,0.03) 1px, transparent 1px, transparent 8px);
    background-blend-mode: overlay;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
  }
  .product-tag {
    position: absolute;
    top: 12px;
    left: 12px;
    background: var(--accent-2);
    color: #fff;
    font-size: 0.7rem;
    font-weight: 700;
    padding: 0.25rem 0.7rem;
    border-radius: 999px;
    text-transform: uppercase;
    box-shadow: 0 2px 8px rgba(0,0,0,0.4);
  }

  .product-info {
    padding: 1rem 1.2rem 1.4rem;
    display: flex;
    flex-direction: column;
    flex: 1;
  }

  .product-style {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 700;
    margin-bottom: 0.4rem;
    background: var(--accent-grad);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
  }

  .product-name {
    font-size: 1rem;
    font-weight: 700;
    margin-bottom: 0.8rem;
  }

  .product-bottom {
    margin-top: auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .price {
    font-size: 1.2rem;
    font-weight: 900;
  }
  .price small { color: var(--muted); font-size: 0.8rem; font-weight: 500; }

  .add-btn {
    background: transparent;
    border: 1px solid var(--accent);
    color: var(--accent-light);
    padding: 0.5rem 1rem;
    border-radius: 999px;
    font-weight: 700;
    font-size: 0.8rem;
    cursor: pointer;
    transition: all 0.2s;
    box-shadow: inset 0 0 0 rgba(255,255,255,0);
  }
  .add-btn:hover {
    background: var(--accent-grad);
    color: #0d0d0f;
    border-color: #e6edf2;
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.7), 0 2px 10px rgba(200,208,216,0.25);
  }
  .add-btn:active { transform: scale(0.95); }

  /* ---------- BACK BUTTON ---------- */
  .back-btn {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: transparent;
    border: 1px solid var(--border);
    color: var(--muted);
    padding: 0.6rem 1.2rem;
    border-radius: 999px;
    font-weight: 600;
    font-size: 0.85rem;
    cursor: pointer;
    margin-bottom: 1.5rem;
    transition: all 0.2s;
  }
  .back-btn:hover {
    color: var(--accent-light);
    border-color: var(--accent);
  }

  /* ---------- ABOUT (РАСКРЫВАЮЩИЙСЯ БЛОК ВНИЗУ) ---------- */
  .about-wrap {
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  .about-toggle {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.6rem;
    background: transparent;
    border: 1px solid var(--border);
    color: var(--muted);
    padding: 1rem 2rem;
    border-radius: 999px;
    font-weight: 700;
    font-size: 0.95rem;
    cursor: pointer;
    transition: all 0.25s;
    margin-top: 2rem;
  }
  .about-toggle:hover {
    color: var(--accent-light);
    border-color: var(--accent);
    box-shadow: 0 4px 20px rgba(200,208,216,0.12);
  }
  .about-toggle .arrow {
    display: inline-block;
    transition: transform 0.35s ease;
    font-size: 0.8rem;
  }
  .about-wrap.open .about-toggle .arrow {
    transform: rotate(180deg);
  }

  /* Контейнер раскрытия — плавно растягивает страницу вниз */
  .about-reveal {
    display: grid;
    grid-template-rows: 0fr;
    transition: grid-template-rows 0.5s ease, opacity 0.4s ease, margin 0.4s ease;
    opacity: 0;
    margin-top: 0;
  }
  .about-wrap.open .about-reveal {
    grid-template-rows: 1fr;
    opacity: 1;
    margin-top: 1.2rem;
  }
  .about-reveal > .about-inner {
    overflow: hidden;
    min-height: 0;
  }

  .about-card {
    background: linear-gradient(160deg, rgba(31,31,38,0.94) 0%, rgba(25,25,32,0.94) 50%, rgba(29,29,36,0.94) 100%);
    backdrop-filter: blur(10px);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 2.2rem 2.5rem 2.4rem;
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.05), 0 12px 40px rgba(0,0,0,0.5);
    position: relative;
    overflow: hidden;
  }
  .about-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, rgba(230,237,242,0.6), transparent);
  }

  .about-card h2 {
    font-size: clamp(1.5rem, 3.5vw, 2.2rem);
    font-weight: 900;
    letter-spacing: -0.02em;
    margin-bottom: 0.4rem;
  }
  .about-card h2 .accent {
    background: var(--accent-grad);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
    font-style: italic;
  }
  .about-lead {
    color: var(--accent-light);
    font-size: 1rem;
    font-weight: 600;
    margin-bottom: 1.4rem;
  }
  .about-text p {
    color: var(--muted);
    font-size: 0.96rem;
    margin-bottom: 1rem;
  }
  .about-text p strong { color: var(--text); font-weight: 700; }
  .about-text p em { color: var(--accent-light); font-style: italic; }

  .about-divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 1.4rem 0;
  }

  .about-signature {
    display: flex;
    align-items: center;
    gap: 0.8rem;
    margin-top: 1.4rem;
    color: var(--muted);
    font-size: 0.85rem;
  }
  .about-signature .sig-line {
    width: 40px;
    height: 2px;
    background: var(--accent-grad);
    border-radius: 2px;
  }

  /* ---------- TOAST ---------- */
  .toast {
    position: fixed;
    bottom: 2rem;
    left: 50%;
    transform: translateX(-50%) translateY(100px);
    background: var(--accent-grad);
    color: #0d0d0f;
    padding: 0.8rem 1.5rem;
    border-radius: 999px;
    font-weight: 700;
    z-index: 300;
    opacity: 0;
    transition: all 0.3s;
    border: 1px solid #e6edf2;
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.7), 0 8px 24px rgba(0,0,0,0.5);
  }
  .toast.show {
    transform: translateX(-50%) translateY(0);
    opacity: 1;
  }

  /* ---------- FOOTER ---------- */
  footer {
    border-top: 1px solid var(--border);
    margin-top: 5rem;
    padding: 3rem 2rem 2rem;
    text-align: center;
    color: var(--muted);
    font-size: 0.9rem;
    background: rgba(13, 13, 15, 0.6);
    backdrop-filter: blur(8px);
  }
  footer .logo { margin-bottom: 1rem; }

  .footer-contacts {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.6rem;
    margin-top: 1.2rem;
    font-size: 0.9rem;
    flex-wrap: wrap;
  }
  .footer-contacts a { color: var(--accent-light); font-weight: 600; }
  .footer-contacts a:hover { text-decoration: underline; }

  .footer-about-link {
    color: var(--accent-light);
    font-weight: 600;
    cursor: pointer;
  }
  .footer-about-link:hover { text-decoration: underline; }

  /* ---------- СКРЫТИЕ / ПОКАЗ СТРАНИЦ ---------- */
  .page { display: none; }
  .page.active { display: block; }

  /* ---------- MOBILE ---------- */
  @media (max-width: 768px) {
    .nav-links { display: none; }
    .nav { padding: 1rem; }
    .hero { padding: 3rem 1.2rem 2rem; }
    .styles-section { padding: 1rem 1.2rem; }
    .about-wrap { padding: 0 1.2rem; }
    .products { grid-template-columns: repeat(auto-fill, minmax(160px, 1fr)); gap: 1rem; }
    .product-info { padding: 0.8rem 0.9rem 1rem; }
    .product-name { font-size: 0.9rem; }
    .price { font-size: 1rem; }
    .add-btn { padding: 0.4rem 0.8rem; font-size: 0.75rem; }
    .about-card { padding: 1.5rem 1.2rem 1.8rem; }
  }
</style>
</head>
<body>

<!-- ===== ВЕРИФИКАЦИЯ (скрытый блок) ===== -->
<div style="display:none" id="verification">Verification: f66d3dcca44a8022</div>

<!-- ============ HEADER ============ -->
<header>
  <nav class="nav">
    <div class="logo" onclick="showHome()">NOMAD<span>WEAR</span></div>
    <ul class="nav-links">
      <li><a onclick="showCatalog()">Каталог</a></li>
      <li><a onclick="showCatalog()">Стили</a></li>
      <li><a onclick="toggleAbout(true)">О нас</a></li>
    </ul>
    <button class="cart-btn" onclick="openCart()">
      Корзина <span class="cart-count" id="cartCount">0</span>
    </button>
  </nav>
</header>

<!-- ============ ГЛАВНАЯ СТРАНИЦА ============ -->
<div id="page-home" class="page active">
  <section class="hero">
    <h1>Одежда, которая<br>говорит <span class="accent">за тебя</span></h1>
    <p>Кастомный принт, ограниченные дропы и стили от sk8 до drill. Купи вещь, которой больше ни у кого не будет.</p>
    <button class="hero-cta" onclick="showCatalog()">Смотреть каталог →</button>
  </section>
</div>

<!-- ============ СТРАНИЦА КАТАЛОГА ============ -->
<div id="page-catalog" class="page">
  <section class="styles-section">
    <button class="back-btn" onclick="showHome()">← Назад на главную</button>

    <h2 class="section-title">Выбери свой стиль</h2>
    <p class="section-sub">Каждая вещь — под конкретную субкультуру и настроение</p>

    <div class="tabs" id="tabs">
      <button class="tab active" data-style="all">Все</button>
      <button class="tab" data-style="sk8">Sk8</button>
      <button class="tab" data-style="streetwear">Streetwear</button>
      <button class="tab" data-style="y2k">Y2K</button>
      <button class="tab" data-style="vintage">Vintage</button>
    </div>

    <div class="products" id="products"></div>
  </section>
</div>

<!-- ============ РАСКРЫВАЮЩИЙСЯ БЛОК "О НАС" (РАСТЯГИВАЕТ САЙТ ВНИЗ) ============ -->
<section class="about-wrap" id="aboutWrap">
  <button class="about-toggle" onclick="toggleAbout()">
    <span class="toggle-label">О нас — предыстория</span>
    <span class="arrow">▼</span>
  </button>

  <div class="about-reveal">
    <div class="about-inner">
      <div class="about-card">
        <h2>Предыстория <span class="accent">NOMAD WEAR</span></h2>
        <p class="about-lead">Как всё начиналось — без маркетинга, честно.</p>

        <div class="about-text">
          <p>
            <strong>NOMAD WEAR</strong> родился не в бизнес-инкубаторе и не на курсах по предпринимательству.
            Он родился в гараже, где пахло краской, старым скейтом и растворителем. Мы красили первые футболки
            вручную — криво, смело и без права на ошибку. Первые двадцать штук ушли друзьям, которые носили их
            в скейт-парках и на квартирниках.
          </p>

          <p>
            Идея была простой: <em>одежда должна говорить за тебя, пока ты молчишь.</em> Никаких
            «трендов сезона» и безликих принтов из масс-маркета. Только вещи, которые отражают
            конкретную субкультуру — <strong>sk8</strong>, <strong>streetwear</strong>,
            <strong>Y2K</strong>, <strong>vintage</strong>.
          </p>

          <p>
            Мы не гонимся за тиражами в тысячи штук. Каждый дроп — ограничен, каждая вещь
            прокрашена с вниманием к деталям. Если ты купил худи NOMAD WEAR — будь уверен:
            такой же точно не будет ни у кого из твоего окружения. Мы делаем ставку на
            <strong>уникальность</strong>, а не на скорость.
          </p>

          <p>
            Сегодня NOMAD WEAR — это команда из нескольких человек, которые всё ещё сами
            красят, пакуют и подписывают каждую посылку. Мы выросли из гаража, но
            <em>остались теми же</em>: делаем вещи с характером для тех, кто не как все.
          </p>
        </div>

        <div class="about-divider"></div>

        <p class="about-text" style="margin-bottom:0">
          <em>Спасибо, что носишь NOMAD WEAR. Это больше, чем одежда.</em>
        </p>

        <div class="about-signature">
          <span class="sig-line"></span>
          <span>Команда NOMAD WEAR · с 2024 года</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ============ CART MODAL ============ -->
<div class="modal-overlay" id="cartOverlay" onclick="closeCartOutside(event)">
  <div class="cart-modal" onclick="event.stopPropagation()">
    <div class="cart-header">
      <h2>Корзина</h2>
      <button class="close-btn" onclick="closeCart()">×</button>
    </div>
    <div id="cartItems"></div>
    <div class="cart-total">
      <span>Итого:</span>
      <span id="cartTotal">0 ₽</span>
    </div>
    <button class="checkout-btn" id="checkoutBtn" onclick="checkout()">Оформить заказ</button>
  </div>
</div>

<!-- ============ CHECKOUT MODAL ============ -->
<div class="modal-overlay" id="payOverlay" onclick="closePayOutside(event)">
  <div class="pay-modal" onclick="event.stopPropagation()">
    <h2>Оплата заказа</h2>
    <p class="pay-sub">Выберите способ оплаты.</p>

    <!-- Выбор метода оплаты -->
    <div id="payMethodsList">
      <label class="pay-method selected" data-method="card">
        <input type="radio" name="payMethod" value="card" checked onchange="selectPayMethod('card')">
        <div>
          <div class="pay-method-label">Банковская карта (Robokassa)</div>
          <div class="pay-method-desc">Безопасная оплата на стороне банка</div>
        </div>
      </label>

      <label class="pay-method" data-method="sbp">
        <input type="radio" name="payMethod" value="sbp" onchange="selectPayMethod('sbp')">
        <div>
          <div class="pay-method-label">СБП (по номеру телефона)</div>
          <div class="pay-method-desc">Перевод по номеру получателя</div>
        </div>
      </label>
    </div>

    <!-- Информация о реквизитах для ручного перевода -->
    <div class="pay-details" id="payDetails"></div>

    <!-- Контейнер для встраиваемой формы Robokassa -->
    <div id="robokassaContainer" style="margin-top: 1rem;">
      <div id="robokassaForm"></div>
    </div>

    <div class="pay-actions" id="payActions">
      <button class="checkout-btn" id="payButton" onclick="processPayment()">Оплатить онлайн</button>
      <button class="pay-cancel" onclick="closePay()">Отмена</button>
    </div>
  </div>
</div>

<!-- ============ TOAST ============ -->
<div class="toast" id="toast">Товар добавлен в корзину</div>

<!-- ============ FOOTER ============ -->
<footer id="footer">
  <div class="logo" onclick="showHome()" style="cursor:pointer">NOMAD<span>WEAR</span></div>
  <p>© 2026 NOMAD WEAR — Кастомная одежда с характером</p>
  <p style="margin-top:0.5rem">Сделано с душой для тех, кто не как все</p>

  <div class="footer-contacts">
    <a href="https://t.me/nomadwearshop" target="_blank" rel="noopener">tg:@nomadwearshop</a>
    <span>·</span>
    <a href="mailto:info@nomadwear.ru">info@nomadwear.ru</a>
    <span>·</span>
    <span class="footer-about-link" onclick="toggleAbout(true)">О нас</span>
  </div>
</footer>

<script>
/* ============================================================
   1. НАСТРОЙКИ ROBOKASSA (ВПИШИТЕ СВОИ ДАННЫЕ)
   ============================================================ */
const ROBOKASSA_CONFIG = {
  login: 'ВАШ_ЛОГИН_В_ROBOKASSA', // Например: 'nomadwear'
  password1: 'ВАШ_ПАРОЛЬ_1',       // Пароль #1 из личного кабинета
  isTestMode: true                 // true для теста (деньги не списываются)
};

/* ============================================================
   ДАННЫЕ ТОВАРОВ
   ============================================================ */
const products = [
  { id: 1,  name: 'Худи',            style: 'sk8',        price: 4900, tag: 'NEW' },
  { id: 2,  name: 'Футболка',        style: 'sk8',        price: 2400 },
  { id: 3,  name: 'Шапка',           style: 'sk8',        price: 1500 },

  { id: 4,  name: 'Худи',            style: 'streetwear', price: 5900, tag: 'HOT' },
  { id: 5,  name: 'Джоггеры',        style: 'streetwear', price: 4200 },
  { id: 6,  name: 'Куртка',          style: 'streetwear', price: 8900 },

  { id: 7,  name: 'Топ',             style: 'y2k',        price: 2900 },
  { id: 8,  name: 'Джинсы',          style: 'y2k',        price: 5400 },
  { id: 9,  name: 'Очки',            style: 'y2k',        price: 1900 },

  { id: 15, name: 'Джинсовка',       style: 'vintage',    price: 6800 },
  { id: 16, name: 'Футболка',        style: 'vintage',    price: 2600 },
];

const styleNames = {
  all: 'Все',
  sk8: 'Sk8',
  streetwear: 'Streetwear',
  y2k: 'Y2K',
  vintage: 'Vintage',
};

/* ============================================================
   РЕКВИЗИТЫ ДЛЯ РУЧНОГО ПЕРЕВОДА (СБП)
   ============================================================ */
const PAYMENT_RECIPIENT = {
  card: {
    label: 'Номер карты',
    value: '0000 0000 0000 0000',
    holder: 'ИВАНОВ ИВАН ИВАНОВИЧ',
    bank: 'Банк получателя'
  },
  sbp: {
    label: 'Телефон для СБП',
    value: '+7 (900) 000-00-00',
    holder: 'ИВАНОВ ИВАН ИВАНОВИЧ'
  }
};

/* ============================================================
   СОСТОЯНИЕ
   ============================================================ */
let currentStyle = 'all';
let cart = JSON.parse(localStorage.getItem('nomadwear_cart') || '[]');
let currentPayMethod = 'card';

/* ============================================================
   НАВИГАЦИЯ МЕЖДУ СТРАНИЦАМИ
   ============================================================ */
function showHome() {
  document.getElementById('page-home').classList.add('active');
  document.getElementById('page-catalog').classList.remove('active');
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function showCatalog() {
  document.getElementById('page-home').classList.remove('active');
  document.getElementById('page-catalog').classList.add('active');
  renderProducts();
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

/* ============================================================
   РАСКРЫВАЮЩИЙСЯ БЛОК "О НАС"
   ============================================================ */
function toggleAbout(forceOpen) {
  const wrap = document.getElementById('aboutWrap');
  const willOpen = (typeof forceOpen === 'boolean') ? forceOpen : !wrap.classList.contains('open');

  wrap.classList.toggle('open', willOpen);
  const label = wrap.querySelector('.toggle-label');
  if (label) label.textContent = willOpen ? 'Свернуть предысторию' : 'О нас — предыстория';

  if (willOpen) {
    // Плавно прокручиваем к раскрытому блоку, чтобы пользователь увидел предысторию
    setTimeout(() => {
      wrap.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }, 120);
  }
}

/* ============================================================
   РЕНДЕР КАТАЛОГА
   ============================================================ */
function renderProducts() {
  const container = document.getElementById('products');
  const filtered = currentStyle === 'all'
    ? products
    : products.filter(p => p.style === currentStyle);

  container.innerHTML = filtered.map(p => `
    <div class="product-card">
      <div class="product-img">
        ${p.tag ? `<span class="product-tag">${p.tag}</span>` : ''}
      </div>
      <div class="product-info">
        <div class="product-style">${styleNames[p.style]}</div>
        <div class="product-name">${p.name}</div>
        <div class="product-bottom">
          <div class="price">${p.price.toLocaleString('ru-RU')} <small>₽</small></div>
          <button class="add-btn" onclick="addToCart(${p.id})">+ В корзину</button>
        </div>
      </div>
    </div>
  `).join('');
}

/* ============================================================
   ВКЛАДКИ СТИЛЕЙ
   ============================================================ */
document.getElementById('tabs').addEventListener('click', (e) => {
  const tab = e.target.closest('.tab');
  if (!tab) return;

  document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
  tab.classList.add('active');
  currentStyle = tab.dataset.style;
  renderProducts();
});

/* ============================================================
   КОРЗИНА
   ============================================================ */
function addToCart(id) {
  const product = products.find(p => p.id === id);
  const existing = cart.find(item => item.id === id);

  if (existing) {
    existing.qty += 1;
  } else {
    cart.push({ ...product, qty: 1 });
  }

  saveCart();
  updateCartUI();
  showToast(`${product.name} добавлен в корзину`);
}

/* Увеличить количество на 1 */
function increaseQty(id) {
  const item = cart.find(item => item.id === id);
  if (!item) return;
  item.qty += 1;
  saveCart();
  updateCartUI();
}

/* Уменьшить количество на 1. Если qty = 1 — удаляем товар полностью */
function decreaseQty(id) {
  const item = cart.find(item => item.id === id);
  if (!item) return;
  if (item.qty > 1) {
    item.qty -= 1;
  } else {
    cart = cart.filter(i => i.id !== id);
  }
  saveCart();
  updateCartUI();
}

function saveCart() {
  localStorage.setItem('nomadwear_cart', JSON.stringify(cart));
}

function updateCartUI() {
  const count = cart.reduce((sum, item) => sum + item.qty, 0);
  document.getElementById('cartCount').textContent = count;

  const itemsContainer = document.getElementById('cartItems');
  const totalEl = document.getElementById('cartTotal');
  const checkoutBtn = document.getElementById('checkoutBtn');

  if (cart.length === 0) {
    itemsContainer.innerHTML = '<div class="cart-empty">Корзина пуста</div>';
    totalEl.textContent = '0 ₽';
    checkoutBtn.disabled = true;
    return;
  }

  itemsContainer.innerHTML = cart.map(item => `
    <div class="cart-item">
      <div class="cart-item-img"></div>
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-price">${(item.price * item.qty).toLocaleString('ru-RU')} ₽</div>
      </div>
      <div class="qty-controls">
        <button class="qty-btn" onclick="decreaseQty(${item.id})" title="Убрать одну">−</button>
        <span class="qty-value">${item.qty}</span>
        <button class="qty-btn" onclick="increaseQty(${item.id})" title="Добавить одну">+</button>
      </div>
    </div>
  `).join('');

  const total = cart.reduce((sum, item) => sum + item.price * item.qty, 0);
  totalEl.textContent = total.toLocaleString('ru-RU') + ' ₽';
  checkoutBtn.disabled = false;
}

/* ============================================================
   МОДАЛКА КОРЗИНЫ
   ============================================================ */
function openCart() {
  document.getElementById('cartOverlay').classList.add('open');
}

function closeCart() {
  document.getElementById('cartOverlay').classList.remove('open');
}

function closeCartOutside(e) {
  if (e.target.id === 'cartOverlay') closeCart();
}

/* ============================================================
   ОФОРМЛЕНИЕ ЗАКАЗА -> ОКНО ОПЛАТЫ
   ============================================================ */
function checkout() {
  if (cart.length === 0) return;
  
  // Сбрасываем окно оплаты
  currentPayMethod = 'card';
  document.querySelectorAll('.pay-method').forEach(el => {
    el.classList.toggle('selected', el.dataset.method === 'card');
    const radio = el.querySelector('input');
    if (radio) radio.checked = (el.dataset.method === 'card');
  });
  
  // Очищаем старую форму
  document.getElementById('robokassaForm').innerHTML = '';
  document.getElementById('robokassaForm').style.display = 'none';
  document.getElementById('payMethodsList').style.display = 'block';
  document.getElementById('payButton').style.display = 'block';
  
  selectPayMethod('card');
  document.getElementById('payOverlay').classList.add('open');
}

function selectPayMethod(method) {
  currentPayMethod = method;
  document.querySelectorAll('.pay-method').forEach(el => {
    el.classList.toggle('selected', el.dataset.method === method);
  });

  const details = document.getElementById('payDetails');
  const robokassaForm = document.getElementById('robokassaForm');
  const payButton = document.getElementById('payButton');

  if (method === 'card') {
    // Для карты показываем кнопку Robokassa, скрываем реквизиты
    details.classList.remove('show');
    robokassaForm.style.display = 'none';
    payButton.style.display = 'block';
    payButton.textContent = 'Оплатить картой';
  } else {
    // Для СБП показываем реквизиты
    const rec = PAYMENT_RECIPIENT[method];
    if (!rec) { details.classList.remove('show'); return; }

    const total = cart.reduce((sum, item) => sum + item.price * item.qty, 0);

    let rows = `
      <div class="pay-row"><span>${rec.label}</span><span>${rec.value}</span></div>
      <div class="pay-row"><span>Получатель</span><span>${rec.holder}</span></div>
    `;
    if (rec.bank) {
      rows += `<div class="pay-row"><span>Банк</span><span>${rec.bank}</span></div>`;
    }
    rows += `<div class="pay-row"><span>Сумма к оплате</span><span>${total.toLocaleString('ru-RU')} ₽</span></div>`;

    details.innerHTML = rows;
    details.classList.add('show');
    robokassaForm.style.display = 'none';
    payButton.style.display = 'none'; // Скрываем кнопку онлайн-оплаты
  }
}

/* ============================================================
   ОПЛАТА ЧЕРЕЗ ROBOKASSA (iFrame)
   ============================================================ */
function processPayment() {
  if (cart.length === 0) return;

  const total = cart.reduce((sum, item) => sum + item.price * item.qty, 0);
  const outSum = total.toFixed(2);
  const invId = Math.floor(Date.now() / 1000);

  // ВНИМАНИЕ: Генерация подписи на клиенте небезопасна.
  // Для продакшена нужен серверный скрипт.
  const signatureString = `${ROBOKASSA_CONFIG.login}:${outSum}:${invId}:${ROBOKASSA_CONFIG.password1}`;
  const signatureValue = md5(signatureString);

  const formContainer = document.getElementById('robokassaForm');
  formContainer.innerHTML = '';
  formContainer.style.display = 'block';

  const iframe = document.createElement('iframe');
  iframe.style.width = '100%';
  iframe.style.height = '500px';
  iframe.style.border = 'none';
  iframe.setAttribute('frameborder', '0');
  iframe.setAttribute('allowtransparency', 'true');

  const params = new URLSearchParams({
    MerchantLogin: ROBOKASSA_CONFIG.login,
    OutSum: outSum,
    InvId: invId,
    Description: 'Оплата заказа в NOMAD WEAR',
    SignatureValue: signatureValue,
    Culture: 'ru',
    Encoding: 'utf-8',
    IsTest: ROBOKASSA_CONFIG.isTestMode ? '1' : '0'
  });

  const baseUrl = 'https://auth.robokassa.ru/Merchant/Index.aspx';
  iframe.src = `${baseUrl}?${params.toString()}`;
  
  formContainer.appendChild(iframe);

  document.getElementById('payMethodsList').style.display = 'none';
  document.getElementById('payButton').style.display = 'none';
  document.getElementById('payDetails').classList.remove('show');

  const cancelBtn = document.querySelector('.pay-cancel');
  cancelBtn.textContent = 'Закрыть';
}

/* ============================================================
   ЗАКРЫТИЕ ОКНА ОПЛАТЫ
   ============================================================ */
function closePay() {
  document.getElementById('payOverlay').classList.remove('open');
  document.getElementById('payMethodsList').style.display = 'block';
  document.getElementById('payButton').style.display = 'block';
  document.getElementById('robokassaForm').style.display = 'none';
  document.getElementById('robokassaForm').innerHTML = '';
  document.querySelector('.pay-cancel').textContent = 'Отмена';
}

function closePayOutside(e) {
  if (e.target.id === 'payOverlay') closePay();
}

/* ============================================================
   TOAST
   ============================================================ */
let toastTimeout;
function showToast(message) {
  const toast = document.getElementById('toast');
  toast.textContent = message;
  toast.classList.add('show');
  clearTimeout(toastTimeout);
  toastTimeout = setTimeout(() => toast.classList.remove('show'), 2000);
}

/* ============================================================
   ИНИЦИАЛИЗАЦИЯ
   ============================================================ */
renderProducts();
updateCartUI();
</script>

</body>
</html>
