# - <!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Мерей Мунай — Поставка нефтепромыслового оборудования</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Montserrat:wght@700;800;900&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
 
  :root {
    --steel: #0F1C2E;
    --steel-mid: #1A2F4A;
    --steel-light: #243C5A;
    --oil: #D4780A;
    --oil-light: #F0921F;
    --cream: #F7F4EF;
    --gray-text: #6B7280;
    --gray-border: #E5E7EB;
    --white: #FFFFFF;
    --font-display: 'Montserrat', sans-serif;
    --font-body: 'Inter', sans-serif;
    --radius: 12px;
    --radius-sm: 8px;
  }
 
  html { scroll-behavior: smooth; }
  body { font-family: var(--font-body); background: var(--white); color: var(--steel); line-height: 1.6; overflow-x: hidden; }
 
  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(15,28,46,0.97); backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(212,120,10,0.2);
    padding: 0 5%; display: flex; align-items: center; justify-content: space-between; height: 68px;
  }
  .nav-logo { font-family: var(--font-display); font-size: 20px; font-weight: 800; color: var(--white); letter-spacing: -0.5px; }
  .nav-logo span { color: var(--oil-light); }
  .nav-links { display: flex; gap: 32px; list-style: none; }
  .nav-links a { color: rgba(255,255,255,0.75); text-decoration: none; font-size: 14px; font-weight: 500; transition: color 0.2s; }
  .nav-links a:hover { color: var(--oil-light); }
  .nav-cta { background: var(--oil); color: var(--white) !important; padding: 10px 22px; border-radius: 6px; font-weight: 600 !important; transition: background 0.2s !important; }
  .nav-cta:hover { background: var(--oil-light) !important; }
 
  /* HERO */
  .hero {
    min-height: 100vh; background: var(--steel);
    display: flex; align-items: center; padding: 100px 5% 60px;
    position: relative; overflow: hidden;
  }
  .hero::before {
    content: ''; position: absolute; top: -20%; right: -10%;
    width: 700px; height: 700px;
    background: radial-gradient(circle, rgba(212,120,10,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; max-width: 1200px; margin: 0 auto; width: 100%; align-items: center; }
  .hero-eyebrow { display: inline-block; font-size: 12px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; color: var(--oil-light); margin-bottom: 20px; padding: 6px 14px; border: 1px solid rgba(240,146,31,0.3); border-radius: 4px; }
  .hero h1 { font-family: var(--font-display); font-size: clamp(36px,4vw,56px); font-weight: 900; color: var(--white); line-height: 1.05; letter-spacing: -1.5px; margin-bottom: 24px; }
  .hero h1 .accent { color: var(--oil-light); }
  .hero-desc { font-size: 17px; color: rgba(255,255,255,0.6); line-height: 1.7; margin-bottom: 40px; max-width: 480px; }
  .hero-btns { display: flex; gap: 14px; flex-wrap: wrap; }
  .btn-primary { background: var(--oil); color: var(--white); padding: 15px 32px; border-radius: 8px; font-weight: 600; font-size: 15px; text-decoration: none; transition: background 0.2s, transform 0.15s; display: inline-block; }
  .btn-primary:hover { background: var(--oil-light); transform: translateY(-1px); }
  .btn-secondary { background: transparent; color: rgba(255,255,255,0.85); padding: 15px 32px; border-radius: 8px; font-weight: 500; font-size: 15px; text-decoration: none; border: 1px solid rgba(255,255,255,0.2); transition: border-color 0.2s, color 0.2s; display: inline-block; }
  .btn-secondary:hover { border-color: rgba(255,255,255,0.5); color: var(--white); }
  .hero-stats { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-top: 48px; }
  .stat-box { background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); border-radius: 10px; padding: 20px; }
  .stat-num { font-family: var(--font-display); font-size: 32px; font-weight: 800; color: var(--oil-light); line-height: 1; margin-bottom: 6px; }
  .stat-label { font-size: 13px; color: rgba(255,255,255,0.5); }
 
  /* HERO PHOTO GRID */
  .hero-visual { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .hero-photo { border-radius: 10px; overflow: hidden; position: relative; }
  .hero-photo img { width: 100%; height: 160px; object-fit: cover; display: block; filter: brightness(0.85); transition: filter 0.3s, transform 0.3s; }
  .hero-photo:hover img { filter: brightness(1); transform: scale(1.03); }
  .hero-photo-label { position: absolute; bottom: 0; left: 0; right: 0; background: linear-gradient(transparent, rgba(0,0,0,0.7)); padding: 20px 12px 10px; font-size: 12px; font-weight: 600; color: #fff; }
  .hero-photo.tall img { height: 332px; }
 
  /* SECTION COMMON */
  section { padding: 80px 5%; }
  .container { max-width: 1200px; margin: 0 auto; }
  .section-label { font-size: 12px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; color: var(--oil); margin-bottom: 12px; }
  .section-title { font-family: var(--font-display); font-size: clamp(28px,3vw,40px); font-weight: 800; color: var(--steel); letter-spacing: -0.8px; line-height: 1.15; margin-bottom: 16px; }
  .section-desc { font-size: 16px; color: var(--gray-text); max-width: 560px; line-height: 1.7; }
 
  /* CATALOG */
  .catalog-bg { background: var(--cream); }
  .catalog-header { display: flex; justify-content: space-between; align-items: flex-end; margin-bottom: 48px; flex-wrap: wrap; gap: 16px; }
  .catalog-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); gap: 20px; }
  .cat-card { background: var(--white); border-radius: var(--radius); border: 1px solid var(--gray-border); overflow: hidden; text-decoration: none; display: block; transition: box-shadow 0.2s, transform 0.2s, border-color 0.2s; }
  .cat-card:hover { box-shadow: 0 8px 32px rgba(0,0,0,0.08); transform: translateY(-3px); border-color: var(--oil); }
  .cat-img { height: 180px; overflow: hidden; background: #eee; }
  .cat-img img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.3s; }
  .cat-card:hover .cat-img img { transform: scale(1.05); }
  .cat-body { padding: 20px; }
  .cat-title { font-weight: 700; font-size: 17px; color: var(--steel); margin-bottom: 6px; }
  .cat-desc { font-size: 13px; color: var(--gray-text); line-height: 1.6; margin-bottom: 14px; }
  .cat-link { font-size: 13px; font-weight: 600; color: var(--oil); display: flex; align-items: center; gap: 6px; }
  .cat-link::after { content: '→'; }
 
  /* POPULAR PRODUCTS */
  .products-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 20px; margin-top: 48px; }
  .prod-card { border: 1px solid var(--gray-border); border-radius: var(--radius); overflow: hidden; background: var(--white); transition: box-shadow 0.2s, transform 0.2s; text-decoration: none; display: block; }
  .prod-card:hover { box-shadow: 0 8px 24px rgba(0,0,0,0.07); transform: translateY(-2px); }
  .prod-img { height: 170px; overflow: hidden; background: var(--cream); border-bottom: 1px solid var(--gray-border); }
  .prod-img img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.3s; }
  .prod-card:hover .prod-img img { transform: scale(1.06); }
  .prod-body { padding: 16px; }
  .prod-name { font-weight: 600; font-size: 14px; color: var(--steel); margin-bottom: 8px; line-height: 1.4; }
  .prod-price { font-family: var(--font-display); font-size: 16px; font-weight: 700; color: var(--oil); }
  .prod-price-na { font-size: 13px; color: var(--gray-text); }
  .prod-btn { display: block; text-align: center; margin-top: 12px; padding: 9px; background: var(--steel); color: var(--white); border-radius: 6px; font-size: 13px; font-weight: 600; transition: background 0.2s; }
  .prod-btn:hover { background: var(--oil); }
 
  /* WHY US */
  .why-bg { background: var(--steel); }
  .why-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 24px; margin-top: 52px; }
  .why-card { background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); border-radius: var(--radius); padding: 28px; }
  .why-icon { font-size: 28px; margin-bottom: 16px; }
  .why-title { font-weight: 600; font-size: 16px; color: var(--white); margin-bottom: 10px; }
  .why-text { font-size: 14px; color: rgba(255,255,255,0.5); line-height: 1.6; }
 
  /* HOW IT WORKS */
  .steps { display: grid; grid-template-columns: repeat(4,1fr); gap: 0; margin-top: 52px; position: relative; }
  .steps::before { content: ''; position: absolute; top: 28px; left: 12.5%; right: 12.5%; height: 1px; background: var(--oil); opacity: 0.2; }
  .step { text-align: center; padding: 0 16px; position: relative; }
  .step-num { width: 56px; height: 56px; background: var(--oil); color: var(--white); border-radius: 50%; display: flex; align-items: center; justify-content: center; font-family: var(--font-display); font-size: 20px; font-weight: 800; margin: 0 auto 20px; position: relative; z-index: 1; }
  .step-title { font-weight: 600; font-size: 15px; color: var(--steel); margin-bottom: 8px; }
  .step-text { font-size: 13px; color: var(--gray-text); line-height: 1.6; }
 
  /* GALLERY */
  .gallery-bg { background: var(--cream); }
  .gallery-grid { display: grid; grid-template-columns: repeat(4, 1fr); grid-template-rows: auto auto; gap: 12px; margin-top: 48px; }
  .gallery-item { border-radius: 10px; overflow: hidden; }
  .gallery-item img { width: 100%; height: 200px; object-fit: cover; display: block; transition: transform 0.3s; }
  .gallery-item:hover img { transform: scale(1.04); }
  .gallery-item.wide { grid-column: span 2; }
  .gallery-item.wide img { height: 200px; }
 
  /* CONTACT */
  .contact-bg { background: var(--white); }
  .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: start; margin-top: 48px; }
  .contact-item { display: flex; gap: 16px; align-items: flex-start; margin-bottom: 24px; }
  .contact-ico { width: 44px; height: 44px; background: rgba(212,120,10,0.1); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 20px; flex-shrink: 0; }
  .contact-label { font-size: 12px; font-weight: 600; text-transform: uppercase; letter-spacing: 1px; color: var(--oil); margin-bottom: 4px; }
  .contact-value { font-size: 15px; font-weight: 500; color: var(--steel); text-decoration: none; display: block; }
  .contact-value:hover { color: var(--oil); }
  .contact-form { background: var(--cream); border-radius: var(--radius); border: 1px solid var(--gray-border); padding: 36px; }
  .form-title { font-family: var(--font-display); font-size: 22px; font-weight: 700; color: var(--steel); margin-bottom: 24px; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
  .form-group { margin-bottom: 16px; }
  .form-group label { display: block; font-size: 13px; font-weight: 500; color: var(--steel); margin-bottom: 7px; }
  .form-group input, .form-group textarea, .form-group select { width: 100%; padding: 11px 14px; border: 1.5px solid var(--gray-border); border-radius: 8px; font-size: 14px; font-family: var(--font-body); color: var(--steel); background: var(--white); outline: none; transition: border-color 0.2s; }
  .form-group input:focus, .form-group textarea:focus, .form-group select:focus { border-color: var(--oil); }
  .form-group textarea { resize: vertical; min-height: 100px; }
  .form-submit { width: 100%; padding: 14px; background: var(--oil); color: var(--white); border: none; border-radius: 8px; font-size: 15px; font-weight: 600; cursor: pointer; font-family: var(--font-body); transition: background 0.2s; margin-top: 4px; }
  .form-submit:hover { background: var(--oil-light); }
 
  /* FOOTER */
  footer { background: #080F18; padding: 52px 5% 28px; color: rgba(255,255,255,0.5); font-size: 14px; }
  .footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 48px; max-width: 1200px; margin: 0 auto 40px; }
  .footer-logo { font-family: var(--font-display); font-size: 22px; font-weight: 800; color: var(--white); margin-bottom: 14px; }
  .footer-logo span { color: var(--oil-light); }
  .footer-about { line-height: 1.7; margin-bottom: 20px; }
  .footer-wa { display: inline-flex; align-items: center; gap: 8px; background: #25D366; color: #fff; padding: 10px 20px; border-radius: 8px; text-decoration: none; font-size: 14px; font-weight: 600; transition: opacity 0.2s; }
  .footer-wa:hover { opacity: 0.85; }
  .footer-col-title { font-size: 13px; font-weight: 600; color: rgba(255,255,255,0.8); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 18px; }
  .footer-links { list-style: none; }
  .footer-links li { margin-bottom: 10px; }
  .footer-links a { color: rgba(255,255,255,0.45); text-decoration: none; font-size: 14px; transition: color 0.2s; }
  .footer-links a:hover { color: var(--oil-light); }
  .footer-bottom { max-width: 1200px; margin: 0 auto; padding-top: 24px; border-top: 1px solid rgba(255,255,255,0.06); display: flex; justify-content: space-between; flex-wrap: wrap; gap: 12px; font-size: 13px; }
  .footer-bottom a { color: var(--oil-light); text-decoration: none; }
 
  .wa-float { position: fixed; bottom: 28px; right: 28px; width: 56px; height: 56px; background: #25D366; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 26px; box-shadow: 0 4px 20px rgba(37,211,102,0.4); text-decoration: none; z-index: 200; transition: transform 0.2s; }
  .wa-float:hover { transform: scale(1.1); }
 
  /* RESPONSIVE */
  @media (max-width: 900px) {
    .hero-grid { grid-template-columns: 1fr; }
    .hero-visual { display: none; }
    .steps { grid-template-columns: 1fr 1fr; gap: 32px; }
    .steps::before { display: none; }
    .contact-grid { grid-template-columns: 1fr; }
    .footer-grid { grid-template-columns: 1fr; gap: 32px; }
    .form-row { grid-template-columns: 1fr; }
    .nav-links { display: none; }
    .gallery-grid { grid-template-columns: 1fr 1fr; }
  }
  @media (max-width: 600px) {
    section { padding: 60px 4%; }
    nav { padding: 0 4%; }
    .steps { grid-template-columns: 1fr; }
    .gallery-grid { grid-template-columns: 1fr; }
    .gallery-item.wide { grid-column: span 1; }
  }
 
  .fade-up { opacity: 0; transform: translateY(24px); transition: opacity 0.5s ease, transform 0.5s ease; }
  .fade-up.visible { opacity: 1; transform: none; }
</style>
</head>
<body>
 
<!-- NAV -->
<nav>
  <div class="nav-logo">Мерей<span>Мунай</span></div>
  <ul class="nav-links">
    <li><a href="#catalog">Каталог</a></li>
    <li><a href="#products">Товары</a></li>
    <li><a href="#gallery">Галерея</a></li>
    <li><a href="#how">Как работаем</a></li>
    <li><a href="#contact" class="nav-cta">Связаться</a></li>
  </ul>
</nav>
 
<!-- HERO -->
<section class="hero">
  <div class="hero-grid">
    <div>
      <span class="hero-eyebrow">Казахстан · Актау</span>
      <h1>Поставка нефтепромыслового <span class="accent">оборудования</span></h1>
      <p class="hero-desc">ЦА-320, НБ125, ППУА, АДПМ, СИН32 и тысячи запасных частей — в наличии и под заказ. Доставка по всему Казахстану.</p>
      <div class="hero-btns">
        <a href="#catalog" class="btn-primary">Смотреть каталог</a>
        <a href="#contact" class="btn-secondary">Запросить цену</a>
      </div>
      <div class="hero-stats">
        <div class="stat-box"><div class="stat-num">500+</div><div class="stat-label">Позиций в наличии</div></div>
        <div class="stat-box"><div class="stat-num">7 лет</div><div class="stat-label">На рынке Казахстана</div></div>
        <div class="stat-box"><div class="stat-num">РК</div><div class="stat-label">Доставка по всем регионам</div></div>
        <div class="stat-box"><div class="stat-num">24ч</div><div class="stat-label">Ответ менеджера</div></div>
      </div>
    </div>
    <div class="hero-visual">
      <div style="display:flex;flex-direction:column;gap:12px">
        <div class="hero-photo">
          <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_15.43.06.jpeg" alt="Труба">
          <div class="hero-photo-label">Трубы и фитинги</div>
        </div>
        <div class="hero-photo">
          <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_15.44.21.jpeg" alt="Рукав">
          <div class="hero-photo-label">Рукава высокого давления</div>
        </div>
      </div>
      <div style="display:flex;flex-direction:column;gap:12px">
        <div class="hero-photo">
          <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_16.00.18.jpeg" alt="Втулка">
          <div class="hero-photo-label">Втулки цилиндровые</div>
        </div>
        <div class="hero-photo">
          <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_15.59.55.jpeg" alt="Поршень">
          <div class="hero-photo-label">Поршни насосные</div>
        </div>
      </div>
    </div>
  </div>
</section>
 
<!-- CATALOG -->
<section class="catalog-bg" id="catalog">
  <div class="container">
    <div class="catalog-header fade-up">
      <div>
        <div class="section-label">Каталог</div>
        <div class="section-title">Категории оборудования</div>
        <p class="section-desc">Специализированная техника и запасные части для нефтяной и газовой промышленности.</p>
      </div>
      <a href="#contact" class="btn-primary" style="white-space:nowrap">Запросить прайс</a>
    </div>
    <div class="catalog-grid">
      <a href="#contact" class="cat-card fade-up">
        <div class="cat-img"><img src="https://merey-munay.kz/sites/default/files/styles/catalog_main/public/cat_1.png" alt="АДПМ"></div>
        <div class="cat-body">
          <div class="cat-title">АДПМ</div>
          <div class="cat-desc">Агрегаты депарафинизации и промывки скважин горячей нефтью.</div>
          <span class="cat-link">Подробнее</span>
        </div>
      </a>
      <a href="#contact" class="cat-card fade-up">
        <div class="cat-img"><img src="https://merey-munay.kz/sites/default/files/styles/catalog_main/public/cat_2.png" alt="ППУА"></div>
        <div class="cat-body">
          <div class="cat-title">ППУА</div>
          <div class="cat-desc">Передвижные парогенераторные установки для закачки пара в пласт.</div>
          <span class="cat-link">Подробнее</span>
        </div>
      </a>
      <a href="#contact" class="cat-card fade-up">
        <div class="cat-img"><img src="https://merey-munay.kz/sites/default/files/styles/catalog_main/public/sa-320_0.jpg" alt="ЦА-320"></div>
        <div class="cat-body">
          <div class="cat-title">ЦА-320</div>
          <div class="cat-desc">Цементировочные агрегаты для крепления скважин и ремонтных работ.</div>
          <span class="cat-link">Подробнее</span>
        </div>
      </a>
      <a href="#contact" class="cat-card fade-up">
        <div class="cat-img"><img src="https://merey-munay.kz/sites/default/files/styles/catalog_main/public/izobrazhenie_2021-11-12_105442.png" alt="НБ125"></div>
        <div class="cat-body">
          <div class="cat-title">НБ125 / НБ50</div>
          <div class="cat-desc">Буровые поршневые насосы и запасные части к ним: поршни, втулки, клапаны.</div>
          <span class="cat-link">Подробнее</span>
        </div>
      </a>
      <a href="#contact" class="cat-card fade-up">
        <div class="cat-img"><img src="https://merey-munay.kz/sites/default/files/styles/catalog_main/public/109126121_w300_h300_shesterennyj-nasos-nmsh.jpg" alt="Насосы"></div>
        <div class="cat-body">
          <div class="cat-title">Насосы</div>
          <div class="cat-desc">Шестерёнчатые, плунжерные и центробежные насосы для нефтяной отрасли.</div>
          <span class="cat-link">Подробнее</span>
        </div>
      </a>
      <a href="#contact" class="cat-card fade-up">
        <div class="cat-img"><img src="https://merey-munay.kz/sites/default/files/styles/catalog_main/public/cat_4.png" alt="СИН32"></div>
        <div class="cat-body">
          <div class="cat-title">СИН32</div>
          <div class="cat-desc">Цементировочные агрегаты и комплектующие для буровых работ.</div>
          <span class="cat-link">Подробнее</span>
        </div>
      </a>
    </div>
  </div>
</section>
 
<!-- POPULAR PRODUCTS -->
<section id="products">
  <div class="container">
    <div class="section-label fade-up">Популярные товары</div>
    <div class="section-title fade-up">Часто заказывают</div>
    <div class="products-grid">
      <a href="#contact" class="prod-card fade-up">
        <div class="prod-img"><img src="https://merey-munay.kz/sites/default/files/styles/popular_products_front/public/whatsapp_image_2021-11-10_at_15.43.06.jpeg" alt="Труба"></div>
        <div class="prod-body">
          <div class="prod-name">Труба</div>
          <div class="prod-price">7 730 ₸</div>
          <span class="prod-btn">Заказать</span>
        </div>
      </a>
      <a href="#contact" class="prod-card fade-up">
        <div class="prod-img"><img src="https://merey-munay.kz/sites/default/files/styles/popular_products_front/public/whatsapp_image_2021-11-10_at_15.50.04.jpeg" alt="Змеевик"></div>
        <div class="prod-body">
          <div class="prod-name">Змеевик</div>
          <div class="prod-price-na">По запросу</div>
          <span class="prod-btn">Заказать</span>
        </div>
      </a>
      <a href="#contact" class="prod-card fade-up">
        <div class="prod-img"><img src="https://merey-munay.kz/sites/default/files/styles/popular_products_front/public/whatsapp_image_2021-11-10_at_15.50.17.jpeg" alt="Заслонка шиберная"></div>
        <div class="prod-body">
          <div class="prod-name">Заслонка шиберная Ф100</div>
          <div class="prod-price-na">По запросу</div>
          <span class="prod-btn">Заказать</span>
        </div>
      </a>
      <a href="#contact" class="prod-card fade-up">
        <div class="prod-img"><img src="https://merey-munay.kz/sites/default/files/styles/popular_products_front/public/whatsapp_image_2021-11-10_at_15.50.41.jpeg" alt="Клапан"></div>
        <div class="prod-body">
          <div class="prod-name">Клапан в сборе Ф111</div>
          <div class="prod-price-na">По запросу</div>
          <span class="prod-btn">Заказать</span>
        </div>
      </a>
      <a href="#contact" class="prod-card fade-up">
        <div class="prod-img"><img src="https://merey-munay.kz/sites/default/files/styles/popular_products_front/public/whatsapp_image_2021-11-10_at_15.51.05.jpeg" alt="Горелочное устройство"></div>
        <div class="prod-body">
          <div class="prod-name">Горелочное устройство</div>
          <div class="prod-price-na">По запросу</div>
          <span class="prod-btn">Заказать</span>
        </div>
      </a>
      <a href="#contact" class="prod-card fade-up">
        <div class="prod-img"><img src="https://merey-munay.kz/sites/default/files/styles/popular_products_front/public/whatsapp_image_2021-11-10_at_15.57.20_0.jpeg" alt="Манометр 160кгс"></div>
        <div class="prod-body">
          <div class="prod-name">Манометр 160 кгс</div>
          <div class="prod-price-na">По запросу</div>
          <span class="prod-btn">Заказать</span>
        </div>
      </a>
      <a href="#contact" class="prod-card fade-up">
        <div class="prod-img"><img src="https://merey-munay.kz/sites/default/files/styles/popular_products_front/public/whatsapp_image_2021-11-10_at_15.59.55.jpeg" alt="Поршень Ф127"></div>
        <div class="prod-body">
          <div class="prod-name">Поршень Ф127</div>
          <div class="prod-price-na">По запросу</div>
          <span class="prod-btn">Заказать</span>
        </div>
      </a>
      <a href="#contact" class="prod-card fade-up">
        <div class="prod-img"><img src="https://merey-munay.kz/sites/default/files/styles/popular_products_front/public/whatsapp_image_2021-11-10_at_15.44.21.jpeg" alt="Рукав Б-2-100"></div>
        <div class="prod-body">
          <div class="prod-name">Рукав Б-2-100 (4 и 6 м)</div>
          <div class="prod-price">7 000 ₸</div>
          <span class="prod-btn">Заказать</span>
        </div>
      </a>
    </div>
  </div>
</section>
 
<!-- WHY US -->
<section class="why-bg">
  <div class="container">
    <div class="section-label fade-up" style="color:var(--oil-light)">Наши преимущества</div>
    <div class="section-title fade-up" style="color:var(--white)">Почему выбирают нас</div>
    <div class="why-grid">
      <div class="why-card fade-up"><div class="why-icon">💰</div><div class="why-title">Доступные цены</div><div class="why-text">Работаем напрямую с производителями, исключая лишних посредников. Конкурентные цены на весь ассортимент.</div></div>
      <div class="why-card fade-up"><div class="why-icon">📦</div><div class="why-title">Широкий ассортимент</div><div class="why-text">Более 500 наименований оборудования и запчастей для нефтяной и газовой отрасли в наличии на складе.</div></div>
      <div class="why-card fade-up"><div class="why-icon">🚚</div><div class="why-title">Доставка по Казахстану</div><div class="why-text">Организуем доставку в любой регион Казахстана. Работаем с надёжными транспортными компаниями.</div></div>
      <div class="why-card fade-up"><div class="why-icon">✅</div><div class="why-title">Качественная продукция</div><div class="why-text">Поставляем только сертифицированное оборудование с гарантией качества и технической документацией.</div></div>
    </div>
  </div>
</section>
 
<!-- GALLERY -->
<section class="gallery-bg" id="gallery">
  <div class="container">
    <div class="section-label fade-up">Фотогалерея</div>
    <div class="section-title fade-up">Наша продукция</div>
    <div class="gallery-grid fade-up">
      <div class="gallery-item wide">
        <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_15.48.04.jpeg" alt="Манжета лобовой крышки">
      </div>
      <div class="gallery-item">
        <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_15.57.38.jpeg" alt="Манометр 0-400кгс">
      </div>
      <div class="gallery-item">
        <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_15.58.27.jpeg" alt="Брс2">
      </div>
      <div class="gallery-item">
        <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_15.58.48.jpeg" alt="Колено шарнирное 50х70">
      </div>
      <div class="gallery-item">
        <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/whatsapp_image_2021-11-10_at_15.45.12.jpeg" alt="Палец крейцкопфа">
      </div>
      <div class="gallery-item wide">
        <img src="https://merey-munay.kz/sites/default/files/styles/popular_custom_sootno/public/izobrazhenie_2021-11-12_133042_0.png" alt="Насос НМШФ 0.6">
      </div>
    </div>
  </div>
</section>
 
<!-- HOW IT WORKS -->
<section id="how">
  <div class="container">
    <div style="text-align:center;margin-bottom:8px" class="fade-up"><div class="section-label" style="display:inline-block">Процесс</div></div>
    <div class="section-title fade-up" style="text-align:center">Как мы работаем</div>
    <div class="steps">
      <div class="step fade-up"><div class="step-num">1</div><div class="step-title">Оформите заказ</div><div class="step-text">Оставьте заявку на сайте или напишите в WhatsApp. Укажите нужную позицию или модель.</div></div>
      <div class="step fade-up"><div class="step-num">2</div><div class="step-title">Менеджер свяжется</div><div class="step-text">Наш специалист уточнит детали заказа, наличие, сроки и стоимость доставки.</div></div>
      <div class="step fade-up"><div class="step-num">3</div><div class="step-title">Оплата</div><div class="step-text">Выставим счёт. Принимаем безналичную оплату для юридических и физических лиц.</div></div>
      <div class="step fade-up"><div class="step-num">4</div><div class="step-title">Доставка</div><div class="step-text">Отправим товар в ваш регион. Предоставим трек-номер для отслеживания груза.</div></div>
    </div>
  </div>
</section>
 
<!-- CONTACT -->
<section class="contact-bg" id="contact">
  <div class="container">
    <div class="section-label fade-up">Контакты</div>
    <div class="section-title fade-up">Свяжитесь с нами</div>
    <div class="contact-grid">
      <div>
        <div class="contact-item fade-up"><div class="contact-ico">📍</div><div><div class="contact-label">Адрес</div><span class="contact-value">г. Актау, Промзона №6, база «Вира»</span></div></div>
        <div class="contact-item fade-up"><div class="contact-ico">📞</div><div><div class="contact-label">Телефон</div><a href="tel:+77763333082" class="contact-value">+7 (776) 333 30 82</a><a href="tel:+77783337785" class="contact-value">+7 (778) 333 77 85</a></div></div>
        <div class="contact-item fade-up"><div class="contact-ico">✉️</div><div><div class="contact-label">Email</div><a href="mailto:info@merey-munay.kz" class="contact-value">info@merey-munay.kz</a></div></div>
        <div class="contact-item fade-up"><div class="contact-ico">💬</div><div><div class="contact-label">WhatsApp</div><a href="https://wa.me/77763333082" class="contact-value" target="_blank">+7 (776) 333 30 82</a></div></div>
        <div class="fade-up" style="margin-top:24px"><a href="https://wa.me/77763333082" target="_blank" class="btn-primary" style="display:inline-flex;align-items:center;gap:8px">💬 Написать в WhatsApp</a></div>
      </div>
      <div class="contact-form fade-up">
        <div class="form-title">Отправить запрос</div>
        <div class="form-row">
          <div class="form-group"><label>Ваше имя</label><input type="text" placeholder="Иван Иванов"></div>
          <div class="form-group"><label>Телефон</label><input type="tel" placeholder="+7 (___) ___ __ __"></div>
        </div>
        <div class="form-group"><label>Компания</label><input type="text" placeholder="ТОО / АО / ИП"></div>
        <div class="form-group"><label>Что вас интересует?</label>
          <select><option value="">Выберите категорию</option><option>АДПМ</option><option>ППУА</option><option>ЦА-320</option><option>НБ125 / НБ50</option><option>Насосы</option><option>СИН32</option><option>Другое</option></select>
        </div>
        <div class="form-group"><label>Сообщение</label><textarea placeholder="Опишите ваш запрос: модель, количество, срочность..."></textarea></div>
        <button class="form-submit" onclick="this.textContent='✓ Отправлено! Мы свяжемся с вами.'; this.style.background='#1A6B3A'">Отправить запрос</button>
      </div>
    </div>
  </div>
</section>
 
<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div>
      <div class="footer-logo">Мерей<span>Мунай</span></div>
      <p class="footer-about">Надёжный поставщик нефтепромыслового оборудования и запасных частей в Казахстане. ТОО «Мерей Мунай».</p>
      <a href="https://wa.me/77763333082" target="_blank" class="footer-wa">💬 WhatsApp</a>
    </div>
    <div>
      <div class="footer-col-title">Каталог</div>
      <ul class="footer-links">
        <li><a href="#catalog">АДПМ</a></li><li><a href="#catalog">ППУА</a></li><li><a href="#catalog">ЦА-320</a></li><li><a href="#catalog">НБ125 / НБ50</a></li><li><a href="#catalog">Насосы</a></li><li><a href="#catalog">СИН32</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">Компания</div>
      <ul class="footer-links">
        <li><a href="#how">О нас</a></li><li><a href="#how">Как работаем</a></li><li><a href="#contact">Оплата и доставка</a></li><li><a href="#contact">Контакты</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <span>© 2024 ТОО «Мерей Мунай». Все права защищены.</span>
    <span>г. Актау · <a href="tel:+77763333082">+7 (776) 333 30 82</a></span>
  </div>
</footer>
 
<a href="https://wa.me/77763333082" target="_blank" class="wa-float" title="WhatsApp">💬</a>
 
<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });
  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));
</script>
</body>
</html>
