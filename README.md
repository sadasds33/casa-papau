!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Casa Papau Resto Bar — Santa Marta</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,600;0,9..144,700;0,9..144,900;1,9..144,600;1,9..144,700&family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400&display=swap" rel="stylesheet">
<style>
  :root{
    --teal-deep:#0B4F49;
    --teal-mid:#146E64;
    --papaya:#F5A527;
    --coral:#EF5B5B;
    --cream:#FBF1DE;
    --sand:#F3E4C8;
    --ink:#1F2A24;
    --ink-soft:#3C4A42;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--cream);
    color:var(--ink);
    font-family:'DM Sans',sans-serif;
    overflow-x:hidden;
  }
  h1,h2,h3,.display{
    font-family:'Fraunces',serif;
    font-weight:700;
    letter-spacing:-0.01em;
  }
  a{text-decoration:none;color:inherit;}
  img,svg{display:block;max-width:100%;}
  .wrap{max-width:1180px;margin:0 auto;padding:0 32px;}
  ::selection{background:var(--papaya);color:var(--ink);}
 
  /* -------- NAV -------- */
  nav{
    position:fixed;top:0;left:0;right:0;z-index:100;
    background:rgba(11,79,73,0.92);
    backdrop-filter:blur(6px);
    transition:padding .3s ease;
  }
  .nav-inner{
    max-width:1180px;margin:0 auto;padding:18px 32px;
    display:flex;align-items:center;justify-content:space-between;
  }
  .logo{
    font-family:'Fraunces',serif;font-weight:900;font-style:italic;
    color:var(--cream);font-size:1.4rem;letter-spacing:0.01em;
  }
  .logo span{color:var(--papaya);}
  .nav-links{display:flex;gap:28px;align-items:center;}
  .nav-links a{
    color:var(--sand);font-size:0.92rem;font-weight:500;
    position:relative;padding:4px 0;
  }
  .nav-links a::after{
    content:"";position:absolute;bottom:0;left:0;width:0;height:1.5px;
    background:var(--papaya);transition:width .25s ease;
  }
  .nav-links a:hover::after{width:100%;}
  .btn{
    display:inline-flex;align-items:center;gap:8px;
    background:var(--coral);color:var(--cream);
    padding:11px 22px;border-radius:100px;
    font-weight:700;font-size:0.9rem;
    box-shadow:0 6px 18px rgba(239,91,91,0.35);
    transition:transform .25s ease, box-shadow .25s ease;
  }
  .btn:hover{transform:translateY(-2px);box-shadow:0 10px 22px rgba(239,91,91,0.45);}
  .btn-outline{
    background:transparent;border:1.5px solid var(--sand);color:var(--sand);
    box-shadow:none;
  }
  .btn-outline:hover{background:var(--sand);color:var(--teal-deep);}
  .nav-cta{display:none;}
  @media(min-width:840px){.nav-cta{display:inline-flex;} .nav-links{display:flex;}}
  @media(max-width:839px){.nav-links{display:none;}}
 
  /* -------- HERO -------- */
  .hero{
    position:relative;
    min-height:100vh;
    background:linear-gradient(180deg,var(--teal-deep) 0%,var(--teal-mid) 70%);
    overflow:hidden;
    display:flex;align-items:center;
    padding-top:90px;
  }
  .hero-layer{position:absolute;inset:0;pointer-events:none;}
  .hero-content{
    position:relative;z-index:5;width:100%;
    max-width:1180px;margin:0 auto;padding:60px 32px 120px;
    display:grid;grid-template-columns:1.1fr 0.9fr;gap:40px;align-items:center;
  }
  @media(max-width:900px){.hero-content{grid-template-columns:1fr;}}
  .eyebrow{
    display:inline-flex;align-items:center;gap:10px;
    background:rgba(245,165,39,0.15);border:1px solid rgba(245,165,39,0.4);
    color:var(--papaya);padding:7px 16px;border-radius:100px;
    font-size:0.82rem;font-weight:700;letter-spacing:0.04em;text-transform:uppercase;
    margin-bottom:26px;
  }
  .hero h1{
    color:var(--cream);font-size:clamp(2.6rem,5.5vw,4.3rem);
    line-height:1.02;margin-bottom:22px;
  }
  .hero h1 em{
    font-style:italic;color:var(--papaya);
  }
  .hero p.lede{
    color:var(--sand);font-size:1.15rem;line-height:1.55;
    max-width:480px;margin-bottom:34px;
  }
  .hero-actions{display:flex;gap:16px;flex-wrap:wrap;}
  .rating-card{
    background:var(--cream);border-radius:20px;padding:26px 28px;
    box-shadow:0 30px 60px rgba(0,0,0,0.35);
    position:relative;
  }
  .rating-top{display:flex;align-items:baseline;gap:10px;margin-bottom:6px;}
  .rating-num{font-family:'Fraunces',serif;font-weight:900;font-size:3rem;color:var(--teal-deep);}
  .stars{color:var(--papaya);font-size:1.1rem;letter-spacing:2px;}
  .rating-sub{color:var(--ink-soft);font-size:0.9rem;margin-bottom:18px;}
  .rating-divider{height:1px;background:var(--sand);margin:18px 0;}
  .rating-row{display:flex;justify-content:space-between;font-size:0.9rem;padding:6px 0;color:var(--ink-soft);}
  .rating-row b{color:var(--ink);}
  .badge-strip{display:flex;gap:10px;margin-top:20px;flex-wrap:wrap;}
  .pill{
    font-size:0.75rem;font-weight:700;padding:6px 12px;border-radius:100px;
    background:var(--teal-deep);color:var(--sand);
  }
 
  /* scallop divider */
  .scallop{
    position:absolute;bottom:-1px;left:0;width:100%;line-height:0;z-index:3;
  }
 
  /* -------- SECTION GENERIC -------- */
  section{position:relative;padding:110px 0;}
  .section-head{max-width:640px;margin-bottom:56px;}
  .kicker{
    color:var(--coral);font-weight:700;font-size:0.85rem;text-transform:uppercase;
    letter-spacing:0.08em;margin-bottom:14px;display:block;
  }
  .section-head h2{font-size:clamp(2rem,4vw,2.9rem);line-height:1.08;color:var(--teal-deep);}
  .section-head p{color:var(--ink-soft);font-size:1.05rem;margin-top:16px;line-height:1.6;}
 
  /* -------- ABOUT -------- */
  .about{background:var(--cream);}
  .about-grid{display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:center;}
  @media(max-width:860px){.about-grid{grid-template-columns:1fr;}}
  .about-art{position:relative;}
  .value-list{display:flex;flex-direction:column;gap:18px;margin-top:8px;}
  .value-item{
    display:flex;gap:16px;align-items:flex-start;
    background:#fff;border:1px solid var(--sand);border-radius:16px;padding:18px 20px;
  }
  .value-icon{
    flex:none;width:42px;height:42px;border-radius:12px;
    background:var(--teal-deep);display:flex;align-items:center;justify-content:center;
  }
  .value-item h3{font-size:1.02rem;color:var(--teal-deep);margin-bottom:4px;}
  .value-item p{font-size:0.92rem;color:var(--ink-soft);}
 
  /* -------- MENU -------- */
  .menu{background:var(--teal-deep);}
  .menu .section-head h2{color:var(--cream);}
  .menu .kicker{color:var(--papaya);}
  .menu .section-head p{color:var(--sand);}
  .menu-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:24px;}
  @media(max-width:760px){.menu-grid{grid-template-columns:1fr;}}
  .menu-card{
    background:var(--cream);border-radius:22px;overflow:hidden;
    display:flex;flex-direction:column;
    box-shadow:0 20px 40px rgba(0,0,0,0.25);
  }
  .menu-card .art{
    aspect-ratio:16/10;overflow:hidden;position:relative;background:var(--sand);
  }
  .menu-card .art svg{width:100%;height:100%;transform:scale(1.15);}
  .menu-card .body{padding:22px 24px 26px;}
  .menu-card .tag{
    font-size:0.72rem;font-weight:700;color:var(--coral);text-transform:uppercase;
    letter-spacing:0.06em;margin-bottom:6px;display:block;
  }
  .menu-card h3{font-size:1.3rem;color:var(--teal-deep);margin-bottom:8px;}
  .menu-card p{font-size:0.92rem;color:var(--ink-soft);line-height:1.5;}
 
  /* -------- GALLERY -------- */
  .gallery{background:var(--cream);}
  .gallery-grid{
    display:grid;grid-template-columns:repeat(3,1fr);gap:22px;
  }
  @media(max-width:760px){.gallery-grid{grid-template-columns:1fr 1fr;}}
  @media(max-width:520px){.gallery-grid{grid-template-columns:1fr;}}
  .gallery-item{
    border-radius:18px;overflow:hidden;aspect-ratio:1/1;
    background:var(--teal-mid);position:relative;
  }
  .gallery-item svg{width:100%;height:100%;}
  .gallery-item.tall{aspect-ratio:1/1.35;grid-row:span 1;}
  .gallery-cap{
    position:absolute;bottom:0;left:0;right:0;padding:14px 16px;
    background:linear-gradient(0deg,rgba(11,79,73,0.85),transparent);
    color:var(--cream);font-size:0.85rem;font-weight:700;
  }
 
  /* -------- TESTIMONIALS -------- */
  .reviews{background:var(--sand);}
  .review-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:24px;}
  @media(max-width:900px){.review-grid{grid-template-columns:1fr;}}
  .review-card{
    background:var(--cream);border-radius:20px;padding:28px 26px;
    border:1px solid rgba(31,42,36,0.08);
  }
  .review-stars{color:var(--papaya);font-size:1rem;margin-bottom:14px;letter-spacing:2px;}
  .review-card p{color:var(--ink-soft);font-size:0.95rem;line-height:1.55;margin-bottom:20px;}
  .review-who{display:flex;align-items:center;gap:12px;}
  .avatar{
    width:38px;height:38px;border-radius:50%;
    background:var(--teal-deep);color:var(--cream);
    display:flex;align-items:center;justify-content:center;font-weight:700;font-size:0.9rem;
    font-family:'Fraunces',serif;
  }
  .review-who b{font-size:0.9rem;display:block;}
  .review-who span{font-size:0.78rem;color:var(--ink-soft);}
 
  /* -------- VISIT -------- */
  .visit{background:var(--teal-deep);color:var(--cream);}
  .visit-grid{display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:center;}
  @media(max-width:860px){.visit-grid{grid-template-columns:1fr;}}
  .visit .kicker{color:var(--papaya);}
  .visit h2{color:var(--cream);}
  .info-row{
    display:flex;gap:16px;padding:18px 0;border-bottom:1px solid rgba(251,241,222,0.15);
  }
  .info-row:first-of-type{border-top:1px solid rgba(251,241,222,0.15);}
  .info-row .ic{flex:none;color:var(--papaya);}
  .info-row h4{font-size:0.95rem;margin-bottom:4px;color:var(--cream);}
  .info-row p{font-size:0.88rem;color:var(--sand);line-height:1.5;}
  .map-card{
    background:var(--teal-mid);border-radius:22px;padding:8px;
    box-shadow:0 30px 60px rgba(0,0,0,0.3);
  }
 
  /* -------- FOOTER -------- */
  footer{background:#08302C;color:var(--sand);padding:60px 0 30px;}
  .foot-grid{display:flex;justify-content:space-between;flex-wrap:wrap;gap:40px;margin-bottom:40px;}
  .foot-logo{font-family:'Fraunces',serif;font-style:italic;font-weight:900;font-size:1.5rem;color:var(--cream);margin-bottom:10px;}
  .foot-logo span{color:var(--papaya);}
  .foot-links{display:flex;gap:60px;flex-wrap:wrap;}
  .foot-col h5{font-size:0.78rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--papaya);margin-bottom:14px;}
  .foot-col a{display:block;font-size:0.9rem;margin-bottom:10px;color:var(--sand);}
  .foot-col a:hover{color:var(--cream);}
  .foot-bottom{
    border-top:1px solid rgba(251,241,222,0.12);padding-top:24px;
    display:flex;justify-content:space-between;flex-wrap:wrap;gap:10px;
    font-size:0.8rem;color:rgba(251,241,222,0.6);
  }
 
  .reveal{opacity:0;transform:translateY(40px);}
 
  @media(prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
  }
</style>
</head>
<body>
 
<nav>
  <div class="nav-inner">
    <a href="#top" class="logo">Casa <span>Papau</span></a>
    <div class="nav-links">
      <a href="#menu">Menú</a>
      <a href="#galeria">Galería</a>
      <a href="#opiniones">Opiniones</a>
      <a href="#visitanos">Cómo llegar</a>
    </div>
    <a href="https://wa.me/573166946289" target="_blank" class="btn nav-cta">Pedir por WhatsApp</a>
  </div>
</nav>
 
<!-- ================= HERO ================= -->
<header class="hero" id="top">
  <div class="hero-layer" id="layer-back">
    <svg width="100%" height="100%" viewBox="0 0 1400 900" preserveAspectRatio="xMidYMid slice" style="position:absolute;inset:0;">
      <circle cx="1180" cy="120" r="260" fill="#0F5850" opacity="0.6"/>
      <circle cx="120" cy="780" r="220" fill="#0F5850" opacity="0.5"/>
    </svg>
  </div>
  <div class="hero-layer" id="layer-mid">
    <svg width="100%" height="100%" viewBox="0 0 1400 900" preserveAspectRatio="xMidYMid slice" style="position:absolute;inset:0;">
      <path d="M-50 150 C 60 60, 120 60, 150 150 C 180 240, 100 280, 40 260 C -20 240, -80 200, -50 150 Z" fill="#146E64" opacity="0.7" transform="translate(1180,60) scale(1.4)"/>
      <path d="M0 0 C 40 -60 100 -70 140 -10 C 100 20 40 30 0 0 Z" fill="#1C7A6E" opacity="0.55" transform="translate(60,650) scale(2)"/>
    </svg>
  </div>
  <div class="hero-layer" id="layer-front">
    <svg width="100%" height="100%" viewBox="0 0 1400 900" preserveAspectRatio="xMidYMid slice" style="position:absolute;inset:0;">
      <!-- palm fronds top right -->
      <g transform="translate(1260,-30)" opacity="0.9">
        <path d="M0 0 C -80 20 -140 90 -150 180 C -80 130 -20 90 0 0 Z" fill="#F5A527" opacity="0.85"/>
        <path d="M0 0 C 60 40 90 110 80 200 C 30 140 0 90 0 0 Z" fill="#EF5B5B" opacity="0.75"/>
        <path d="M0 0 C -30 60 -20 140 30 200 C 50 120 40 60 0 0 Z" fill="#F5A527" opacity="0.65"/>
      </g>
      <g transform="translate(-60,860)" opacity="0.9">
        <path d="M0 0 C 80 -20 140 -90 150 -180 C 80 -130 20 -90 0 0 Z" fill="#EF5B5B" opacity="0.7"/>
        <path d="M0 0 C -60 -40 -90 -110 -80 -200 C -30 -140 0 -90 0 0 Z" fill="#F5A527" opacity="0.6"/>
      </g>
    </svg>
  </div>
 
  <div class="hero-content">
    <div>
      <span class="eyebrow">Santa Marta · Comuna 2</span>
      <h1>Sabor costeño,<br><em>ambiente</em> de casa.</h1>
      <p class="lede">Resto bar al aire libre en el corazón de Santa Marta: parrilla, hamburguesas de autor y ese trato cálido que solo se siente en familia.</p>
      <div class="hero-actions">
        <a href="https://wa.me/573166946289" target="_blank" class="btn">Pedir por WhatsApp →</a>
        <a href="#menu" class="btn btn-outline">Ver el menú</a>
      </div>
      <div class="badge-strip">
        <span class="pill">🏳️‍🌈 LGBTQ+ friendly</span>
        <span class="pill">Liderado por mujer empresaria</span>
        <span class="pill">Domicilio disponible</span>
      </div>
    </div>
 
    <div class="rating-card reveal" id="rating-card">
      <div class="rating-top">
        <span class="rating-num">4.8</span>
        <span class="stars">★★★★★</span>
      </div>
      <p class="rating-sub">761 opiniones en Google</p>
      <div class="rating-divider"></div>
      <div class="rating-row"><span>Rango de precio</span><b>$20.000–$40.000</b></div>
      <div class="rating-row"><span>Horario hoy</span><b>Hasta 9:30 p.m.</b></div>
      <div class="rating-row"><span>Mayor afluencia</span><b>Viernes noche</b></div>
      <div class="rating-row"><span>Servicio</span><b>Local · Para llevar · Domicilio</b></div>
    </div>
  </div>
 
  <div class="scallop">
    <svg viewBox="0 0 1400 60" preserveAspectRatio="none" width="100%" height="60">
      <path d="M0,0 Q35,60 70,0 T140,0 T210,0 T280,0 T350,0 T420,0 T490,0 T560,0 T630,0 T700,0 T770,0 T840,0 T910,0 T980,0 T1050,0 T1120,0 T1190,0 T1260,0 T1330,0 T1400,0 L1400,0 L0,0 Z" fill="#FBF1DE"/>
    </svg>
  </div>
</header>
 
<!-- ================= ABOUT ================= -->
<section class="about" id="nosotros">
  <div class="wrap about-grid">
    <div class="reveal">
      <span class="kicker">Sobre nosotros</span>
      <h2>El espacio te hace sentir como en casa.</h2>
      <p style="margin-top:18px;color:var(--ink-soft);font-size:1.03rem;line-height:1.65;">
        Casa Papau nació para recibir a cada persona como familia. Un patio abierto, música de fondo y un equipo que se acuerda de tu nombre desde la segunda visita — así lo describen quienes ya nos conocen.
      </p>
      <div class="value-list">
        <div class="value-item">
          <div class="value-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none"><path d="M12 21s-7-4.35-9.5-8.5C.7 8.9 2.4 5 6 5c2 0 3.5 1.2 4.2 2.6C10.9 6.2 12.4 5 14.4 5c3.6 0 5.3 3.9 3.5 7.5C19 16.65 12 21 12 21z" fill="#F5A527"/></svg>
          </div>
          <div><h3>Trato de familia</h3><p>Personal cercano que recibe a cada visitante como si llegara a casa.</p></div>
        </div>
        <div class="value-item">
          <div class="value-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none"><path d="M12 2l2.4 6.8L21 10l-5.5 4.2L17 21l-5-3.6L7 21l1.5-6.8L3 10l6.6-1.2L12 2z" fill="#F5A527"/></svg>
          </div>
          <div><h3>Ambiente al aire libre</h3><p>Patio tranquilo y aventurero, ideal para desayunos largos o noches de viernes.</p></div>
        </div>
        <div class="value-item">
          <div class="value-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="12" r="9" fill="#F5A527"/></svg>
          </div>
          <div><h3>Espacio incluyente</h3><p>Amigable con la comunidad LGBTQ+ y liderado por una mujer empresaria samaria.</p></div>
        </div>
      </div>
    </div>
 
    <div class="about-art reveal">
      <svg viewBox="0 0 520 560" width="100%" id="about-illustration">
        <rect x="20" y="60" width="480" height="440" rx="28" fill="#146E64"/>
        <rect x="20" y="60" width="480" height="130" rx="28" fill="#0B4F49"/>
        <circle cx="90" cy="125" r="14" fill="#EF5B5B"/>
        <circle cx="135" cy="125" r="14" fill="#F5A527"/>
        <circle cx="180" cy="125" r="14" fill="#FBF1DE"/>
        <!-- table scene -->
        <ellipse cx="260" cy="400" rx="170" ry="26" fill="#0B4F49" opacity="0.5"/>
        <rect x="130" y="250" width="260" height="14" rx="7" fill="#FBF1DE"/>
        <rect x="150" y="264" width="220" height="130" fill="#F3E4C8"/>
        <circle cx="200" cy="300" r="34" fill="#EF5B5B"/>
        <circle cx="200" cy="300" r="20" fill="#F5A527"/>
        <rect x="255" y="280" width="90" height="60" rx="10" fill="#0B4F49"/>
        <rect x="265" y="292" width="70" height="8" rx="4" fill="#F5A527"/>
        <rect x="265" y="308" width="50" height="8" rx="4" fill="#EF5B5B"/>
        <path d="M340 470 C 320 430 320 400 350 380 C 380 400 380 430 360 470 Z" fill="#F5A527"/>
        <path d="M180 480 C 160 440 160 410 190 390 C 220 410 220 440 200 480 Z" fill="#EF5B5B"/>
      </svg>
    </div>
  </div>
</section>
 
<!-- ================= MENU ================= -->
<section class="menu" id="menu">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="kicker">Menú destacado</span>
      <h2>Lo que no te puedes perder</h2>
      <p>Cuatro clásicos de la casa — del carbón al plato, con sazón costeña.</p>
    </div>
 
    <div class="menu-grid">
      <div class="menu-card reveal parallax-img">
        <div class="art">
          <svg viewBox="0 0 400 250" preserveAspectRatio="xMidYMid slice">
            <rect width="400" height="250" fill="#F5A527"/>
            <ellipse cx="200" cy="190" rx="150" ry="30" fill="#EF5B5B" opacity="0.4"/>
            <g transform="translate(90,60)">
              <rect x="0" y="70" width="220" height="24" rx="12" fill="#8B3A1F"/>
              <rect x="10" y="40" width="200" height="34" rx="14" fill="#A8461F"/>
              <rect x="20" y="10" width="180" height="34" rx="14" fill="#8B3A1F"/>
              <rect x="20" y="10" width="180" height="10" rx="5" fill="#EF5B5B" opacity="0.6"/>
            </g>
          </svg>
        </div>
        <div class="body">
          <span class="tag">Parrilla</span>
          <h3>Costillas BBQ</h3>
          <p>Cocción lenta al carbón bañada en salsa BBQ de la casa, acompañada de papas o patacón.</p>
        </div>
      </div>
 
      <div class="menu-card reveal parallax-img">
        <div class="art">
          <svg viewBox="0 0 400 250" preserveAspectRatio="xMidYMid slice">
            <rect width="400" height="250" fill="#EF5B5B"/>
            <g transform="translate(120,50)">
              <ellipse cx="80" cy="150" rx="90" ry="14" fill="#5C1A1A" opacity="0.3"/>
              <rect x="0" y="120" width="160" height="26" rx="13" fill="#7A3B14"/>
              <rect x="10" y="95" width="140" height="30" rx="10" fill="#3D8B3D"/>
              <rect x="15" y="70" width="130" height="30" rx="15" fill="#4A2A16"/>
              <rect x="20" y="45" width="120" height="30" rx="15" fill="#E8B23D"/>
              <rect x="0" y="18" width="160" height="26" rx="13" fill="#7A3B14"/>
            </g>
          </svg>
        </div>
        <div class="body">
          <span class="tag">Burger</span>
          <h3>Costeñita Burguer</h3>
          <p>Carne jugosa, queso costeño derretido y vegetales frescos en pan brioche tostado.</p>
        </div>
      </div>
 
      <div class="menu-card reveal parallax-img">
        <div class="art">
          <svg viewBox="0 0 400 250" preserveAspectRatio="xMidYMid slice">
            <rect width="400" height="250" fill="#146E64"/>
            <g transform="translate(110,45)">
              <ellipse cx="90" cy="160" rx="95" ry="14" fill="#0B4F49" opacity="0.5"/>
              <rect x="0" y="128" width="180" height="24" rx="12" fill="#7A3B14"/>
              <rect x="10" y="100" width="160" height="32" rx="10" fill="#F5A527"/>
              <rect x="20" y="72" width="140" height="32" rx="16" fill="#4A2A16"/>
              <rect x="0" y="44" width="180" height="24" rx="12" fill="#7A3B14"/>
              <text x="90" y="20" text-anchor="middle" font-size="26" fill="#F5A527">🌶</text>
            </g>
          </svg>
        </div>
        <div class="body">
          <span class="tag">Firma de la casa</span>
          <h3>Hamburguesa "Cógela Suave"</h3>
          <p>Doble carne, tocineta ahumada y salsa picante suave — la más pedida los viernes.</p>
        </div>
      </div>
 
      <div class="menu-card reveal parallax-img">
        <div class="art">
          <svg viewBox="0 0 400 250" preserveAspectRatio="xMidYMid slice">
            <rect width="400" height="250" fill="#F3E4C8"/>
            <circle cx="200" cy="140" r="80" fill="#F5A527"/>
            <circle cx="200" cy="140" r="80" fill="none" stroke="#EF5B5B" stroke-width="6" stroke-dasharray="10 8"/>
            <circle cx="170" cy="120" r="26" fill="#FBF1DE"/>
            <circle cx="170" cy="120" r="10" fill="#F5A527"/>
            <circle cx="225" cy="150" r="22" fill="#FBF1DE"/>
            <circle cx="225" cy="150" r="8" fill="#F5A527"/>
          </svg>
        </div>
        <div class="body">
          <span class="tag">Desayunos</span>
          <h3>Huevos con arepa y queso costeño</h3>
          <p>El desayuno más recomendado de la casa: arepa caliente, huevos al gusto y queso costeño.</p>
        </div>
      </div>
    </div>
  </div>
</section>
 
<!-- ================= GALLERY ================= -->
<section class="gallery" id="galeria">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="kicker">Galería</span>
      <h2>El ambiente de Casa Papau</h2>
      <p>Un vistazo al patio, la parrilla y los platos que definen la casa.</p>
    </div>
 
    <div class="gallery-grid">
      <div class="gallery-item tall parallax-img">
        <svg viewBox="0 0 300 400" preserveAspectRatio="xMidYMid slice">
          <rect width="300" height="400" fill="#0B4F49"/>
          <circle cx="230" cy="70" r="60" fill="#146E64"/>
          <rect x="40" y="260" width="220" height="12" rx="6" fill="#F5A527"/>
          <rect x="60" y="272" width="180" height="90" fill="#F3E4C8"/>
          <circle cx="110" cy="230" r="26" fill="#EF5B5B"/>
          <circle cx="190" cy="230" r="26" fill="#F5A527"/>
        </svg>
        <div class="gallery-cap">Patio principal</div>
      </div>
      <div class="gallery-item parallax-img">
        <svg viewBox="0 0 300 300" preserveAspectRatio="xMidYMid slice">
          <rect width="300" height="300" fill="#EF5B5B"/>
          <path d="M60 260 C 40 180 90 140 150 140 C 210 140 260 180 240 260 Z" fill="#F5A527"/>
          <rect x="90" y="255" width="120" height="16" rx="8" fill="#0B4F49"/>
        </svg>
        <div class="gallery-cap">Parrilla en vivo</div>
      </div>
      <div class="gallery-item parallax-img">
        <svg viewBox="0 0 300 300" preserveAspectRatio="xMidYMid slice">
          <rect width="300" height="300" fill="#F5A527"/>
          <rect x="70" y="60" width="18" height="180" fill="#0B4F49"/>
          <rect x="130" y="90" width="18" height="150" fill="#0B4F49"/>
          <rect x="190" y="40" width="18" height="200" fill="#0B4F49"/>
          <circle cx="79" cy="55" r="16" fill="#EF5B5B"/>
          <circle cx="139" cy="85" r="16" fill="#EF5B5B"/>
          <circle cx="199" cy="35" r="16" fill="#EF5B5B"/>
        </svg>
        <div class="gallery-cap">Bebidas de la casa</div>
      </div>
      <div class="gallery-item parallax-img">
        <svg viewBox="0 0 300 300" preserveAspectRatio="xMidYMid slice">
          <rect width="300" height="300" fill="#146E64"/>
          <rect x="50" y="120" width="200" height="30" rx="15" fill="#7A3B14"/>
          <rect x="60" y="95" width="180" height="34" rx="12" fill="#F5A527"/>
          <rect x="70" y="70" width="160" height="30" rx="15" fill="#4A2A16"/>
        </svg>
        <div class="gallery-cap">Costeñita Burguer</div>
      </div>
      <div class="gallery-item tall parallax-img">
        <svg viewBox="0 0 300 400" preserveAspectRatio="xMidYMid slice">
          <rect width="300" height="400" fill="#F3E4C8"/>
          <circle cx="150" cy="180" r="100" fill="#F5A527"/>
          <circle cx="150" cy="180" r="100" fill="none" stroke="#EF5B5B" stroke-width="8" stroke-dasharray="14 10"/>
          <circle cx="120" cy="150" r="30" fill="#FBF1DE"/>
          <circle cx="120" cy="150" r="12" fill="#F5A527"/>
        </svg>
        <div class="gallery-cap">Desayunos costeños</div>
      </div>
      <div class="gallery-item parallax-img">
        <svg viewBox="0 0 300 300" preserveAspectRatio="xMidYMid slice">
          <rect width="300" height="300" fill="#0B4F49"/>
          <g stroke="#F5A527" stroke-width="4" fill="none">
            <path d="M40 250 Q150 180 260 250"/>
            <path d="M40 220 Q150 150 260 220"/>
            <path d="M40 190 Q150 120 260 190"/>
          </g>
          <circle cx="150" cy="90" r="34" fill="#EF5B5B"/>
        </svg>
        <div class="gallery-cap">Atardecer en el patio</div>
      </div>
    </div>
  </div>
</section>
 
<!-- ================= TESTIMONIALS ================= -->
<section class="reviews" id="opiniones">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="kicker">Opiniones</span>
      <h2>Lo que dicen quienes ya nos visitaron</h2>
      <p>761 opiniones en Google con una calificación de 4.8 sobre 5.</p>
    </div>
 
    <div class="review-grid">
      <div class="review-card reveal">
        <div class="review-stars">★★★★★</div>
        <p>El espacio se siente como en casa y el equipo recibe a cada visitante como si fuera de la familia — un ambiente divertido y aventurero desde la recepción.</p>
        <div class="review-who">
          <div class="avatar">AM</div>
          <div><b>Axel Malo</b><span>Local Guide · hace 7 meses</span></div>
        </div>
      </div>
      <div class="review-card reveal">
        <div class="review-stars">★★★★★</div>
        <p>Un lugar tranquilo y al aire libre. La atención de Valentina, diez de diez, y los huevos con arepa y queso costeño son muy recomendados.</p>
        <div class="review-who">
          <div class="avatar">DR</div>
          <div><b>Daniela Rodríguez</b><span>Local Guide · hace 8 meses</span></div>
        </div>
      </div>
      <div class="review-card reveal">
        <div class="review-stars">★★★★★</div>
        <p>Servicio excelente: atención comprensible y muy atenta, en un lugar que se mantiene en excelentes condiciones.</p>
        <div class="review-who">
          <div class="avatar">DG</div>
          <div><b>Dayana González</b><span>hace 9 meses</span></div>
        </div>
      </div>
    </div>
  </div>
</section>
 
<!-- ================= VISIT ================= -->
<section class="visit" id="visitanos">
  <div class="wrap visit-grid">
    <div class="reveal">
      <span class="kicker">Visítanos</span>
      <h2>Te esperamos en Santa Marta</h2>
 
      <div class="info-row">
        <div class="ic"><svg width="22" height="22" viewBox="0 0 24 24" fill="none"><path d="M12 2C7.6 2 4 5.6 4 10c0 6 8 12 8 12s8-6 8-12c0-4.4-3.6-8-8-8zm0 11a3 3 0 110-6 3 3 0 010 6z" fill="#F5A527"/></svg></div>
        <div><h4>Dirección</h4><p>Calle 26 # 4-100, Comuna 2, Santa Marta, Magdalena</p></div>
      </div>
      <div class="info-row">
        <div class="ic"><svg width="22" height="22" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="12" r="9" stroke="#F5A527" stroke-width="2"/><path d="M12 7v5l4 2" stroke="#F5A527" stroke-width="2" stroke-linecap="round"/></svg></div>
        <div><h4>Horario</h4><p>Abierto hoy · cierra a las 9:30 p.m. Mayor afluencia los viernes en la noche.</p></div>
      </div>
      <div class="info-row">
        <div class="ic"><svg width="22" height="22" viewBox="0 0 24 24" fill="none"><path d="M4 4h4l2 5-2.5 1.5a11 11 0 005 5L14 13l5 2v4a2 2 0 01-2 2C9.2 21 3 14.8 3 7a2 2 0 011-2z" fill="#F5A527"/></svg></div>
        <div><h4>Reservas y pedidos</h4><p>316 694 6289 — WhatsApp, llamada o domicilio.</p></div>
      </div>
 
      <div style="margin-top:32px;display:flex;gap:16px;flex-wrap:wrap;">
        <a href="https://wa.me/573166946289" target="_blank" class="btn">Escribir por WhatsApp →</a>
        <a href="https://www.google.com/maps/search/?api=1&query=Casa+Papau+Resto+Bar+Calle+26+%234-100+Santa+Marta" target="_blank" class="btn btn-outline">Cómo llegar</a>
      </div>
    </div>
 
    <div class="reveal">
      <div class="map-card">
        <svg viewBox="0 0 480 420" width="100%">
          <rect width="480" height="420" rx="16" fill="#0B4F49"/>
          <g stroke="#1C7A6E" stroke-width="2">
            <line x1="0" y1="90" x2="480" y2="90"/>
            <line x1="0" y1="190" x2="480" y2="190"/>
            <line x1="0" y1="290" x2="480" y2="290"/>
            <line x1="120" y1="0" x2="120" y2="420"/>
            <line x1="280" y1="0" x2="280" y2="420"/>
            <line x1="380" y1="0" x2="380" y2="420"/>
          </g>
          <circle cx="240" cy="190" r="16" fill="#EF5B5B"/>
          <path d="M240 150 C 210 150 195 175 195 200 C 195 235 240 270 240 270 C 240 270 285 235 285 200 C 285 175 270 150 240 150Z" fill="#F5A527"/>
          <circle cx="240" cy="198" r="14" fill="#0B4F49"/>
          <text x="240" y="330" text-anchor="middle" fill="#FBF1DE" font-family="DM Sans, sans-serif" font-size="14" font-weight="700">Calle 26 # 4-100</text>
          <text x="240" y="350" text-anchor="middle" fill="#F3E4C8" font-family="DM Sans, sans-serif" font-size="12">Comuna 2, Santa Marta</text>
        </svg>
      </div>
    </div>
  </div>
</section>
 
<!-- ================= FOOTER ================= -->
<footer>
  <div class="wrap">
    <div class="foot-grid">
      <div>
        <div class="foot-logo">Casa <span>Papau</span></div>
        <p style="max-width:260px;font-size:0.88rem;color:var(--sand);">Resto bar costeño en Santa Marta. Sabor, calidez y un patio que se siente como en casa.</p>
      </div>
      <div class="foot-links">
        <div class="foot-col">
          <h5>Explora</h5>
          <a href="#menu">Menú</a>
          <a href="#galeria">Galería</a>
          <a href="#opiniones">Opiniones</a>
          <a href="#visitanos">Ubicación</a>
        </div>
        <div class="foot-col">
          <h5>Contacto</h5>
          <a href="tel:+573166946289">316 694 6289</a>
          <a href="https://wa.me/573166946289" target="_blank">WhatsApp</a>
          <a href="https://instagram.com" target="_blank">Instagram</a>
        </div>
      </div>
    </div>
    <div class="foot-bottom">
      <span>© 2026 Casa Papau Resto Bar · Santa Marta, Magdalena</span>
      <span>Amigable con LGBTQ+ · Liderado por una mujer empresaria</span>
    </div>
  </div>
</footer>
 
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
<script>
  gsap.registerPlugin(ScrollTrigger);
  const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
 
  if(!reduceMotion){
    // Hero parallax layers
    gsap.to("#layer-back", { y: 120, ease: "none",
      scrollTrigger: { trigger: ".hero", start: "top top", end: "bottom top", scrub: 0.6 }
    });
    gsap.to("#layer-mid", { y: 70, ease: "none",
      scrollTrigger: { trigger: ".hero", start: "top top", end: "bottom top", scrub: 0.6 }
    });
    gsap.to("#layer-front", { y: -40, ease: "none",
      scrollTrigger: { trigger: ".hero", start: "top top", end: "bottom top", scrub: 0.6 }
    });
 
    // Rating card gentle float-in
    gsap.fromTo("#rating-card", { y: 60, opacity: 0, rotate: 3 },
      { y: 0, opacity: 1, rotate: 0, duration: 1.1, ease: "power3.out", delay: 0.3 });
 
    // Generic reveal-on-scroll for sections
    gsap.utils.toArray(".reveal").forEach((el) => {
      gsap.fromTo(el, { y: 40, opacity: 0 }, {
        y: 0, opacity: 1, duration: 0.9, ease: "power2.out",
        scrollTrigger: { trigger: el, start: "top 85%" }
      });
    });
 
    // Images expand smoothly on scroll
    gsap.utils.toArray(".parallax-img").forEach((el) => {
      const img = el.querySelector("svg");
      gsap.fromTo(img, { scale: 1.25 }, {
        scale: 1, ease: "none",
        scrollTrigger: {
          trigger: el,
          start: "top bottom",
          end: "bottom top",
          scrub: 0.8
        }
      });
      gsap.fromTo(el, { scale: 0.92, opacity: 0 }, {
        scale: 1, opacity: 1, duration: 1, ease: "power3.out",
        scrollTrigger: { trigger: el, start: "top 90%" }
      });
    });
 
    // Menu card art subtle parallax float
    gsap.utils.toArray(".menu-card .art svg").forEach((svg) => {
      gsap.to(svg, {
        y: -18, ease: "none",
        scrollTrigger: {
          trigger: svg,
          start: "top bottom",
          end: "bottom top",
          scrub: 1
        }
      });
    });
  } else {
    gsap.set(".reveal, .parallax-img", { opacity: 1, y: 0, scale: 1 });
  }
</script>
</body>
</html>
