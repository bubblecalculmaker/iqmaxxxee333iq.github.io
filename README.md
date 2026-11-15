<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ателье — дизайн и разработка</title>
<meta name="description" content="Ателье — дизайн-студия в Москве. Лендинги, корпоративные сайты и интернет-магазины. Цены от 90 000 ₽.">
<meta name="theme-color" content="#0f0f10">
<meta property="og:type" content="website">
<meta property="og:title" content="Ателье — дизайн и разработка">
<meta property="og:description" content="Делаем сайты, которые продают за вас.">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Crect width='32' height='32' rx='8' fill='%230f0f10'/%3E%3Ccircle cx='16' cy='16' r='6' fill='%23e8ff6a'/%3E%3C/svg%3E">
<script>try{var t=localStorage.getItem('theme');if(t)document.documentElement.dataset.theme=t}catch(e){}</script>
<noscript><style>.reveal{opacity:1}
  </style></noscript>
<style>
  :root{
    --bg:#0f0f10; --surface:#17181a; --surface2:#1e1f22;
    --text:#f2f2f0; --muted:#a2a3a7; --line:#2a2b2f;
    --accent:#e8ff6a; --radius:16px; --on-accent:#111; --line2:#3a3b40; --hdr:rgba(15,15,16,.8); color-scheme:dark;
  }
  *{margin:0;padding:0;box-sizing:border-box}
  html{scroll-behavior:smooth;scroll-padding-top:80px}
  body{
    font-family:system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;
    background:var(--bg); color:var(--text);
    line-height:1.6; -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  .container{max-width:1120px;margin:0 auto;padding:0 24px}

  /* ===== Вход: всё проявляется по очереди ===== */
  @keyframes fadeUp{from{opacity:0;transform:translateY(28px)}to{opacity:1;transform:translateY(0)}}
  @keyframes fadeIn{from{opacity:0}to{opacity:1}}
  @keyframes grow{from{transform:scaleX(0)}to{transform:scaleX(1)}}

  /* Шапка */
  header{
    position:sticky;top:0;z-index:10;
    background:var(--hdr);-webkit-backdrop-filter:blur(12px);backdrop-filter:blur(12px);
    border-bottom:1px solid var(--line);
    animation:fadeIn .6s ease both;
  }
  .nav{display:flex;align-items:center;justify-content:space-between;height:64px}
  .logo{font-weight:700;font-size:20px;letter-spacing:.5px}
  .logo span{color:var(--accent)}
  .nav-links{display:flex;gap:32px;list-style:none}
  .nav-links a{
    color:var(--muted);text-decoration:none;font-size:15px;
    position:relative;transition:color .2s;
  }
  .nav-links a::after{
    content:"";position:absolute;left:0;bottom:-6px;height:2px;width:100%;
    background:var(--accent);border-radius:2px;
    transform:scaleX(0);transform-origin:left;transition:transform .25s ease;
  }
  .nav-links a:hover{color:var(--text)}
  .nav-links a:hover::after{transform:scaleX(1)}
  .btn{
    display:inline-block;padding:12px 24px;border-radius:999px;
    font-weight:600;font-size:15px;text-decoration:none;cursor:pointer;border:none;
    transition:transform .15s, box-shadow .15s, background .2s;
  }
  .btn-accent{background:var(--accent);color:var(--on-accent)}
  .btn-accent:hover{transform:translateY(-2px);box-shadow:0 8px 24px rgba(232,255,106,.25)}
  .btn-ghost{background:transparent;color:var(--text);border:1px solid var(--line)}
  .btn-ghost:hover{border-color:var(--muted)}

  /* Герой */
  .hero{padding:120px 0 96px;position:relative;overflow:hidden}
  .hero::after{
    content:"";position:absolute;inset:auto -10% -40% -10%;height:70%;
    background:radial-gradient(ellipse at center,rgba(232,255,106,.12),transparent 65%);
    pointer-events:none;
    animation:pulse 6s ease-in-out infinite alternate;
  }
  @keyframes pulse{from{opacity:.6}to{opacity:1}}
  .tag{
    display:inline-block;font-size:13px;color:var(--accent);
    border:1px solid rgba(232,255,106,.35);border-radius:999px;
    padding:6px 14px;margin-bottom:24px;
    animation:fadeUp .7s .15s ease both;
  }
  h1{
    font-size:clamp(40px,6vw,72px);line-height:1.05;font-weight:800;
    letter-spacing:-1px;max-width:800px;
    animation:fadeUp .7s .3s ease both;
  }
  h1 em{font-style:normal;color:var(--accent)}
  /* подчёркивание под акцентным словом */
  h1 em{position:relative;white-space:nowrap}
  h1 em::after{
    content:"";position:absolute;left:0;right:0;bottom:4px;height:.12em;
    background:var(--accent);border-radius:4px;opacity:.35;
    transform:scaleX(0);transform-origin:left;
    animation:grow .8s .9s ease forwards;
  }
  .hero p{
    margin:24px 0 40px;font-size:19px;color:var(--muted);max-width:560px;
    animation:fadeUp .7s .45s ease both;
  }
  .hero-actions{display:flex;gap:16px;flex-wrap:wrap;animation:fadeUp .7s .6s ease both}

  /* Появление при скролле */
  .reveal{opacity:0}
  .reveal.visible{opacity:1;animation:fadeUp .7s var(--d,0s) ease backwards}
  .reveal-d1{--d:.1s}
  .reveal-d2{--d:.2s}
  .reveal-d3{--d:.3s}

  /* Секции */
  section{padding:96px 0}
  .section-title{font-size:clamp(28px,4vw,44px);font-weight:700;letter-spacing:-.5px;margin-bottom:16px}
  .section-sub{color:var(--muted);max-width:520px;margin-bottom:56px}

  .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:24px}
  .card{
    background:var(--surface);border:1px solid var(--line);
    border-radius:var(--radius);padding:32px;
    transition:transform .25s,border-color .25s,box-shadow .25s;
  }
  .card:hover{
    transform:translateY(-6px);border-color:var(--line2);
    box-shadow:0 16px 40px rgba(0,0,0,.35);
  }
  .card .num{font-size:14px;color:var(--accent);font-weight:600;margin-bottom:40px}
  .card h3{font-size:20px;margin-bottom:12px}
  .card p{color:var(--muted);font-size:15px}

  /* Портфолио */
  .grid-2{display:grid;grid-template-columns:repeat(2,1fr);gap:24px}
  .work{
    border-radius:var(--radius);overflow:hidden;border:1px solid var(--line);
    aspect-ratio:16/10;position:relative;background:var(--surface2);
    display:flex;align-items:flex-end;padding:32px;cursor:pointer;
  }
  .work::before{content:"";position:absolute;inset:0;transition:transform .5s ease,opacity .3s;opacity:.85}
  .work:nth-child(1)::before{background:linear-gradient(135deg,#1d2b1f,#3b5d3f)}
  .work:nth-child(2)::before{background:linear-gradient(135deg,#241f33,#524a7a)}
  .work:nth-child(3)::before{background:linear-gradient(135deg,#33241f,#7a5c4a)}
  .work:nth-child(4)::before{background:linear-gradient(135deg,#1f2a33,#3f6b8a)}
  .work:hover::before{transform:scale(1.06);opacity:1}
  .work .info{position:relative;z-index:1;transition:transform .35s ease}
  .work:hover .info{transform:translateY(-6px)}
  .work h3{font-size:22px}
  .work p{color:rgba(255,255,255,.65);font-size:14px}
  /* стрелка, вылетающая при наведении */
  .work .arrow{
    position:absolute;top:24px;right:24px;width:44px;height:44px;z-index:1;
    border-radius:50%;background:rgba(255,255,255,.12);backdrop-filter:blur(6px);
    display:flex;align-items:center;justify-content:center;
    opacity:0;transform:translate(-8px,8px);transition:all .3s ease;
  }
  .work:hover .arrow{opacity:1;transform:translate(0,0)}
  .work .arrow svg{width:18px;height:18px;stroke:#fff}

  /* Цены */
  .price-card{display:flex;flex-direction:column}
  .price{font-size:40px;font-weight:800;letter-spacing:-1px;margin:16px 0 24px}
  .price small{font-size:15px;color:var(--muted);font-weight:400}
  .price-card ul{list-style:none;margin-bottom:32px;flex:1}
  .price-card li{
    padding:10px 0;border-bottom:1px solid var(--line);color:var(--muted);
    font-size:15px;transition:color .2s,padding-left .2s;
  }
  .price-card li:hover{color:var(--text);padding-left:6px}
  .price-card li::before{content:"—";color:var(--accent);margin-right:10px}
  .featured{border-color:var(--accent);position:relative;transition:transform .25s,box-shadow .25s}
  .featured:hover{box-shadow:0 16px 48px rgba(232,255,106,.12)}
  .featured::after{
    content:"Популярный";position:absolute;top:-13px;left:32px;
    background:var(--accent);color:var(--on-accent);font-size:12px;font-weight:700;
    padding:4px 12px;border-radius:999px;
    animation:bob 2.5s ease-in-out infinite;
  }
  @keyframes bob{0%,100%{transform:translateY(0)}50%{transform:translateY(-4px)}}

  /* Счётчики */
  .stats{display:grid;grid-template-columns:repeat(4,1fr);gap:24px;margin-top:64px}
  .stat{text-align:center;padding:24px 8px;border:1px solid var(--line);border-radius:var(--radius)}
  .stat b{display:block;font-size:clamp(28px,4vw,44px);font-weight:800;letter-spacing:-1px;color:var(--accent)}
  .stat span{color:var(--muted);font-size:14px}

  /* Контакты */
  .contact{background:var(--surface);border-top:1px solid var(--line);border-bottom:1px solid var(--line);text-align:center}
  .contact h2{font-size:clamp(30px,4.5vw,48px);font-weight:800;letter-spacing:-.5px;margin-bottom:20px}
  .contact p{color:var(--muted);margin-bottom:40px}
  .email{
    font-size:clamp(20px,3vw,32px);font-weight:700;color:var(--accent);
    text-decoration:none;display:inline-block;transition:transform .2s;
  }
  .email:hover{transform:scale(1.04);text-decoration:underline}

  footer{padding:32px 0;color:var(--muted);font-size:14px}
  .footer-inner{display:flex;justify-content:space-between;flex-wrap:wrap;gap:12px}

  @media(max-width:820px){
    .grid,.grid-2,.stats{grid-template-columns:1fr}
    .nav-links{display:none}
    .hero{padding:80px 0 64px}
    section{padding:64px 0}
  }
  /* Уважение к настройке «меньше движения» */
  @media(prefers-reduced-motion:reduce){
    *,*::before,*::after{animation:none!important;transition:none!important}
    .reveal{opacity:1;transform:none}
  }
/* ===== Добавлено ===== */
  :root[data-theme=light]{color-scheme:light;--bg:#fafaf7;--surface:#fff;--surface2:#f0f0ec;--text:#18181a;--muted:#5f6065;--line:#e2e2dd;--line2:#c9c9c2;--accent:#5c6e00;--on-accent:#fff;--hdr:rgba(250,250,247,.85)}
  [data-theme=light] .tag{border-color:rgba(92,110,0,.35)}
  :focus-visible{outline:2px solid var(--accent);outline-offset:3px}
  section + section{padding-top:0}
  .contact{padding-top:96px}
  .nav-links{gap:28px}
  .nav-right{display:flex;align-items:center;gap:12px}
  .icon-btn{width:44px;height:44px;border-radius:50%;border:1px solid var(--line);background:transparent;color:var(--text);font-size:18px;cursor:pointer;transition:border-color .2s}
  .icon-btn:hover{border-color:var(--muted)}
  .burger{display:none}
  .logos-wrap{border-block:1px solid var(--line);padding:32px 0}
  .logos-wrap p{font-size:13px;color:var(--muted);text-align:center;margin-bottom:20px}
  .logos{display:flex;flex-wrap:wrap;justify-content:center;gap:16px 48px}
  .logos span{font-weight:800;font-size:18px;letter-spacing:1px;color:var(--muted);opacity:.75}
  .steps{display:grid;grid-template-columns:repeat(4,1fr);gap:24px}
  .quote p{font-size:16px;color:var(--text);margin-bottom:24px}
  .who b{display:block}
  .who span{color:var(--muted);font-size:14px}
  .team{display:grid;grid-template-columns:repeat(4,1fr);gap:24px}
  .member{text-align:center;padding:28px 16px}
  .ava{width:72px;height:72px;border-radius:50%;margin:0 auto 16px;display:grid;place-items:center;font-weight:700;font-size:22px;color:#fff;background:linear-gradient(135deg,#3b5d3f,#524a7a)}
  .member h3{font-size:17px;margin-bottom:4px}
  .faq{max-width:760px}
  .faq details{border-bottom:1px solid var(--line);padding:20px 0}
  .faq summary{cursor:pointer;font-weight:600;list-style:none;display:flex;justify-content:space-between;gap:16px}
  .faq summary::-webkit-details-marker{display:none}
  .faq summary::after{content:"+";color:var(--accent);font-size:22px;line-height:1;transition:transform .2s}
  .faq details[open] summary::after{transform:rotate(45deg)}
  .faq details p{color:var(--muted);margin-top:12px}
  .channels{display:flex;flex-wrap:wrap;justify-content:center;gap:12px;margin-top:24px}
  .form{display:grid;grid-template-columns:1fr 1fr;gap:16px;max-width:680px;margin:56px auto 0;text-align:left}
  .form .full{grid-column:1/-1}
  .form label{font-size:14px;color:var(--muted)}
  .form input,.form select,.form textarea{display:block;width:100%;margin-top:6px;padding:14px 16px;font:inherit;color:var(--text);background:var(--bg);border:1px solid var(--line);border-radius:12px}
  .form input:focus,.form select:focus,.form textarea:focus{outline:none;border-color:var(--accent)}
  .form textarea{min-height:120px;resize:vertical}
  .form .check{display:flex;gap:10px;align-items:flex-start;font-size:13px}
  .form .check input{width:auto;margin:3px 0 0}
  .form a{color:var(--accent)}
  .form .btn{grid-column:1/-1;justify-self:start}
  #status{color:var(--muted);font-size:14px}
  footer a{color:inherit}
  dialog{background:var(--surface);color:var(--text);border:1px solid var(--line);border-radius:var(--radius);padding:0;max-width:520px;width:calc(100% - 32px)}
  dialog::backdrop{background:rgba(0,0,0,.6)}
  .dlg{padding:32px}
  .dlg h3{font-size:24px;margin-bottom:16px}
  .dlg p{color:var(--muted);margin-bottom:12px}
  .dlg dt{color:var(--accent);font-size:13px;margin-top:16px}
  .dlg dd{color:var(--muted)}
  .dlg .btn{margin-top:24px}
  @media(max-width:820px){
    .burger{display:inline-block}
    .nav-links.open{display:flex;flex-direction:column;position:absolute;top:64px;left:0;right:0;gap:16px;padding:20px 24px 28px;background:var(--bg);border-bottom:1px solid var(--line)}
    .steps,.form{grid-template-columns:1fr}
    .team{grid-template-columns:repeat(2,1fr)}
    .contact{padding-top:64px}
    .form .btn{justify-self:stretch}
  }
  @media(max-width:560px){.nav-right .btn{display:none}}

  /* ===== Телефоны и шрифт ===== */
  html{-webkit-text-size-adjust:100%}
  button,input,select,textarea,dialog{font-family:inherit}
  button{line-height:inherit}
  .btn{text-align:center;touch-action:manipulation}
  .featured:hover{border-color:var(--accent)}
  dialog{max-height:calc(100dvh - 32px);overflow:auto}
  @media(hover:none){
    .card:hover{transform:none;box-shadow:none}
    .work:hover::before{transform:none;opacity:.85}
    .work:hover .info{transform:none}
    .work .arrow{opacity:1;transform:none}
    .btn-accent:hover{transform:none;box-shadow:none}
    .price-card li:hover{padding-left:0}
  }
  @media(max-width:820px){
    .nav-links.open{max-height:calc(100dvh - 64px);overflow:auto;gap:0;padding:8px 24px 24px}
    .nav-links.open a{display:block;padding:14px 0;font-size:18px}
    .nav-links.open a::after{display:none}
    .stats{grid-template-columns:repeat(2,1fr);gap:12px;margin-top:48px}
    .logos{gap:12px 28px}
  }
  @media(max-width:560px){
    .container{padding:0 20px}
    h1{font-size:clamp(34px,10.5vw,48px)}
    .hero{padding:56px 0 48px}
    .hero p{font-size:17px;margin:20px 0 32px}
    .hero-actions .btn{flex:1 1 100%}
    section{padding:56px 0}
    .contact{padding-top:56px}
    .section-sub{margin-bottom:36px}
    .card{padding:24px}
    .card .num{margin-bottom:24px}
    .price{font-size:32px;margin:12px 0 20px}
    .featured::after{left:24px}
    .work{padding:24px}
    .work h3{font-size:20px}
    .work .arrow{top:16px;right:16px}
    .team{gap:12px}
    .member{padding:24px 12px}
    .stat{padding:20px 8px}
    .form{margin-top:40px}
    .form .check{font-size:14px}
    .form .check input{width:20px;height:20px;flex:none}
    .dlg{padding:24px}
  }

  /* ===== Анимации ===== */
  @keyframes pop{from{opacity:0;transform:scale(.85)}}
  @keyframes wipe{from{clip-path:inset(0 100% 0 0);transform:scale(.96)}to{clip-path:inset(0 0 0 0)}}
  @keyframes slideIn{from{opacity:0;transform:translateY(-8px)}}
  @keyframes shimmer{to{background-position:-200% 0}}
  @keyframes drift{from{transform:translate(0,0) scale(1)}to{transform:translate(-40px,30px) scale(1.15)}}
  @keyframes ping{0%{box-shadow:0 0 0 0 color-mix(in srgb,var(--accent) 60%,transparent)}100%{box-shadow:0 0 0 8px transparent}}
  @keyframes ring{0%{box-shadow:0 0 0 0 color-mix(in srgb,var(--accent) 45%,transparent)}70%,100%{box-shadow:0 0 0 14px transparent}}
  @keyframes glow{0%,100%{box-shadow:0 0 0 transparent}50%{box-shadow:0 0 36px color-mix(in srgb,var(--accent) 16%,transparent)}}
  @keyframes marquee{to{transform:translateX(calc(-50% - var(--g)/2))}}
  @keyframes shake{25%{transform:translateX(-5px)}75%{transform:translateX(5px)}}
  @keyframes spin{to{transform:rotate(360deg)}}
  @keyframes dlgIn{from{opacity:0;transform:translateY(16px) scale(.97)}}

  /* прогресс, «наверх», шапка */
  .progress{position:fixed;top:0;left:0;right:0;height:3px;background:var(--accent);transform:scaleX(0);transform-origin:left;z-index:20;pointer-events:none}
  .to-top{position:fixed;right:16px;bottom:calc(16px + env(safe-area-inset-bottom));width:48px;height:48px;border-radius:50%;border:1px solid var(--line);background:var(--surface);color:var(--text);font-size:20px;cursor:pointer;z-index:9;opacity:0;transform:translateY(16px) scale(.8);pointer-events:none;transition:opacity .3s,transform .3s,border-color .2s}
  .to-top.show{opacity:1;transform:none;pointer-events:auto}
  .to-top:hover{border-color:var(--accent)}
  header{transition:box-shadow .3s}
  header.scrolled{box-shadow:0 8px 30px rgba(0,0,0,.25)}
  .nav-links a.active{color:var(--text)}
  .nav-links a.active::after{transform:scaleX(1)}
  .logo span{display:inline-block}
  .logo:hover span{animation:bob .6s ease}
  html.theme-anim *,html.theme-anim *::before,html.theme-anim *::after{transition:background-color .35s,color .35s,border-color .35s!important}
  .icon-btn.spin{animation:spin .5s ease}
  .burger{transition:transform .25s,border-color .2s}
  .burger[aria-expanded=true]{transform:rotate(90deg);border-color:var(--accent)}
  .nav-links.open{animation:slideIn .25s ease}
  .nav-links.open li{animation:slideIn .3s calc(var(--i,0)*.05s) ease backwards}

  /* герой */
  .hero .container{position:relative;z-index:1}
  .hero::before{content:"";position:absolute;inset:0;pointer-events:none;background:radial-gradient(420px circle at var(--hx,70%) var(--hy,30%),color-mix(in srgb,var(--accent) 10%,transparent),transparent 60%)}
  .blob{position:absolute;border-radius:50%;filter:blur(70px);pointer-events:none;animation:drift 14s ease-in-out infinite alternate}
  .b1{width:320px;height:320px;top:6%;right:4%;background:color-mix(in srgb,var(--accent) 22%,transparent)}
  .b2{width:260px;height:260px;bottom:2%;left:32%;background:rgba(124,108,255,.22);animation-duration:18s;animation-delay:-6s}
  .tag::before{content:"";display:inline-block;width:6px;height:6px;margin-right:8px;border-radius:50%;background:var(--accent);vertical-align:middle;animation:ping 2s ease-out infinite}
  h1 em{background:linear-gradient(90deg,var(--accent),var(--text),var(--accent));background-size:200% 100%;-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent;animation:shimmer 5s linear infinite}
  .hero-actions .btn-accent{animation:ring 2.6s 2s infinite}
  .hero-actions .btn-accent:hover{animation:none}

  /* кнопки */
  .btn-accent{position:relative;overflow:hidden}
  .btn-accent::after{content:"";position:absolute;top:0;left:-70%;width:50%;height:100%;background:linear-gradient(100deg,transparent,rgba(255,255,255,.55),transparent);transform:skewX(-20deg);transition:left .6s ease}
  .btn-accent:hover::after{left:130%}
  .btn:active{transform:scale(.97)}

  /* бегущая строка логотипов */
  .logos{--g:48px;display:block;overflow:hidden;text-align:center;-webkit-mask-image:linear-gradient(90deg,transparent,#000 10%,#000 90%,transparent);mask-image:linear-gradient(90deg,transparent,#000 10%,#000 90%,transparent)}
  .logos>span{display:inline-block;margin:6px 14px}
  .logos span{white-space:nowrap}
  .logos-track{display:flex;width:max-content;gap:var(--g);animation:marquee 26s linear infinite}
  .logos:hover .logos-track{animation-play-state:paused}

  /* появление: разные для разных блоков */
  .work.reveal.visible{animation-name:wipe}
  .stat.reveal.visible{animation-name:pop}
  .member.visible .ava{animation:pop .6s calc(var(--d,0s) + .25s) cubic-bezier(.3,1.6,.5,1) backwards}
  .featured.reveal.visible{animation:fadeUp .7s var(--d,0s) ease backwards,glow 4s 1s ease-in-out infinite}
  .card{position:relative;isolation:isolate}
  .card::before{content:"";position:absolute;inset:0;border-radius:inherit;z-index:-1;pointer-events:none;opacity:0;transition:opacity .3s;background:radial-gradient(320px circle at var(--mx,50%) var(--my,50%),color-mix(in srgb,var(--accent) 12%,transparent),transparent 60%)}
  .card:hover::before{opacity:1}
  .steps .card::after{content:"";position:absolute;left:24px;right:24px;top:-1px;height:2px;background:var(--accent);transform:scaleX(0);transform-origin:left}
  .steps .card.visible::after{animation:grow .9s .3s ease forwards}
  .work{transition:transform .25s ease}
  .faq details[open] p{animation:slideIn .35s ease}

  /* форма, окна */
  .form input,.form select,.form textarea{transition:border-color .2s,box-shadow .2s}
  .form input:focus,.form select:focus,.form textarea:focus{box-shadow:0 0 0 3px color-mix(in srgb,var(--accent) 25%,transparent)}
  .form :user-invalid{border-color:#ff6b6b;animation:shake .35s}
  #status:not(:empty){animation:fadeUp .4s ease}
  dialog[open]{animation:dlgIn .28s ease}
  dialog[open]::backdrop{animation:fadeIn .28s ease}
  .contact{position:relative;overflow:hidden}
  .contact .container{position:relative}
  .contact::before{content:"";position:absolute;inset:-30% 10% auto 10%;height:80%;pointer-events:none;background:radial-gradient(ellipse at center,color-mix(in srgb,var(--accent) 10%,transparent),transparent 65%);animation:pulse 6s ease-in-out infinite alternate}
  @media(hover:none){.card:hover::before{opacity:0}}
  @media(max-width:820px){.logos{--g:28px}}
  @media(max-width:560px){.blob{filter:blur(50px)}.b1{width:200px;height:200px}.b2{width:170px;height:170px}}
  .form .note{font-size:13px;color:var(--muted)}

  /* ===== Cookie ===== */
  .cookie{position:fixed;left:16px;bottom:calc(16px + env(safe-area-inset-bottom));max-width:440px;z-index:30;padding:20px;background:var(--surface);border:1px solid var(--line);border-radius:var(--radius);box-shadow:0 16px 48px rgba(0,0,0,.35);animation:fadeUp .5s ease both}
  .cookie p{font-size:14px;color:var(--muted);margin-bottom:16px}
  .cookie a{color:var(--accent)}
  .cookie-actions{display:flex;gap:10px}
  .cookie .btn{flex:1;padding:12px 16px;font-size:14px}
  @media(max-width:560px){.cookie{left:12px;right:12px;max-width:none;bottom:calc(12px + env(safe-area-inset-bottom))}}
</style>
</head>
<body>
<div class="progress" id="progress"></div>

<header>
  <div class="container nav">
    <div class="logo">ателье<span>.</span></div>
    <nav aria-label="Основная навигация"><ul class="nav-links" id="menu">
      <li><a href="#services">Услуги</a></li>
      <li><a href="#work">Работы</a></li>
      <li><a href="#process">Процесс</a></li>
      <li><a href="#pricing">Цены</a></li>
      <li><a href="#faq">FAQ</a></li>
      <li><a href="#contact">Контакты</a></li>
    </ul></nav>
    <div class="nav-right">
      <button class="icon-btn" id="theme" type="button" aria-label="Сменить тему">◐</button>
      <a href="#contact" class="btn btn-accent">Обсудить проект</a>
      <button class="icon-btn burger" id="burger" type="button" aria-label="Меню" aria-expanded="false" aria-controls="menu">☰</button>
    </div>
  </div>
</header>

<div class="hero">
  <i class="blob b1"></i><i class="blob b2"></i>
  <div class="container">
    <span class="tag">Дизайн-студия · Москва</span>
    <h1>Делаем сайты, которые <em>продают</em> за вас</h1>
    <p>Проектируем и разрабатываем быстрые, красивые и удобные сайты для бизнеса — от лендинга до интернет-магазина.</p>
    <div class="hero-actions">
      <a href="#contact" class="btn btn-accent">Начать проект</a>
      <a href="#work" class="btn btn-ghost">Смотреть работы</a>
    </div>
  </div>
</div>

<div class="logos-wrap"><div class="container"><p>Нам доверяют</p><div class="logos"><span>Nordwind</span><span>Pixel</span><span>Terra</span><span>Wave</span><span>Kontur</span><span>Lumen</span></div></div></div>

<section id="services">
  <div class="container">
    <h2 class="section-title reveal">Что мы делаем</h2>
    <p class="section-sub reveal reveal-d1">Три направления, в которых мы сильны — и ничего лишнего.</p>
    <div class="grid">
      <div class="card reveal"><div class="num">01</div><h3>Веб-дизайн</h3><p>Интерфейсы, которые нравятся людям и работают на метрики. Исследуем, проектируем, тестируем.</p></div>
      <div class="card reveal reveal-d1"><div class="num">02</div><h3>Разработка</h3><p>Чистый код, скорость загрузки меньше секунды, адаптив под любые устройства.</p></div>
      <div class="card reveal reveal-d2"><div class="num">03</div><h3>Брендинг</h3><p>Логотип, фирменный стиль и айдентика, которые запоминаются и отстраивают от конкурентов.</p></div>
    </div>
    <div class="stats">
      <div class="stat reveal"><b data-count="120" data-suffix="+">120+</b><span>проектов запущено</span></div>
      <div class="stat reveal reveal-d1"><b data-count="9">9</b><span>лет на рынке</span></div>
      <div class="stat reveal reveal-d2"><b data-count="98" data-suffix="%">98%</b><span>довольных клиентов</span></div>
      <div class="stat reveal reveal-d3"><b data-count="14">14</b><span>наград за дизайн</span></div>
    </div>
  </div>
</section>

<section id="work" style="padding-top:0">
  <div class="container">
    <h2 class="section-title reveal">Избранные работы</h2>
    <p class="section-sub reveal reveal-d1">Несколько проектов, которыми мы гордимся.</p>
    <div class="grid-2">
      <div class="work reveal">
        <div class="arrow"><svg fill="none" viewBox="0 0 24 24" stroke-width="2"><path d="M7 17L17 7M9 7h8v8" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="info"><h3>Nordwind Coffee</h3><p>Сеть кофеен — сайт и брендинг</p></div>
      </div>
      <div class="work reveal reveal-d1">
        <div class="arrow"><svg fill="none" viewBox="0 0 24 24" stroke-width="2"><path d="M7 17L17 7M9 7h8v8" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="info"><h3>Pixel Finance</h3><p>Финтех-платформа — интерфейс</p></div>
      </div>
      <div class="work reveal reveal-d1">
        <div class="arrow"><svg fill="none" viewBox="0 0 24 24" stroke-width="2"><path d="M7 17L17 7M9 7h8v8" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="info"><h3>Terra Hotel</h3><p>Отель в горах — бронирование</p></div>
      </div>
      <div class="work reveal reveal-d2">
        <div class="arrow"><svg fill="none" viewBox="0 0 24 24" stroke-width="2"><path d="M7 17L17 7M9 7h8v8" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
        <div class="info"><h3>Wave Store</h3><p>Магазин электроники — e-commerce</p></div>
      </div>
    </div>
  </div>
</section>

<section id="process">
  <div class="container">
    <h2 class="section-title reveal">Как мы работаем</h2>
    <p class="section-sub reveal reveal-d1">Четыре шага от первого разговора до запуска. Вы всегда знаете, на каком мы этапе.</p>
    <div class="steps">
      <div class="card reveal"><div class="num">01 · 1–3 дня</div><h3>Бриф</h3><p>Обсуждаем цели, аудиторию и конкурентов. Фиксируем смету и сроки.</p></div>
      <div class="card reveal reveal-d1"><div class="num">02 · 1–3 недели</div><h3>Дизайн</h3><p>Прототип и макеты. Вы вносите правки до утверждения.</p></div>
      <div class="card reveal reveal-d2"><div class="num">03 · 2–5 недель</div><h3>Разработка</h3><p>Вёрстка, система управления, тесты на разных устройствах.</p></div>
      <div class="card reveal reveal-d3"><div class="num">04 · 1 день</div><h3>Запуск</h3><p>Переносим на ваш хостинг, подключаем аналитику, обучаем команду.</p></div>
    </div>
  </div>
</section>

<section id="pricing" style="padding-top:0">
  <div class="container">
    <h2 class="section-title reveal">Цены</h2>
    <p class="section-sub reveal reveal-d1">Прозрачные пакеты без скрытых доплат.</p>
    <div class="grid">
      <div class="card price-card reveal">
        <h3>Лендинг</h3>
        <div class="price">от 90 000 ₽ <small>/ проект</small></div>
        <ul><li>Дизайн одной страницы</li><li>Адаптив под мобильные</li><li>Базовая SEO-настройка</li><li>Запуск за 2 недели</li></ul>
        <a href="#contact" class="btn btn-ghost">Выбрать</a>
      </div>
      <div class="card price-card featured reveal reveal-d1">
        <h3>Корпоративный сайт</h3>
        <div class="price">от 220 000 ₽ <small>/ проект</small></div>
        <ul><li>До 10 страниц</li><li>Уникальный дизайн</li><li>Система управления</li><li>Поддержка 3 месяца</li></ul>
        <a href="#contact" class="btn btn-accent">Выбрать</a>
      </div>
      <div class="card price-card reveal reveal-d2">
        <h3>Интернет-магазин</h3>
        <div class="price">от 380 000 ₽ <small>/ проект</small></div>
        <ul><li>Каталог и корзина</li><li>Интеграции с оплатой</li><li>Аналитика</li><li>Обучение команде</li></ul>
        <a href="#contact" class="btn btn-ghost">Выбрать</a>
      </div>
    </div>
  </div>
</section>

<section id="reviews">
  <div class="container">
    <h2 class="section-title reveal">Что говорят клиенты</h2>
    <p class="section-sub reveal reveal-d1">Отзывы тех, с кем мы уже запустили проекты.</p>
    <div class="grid">
      <figure class="card quote reveal"><blockquote><p>«Сайт запустили на неделю раньше срока. Онлайн-заказы выросли уже в первый месяц.»</p></blockquote><figcaption class="who"><b>Анна Корнева</b><span>Основатель, Nordwind Coffee</span></figcaption></figure>
      <figure class="card quote reveal reveal-d1"><blockquote><p>«Команда разобралась в нашем продукте глубже, чем мы ожидали. Конверсия в регистрацию выросла на четверть.»</p></blockquote><figcaption class="who"><b>Дмитрий Власов</b><span>Директор по продукту, Pixel Finance</span></figcaption></figure>
      <figure class="card quote reveal reveal-d2"><blockquote><p>«Гости бронируют напрямую, а не через агрегаторы. Комиссии сократились почти вдвое.»</p></blockquote><figcaption class="who"><b>Елена Романова</b><span>Управляющая, Terra Hotel</span></figcaption></figure>
    </div>
  </div>
</section>

<section id="team">
  <div class="container">
    <h2 class="section-title reveal">Команда</h2>
    <p class="section-sub reveal reveal-d1">Те, кто будет работать над вашим проектом каждый день.</p>
    <div class="team">
      <div class="card member reveal"><div class="ava">ИО</div><h3>Илья Орлов</h3><p>Основатель, арт-директор</p></div>
      <div class="card member reveal reveal-d1"><div class="ava">МБ</div><h3>Мария Белова</h3><p>Ведущий дизайнер</p></div>
      <div class="card member reveal reveal-d2"><div class="ava">АЖ</div><h3>Артём Журавлёв</h3><p>Руководитель разработки</p></div>
      <div class="card member reveal reveal-d3"><div class="ava">СК</div><h3>Софья Ким</h3><p>Менеджер проектов</p></div>
    </div>
  </div>
</section>

<section id="faq">
  <div class="container">
    <h2 class="section-title reveal">Частые вопросы</h2>
    <div class="faq reveal">
      <details><summary>Сколько времени занимает проект?</summary><p>Лендинг — около двух недель, корпоративный сайт — 4–8 недель, интернет-магазин — от 8 недель. Точные сроки фиксируем после брифа.</p></details>
      <details><summary>Сколько правок входит в стоимость?</summary><p>Три круга правок на этапе дизайна и один на этапе вёрстки. Дополнительные согласуем отдельно.</p></details>
      <details><summary>Что входит в поддержку?</summary><p>Исправляем ошибки, обновляем систему управления и помогаем с контентом. В корпоративном пакете поддержка включена на 3 месяца, дальше — по абонементу.</p></details>
      <details><summary>Как проходит оплата?</summary><p>50% предоплаты, 50% после запуска. Работаем по договору, выставляем счёт на юрлицо или ИП.</p></details>
      <details><summary>Кому принадлежит сайт после запуска?</summary><p>Вам. Мы передаём исходники, доступы и документацию.</p></details>
    </div>
  </div>
</section>

<section class="contact" id="contact">
  <div class="container">
    <h2 class="reveal">Есть проект? Давайте обсудим.</h2>
    <p class="reveal reveal-d1">Напишите нам — ответим в течение часа в рабочее время.</p>
    <a class="email reveal reveal-d2" href="mailto:hello@atelier.ru">hello@atelier.ru</a>
    <div class="channels"><a class="btn btn-ghost" href="https://t.me/atelier_studio" target="_blank" rel="noopener">Telegram</a><a class="btn btn-ghost" href="tel:+74950000000">+7 (495) 000-00-00</a></div>
    <form class="form" id="form">
      <label>Имя<input name="name" required autocomplete="name"></label>
      <label>Телефон, Telegram или почта<input name="contact" required></label>
      <label>Что нужно<select id="type" name="type"><option>Лендинг</option><option>Корпоративный сайт</option><option>Интернет-магазин</option><option>Дизайн или брендинг</option><option>Другое</option></select></label>
      <label>Бюджет<select name="budget"><option>До 100 000 ₽</option><option>100–250 тыс. ₽</option><option>250–500 тыс. ₽</option><option>От 500 тыс. ₽</option><option>Пока не знаю</option></select></label>
      <label class="full">О задаче<textarea name="msg" rows="4" placeholder="Что хотите сделать и к какому сроку"></textarea></label>
      <label class="full check"><input type="checkbox" required><span>Даю <a href="consent.html" target="_blank" rel="noopener">согласие на обработку персональных данных</a></span></label>
      <div class="full note">Как мы храним и защищаем данные — в <a href="privacy.html" target="_blank" rel="noopener">политике конфиденциальности</a>.</div>
      <button class="btn btn-accent" type="submit">Отправить заявку</button>
      <div class="full" id="status" role="status"></div>
    </form>
  </div>
</section>

<footer>
  <div class="container footer-inner">
    <span>© 2026 Ателье. Все права защищены.</span>
    <span><a href="privacy.html">Политика конфиденциальности</a> · <a href="consent.html">Согласие на обработку данных</a> · <a href="#" id="cookie-settings">Настройки cookie</a> · Сделано с любовью к деталям</span>
  </div>
</footer>

<div class="cookie" id="cookie" role="region" aria-label="Использование cookie" hidden>
  <p>Мы используем cookie «Яндекс Метрики», чтобы понимать, как пользуются сайтом. Они нужны только для аналитики и включаются с вашего согласия. <a href="privacy.html#cookie">Подробнее</a></p>
  <div class="cookie-actions"><button class="btn btn-accent" id="cookie-yes" type="button">Принять</button><button class="btn btn-ghost" id="cookie-no" type="button">Отклонить</button></div>
</div>
<button class="to-top" id="to-top" type="button" aria-label="Наверх">↑</button>
<dialog id="case"><div class="dlg"><h3 id="case-title"></h3><dl id="case-body"></dl><form method="dialog"><button class="btn btn-ghost">Закрыть</button></form></div></dialog>

<script>
  // Появление блоков при скролле
  const observer = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('visible'); observer.unobserve(e.target);} });
  },{threshold:.15});
  document.querySelectorAll('.reveal').forEach(el=>observer.observe(el));

  // Анимированные счётчики
  const counters = document.querySelectorAll('[data-count]');
  const counterObserver = new IntersectionObserver((entries)=>{
    entries.forEach(entry=>{
      if(!entry.isIntersecting) return;
      const el = entry.target, target = +el.dataset.count, dur = 1400, t0 = performance.now();
      (function tick(now){
        const p = Math.min((now-t0)/dur, 1);
        el.textContent = Math.round(target * (1-Math.pow(1-p,3))) + (el.dataset.suffix||""); // easeOutCubic
        if(p<1) requestAnimationFrame(tick);
      })(t0);
      counterObserver.unobserve(el);
    });
  },{threshold:.6});
  counters.forEach(c=>counterObserver.observe(c));

  // ===== Добавлено: тема, меню, кейсы, форма =====
  const $=id=>document.getElementById(id), root=document.documentElement;
  $('theme').onclick=()=>{const t=root.dataset.theme==='light'?'dark':'light';root.dataset.theme=t;try{localStorage.setItem('theme',t)}catch(e){}};

  const menu=$('menu'), burger=$('burger');
  const setMenu=o=>{menu.classList.toggle('open',o);burger.setAttribute('aria-expanded',o);burger.textContent=o?'✕':'☰'};
  burger.onclick=()=>setMenu(!menu.classList.contains('open'));
  menu.querySelectorAll('a').forEach(a=>a.addEventListener('click',()=>setMenu(false)));

  const cases=[
    ['Nordwind Coffee','Единый образ для сети кофеен и сайт с заказом навынос.','Фирменный стиль, дизайн-система, сайт с онлайн-заказом.','Онлайн-заказы выросли на 38% за три месяца.'],
    ['Pixel Finance','Сложная регистрация отпугивала новых пользователей.','Пересобрали сценарии онбординга и библиотеку компонентов.','Конверсия в регистрацию выросла на 27%.'],
    ['Terra Hotel','Гости бронировали через агрегаторы, и отель платил комиссии.','Сайт с календарём цен и бронированием в три шага.','46% броней теперь приходит напрямую.'],
    ['Wave Store','Каталог на 5 000 товаров грузился медленно.','Быстрый каталог, фильтры и оплата в один шаг.','Карточка товара открывается быстрее секунды, конверсия корзины выросла на 19%.']
  ];
  document.querySelectorAll('.work').forEach((w,i)=>{
    const open=()=>{const c=cases[i];$('case-title').textContent=c[0];
      $('case-body').innerHTML=`<dt>Задача</dt><dd>${c[1]}</dd><dt>Решение</dt><dd>${c[2]}</dd><dt>Результат</dt><dd>${c[3]}</dd>`;
      $('case').showModal()};
    w.tabIndex=0; w.setAttribute('role','button'); w.onclick=open;
    w.onkeydown=e=>{if(e.key==='Enter'||e.key===' '){e.preventDefault();open()}};
  });
  document.querySelectorAll('dialog').forEach(d=>d.addEventListener('click',e=>{if(e.target===d)d.close()}));
  document.querySelectorAll('[data-open]').forEach(a=>a.onclick=e=>{e.preventDefault();$(a.dataset.open).showModal()});

  // Кнопка «Выбрать» подставляет тариф в форму
  document.querySelectorAll('.price-card .btn').forEach(b=>b.addEventListener('click',()=>{
    $('type').value=b.closest('.price-card').querySelector('h3').textContent;
  }));
  // Заявка уходит через почтовое приложение; для отправки без него подключите свой обработчик
  $('form').onsubmit=e=>{
    e.preventDefault();
    const f=new FormData(e.target);
    const body=`Имя: ${f.get('name')}\nКонтакт: ${f.get('contact')}\nУслуга: ${f.get('type')}\nБюджет: ${f.get('budget')}\n\n${f.get('msg')}\n\nСогласие на обработку персональных данных дано: ${new Date().toLocaleString('ru-RU')}`;
    location.href='mailto:hello@atelier.ru?subject='+encodeURIComponent('Заявка с сайта: '+f.get('type'))+'&body='+encodeURIComponent(body);
    $('status').textContent='Открываем почтовое приложение. Если оно не открылось, напишите на hello@atelier.ru или в Telegram.';
  };
  document.addEventListener('click',e=>{if(!e.target.closest('header'))setMenu(false)});
  document.addEventListener('keydown',e=>{if(e.key==='Escape')setMenu(false)});

  // ===== Анимации =====
  const fine=matchMedia('(hover:hover) and (pointer:fine)').matches, calm=matchMedia('(prefers-reduced-motion:reduce)').matches;

  // полоса прогресса, тень шапки, кнопка «наверх»
  const bar=$('progress'), toTop=$('to-top'), hdr=document.querySelector('header');
  let ticking=false;
  const onScroll=()=>{ticking=false;const y=scrollY,h=root.scrollHeight-innerHeight;
    bar.style.transform=`scaleX(${h>0?y/h:0})`;hdr.classList.toggle('scrolled',y>10);toTop.classList.toggle('show',y>600)};
  addEventListener('scroll',()=>{if(!ticking){ticking=true;requestAnimationFrame(onScroll)}},{passive:true});
  onScroll();
  toTop.onclick=()=>scrollTo({top:0});

  // подсветка текущего раздела в меню
  const links=[...document.querySelectorAll('.nav-links a')];
  const spy=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting)links.forEach(a=>a.classList.toggle('active',a.getAttribute('href')==='#'+e.target.id))}),{rootMargin:'-45% 0px -50% 0px'});
  links.forEach(a=>{const t=document.querySelector(a.getAttribute('href'));if(t)spy.observe(t)});
  menu.querySelectorAll('li').forEach((li,i)=>li.style.setProperty('--i',i));

  // плавная смена темы
  $('theme').addEventListener('click',()=>{const b=$('theme');root.classList.add('theme-anim');b.classList.add('spin');
    setTimeout(()=>{root.classList.remove('theme-anim');b.classList.remove('spin')},500)});

  // появление дополнительных элементов по очереди
  const stag=(sel,step)=>document.querySelectorAll(sel).forEach((el,i)=>{el.classList.add('reveal');el.style.setProperty('--d',i*step+'ms');observer.observe(el)});
  document.querySelector('.faq').classList.remove('reveal');
  stag('.faq details',70); stag('.form > :not(#status)',60); stag('.channels .btn',80); stag('.footer-inner',0);

  if(!calm){
    // бегущая строка логотипов
    const logos=document.querySelector('.logos'), track=document.createElement('div');
    track.className='logos-track'; track.append(...logos.children);
    [...track.children].forEach(c=>{const k=c.cloneNode(true);k.setAttribute('aria-hidden','true');track.append(k)});
    logos.append(track);

    // цены считаются от нуля
    document.querySelectorAll('.price').forEach(p=>{
      const n=parseInt(p.firstChild.nodeValue.replace(/\D/g,''),10);
      p.firstChild.nodeValue='от 0 ₽ ';
      new IntersectionObserver((es,o)=>{if(!es[0].isIntersecting)return;o.disconnect();const t0=performance.now();
        (function f(now){const k=Math.min((now-t0)/1200,1);
          p.firstChild.nodeValue='от '+Math.round(n*(1-Math.pow(1-k,3))).toLocaleString('ru-RU')+' ₽ ';
          if(k<1)requestAnimationFrame(f)})(t0)},{threshold:.8}).observe(p);
    });
  }

  if(fine&&!calm){
    // наклон карточек работ, подсветка карточек и героя за курсором
    document.querySelectorAll('.work').forEach(w=>{
      w.addEventListener('mousemove',e=>{const r=w.getBoundingClientRect(),x=(e.clientX-r.left)/r.width-.5,y=(e.clientY-r.top)/r.height-.5;
        w.style.transform=`perspective(900px) rotateY(${x*8}deg) rotateX(${-y*8}deg)`});
      w.addEventListener('mouseleave',()=>{w.style.transform=''});
    });
    const glow=(el,a,b)=>el.addEventListener('mousemove',e=>{const r=el.getBoundingClientRect();
      el.style.setProperty(a,e.clientX-r.left+'px');el.style.setProperty(b,e.clientY-r.top+'px')});
    document.querySelectorAll('.card').forEach(c=>glow(c,'--mx','--my'));
    glow(document.querySelector('.hero'),'--hx','--hy');
  }

  // ===== Cookie и аналитика («Яндекс Метрика» включается только после согласия) =====
  const METRIKA_ID=0; // ← вставьте номер счётчика с metrika.yandex.ru
  const KEY='cookie-consent', banner=$('cookie');
  const getChoice=()=>{try{return localStorage.getItem(KEY)}catch(e){return null}};
  const setChoice=v=>{try{localStorage.setItem(KEY,v)}catch(e){}};
  let metrikaOn=false;
  function loadMetrika(){
    if(!METRIKA_ID||metrikaOn)return; metrikaOn=true;
    (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};m[i].l=1*new Date();
      k=e.createElement(t);a=e.getElementsByTagName(t)[0];k.async=1;k.src=r;a.parentNode.insertBefore(k,a)})
      (window,document,'script','https://mc.yandex.ru/metrika/tag.js','ym');
    ym(METRIKA_ID,'init',{clickmap:true,trackLinks:true,accurateTrackBounce:true,webvisor:false});
  }
  const goal=n=>{if(metrikaOn&&window.ym)ym(METRIKA_ID,'reachGoal',n)};
  const clearYm=()=>{
    const parts=location.hostname.split('.'), old='=;expires=Thu, 01 Jan 1970 00:00:00 GMT;path=/';
    document.cookie.split(';').map(c=>c.split('=')[0].trim()).filter(n=>n.startsWith('_ym')).forEach(n=>{
      for(let i=0;i<parts.length-1;i++)document.cookie=n+old+';domain=.'+parts.slice(i).join('.');
      document.cookie=n+old;
    });
  };
  const choose=v=>{
    setChoice(v); banner.hidden=true;
    if(v==='yes')loadMetrika();
    else{const was=metrikaOn;clearYm();if(was)location.reload()}
  };
  $('cookie-yes').onclick=()=>choose('yes');
  $('cookie-no').onclick=()=>choose('no');
  $('cookie-settings').onclick=e=>{e.preventDefault();banner.hidden=false};
  const saved=getChoice();
  if(saved==='yes')loadMetrika(); else if(!saved)setTimeout(()=>{banner.hidden=false},1200);

  // цели для Метрики (срабатывают только при согласии)
  $('form').addEventListener('submit',()=>goal('form_submit'));
  document.querySelectorAll('.work').forEach(w=>w.addEventListener('click',()=>goal('case_open')));
  document.querySelectorAll('.price-card .btn').forEach(b=>b.addEventListener('click',()=>goal('price_select')));
</script>

</body>
</html>
