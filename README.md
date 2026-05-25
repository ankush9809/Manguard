<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Manguard | Your Privacy. Your Protection.</title>
  <meta name="description" content="A premium, privacy-first Manguard website concept for men's protection and responsible intimate wellness." />
  <meta name="theme-color" content="#05070f" />
  <style>
    :root{
      --bg:#05070f;
      --bg-soft:#0b1020;
      --card:#10182d;
      --card-2:#111827;
      --text:#f7f9ff;
      --muted:#adb8ca;
      --line:rgba(255,255,255,.12);
      --red:#e72840;
      --red-dark:#9f1128;
      --silver:#d7dde8;
      --gold:#d8b65c;
      --blue:#6eb6ff;
      --green:#57d68d;
      --shadow:0 24px 80px rgba(0,0,0,.38);
      --radius:28px;
      --container:1180px;
    }

    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background:
        radial-gradient(circle at 12% 4%, rgba(231,40,64,.22), transparent 32rem),
        radial-gradient(circle at 82% 0%, rgba(110,182,255,.12), transparent 30rem),
        linear-gradient(180deg, #05070f 0%, #090d18 42%, #05070f 100%);
      color:var(--text);
      overflow-x:hidden;
    }

    a{color:inherit;text-decoration:none}
    img{max-width:100%;display:block}
    button,input,select,textarea{font:inherit}
    .container{width:min(var(--container), calc(100% - 36px));margin-inline:auto}

    .top-strip{
      background:linear-gradient(90deg, #e72840, #6b1021 45%, #111827);
      color:white;
      font-weight:800;
      font-size:.82rem;
      letter-spacing:.08em;
      text-transform:uppercase;
      text-align:center;
      padding:10px 16px;
    }

    .navbar{
      position:sticky;
      top:0;
      z-index:50;
      backdrop-filter:blur(18px);
      background:rgba(5,7,15,.75);
      border-bottom:1px solid var(--line);
    }

    .nav-inner{
      height:76px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:18px;
    }

    .brand{
      display:flex;
      align-items:center;
      gap:12px;
      font-weight:950;
      letter-spacing:.04em;
      text-transform:uppercase;
      min-width:max-content;
    }

    .brand-mark{
      width:44px;
      height:44px;
      display:grid;
      place-items:center;
      border-radius:16px;
      background:linear-gradient(135deg, #e72840, #4c0715);
      box-shadow:0 12px 32px rgba(231,40,64,.35);
      border:1px solid rgba(255,255,255,.16);
      font-size:1.4rem;
    }

    .brand small{
      display:block;
      color:var(--muted);
      font-size:.62rem;
      letter-spacing:.16em;
      margin-top:2px;
      font-weight:800;
    }

    .nav-links{
      display:flex;
      align-items:center;
      gap:24px;
      color:rgba(255,255,255,.82);
      font-weight:700;
      font-size:.94rem;
    }

    .nav-links a:hover{color:white}
    .nav-actions{display:flex;align-items:center;gap:12px}
    .icon-btn{
      width:44px;height:44px;border-radius:16px;border:1px solid var(--line);
      background:rgba(255,255,255,.06);color:white;display:grid;place-items:center;cursor:pointer;
    }
    .menu-btn{display:none}

    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
      border:0;
      border-radius:999px;
      padding:14px 22px;
      cursor:pointer;
      font-weight:900;
      transition:.24s ease;
      white-space:nowrap;
    }

    .btn-primary{
      color:white;
      background:linear-gradient(135deg, var(--red), var(--red-dark));
      box-shadow:0 18px 38px rgba(231,40,64,.34);
    }
    .btn-primary:hover{transform:translateY(-2px);box-shadow:0 24px 54px rgba(231,40,64,.45)}
    .btn-secondary{
      color:white;
      background:rgba(255,255,255,.07);
      border:1px solid rgba(255,255,255,.16);
    }
    .btn-secondary:hover{background:rgba(255,255,255,.12);transform:translateY(-2px)}
    .btn-dark{
      background:#05070f;color:white;border:1px solid rgba(255,255,255,.14);
    }

    .hero{
      position:relative;
      isolation:isolate;
      padding:86px 0 54px;
      min-height:calc(100vh - 116px);
      display:grid;
      align-items:center;
    }

    .hero::before{
      content:"";
      position:absolute;inset:0;
      background:
        linear-gradient(90deg, rgba(5,7,15,.98), rgba(5,7,15,.76), rgba(5,7,15,.3)),
        url('https://manguard.in/wp-content/uploads/2025/08/Manguard-Strawberry-600x600.jpg') right 8% center/520px no-repeat;
      z-index:-2;
      opacity:.42;
      filter:saturate(1.12);
    }
    .hero::after{
      content:"";
      position:absolute;
      width:620px;height:620px;border-radius:50%;
      background:radial-gradient(circle, rgba(231,40,64,.24), transparent 64%);
      right:-190px;top:26px;z-index:-1;
    }

    .hero-grid{
      display:grid;
      grid-template-columns: minmax(0, 1.08fr) minmax(330px, .92fr);
      gap:38px;
      align-items:center;
    }

    .eyebrow{
      display:inline-flex;
      align-items:center;
      gap:10px;
      color:#ffdce2;
      background:rgba(231,40,64,.15);
      border:1px solid rgba(231,40,64,.35);
      border-radius:999px;
      padding:9px 13px;
      font-weight:900;
      text-transform:uppercase;
      letter-spacing:.12em;
      font-size:.74rem;
    }

    .hero h1{
      margin:20px 0 18px;
      font-size:clamp(3.1rem, 8vw, 7.8rem);
      line-height:.88;
      letter-spacing:-.075em;
      max-width:820px;
    }
    .hero h1 span{
      display:block;
      background:linear-gradient(92deg, #fff, #d7dde8 42%, #ff7184 88%);
      -webkit-background-clip:text;
      color:transparent;
    }

    .hero p{
      color:#d8dfeb;
      font-size:clamp(1.05rem, 2vw, 1.34rem);
      line-height:1.72;
      max-width:670px;
      margin:0 0 26px;
    }

    .hero-actions{display:flex;gap:14px;flex-wrap:wrap;margin-bottom:30px}

    .micro-trust{
      display:grid;
      grid-template-columns:repeat(3, minmax(0,1fr));
      gap:12px;
      max-width:760px;
    }

    .micro{
      padding:16px;
      border:1px solid var(--line);
      border-radius:22px;
      background:rgba(255,255,255,.055);
      backdrop-filter:blur(14px);
      min-height:108px;
    }
    .micro strong{display:block;font-size:1rem}
    .micro span{display:block;margin-top:6px;color:var(--muted);font-size:.88rem;line-height:1.45}

    .product-stage{
      position:relative;
      border-radius:36px;
      padding:24px;
      background:linear-gradient(180deg, rgba(255,255,255,.13), rgba(255,255,255,.04));
      border:1px solid rgba(255,255,255,.18);
      box-shadow:var(--shadow);
      overflow:hidden;
    }
    .product-stage::before{
      content:"";
      position:absolute;inset:-1px;
      background:
        radial-gradient(circle at 72% 10%, rgba(231,40,64,.35), transparent 26rem),
        radial-gradient(circle at 12% 82%, rgba(110,182,255,.16), transparent 22rem);
      z-index:-1;
    }
    .product-stage img{
      width:100%;
      aspect-ratio:1/1;
      object-fit:contain;
      transform:rotate(-2deg);
      filter:drop-shadow(0 30px 55px rgba(0,0,0,.42));
    }
    .stage-badge{
      position:absolute;
      top:22px;right:22px;
      background:rgba(0,0,0,.48);
      border:1px solid rgba(255,255,255,.2);
      border-radius:999px;
      padding:10px 13px;
      font-size:.82rem;
      font-weight:900;
    }
    .stage-card{
      position:absolute;
      left:22px;bottom:22px;
      max-width:260px;
      padding:16px;
      border-radius:22px;
      background:rgba(5,7,15,.76);
      border:1px solid rgba(255,255,255,.16);
      backdrop-filter:blur(12px);
    }
    .stage-card h3{margin:0 0 6px;font-size:1.05rem}
    .stage-card p{margin:0;color:var(--muted);font-size:.9rem;line-height:1.45}

    section{padding:84px 0}
    .section-head{
      display:flex;
      align-items:end;
      justify-content:space-between;
      gap:24px;
      margin-bottom:32px;
    }
    .section-head h2{
      margin:0;
      font-size:clamp(2rem,4vw,4.2rem);
      line-height:.98;
      letter-spacing:-.055em;
    }
    .section-head p{
      margin:0;
      max-width:520px;
      color:var(--muted);
      line-height:1.7;
    }

    .trust-band{
      margin-top:-12px;
      position:relative;
      z-index:3;
    }
    .trust-grid{
      display:grid;
      grid-template-columns:repeat(5,1fr);
      border:1px solid var(--line);
      background:rgba(255,255,255,.065);
      backdrop-filter:blur(18px);
      border-radius:26px;
      overflow:hidden;
      box-shadow:var(--shadow);
    }
    .trust-item{
      padding:22px 18px;
      border-right:1px solid var(--line);
    }
    .trust-item:last-child{border-right:0}
    .trust-item .ico{font-size:1.4rem}
    .trust-item strong{display:block;margin:8px 0 4px}
    .trust-item span{display:block;color:var(--muted);font-size:.86rem;line-height:1.4}

    .stat-grid{
      display:grid;
      grid-template-columns:1fr 1.5fr 1fr;
      gap:18px;
    }
    .stat-card{
      border-radius:var(--radius);
      background:linear-gradient(180deg, rgba(255,255,255,.09), rgba(255,255,255,.035));
      border:1px solid var(--line);
      padding:28px;
      overflow:hidden;
      position:relative;
    }
    .stat-card.big{
      min-height:310px;
      display:flex;
      flex-direction:column;
      justify-content:space-between;
      background:
        radial-gradient(circle at 70% 10%, rgba(231,40,64,.28), transparent 22rem),
        linear-gradient(180deg, rgba(255,255,255,.1), rgba(255,255,255,.035));
    }
    .stat-number{
      font-size:clamp(2.8rem, 7vw, 6.2rem);
      line-height:.86;
      letter-spacing:-.07em;
      font-weight:950;
    }
    .stat-card p{margin:12px 0 0;color:var(--muted);line-height:1.55}
    .stat-card h3{margin:0 0 10px;font-size:1.15rem}

    .filters{
      display:flex;
      flex-wrap:wrap;
      gap:10px;
      margin-bottom:22px;
    }
    .filter-btn{
      border:1px solid var(--line);
      background:rgba(255,255,255,.06);
      color:white;
      border-radius:999px;
      padding:10px 16px;
      font-weight:850;
      cursor:pointer;
      transition:.2s ease;
    }
    .filter-btn.active,.filter-btn:hover{background:var(--red);border-color:var(--red)}
    .product-grid{
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:18px;
    }
    .product-card{
      position:relative;
      border:1px solid var(--line);
      background:linear-gradient(180deg, rgba(255,255,255,.09), rgba(255,255,255,.035));
      border-radius:28px;
      padding:18px;
      overflow:hidden;
      box-shadow:0 16px 54px rgba(0,0,0,.22);
      transition:.24s ease;
    }
    .product-card:hover{transform:translateY(-7px);border-color:rgba(231,40,64,.52)}
    .product-media{
      height:230px;
      border-radius:22px;
      background:
        radial-gradient(circle at center, rgba(255,255,255,.18), transparent 60%),
        linear-gradient(135deg, rgba(231,40,64,.24), rgba(110,182,255,.08));
      display:grid;
      place-items:center;
      overflow:hidden;
      margin-bottom:16px;
      position:relative;
    }
    .product-media img{width:100%;height:100%;object-fit:contain;padding:8px}
    .placeholder-pack{
      width:78%;
      min-height:150px;
      border-radius:20px;
      background:linear-gradient(135deg, #141414, #2c0a13 52%, #e72840);
      border:1px solid rgba(255,255,255,.18);
      display:grid;
      place-items:center;
      text-align:center;
      padding:18px;
      font-size:1.45rem;
      font-weight:950;
      box-shadow:0 30px 60px rgba(0,0,0,.33);
    }
    .tag{
      display:inline-flex;
      align-items:center;
      border:1px solid rgba(255,255,255,.16);
      background:rgba(255,255,255,.07);
      padding:7px 10px;
      border-radius:999px;
      color:#f3d5d9;
      font-weight:850;
      font-size:.75rem;
    }
    .product-card h3{margin:12px 0 8px;font-size:1.15rem}
    .product-card p{margin:0 0 14px;color:var(--muted);line-height:1.5;font-size:.92rem}
    .price-row{display:flex;align-items:center;justify-content:space-between;gap:12px;margin-top:auto}
    .price strong{font-size:1.25rem}
    .price del{display:block;color:rgba(255,255,255,.45);font-size:.82rem;margin-bottom:2px}
    .add-btn{
      border:0;
      background:rgba(231,40,64,.16);
      color:white;
      border:1px solid rgba(231,40,64,.44);
      border-radius:999px;
      padding:10px 12px;
      font-weight:900;
      cursor:pointer;
    }

    .journey{
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:18px;
      counter-reset:step;
    }
    .journey-card{
      counter-increment:step;
      padding:24px;
      border-radius:var(--radius);
      background:linear-gradient(180deg, rgba(255,255,255,.08), rgba(255,255,255,.035));
      border:1px solid var(--line);
      min-height:230px;
      position:relative;
    }
    .journey-card::before{
      content:"0" counter(step);
      display:inline-grid;
      place-items:center;
      width:46px;height:46px;
      border-radius:16px;
      background:rgba(231,40,64,.2);
      border:1px solid rgba(231,40,64,.4);
      color:#ffdce2;
      font-weight:950;
      margin-bottom:22px;
    }
    .journey-card h3{margin:0 0 10px}
    .journey-card p{margin:0;color:var(--muted);line-height:1.62}

    .split{
      display:grid;
      grid-template-columns: .9fr 1.1fr;
      gap:22px;
      align-items:stretch;
    }
    .panel{
      border-radius:var(--radius);
      background:linear-gradient(180deg, rgba(255,255,255,.09), rgba(255,255,255,.035));
      border:1px solid var(--line);
      padding:30px;
      box-shadow:0 16px 54px rgba(0,0,0,.22);
    }
    .panel h2{margin:0 0 16px;font-size:clamp(2rem,4vw,3.6rem);line-height:.98;letter-spacing:-.05em}
    .panel p{color:var(--muted);line-height:1.75}
    .feature-list{display:grid;gap:12px;margin-top:22px}
    .feature{
      display:grid;
      grid-template-columns:auto 1fr;
      gap:12px;
      align-items:start;
      padding:14px;
      border-radius:18px;
      background:rgba(255,255,255,.05);
      border:1px solid rgba(255,255,255,.09);
    }
    .feature b{display:block}
    .feature span{display:block;color:var(--muted);font-size:.9rem;margin-top:4px;line-height:1.45}

    .blog-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:18px;
    }
    .blog-card{
      border-radius:var(--radius);
      overflow:hidden;
      border:1px solid var(--line);
      background:linear-gradient(180deg, rgba(255,255,255,.09), rgba(255,255,255,.035));
      transition:.24s ease;
    }
    .blog-card:hover{transform:translateY(-6px)}
    .blog-art{
      height:180px;
      display:grid;
      place-items:center;
      background:
        linear-gradient(135deg, rgba(231,40,64,.38), rgba(110,182,255,.12)),
        radial-gradient(circle at 80% 0%, rgba(255,255,255,.18), transparent 18rem);
      font-size:3rem;
    }
    .blog-body{padding:22px}
    .blog-body h3{margin:0 0 10px}
    .blog-body p{margin:0 0 16px;color:var(--muted);line-height:1.55}
    .read-link{color:#ff9aa8;font-weight:900}

    .faq-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:16px;
    }
    .faq{
      border:1px solid var(--line);
      border-radius:22px;
      background:rgba(255,255,255,.055);
      overflow:hidden;
    }
    .faq button{
      width:100%;
      background:none;
      border:0;
      color:white;
      padding:19px 20px;
      text-align:left;
      cursor:pointer;
      display:flex;
      justify-content:space-between;
      gap:16px;
      font-weight:900;
    }
    .faq div{
      display:none;
      padding:0 20px 20px;
      color:var(--muted);
      line-height:1.6;
    }
    .faq.open div{display:block}

    .cta{
      padding:34px;
      border-radius:38px;
      background:
        radial-gradient(circle at 85% 5%, rgba(255,255,255,.22), transparent 22rem),
        linear-gradient(135deg, #e72840, #5a0917 54%, #0b1020);
      display:grid;
      grid-template-columns:1.2fr .8fr;
      gap:24px;
      align-items:center;
      overflow:hidden;
    }
    .cta h2{margin:0;font-size:clamp(2rem,5vw,4.6rem);line-height:.95;letter-spacing:-.06em}
    .cta p{color:#ffdce2;line-height:1.65}
    .cta-card{
      background:rgba(5,7,15,.52);
      border:1px solid rgba(255,255,255,.18);
      border-radius:28px;
      padding:22px;
      backdrop-filter:blur(12px);
    }
    .cta-card input{
      width:100%;
      background:rgba(255,255,255,.09);
      border:1px solid rgba(255,255,255,.16);
      border-radius:16px;
      padding:14px 15px;
      color:white;
      margin-bottom:12px;
      outline:none;
    }

    footer{
      padding:60px 0 24px;
      background:#03050a;
      border-top:1px solid var(--line);
    }
    .footer-grid{
      display:grid;
      grid-template-columns:1.1fr repeat(3,1fr);
      gap:24px;
      margin-bottom:34px;
    }
    .footer-grid h4{margin:0 0 14px}
    .footer-grid a,.footer-grid p{display:block;color:var(--muted);margin:0 0 10px;line-height:1.55}
    .footer-bottom{
      border-top:1px solid var(--line);
      padding-top:18px;
      display:flex;
      justify-content:space-between;
      gap:18px;
      flex-wrap:wrap;
      color:rgba(255,255,255,.55);
      font-size:.86rem;
    }

    .cart-toast{
      position:fixed;
      right:20px;
      bottom:20px;
      z-index:80;
      background:#101827;
      color:white;
      border:1px solid rgba(255,255,255,.16);
      border-radius:20px;
      padding:15px 18px;
      box-shadow:var(--shadow);
      transform:translateY(120px);
      opacity:0;
      transition:.28s ease;
    }
    .cart-toast.show{transform:translateY(0);opacity:1}

    .age-gate{
      position:fixed;
      inset:0;
      z-index:100;
      display:grid;
      place-items:center;
      padding:20px;
      background:rgba(3,5,10,.88);
      backdrop-filter:blur(18px);
    }
    .age-card{
      max-width:520px;
      border-radius:34px;
      padding:30px;
      background:linear-gradient(180deg, rgba(255,255,255,.13), rgba(255,255,255,.06));
      border:1px solid rgba(255,255,255,.18);
      box-shadow:var(--shadow);
      text-align:center;
    }
    .age-card h2{font-size:2.3rem;margin:12px 0 10px;letter-spacing:-.04em}
    .age-card p{color:var(--muted);line-height:1.6}
    .age-actions{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-top:20px}

    @media (max-width: 1040px){
      .nav-links{display:none}
      .menu-btn{display:grid}
      .hero-grid,.split,.cta{grid-template-columns:1fr}
      .hero::before{background:linear-gradient(180deg, rgba(5,7,15,.98), rgba(5,7,15,.72)), url('https://manguard.in/wp-content/uploads/2025/08/Manguard-Strawberry-600x600.jpg') center bottom/460px no-repeat}
      .trust-grid{grid-template-columns:repeat(2,1fr)}
      .trust-item{border-right:0;border-bottom:1px solid var(--line)}
      .product-grid{grid-template-columns:repeat(2,1fr)}
      .journey{grid-template-columns:repeat(2,1fr)}
      .stat-grid{grid-template-columns:1fr}
    }

    @media (max-width: 720px){
      .top-strip{font-size:.68rem}
      .nav-inner{height:68px}
      .brand small{display:none}
      .nav-actions .btn{display:none}
      .hero{padding:54px 0 34px}
      .hero h1{font-size:clamp(3rem, 17vw, 5rem)}
      .micro-trust,.product-grid,.journey,.blog-grid,.faq-grid,.footer-grid,.trust-grid{grid-template-columns:1fr}
      .section-head{display:block}
      .section-head p{margin-top:14px}
      section{padding:56px 0}
      .product-media{height:210px}
      .stage-card{position:static;max-width:none;margin-top:14px}
      .footer-bottom{display:block}
    }
  </style>
</head>
<body>
  <div class="age-gate" id="ageGate" aria-modal="true" role="dialog">
    <div class="age-card">
      <div class="brand" style="justify-content:center;">
        <span class="brand-mark">M</span>
        <span>Manguard <small>Privacy-first wellness</small></span>
      </div>
      <h2>Adults only, 18+</h2>
      <p>This website concept contains sexual wellness products and education. Please continue only if you are 18 years or older.</p>
      <div class="age-actions">
        <button class="btn btn-primary" id="enterSite">I am 18+ — Enter</button>
        <a class="btn btn-secondary" href="https://manguard.in/">Leave</a>
      </div>
    </div>
  </div>

  <div class="top-strip">Discreet packaging • Secure checkout • Responsible intimate care</div>

  <header class="navbar">
    <div class="container nav-inner">
      <a class="brand" href="#home" aria-label="Manguard Home">
        <span class="brand-mark">M</span>
        <span>Manguard <small>Your Privacy. Your Protection.</small></span>
      </a>
      <nav class="nav-links" aria-label="Primary Navigation">
        <a href="#products">Products</a>
        <a href="#privacy">Privacy Journey</a>
        <a href="#education">Talk Protection</a>
        <a href="#faq">FAQs</a>
        <a href="#contact">Contact</a>
      </nav>
      <div class="nav-actions">
        <button class="icon-btn menu-btn" id="menuBtn" aria-label="Open menu">☰</button>
        <button class="icon-btn" aria-label="Cart">🛒 <span id="cartCount">0</span></button>
        <a class="btn btn-primary" href="#products">Shop Now</a>
      </div>
    </div>
  </header>

  <main id="home">
    <section class="hero">
      <div class="container hero-grid">
        <div>
          <span class="eyebrow">Modern men’s protection</span>
          <h1><span>Your Privacy.</span><span>Your Protection.</span></h1>
          <p>Discreet, safe and responsible men’s intimate care delivered privately. Manguard is built for modern Indian buyers who want confidence without awkwardness.</p>
          <div class="hero-actions">
            <a href="#products" class="btn btn-primary">Explore Products →</a>
            <a href="#privacy" class="btn btn-secondary">See Privacy Promise</a>
          </div>
          <div class="micro-trust" aria-label="Manguard Trust Benefits">
            <div class="micro"><strong>Plain Packaging</strong><span>No loud labels. No awkward delivery moments.</span></div>
            <div class="micro"><strong>Quality Tested</strong><span>Skin-safe, reliable protection-focused product communication.</span></div>
            <div class="micro"><strong>Buyer Support</strong><span>Private help through website, WhatsApp and customer care.</span></div>
          </div>
        </div>

        <aside class="product-stage" aria-label="Featured product">
          <span class="stage-badge">Featured Pack</span>
          <img src="https://manguard.in/wp-content/uploads/2025/08/Manguard-Strawberry-600x600.jpg" alt="Manguard Strawberry Condoms Pack" />
          <div class="stage-card">
            <h3>Strawberry Dotted</h3>
            <p>Premium flavoured protection with a privacy-first shopping experience.</p>
          </div>
        </aside>
      </div>
    </section>

    <div class="trust-band">
      <div class="container">
        <div class="trust-grid">
          <div class="trust-item"><span class="ico">📦</span><strong>Discreet Delivery</strong><span>Plain outer packaging for privacy.</span></div>
          <div class="trust-item"><span class="ico">🔒</span><strong>Secure Checkout</strong><span>Designed for safe online ordering.</span></div>
          <div class="trust-item"><span class="ico">✅</span><strong>Quality Promise</strong><span>Clear product details and safety-first copy.</span></div>
          <div class="trust-item"><span class="ico">💬</span><strong>Private Support</strong><span>Confidential help and reorder guidance.</span></div>
          <div class="trust-item"><span class="ico">🧾</span><strong>Responsible Wellness</strong><span>Prescription products require medical guidance.</span></div>
        </div>
      </div>
    </div>

    <section aria-label="Manguard highlights">
      <div class="container">
        <div class="stat-grid">
          <div class="stat-card">
            <h3>Built for privacy</h3>
            <p>Every major purchase step highlights discreet packaging, secure checkout and responsible support.</p>
          </div>
          <div class="stat-card big">
            <div>
              <span class="eyebrow">Brand direction</span>
              <div class="stat-number">Safe.<br>Private.<br>Ready.</div>
            </div>
            <p>A sharper, premium website system for Manguard’s D2C growth, inspired by strong category UX but built around its own privacy-first positioning.</p>
          </div>
          <div class="stat-card">
            <h3>Made for modern buyers</h3>
            <p>Young men, couples, pharmacy customers and privacy-conscious online buyers get a cleaner journey.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="products">
      <div class="container">
        <div class="section-head">
          <h2>How do you want to stay protected?</h2>
          <p>A product-led section inspired by leading condom brand pages, redesigned for Manguard with a mature privacy-first tone and simple comparison.</p>
        </div>

        <div class="filters" aria-label="Product filters">
          <button class="filter-btn active" data-filter="all">All</button>
          <button class="filter-btn" data-filter="flavour">Flavours</button>
          <button class="filter-btn" data-filter="comfort">Comfort</button>
          <button class="filter-btn" data-filter="bundle">Bundles</button>
          <button class="filter-btn" data-filter="prescription">Medical Guidance</button>
        </div>

        <div class="product-grid">
          <article class="product-card" data-category="flavour comfort">
            <div class="product-media">
              <img src="https://manguard.in/wp-content/uploads/2025/08/Manguard-Strawberry-600x600.jpg" alt="Manguard Strawberry Condoms" />
            </div>
            <span class="tag">Flavoured • Dotted</span>
            <h3>Manguard Strawberry Condoms</h3>
            <p>Pack of 6. Fruity experience with reliable protection, comfort and discreet delivery.</p>
            <div class="price-row">
              <div class="price"><del>₹204</del><strong>₹160</strong></div>
              <button class="add-btn" data-product="Strawberry Condoms">Add</button>
            </div>
          </article>

          <article class="product-card" data-category="flavour comfort">
            <div class="product-media">
              <img src="https://manguard.in/wp-content/uploads/2025/08/Manguard-Chocolate-600x600.jpg" alt="Manguard Chocolate Condoms" />
            </div>
            <span class="tag">Flavoured • Smooth</span>
            <h3>Manguard Chocolate Condoms</h3>
            <p>Pack of 6. Rich flavour, ultra-soft latex feel and privacy-safe ordering journey.</p>
            <div class="price-row">
              <div class="price"><del>₹204</del><strong>₹160</strong></div>
              <button class="add-btn" data-product="Chocolate Condoms">Add</button>
            </div>
          </article>

          <article class="product-card" data-category="comfort">
            <div class="product-media">
              <div class="placeholder-pack">Manguard<br>Ultra Thin</div>
            </div>
            <span class="tag">Concept Variant</span>
            <h3>Ultra-Thin Comfort</h3>
            <p>Suggested new SKU for a natural-feel segment. Add lab proof, fit details and safety FAQs.</p>
            <div class="price-row">
              <div class="price"><strong>Coming Soon</strong></div>
              <button class="add-btn" data-product="Ultra-Thin Comfort">Notify</button>
            </div>
          </article>

          <article class="product-card" data-category="bundle">
            <div class="product-media">
              <div class="placeholder-pack">Variety<br>Trial Pack</div>
            </div>
            <span class="tag">Recommended Bundle</span>
            <h3>Discovery Trial Pack</h3>
            <p>Suggested mixed pack: strawberry, chocolate, classic and dotted variants for first-time buyers.</p>
            <div class="price-row">
              <div class="price"><strong>Concept</strong></div>
              <button class="add-btn" data-product="Discovery Trial Pack">Notify</button>
            </div>
          </article>

          <article class="product-card" data-category="bundle comfort">
            <div class="product-media">
              <div class="placeholder-pack">Monthly<br>Protection</div>
            </div>
            <span class="tag">Repeat Purchase</span>
            <h3>Monthly Protection Pack</h3>
            <p>Recommended value pack with reorder reminders and discreet monthly delivery.</p>
            <div class="price-row">
              <div class="price"><strong>Concept</strong></div>
              <button class="add-btn" data-product="Monthly Protection Pack">Notify</button>
            </div>
          </article>

          <article class="product-card" data-category="bundle">
            <div class="product-media">
              <div class="placeholder-pack">Couple<br>Care Kit</div>
            </div>
            <span class="tag">Couple-Safe</span>
            <h3>Couple Care Kit</h3>
            <p>Suggested bundle with protection, privacy card and responsible intimacy education.</p>
            <div class="price-row">
              <div class="price"><strong>Concept</strong></div>
              <button class="add-btn" data-product="Couple Care Kit">Notify</button>
            </div>
          </article>

          <article class="product-card" data-category="prescription">
            <div class="product-media">
              <div class="placeholder-pack">Doctor<br>Guidance</div>
            </div>
            <span class="tag">Prescription Required</span>
            <h3>Men’s Wellness Consultation</h3>
            <p>Prescription-related products should use medical guidance, verification and conservative claims.</p>
            <div class="price-row">
              <div class="price"><strong>Safety First</strong></div>
              <button class="add-btn" data-product="Wellness Consultation">Learn</button>
            </div>
          </article>

          <article class="product-card" data-category="flavour">
            <div class="product-media">
              <div class="placeholder-pack">Manguard<br>Flavour Range</div>
            </div>
            <span class="tag">Future Range</span>
            <h3>Banana / Vanilla Range</h3>
            <p>Keep flavour naming simple, tasteful and supported by clear fit, safety and storage details.</p>
            <div class="price-row">
              <div class="price"><strong>Coming Soon</strong></div>
              <button class="add-btn" data-product="Flavour Range">Notify</button>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="privacy">
      <div class="container">
        <div class="section-head">
          <h2>Your private buying journey.</h2>
          <p>Each step reduces hesitation: clear product details, privacy reassurance, safe checkout, and confidential support.</p>
        </div>

        <div class="journey">
          <div class="journey-card">
            <h3>Choose privately</h3>
            <p>Browse products by benefit: flavour, comfort, texture, value pack or medical guidance.</p>
          </div>
          <div class="journey-card">
            <h3>Understand clearly</h3>
            <p>Product pages explain material, expiry, storage, usage, delivery and FAQs without awkward wording.</p>
          </div>
          <div class="journey-card">
            <h3>Checkout securely</h3>
            <p>Privacy reminders before payment: plain packaging, discreet billing and customer support.</p>
          </div>
          <div class="journey-card">
            <h3>Reorder easily</h3>
            <p>Monthly pack and WhatsApp reorder nudges improve repeat purchase without pressure.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="proof">
      <div class="container split">
        <div class="panel">
          <span class="eyebrow">Why Manguard</span>
          <h2>Premium trust without loud branding.</h2>
          <p>Manguard should not look like a generic product website. It should look private, modern, proof-led and conversion-ready.</p>
          <div class="feature-list">
            <div class="feature"><span>🔐</span><div><b>Privacy-first UX</b><span>Discreet delivery appears in hero, product cards, checkout and FAQs.</span></div></div>
            <div class="feature"><span>🧪</span><div><b>Quality proof area</b><span>Space for ISO, dermatology, batch, expiry and parent-company credentials.</span></div></div>
            <div class="feature"><span>⭐</span><div><b>Review-ready layout</b><span>Verified reviews, ratings and product FAQs improve buyer trust.</span></div></div>
          </div>
        </div>

        <div class="panel">
          <span class="eyebrow">Website modules</span>
          <h2>Sections included.</h2>
          <div class="feature-list">
            <div class="feature"><span>01</span><div><b>Hero + CTA</b><span>Strong first impression with product image and privacy promise.</span></div></div>
            <div class="feature"><span>02</span><div><b>Product Range</b><span>Filterable product cards inspired by category-leading product architecture.</span></div></div>
            <div class="feature"><span>03</span><div><b>Education Hub</b><span>Blogs for safe usage, privacy buying guide and myths.</span></div></div>
            <div class="feature"><span>04</span><div><b>Compliance Notice</b><span>Prescription-related product guidance separated from condom marketing.</span></div></div>
          </div>
        </div>
      </div>
    </section>

    <section id="education">
      <div class="container">
        <div class="section-head">
          <h2>Talk Protection.</h2>
          <p>An education-first content section that builds trust before selling. Mature, respectful and SEO-friendly.</p>
        </div>

        <div class="blog-grid">
          <article class="blog-card">
            <div class="blog-art">🛡️</div>
            <div class="blog-body">
              <h3>How to choose the right condom</h3>
              <p>A clear guide on fit, material, texture, storage and expiry for safe intimacy.</p>
              <a href="#" class="read-link">Read guide →</a>
            </div>
          </article>
          <article class="blog-card">
            <div class="blog-art">📦</div>
            <div class="blog-body">
              <h3>Why discreet delivery matters</h3>
              <p>Privacy-safe buying can make wellness purchases less stressful and more responsible.</p>
              <a href="#" class="read-link">Read guide →</a>
            </div>
          </article>
          <article class="blog-card">
            <div class="blog-art">💬</div>
            <div class="blog-body">
              <h3>Protection is care, not awkwardness</h3>
              <p>How couples can discuss comfort, consent and protection with confidence.</p>
              <a href="#" class="read-link">Read guide →</a>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="faq">
      <div class="container">
        <div class="section-head">
          <h2>Questions buyers ask privately.</h2>
          <p>FAQs reduce hesitation and improve conversion, especially in a sensitive wellness category.</p>
        </div>

        <div class="faq-grid">
          <div class="faq open">
            <button type="button">Will my order be packed discreetly? <span>−</span></button>
            <div>Yes. The website should clearly promise plain, unbranded outer packaging and privacy-safe delivery communication.</div>
          </div>
          <div class="faq">
            <button type="button">Are condoms 100% protective? <span>+</span></button>
            <div>No method is 100% effective. Condoms reduce risk when used correctly. Always check expiry, storage instructions and usage guidance.</div>
          </div>
          <div class="faq">
            <button type="button">Can Manguard sell prescription products online? <span>+</span></button>
            <div>Prescription-related products should use doctor consultation guidance, prescription verification and conservative medical language before purchase.</div>
          </div>
          <div class="faq">
            <button type="button">What should be added to product pages? <span>+</span></button>
            <div>Material, pack size, flavour, texture, expiry, storage, safety instructions, FAQs, verified reviews and trust proof.</div>
          </div>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="cta">
          <div>
            <span class="eyebrow">Manguard D2C funnel</span>
            <h2>Order privately. Stay protected responsibly.</h2>
            <p>Use this section for WhatsApp ordering, newsletter signup, monthly protection reminders and distributor inquiries.</p>
          </div>
          <form class="cta-card" onsubmit="event.preventDefault(); showToast('Thank you! We will contact you privately.');">
            <input type="text" placeholder="Your name" aria-label="Your name" required>
            <input type="tel" placeholder="WhatsApp number" aria-label="WhatsApp number" required>
            <button class="btn btn-primary" type="submit" style="width:100%;">Request Private Support</button>
          </form>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <div class="footer-grid">
        <div>
          <a class="brand" href="#home">
            <span class="brand-mark">M</span>
            <span>Manguard <small>Privacy-first wellness</small></span>
          </a>
          <p style="margin-top:16px;">A premium website concept for safe, private and responsible men’s intimate care.</p>
        </div>
        <div>
          <h4>Shop</h4>
          <a href="#products">Condoms</a>
          <a href="#products">Bundles</a>
          <a href="#products">Monthly Packs</a>
          <a href="#products">Medical Guidance</a>
        </div>
        <div>
          <h4>Learn</h4>
          <a href="#education">Protection Guide</a>
          <a href="#education">Privacy Buying</a>
          <a href="#faq">FAQs</a>
          <a href="#proof">Quality Proof</a>
        </div>
        <div>
          <h4>Company</h4>
          <a href="https://manguard.in/about-us/">About Manguard</a>
          <a href="https://manguard.in/contact-us/">Contact</a>
          <a href="https://manguard.in/shop-2/">Official Shop</a>
          <a href="#contact">Distributor Inquiry</a>
        </div>
      </div>

      <div class="footer-bottom">
        <span>© 2026 Manguard website concept. For adults 18+ only.</span>
        <span>Medical disclaimer: prescription-related products require consultation with a registered medical practitioner.</span>
      </div>
    </div>
  </footer>

  <div class="cart-toast" id="toast">Added to cart</div>

  <script>
    const ageGate = document.getElementById('ageGate');
    const enterSite = document.getElementById('enterSite');
    const cartCount = document.getElementById('cartCount');
    const toast = document.getElementById('toast');
    let cart = 0;

    if(localStorage.getItem('manguardAgeOk') === 'yes'){
      ageGate.style.display = 'none';
    }

    enterSite?.addEventListener('click', () => {
      localStorage.setItem('manguardAgeOk', 'yes');
      ageGate.style.display = 'none';
    });

    function showToast(message){
      toast.textContent = message;
      toast.classList.add('show');
      setTimeout(() => toast.classList.remove('show'), 2400);
    }

    document.querySelectorAll('.add-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        cart++;
        cartCount.textContent = cart;
        showToast(btn.dataset.product + ' added / selected');
      });
    });

    document.querySelectorAll('.filter-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        const filter = btn.dataset.filter;
        document.querySelectorAll('.product-card').forEach(card => {
          const show = filter === 'all' || card.dataset.category.includes(filter);
          card.style.display = show ? 'block' : 'none';
        });
      });
    });

    document.querySelectorAll('.faq button').forEach(button => {
      button.addEventListener('click', () => {
        const faq = button.parentElement;
        const isOpen = faq.classList.contains('open');
        document.querySelectorAll('.faq').forEach(item => {
          item.classList.remove('open');
          item.querySelector('span').textContent = '+';
        });
        if(!isOpen){
          faq.classList.add('open');
          button.querySelector('span').textContent = '−';
        }
      });
    });

    document.getElementById('menuBtn')?.addEventListener('click', () => {
      const links = document.querySelector('.nav-links');
      if(links.style.display === 'flex'){
        links.style.display = '';
      } else {
        links.style.display = 'flex';
        links.style.position = 'absolute';
        links.style.top = '68px';
        links.style.left = '18px';
        links.style.right = '18px';
        links.style.flexDirection = 'column';
        links.style.alignItems = 'stretch';
        links.style.padding = '18px';
        links.style.background = 'rgba(5,7,15,.96)';
        links.style.border = '1px solid rgba(255,255,255,.14)';
        links.style.borderRadius = '22px';
      }
    });
  </script>
</body>
</html>
