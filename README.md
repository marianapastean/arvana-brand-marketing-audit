
<!DOCTYPE html>
<html lang="ro">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#28183f">
  <meta name="description" content="ARVANA Brand & Marketing Audit. Descoperă cât de clar, coerent și strategic este construit businessul tău.">

  <title>ARVANA | Brand & Marketing Audit</title>

  <!-- Elegant typography -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@400;500;600;700;800&family=Playfair+Display:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    :root {
      --ink: #28183f;
      --purple: #49316f;
      --purple-2: #73559a;
      --lavender: #a992c8;
      --soft: #eee8f5;
      --paper: #faf9fc;
      --white: #ffffff;
      --muted: #837b8c;
      --line: #e9e3ef;
      --green: #638c76;
      --shadow: 0 22px 65px rgba(45, 27, 68, .08);
      --serif: "Playfair Display", Georgia, serif;
      --sans: "Manrope", sans-serif;
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      background: var(--paper);
      color: var(--ink);
      font-family: "DM Sans", sans-serif;
      line-height: 1.65;
      overflow-x: hidden;
    }

    button {
      font: inherit;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .ambient {
      position: fixed;
      pointer-events: none;
      z-index: -1;
      border-radius: 50%;
      filter: blur(90px);
      opacity: .35;
    }

    .ambient.one {
      width: 360px;
      height: 360px;
      background: #d9c9eb;
      top: 130px;
      left: -200px;
    }

    .ambient.two {
      width: 320px;
      height: 320px;
      background: #e5dced;
      right: -180px;
      top: 650px;
    }

    /* HEADER */

    .header {
      position: relative;
      z-index: 5;
      background: rgba(250, 249, 252, .88);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(73, 49, 111, .09);
    }

    .header-inner {
      max-width: 1160px;
      min-height: 83px;
      padding: 12px 30px;
      margin: auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      display: block;
      width: 185px;
      max-height: 58px;
      object-fit: contain;
      object-position: left center;
    }

    .header-note {
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 2px;
      color: var(--purple);
      text-transform: uppercase;
      text-align: right;
    }

    .header-note span {
      display: block;
      color: var(--muted);
      font-size: 9px;
      font-weight: 500;
      letter-spacing: 1.5px;
      margin-top: 4px;
    }

    /* HERO */

    .hero {
      position: relative;
      padding: 90px 24px 72px;
      overflow: hidden;
      background:
        radial-gradient(ellipse at 80% 20%, rgba(176, 151, 208, .19), transparent 38%),
        linear-gradient(135deg, #f7f4fa 0%, #fcfbfd 55%, #f1ecf7 100%);
    }

    .hero-inner {
      max-width: 960px;
      margin: auto;
      text-align: center;
      animation: fadeUp .9s ease both;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      color: var(--purple-2);
      font-size: 10px;
      font-weight: 800;
      letter-spacing: 2.8px;
      text-transform: uppercase;
    }

    .eyebrow::before,
    .eyebrow::after {
      content: "";
      width: 25px;
      height: 1px;
      background: var(--lavender);
    }

    .hero h1 {
      font-family: var(--serif);
      font-weight: 400;
      color: var(--ink);
      font-size: clamp(42px, 7vw, 76px);
      line-height: 1.08;
      letter-spacing: -2px;
      margin: 23px 0 20px;
    }

    .hero h1 em {
      color: var(--purple-2);
      font-weight: 400;
    }

    .hero-description {
      max-width: 720px;
      margin: 0 auto;
      color: #70687b;
      font-size: 15px;
      line-height: 1.9;
    }

    .hero-description strong {
      color: var(--purple);
      font-weight: 700;
    }

    .hero-divider {
      width: 55px;
      height: 1px;
      background: var(--lavender);
      margin: 30px auto;
    }

    .hero-statement {
      max-width: 650px;
      margin: auto;
      color: var(--purple);
      font-family: var(--serif);
      font-size: clamp(19px, 3vw, 25px);
      line-height: 1.5;
    }

    .hero-meta {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 28px;
      margin-top: 32px;
    }

    .meta-item {
      display: flex;
      align-items: center;
      gap: 8px;
      color: var(--muted);
      font-size: 11px;
      font-weight: 600;
    }

    .meta-dot {
      width: 6px;
      height: 6px;
      background: var(--lavender);
      border-radius: 50%;
    }

    /* MAIN */

    .main {
      max-width: 900px;
      margin: auto;
      padding: 0 24px 90px;
    }

    .intro-panel {
      position: relative;
      margin-top: -20px;
      padding: 29px 34px;
      background: rgba(255,255,255,.88);
      border: 1px solid rgba(73,49,111,.09);
      border-radius: 18px;
      box-shadow: var(--shadow);
      display: grid;
      grid-template-columns: 1fr auto;
      align-items: center;
      gap: 20px;
      animation: fadeUp .8s .15s ease both;
    }

    .intro-panel h2 {
      font-family: var(--serif);
      font-size: 24px;
      font-weight: 400;
      color: var(--ink);
      margin: 0 0 5px;
    }

    .intro-panel p {
      color: var(--muted);
      font-size: 12px;
      margin: 0;
    }

    .intro-number {
      color: var(--lavender);
      font-family: var(--serif);
      font-size: 54px;
      line-height: 1;
    }

    /* QUESTION AREA */

    .audit-area {
      margin-top: 55px;
    }

    .audit-heading {
      text-align: center;
      margin-bottom: 27px;
    }

    .audit-heading h2 {
      font-family: var(--serif);
      font-size: 34px;
      font-weight: 400;
      margin: 10px 0 5px;
      color: var(--ink);
    }

    .audit-heading p {
      font-size: 12px;
      color: var(--muted);
      margin: 0;
    }

    .progress-panel {
      background: rgba(255,255,255,.75);
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 18px 21px;
      margin-bottom: 16px;
    }

    .progress-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      margin-bottom: 11px;
    }

    .progress-label {
      color: var(--purple);
      font-size: 11px;
      font-weight: 700;
    }

    .progress-percent {
      color: var(--muted);
      font-size: 11px;
    }

    .progress-track {
      height: 4px;
      background: #eee9f3;
      border-radius: 20px;
      overflow: hidden;
    }

    .progress-fill {
      height: 100%;
      width: 0;
      background: linear-gradient(90deg, var(--purple), #a68bc9);
      border-radius: 20px;
      transition: width .5s cubic-bezier(.2,.8,.2,1);
    }

    .question-card {
      position: relative;
      overflow: hidden;
      background: var(--white);
      border: 1px solid rgba(73,49,111,.1);
      border-radius: 20px;
      padding: 38px 42px 35px;
      box-shadow: var(--shadow);
      min-height: 355px;
      animation: cardEnter .45s ease both;
    }

    .question-card::after {
      content: "";
      position: absolute;
      width: 180px;
      height: 180px;
      right: -95px;
      bottom: -100px;
      border: 1px solid rgba(165,138,203,.2);
      border-radius: 50%;
      box-shadow:
        0 0 0 20px rgba(165,138,203,.035),
        0 0 0 40px rgba(165,138,203,.025);
      pointer-events: none;
    }

    .question-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      margin-bottom: 25px;
    }

    .dimension-tag {
      display: inline-block;
      background: #f1ebf7;
      color: var(--purple);
      padding: 7px 13px;
      border-radius: 30px;
      font-size: 9px;
      font-weight: 800;
      letter-spacing: 1.5px;
      text-transform: uppercase;
    }

    .question-index {
      color: #b0a8b9;
      font-family: var(--serif);
      font-size: 19px;
    }

    .question-title {
      max-width: 650px;
      font-family: var(--serif);
      font-size: clamp(24px, 4vw, 32px);
      font-weight: 400;
      line-height: 1.35;
      color: var(--ink);
      margin: 0 0 10px;
    }

    .question-description {
      max-width: 620px;
      color: var(--muted);
      font-size: 13px;
      margin: 0 0 29px;
    }

    .scale {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 10px;
      position: relative;
      z-index: 1;
    }

    .scale-option {
      border: 1px solid var(--line);
      background: #fdfcfe;
      color: var(--purple);
      border-radius: 12px;
      min-height: 83px;
      padding: 12px 5px;
      cursor: pointer;
      transition: transform .22s, border .22s, background .22s, box-shadow .22s;
    }

    .scale-option:hover {
      transform: translateY(-4px);
      border-color: var(--lavender);
      box-shadow: 0 8px 20px rgba(73,49,111,.08);
    }

    .scale-option.selected {
      color: white;
      background: linear-gradient(145deg, var(--purple), #6a4c91);
      border-color: var(--purple);
      box-shadow: 0 8px 22px rgba(73,49,111,.2);
      transform: translateY(-3px);
    }

    .scale-option strong {
      display: block;
      font-family: var(--serif);
      font-size: 25px;
      font-weight: 400;
      margin-bottom: 2px;
    }

    .scale-option span {
      display: block;
      font-size: 9px;
      line-height: 1.35;
    }

    .scale-hint {
      display: flex;
      justify-content: space-between;
      gap: 10px;
      color: #a39aaa;
      font-size: 10px;
      margin-top: 12px;
    }

    .error {
      display: none;
      color: #a64c58;
      font-size: 11px;
      margin-top: 13px;
    }

    .navigation {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      margin-top: 20px;
    }

    .btn {
      border: 0;
      cursor: pointer;
      border-radius: 40px;
      padding: 14px 24px;
      font-size: 11px;
      font-weight: 800;
      letter-spacing: .5px;
      transition: transform .2s, box-shadow .2s, background .2s;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
    }

    .btn:hover:not(:disabled) {
      transform: translateY(-2px);
    }

    .btn:disabled {
      opacity: .35;
      cursor: not-allowed;
    }

    .btn-primary {
      background: var(--purple);
      color: white;
      box-shadow: 0 8px 20px rgba(73,49,111,.15);
    }

    .btn-primary:hover:not(:disabled) {
      background: var(--ink);
      box-shadow: 0 12px 25px rgba(73,49,111,.2);
    }

    .btn-light {
      background: #f0ebf6;
      color: var(--purple);
    }

    .btn-light:hover:not(:disabled) {
      background: #e5dbee;
    }

    /* RESULTS */

    .results {
      animation: fadeUp .65s ease both;
    }

    .result-card {
      background: white;
      border: 1px solid var(--line);
      border-radius: 20px;
      box-shadow: var(--shadow);
      padding: 38px;
    }

    .result-heading {
      text-align: center;
    }

    .result-heading h2 {
      font-family: var(--serif);
      font-size: 36px;
      font-weight: 400;
      color: var(--ink);
      margin: 9px 0 4px;
    }

    .result-heading p {
      color: var(--muted);
      font-size: 12px;
      margin: 0;
    }

    .score-circle {
      width: 190px;
      height: 190px;
      margin: 30px auto 20px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: conic-gradient(var(--purple) var(--score), #eee9f3 var(--score));
      position: relative;
      animation: scoreIn .9s ease both;
    }

    .score-circle::before {
      content: "";
      position: absolute;
      width: 162px;
      height: 162px;
      background: white;
      border-radius: 50%;
    }

    .score-content {
      position: relative;
      text-align: center;
      z-index: 1;
    }

    .score-number {
      display: block;
      color: var(--ink);
      font-family: var(--serif);
      font-size: 57px;
      line-height: 1;
    }

    .score-out-of {
      display: block;
      color: var(--muted);
      font-size: 10px;
      margin-top: 5px;
    }

    .result-level-wrap {
      text-align: center;
    }

    .result-level {
      display: inline-block;
      padding: 9px 17px;
      border-radius: 30px;
      background: var(--lavender);
      color: var(--purple);
      font-size: 11px;
      font-weight: 800;
    }

    .result-summary {
      max-width: 620px;
      color: var(--muted);
      text-align: center;
      font-size: 13px;
      margin: 17px auto 0;
    }

    .section-title {
      font-family: var(--serif);
      font-size: 25px;
      font-weight: 400;
      color: var(--ink);
      margin: 35px 0 18px;
    }

    .dimension-result {
      margin-bottom: 19px;
    }

    .dimension-top {
      display: flex;
      justify-content: space-between;
      gap: 12px;
      font-size: 12px;
      margin-bottom: 7px;
    }

    .dimension-top strong {
      color: var(--purple);
      font-weight: 700;
    }

    .dimension-top span {
      color: var(--purple-2);
      font-weight: 800;
    }

    .dimension-track {
      height: 7px;
      border-radius: 20px;
      background: #eee9f3;
      overflow: hidden;
    }

    .dimension-fill {
      height: 100%;
      border-radius: 20px;
      background: linear-gradient(90deg, #715394, #b39bcf);
      animation: barIn .8s ease both;
    }

    .insight-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 13px;
      margin-top: 25px;
    }

    .insight {
      background: #f8f6fa;
      border: 1px solid var(--line);
      border-radius: 13px;
      padding: 19px;
    }

    .insight small {
      display: block;
      color: var(--muted);
      font-size: 9px;
      font-weight: 800;
      letter-spacing: 1.3px;
      text-transform: uppercase;
      margin-bottom: 7px;
    }

    .insight strong {
      color: var(--purple);
      font-size: 13px;
    }

    .recommendation {
      border-left: 2px solid var(--lavender);
      background: #faf9fc;
      border-radius: 0 12px 12px 0;
      padding: 17px 19px;
      margin-bottom: 11px;
    }

    .recommendation h4 {
      color: var(--purple);
      font-size: 12px;
      margin: 0 0 6px;
    }

    .recommendation p {
      color: var(--muted);
      font-size: 12px;
      margin: 0;
    }

    .disclaimer {
      text-align: center;
      color: #9991a0;
      font-size: 10px;
      max-width: 650px;
      margin: 25px auto 0;
    }

    .result-actions {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 23px;
    }

    /* CTA */

    .cta {
      margin-top: 22px;
      background:
        radial-gradient(circle at 90% 0%, rgba(180,153,212,.24), transparent 35%),
        linear-gradient(135deg, #2c1b46, #49316f);
      border-radius: 20px;
      padding: 40px 30px;
      text-align: center;
      color: white;
      position: relative;
      overflow: hidden;
    }

    .cta .eyebrow {
      color: #d5c5e8;
    }

    .cta h3 {
      font-family: var(--serif);
      font-size: 31px;
      font-weight: 400;
      margin: 12px 0;
    }

    .cta p {
      color: #ddd4e9;
      font-size: 12px;
      max-width: 530px;
      margin: 0 auto 22px;
    }

    .cta .btn {
      background: white;
      color: var(--purple);
    }

    .cta .btn:hover {
      background: #f0eaf7;
    }

    /* FOOTER */

    .footer {
      padding: 30px 20px;
      text-align: center;
      border-top: 1px solid var(--line);
    }

    .footer img {
      width: 145px;
      max-height: 45px;
      object-fit: contain;
      margin-bottom: 7px;
    }

    .footer p {
      color: var(--muted);
      font-size: 10px;
      margin: 0;
    }

    .hidden {
      display: none !important;
    }

    /* ANIMATIONS */

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(22px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes cardEnter {
      from {
        opacity: 0;
        transform: translateY(12px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes scoreIn {
      from {
        opacity: 0;
        transform: scale(.85);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    @keyframes barIn {
      from { width: 0; }
    }

    @media (max-width: 650px) {
      .header-inner {
        padding: 12px 17px;
        min-height: 70px;
      }

      .logo {
        width: 145px;
        max-height: 48px;
      }

      .header-note {
        font-size: 8px;
        letter-spacing: 1px;
      }

      .header-note span {
        font-size: 8px;
      }

      .hero {
        padding: 65px 18px 55px;
      }

      .hero h1 {
        letter-spacing: -1px;
      }

      .hero-description {
        font-size: 13px;
      }

      .hero-meta {
        gap: 13px 19px;
      }

      .meta-item {
        font-size: 10px;
      }

      .main {
        padding: 0 14px 55px;
      }

      .intro-panel {
        grid-template-columns: 1fr;
        padding: 23px;
        text-align: center;
      }

      .intro-number {
        display: none;
      }

      .audit-area {
        margin-top: 43px;
      }

      .audit-heading h2 {
        font-size: 29px;
      }

      .question-card {
        padding: 25px 19px;
        min-height: auto;
      }

      .question-title {
        font-size: 25px;
      }

      .scale {
        gap: 5px;
      }

      .scale-option {
        min-height: 72px;
        padding: 8px 2px;
      }

      .scale-option strong {
        font-size: 20px;
      }

      .scale-option span {
        font-size: 8px;
      }

      .scale-hint {
        font-size: 8px;
      }

      .navigation .btn {
        padding: 12px 15px;
        font-size: 10px;
      }

      .result-card {
        padding: 25px 19px;
      }

      .result-heading h2 {
        font-size: 30px;
      }

      .insight-grid {
        grid-template-columns: 1fr;
      }

      .result-actions .btn {
        width: 100%;
      }

      .cta {
        padding: 33px 21px;
      }

      .cta h3 {
        font-size: 27px;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        scroll-behavior: auto !important;
        animation-duration: .01ms !important;
        transition-duration: .01ms !important;
      }
    }

    @media print {
      body {
        background: white;
      }

      .header {
        background: white;
      }

      .hero,
      .intro-panel,
      .audit-area,
      .footer,
      .result-actions,
      .cta .btn {
        display: none !important;
      }

      .main {
        padding: 10px;
      }

      .result-card {
        box-shadow: none;
        border: 0;
      }

      .cta {
        background: white;
        border: 1px solid #ddd;
        color: var(--ink);
      }

      .cta p {
        color: #555;
      }

      .recommendation,
      .insight {
        break-inside: avoid;
      }
    }
  </style>
</head>

<body>

  <div class="ambient one"></div>
  <div class="ambient two"></div>

  <header class="header">
    <div class="header-inner">
      <a href="https://marianapastean.my.canva.site/mariana-pastean-portfolio" aria-label="ARVANA Digital Marketing">
        <img
          class="logo"
          src="./Logo%20-%20ARVANA%20Digital%20Marketing%20(1).png"
          alt="ARVANA Digital Marketing"
          onerror="this.style.display='none';document.getElementById('logoFallback').style.display='block';"
        >
        <span id="logoFallback" style="display:none;font-family:Manrope,sans-serif;font-weight:800;letter-spacing:3px;color:#49316f;">
          ARVANA
        </span>
      </a>

      <div class="header-note">
        Strategic Marketing
        <span>& Brand Development</span>
      </div>
    </div>
  </header>

  <section class="hero">
    <div class="hero-inner">

      <div class="eyebrow">Un instrument pentru businessul tău</div>

      <h1>
        Înainte de marketing,<br>
        ai nevoie de <em>claritate.</em>
      </h1>

      <p class="hero-description">
        Un business se dezvoltă mai bine atunci când îi cunoști
        activitatea, publicul și valoarea pe care o oferă.
        Înainte să alegi cum comunici, unde investești sau cum
        îți promovezi brandul, este important să înțelegi
        <strong>ce reprezintă businessul tău și în ce direcție vrei să îl dezvolți.</strong>
      </p>

      <div class="hero-divider"></div>

      <p class="hero-statement">
        Claritatea este primul pas către un marketing construit cu sens.
      </p>

      <div class="hero-meta">
        <div class="meta-item">
          <span class="meta-dot"></span>
          15 întrebări
        </div>
        <div class="meta-item">
          <span class="meta-dot"></span>
          5 dimensiuni
        </div>
        <div class="meta-item">
          <span class="meta-dot"></span>
          Raport personalizat
        </div>
        <div class="meta-item">
          <span class="meta-dot"></span>
          Gratuit
        </div>
      </div>

    </div>
  </section>

  <main class="main">

    <section class="intro-panel">
      <div>
        <h2>Începe cu o perspectivă mai clară.</h2>
        <p>
          Evaluează fundația brandului și a activităților tale de marketing.
          Răspunde sincer, în funcție de situația actuală a businessului.
        </p>
      </div>
      <div class="intro-number">01</div>
    </section>

    <section class="audit-area" id="audit">

      <div class="audit-heading">
        <div class="eyebrow">Autoevaluare</div>
        <h2>Descoperă unde te afli.</h2>
        <p>Nu există răspunsuri corecte sau greșite. Contează perspectiva ta reală.</p>
      </div>

      <div class="progress-panel">
        <div class="progress-top">
          <span class="progress-label" id="progressText">Întrebarea 1 din 15</span>
          <span class="progress-percent" id="progressPercent">0% completat</span>
        </div>
        <div class="progress-track">
          <div class="progress-fill" id="progressFill"></div>
        </div>
      </div>

      <div id="questionContainer"></div>

      <div class="navigation">
        <button class="btn btn-light" id="prevBtn" type="button" disabled>
          ← Înapoi
        </button>

        <button class="btn btn-primary" id="nextBtn" type="button" disabled>
          Următoarea întrebare →
        </button>
      </div>

      <div class="error" id="errorMessage">
        Selectează un răspuns pentru a continua.
      </div>

    </section>

    <section id="results" class="results hidden">

      <div class="result-card">

        <div class="result-heading">
          <div class="eyebrow">Rezultatul evaluării</div>
          <h2>Imaginea de ansamblu.</h2>
          <p>ARVANA BRAND & MARKETING AUDIT</p>
        </div>

        <div class="score-circle" id="scoreCircle">
          <div class="score-content">
            <span class="score-number" id="overallScore">0</span>
            <span class="score-out-of">din 100 puncte</span>
          </div>
        </div>

        <div class="result-level-wrap">
          <span class="result-level" id="resultLevel"></span>
        </div>

        <p class="result-summary" id="resultSummary"></p>

        <h3 class="section-title">Evaluarea pe dimensiuni</h3>
        <div id="dimensionResults"></div>

        <div class="insight-grid">
          <div class="insight">
            <small>Punctul forte</small>
            <strong id="strongestArea"></strong>
          </div>

          <div class="insight">
            <small>Prioritatea de îmbunătățire</small>
            <strong id="weakestArea"></strong>
          </div>
        </div>

        <h3 class="section-title">Direcții de îmbunătățire</h3>
        <div id="recommendations"></div>

        <p class="disclaimer">
          Acest raport este generat pe baza răspunsurilor oferite și are
          scop orientativ. Reprezintă o autoevaluare, nu un audit
          profesional complet, o analiză de piață sau o evaluare
          comparativă cu alte businessuri.
        </p>

        <div class="result-actions">
          <button class="btn btn-primary" id="copyReportBtn" type="button">
            Copiază raportul
          </button>

          <button class="btn btn-light" id="pdfBtn" type="button">
            Salvează PDF
          </button>

          <button class="btn btn-light" id="restartBtn" type="button">
            Reia evaluarea
          </button>
        </div>

      </div>

      <section class="cta">
        <div class="eyebrow">Următorul pas</div>
        <h3>Direcția potrivită începe cu o decizie clară.</h3>
        <p>
          Dacă rezultatele evaluării ți-au oferit o perspectivă asupra
          businessului, descoperă cum poate contribui o abordare
          strategică la dezvoltarea brandului și a comunicării tale.
        </p>

        <a
          class="btn"
          href="https://marianapastean.my.canva.site/mariana-pastean-portfolio"
          target="_blank"
          rel="noopener noreferrer"
        >
          Descoperă ARVANA →
        </a>
      </section>

    </section>

  </main>

  <footer class="footer">
    <img
      src="./Logo%20-%20ARVANA%20Digital%20Marketing%20(1).png"
      alt="ARVANA Digital Marketing"
      onerror="this.style.display='none';"
    >
    <p>Direcție clară. Branduri cu valoare.</p>
  </footer>

  <script>
    const dimensions = [
      {
        name: "Poziționare",
        recommendations: [
          "Definește cât mai precis publicul căruia i te adresezi. Identifică nevoile, provocările și motivațiile clienților potriviți.",
          "Clarifică oferta: ce problemă rezolvă, ce valoare oferă și de ce ar alege un client businessul tău.",
          "Identifică elementele care diferențiază businessul tău. Construiește un mesaj de poziționare simplu, relevant și ușor de înțeles."
        ]
      },
      {
        name: "Identitate de brand",
        recommendations: [
          "Stabilește un sistem vizual coerent: logo, paletă cromatică, tipografie și reguli de utilizare. Aplică-l consecvent în toate materialele.",
          "Definește personalitatea brandului și valorile pe care dorești să le transmită. Acestea trebuie să se reflecte în limbaj, design și comportament.",
          "Analizează experiența oferită clientului în toate punctele de contact: website, social media, comunicare și interacțiunea directă."
        ]
      },
      {
        name: "Comunicare",
        recommendations: [
          "Construiește un mesaj central care explică limpede cine ești, ce oferi și cui te adresezi. Elimină formulările care nu transmit valoare concretă.",
          "Creează reguli de comunicare și un ton al vocii recognoscibil. Asigură-te că mesajele sunt coerente pe toate canalele.",
          "Pornește de la întrebările și preocupările publicului. Comunică beneficii, soluții și perspective relevante, nu doar informații despre produse sau servicii."
        ]
      },
      {
        name: "Strategie de conținut",
        recommendations: [
          "Definește 3–5 piloni de conținut care susțin poziționarea brandului și răspund intereselor publicului tău.",
          "Planifică fiecare material în funcție de un obiectiv: vizibilitate, educare, încredere, interacțiune sau conversie.",
          "Urmărește performanța conținutului prin indicatori relevanți. Analizează ce funcționează și ajustează planul în consecință."
        ]
      },
      {
        name: "Strategie de marketing",
        recommendations: [
          "Stabilește obiective de marketing concrete și măsurabile. Leagă activitățile de marketing de obiectivele reale ale businessului.",
          "Alege canalele în funcție de public, resurse și obiective. Nu este necesar să fii prezent peste tot dacă nu poți susține o comunicare relevantă.",
          "Construiește un proces periodic de analiză. Evaluează rezultatele, identifică blocajele și ajustează acțiunile în funcție de date."
        ]
      }
    ];

    const questions = [
      {
        dimension: 0,
        title: "Știi exact cui se adresează businessul tău?",
        description: "Ai definit publicul țintă prin nevoi, comportamente și caracteristici relevante?"
      },
      {
        dimension: 0,
        title: "Poți explica simplu ce valoare oferă businessul tău?",
        description: "Este clar ce problemă rezolvi și de ce oferta ta este relevantă?"
      },
      {
        dimension: 0,
        title: "Știi ce diferențiază brandul tău de alternativele existente?",
        description: "Poți identifica motive concrete pentru care un client ar trebui să te aleagă?"
      },
      {
        dimension: 1,
        title: "Identitatea vizuală este consecventă pe toate canalele?",
        description: "Logo-ul, culorile, fonturile și materialele transmit aceeași direcție vizuală?"
      },
      {
        dimension: 1,
        title: "Brandul tău are o personalitate și valori clar definite?",
        description: "Știi ce dorești să transmită brandul și cum vrei să fie perceput?"
      },
      {
        dimension: 1,
        title: "Experiența oferită clienților este coerentă?",
        description: "Există continuitate între promisiunea brandului și experiența reală?"
      },
      {
        dimension: 2,
        title: "Mesajele tale explică limpede ce oferi și cui te adresezi?",
        description: "Un potențial client poate înțelege rapid valoarea serviciilor sau produselor tale?"
      },
      {
        dimension: 2,
        title: "Comunicarea brandului este consecventă?",
        description: "Tonul vocii și mesajele sunt recognoscibile pe canalele folosite?"
      },
      {
        dimension: 2,
        title: "Conținutul tău răspunde nevoilor și întrebărilor publicului?",
        description: "Comunici subiecte relevante pentru potențialii clienți, nu doar despre businessul tău?"
      },
      {
        dimension: 3,
        title: "Ai piloni de conținut bine definiți?",
        description: "Știi care sunt principalele teme pe care trebuie să le abordezi?"
      },
      {
        dimension: 3,
        title: "Planifici conținutul în funcție de obiective?",
        description: "Fiecare material are un rol clar în comunicarea și marketingul businessului?"
      },
      {
        dimension: 3,
        title: "Analizezi rezultatele conținutului publicat?",
        description: "Urmărești indicatori și folosești concluziile pentru a îmbunătăți conținutul?"
      },
      {
        dimension: 4,
        title: "Ai obiective de marketing clare și măsurabile?",
        description: "Știi ce rezultate urmărești și cum vei evalua progresul?"
      },
      {
        dimension: 4,
        title: "Ai ales canalele de marketing potrivite businessului tău?",
        description: "Canalele folosite sunt relevante pentru public și pentru obiectivele tale?"
      },
      {
        dimension: 4,
        title: "Analizezi și optimizezi periodic activitățile de marketing?",
        description: "Evaluezi rezultatele și adaptezi acțiunile în funcție de ceea ce observi?"
      }
    ];

    const scaleLabels = [
      "Deloc",
      "În mică măsură",
      "Parțial",
      "În mare măsură",
      "Complet"
    ];

    let answers = Array(questions.length).fill(null);
    let currentQuestion = 0;
    let finalReport = "";

    const questionContainer =
      document.getElementById("questionContainer");

    const nextBtn =
      document.getElementById("nextBtn");

    const prevBtn =
      document.getElementById("prevBtn");

    function renderQuestion() {
      const question = questions[currentQuestion];
      const dimension = dimensions[question.dimension];

      const completed = answers.filter(
        value => value !== null
      ).length;

      const percentage = Math.round(
        completed / questions.length * 100
      );

      document.getElementById("progressText").textContent =
        `Întrebarea ${currentQuestion + 1} din ${questions.length}`;

      document.getElementById("progressPercent").textContent =
        `${percentage}% completat`;

      document.getElementById("progressFill").style.width =
        `${percentage}%`;

      questionContainer.innerHTML = `
        <div class="question-card" id="activeQuestion">

          <div class="question-top">
            <span class="dimension-tag">${dimension.name}</span>
            <span class="question-index">
              ${String(currentQuestion + 1).padStart(2, "0")} / 15
            </span>
          </div>

          <h3 class="question-title">${question.title}</h3>

          <p class="question-description">
            ${question.description}
          </p>

          <div class="scale">
            ${scaleLabels.map((label, index) => `
              <button
                type="button"
                class="scale-option ${
                  answers[currentQuestion] === index + 1
                    ? "selected"
                    : ""
                }"
                data-value="${index + 1}"
                aria-pressed="${
                  answers[currentQuestion] === index + 1
                }"
                aria-label="${index + 1}: ${label}"
              >
                <strong>${index + 1}</strong>
                <span>${label}</span>
              </button>
            `).join("")}
          </div>

          <div class="scale-hint">
            <span>1 · Nivel foarte scăzut</span>
            <span>5 · Nivel foarte ridicat</span>
          </div>

        </div>
      `;

      questionContainer
        .querySelectorAll(".scale-option")
        .forEach(button => {
          button.addEventListener("click", () => {
            answers[currentQuestion] =
              Number(button.dataset.value);

            document.getElementById(
              "errorMessage"
            ).style.display = "none";

            renderQuestion();
          });
        });

      prevBtn.disabled = currentQuestion === 0;

      nextBtn.disabled =
        answers[currentQuestion] === null;

      nextBtn.textContent =
        currentQuestion === questions.length - 1
          ? "Vezi raportul →"
          : "Următoarea întrebare →";
    }

    function calculateScores() {
      return dimensions.map((dimension, dimensionIndex) => {
        const dimensionAnswers = questions
          .map((question, index) => ({
            dimension: question.dimension,
            answer: answers[index]
          }))
          .filter(item => item.dimension === dimensionIndex)
          .map(item => item.answer);

        const average =
          dimensionAnswers.reduce(
            (sum, value) => sum + value, 0
          ) / dimensionAnswers.length;

        return Math.round(average / 5 * 100);
      });
    }

    function getScoreLevel(score) {
      if (score <= 39) {
        return {
          title: "Este nevoie de mai multă claritate",
          summary:
            "Rezultatele indică mai multe zone care au nevoie de structură. Înainte de a intensifica activitățile de marketing, merită să clarifici fundația brandului și direcția businessului."
        };
      }

      if (score <= 59) {
        return {
          title: "Fundație în curs de consolidare",
          summary:
            "Există elemente deja conturate, însă unele dimensiuni au nevoie de mai multă coerență și consecvență. O abordare structurată te poate ajuta să construiești o direcție mai clară."
        };
      }

      if (score <= 79) {
        return {
          title: "Direcție bună, cu oportunități de optimizare",
          summary:
            "Businessul tău are o bază relativ bine definită. Următorul pas este să identifici punctele care pot fi îmbunătățite și să conectezi mai bine strategia, brandul și comunicarea."
        };
      }

      return {
        title: "Fundație bine definită",
        summary:
          "Răspunsurile indică un nivel ridicat de claritate și coerență. Menține această direcție prin analiză periodică, adaptare și optimizarea continuă a activităților."
      };
    }

    function buildRecommendations(scores) {
      const ranked = scores
        .map((score, index) => ({
          score,
          index
        }))
        .sort((a, b) => a.score - b.score);

      return ranked.slice(0, 3).map(item => {
        let recommendationIndex = 0;

        if (item.score >= 60) {
          recommendationIndex = 1;
        }

        if (item.score >= 80) {
          recommendationIndex = 2;
        }

        return {
          name: dimensions[item.index].name,
          score: item.score,
          text: dimensions[item.index]
            .recommendations[recommendationIndex]
        };
      });
    }

    function buildPlainTextReport(
      overall,
      level,
      scores,
      ranked,
      recommendations
    ) {
      let report = "";

      report += "ARVANA BRAND & MARKETING AUDIT\n";
      report += "Direcție clară. Branduri cu valoare.\n\n";

      report += `SCOR GENERAL: ${overall}/100\n`;
      report += `${level.title}\n\n`;
      report += `${level.summary}\n\n`;

      report += "SCOR PE DIMENSIUNI\n";

      scores.forEach((score, index) => {
        report += `${dimensions[index].name}: ${score}/100\n`;
      });

      report += "\nPUNCTUL FORTE\n";
      report +=
        `${dimensions[ranked[0].index].name} (${ranked[0].score}/100)\n`;

      report += "\nPRIORITATE DE ÎMBUNĂTĂȚIRE\n";
      report +=
        `${dimensions[ranked[ranked.length - 1].index].name} (${ranked[ranked.length - 1].score}/100)\n`;

      report += "\nRECOMANDĂRI\n";

      recommendations.forEach((item, index) => {
        report += `\n${index + 1}. ${item.name} (${item.score}/100)\n`;
        report += `${item.text}\n`;
      });

      report +=
        "\nNotă: Acest raport este o autoevaluare orientativă, nu un audit profesional complet.\n";

      report += "ARVANA DIGITAL MARKETING\n";

      return report;
    }

    function generateResults() {
      const scores = calculateScores();

      const overall = Math.round(
        answers.reduce((sum, value) => sum + value, 0)
        / answers.length / 5 * 100
      );

      const level = getScoreLevel(overall);

      const ranked = scores
        .map((score, index) => ({
          score,
          index
        }))
        .sort((a, b) => b.score - a.score);

      document.getElementById("overallScore").textContent =
        overall;

      document.getElementById("scoreCircle")
        .style.setProperty(
          "--score",
          `${overall * 3.6}deg`
        );

      document.getElementById("resultLevel").textContent =
        level.title;

      document.getElementById("resultSummary").textContent =
        level.summary;

      document.getElementById("dimensionResults").innerHTML =
        scores.map((score, index) => `
          <div class="dimension-result">
            <div class="dimension-top">
              <strong>${dimensions[index].name}</strong>
              <span>${score}/100</span>
            </div>

            <div class="dimension-track">
              <div
                class="dimension-fill"
                style="width:${score}%"
              ></div>
            </div>
          </div>
        `).join("");

      document.getElementById("strongestArea").textContent =
        `${dimensions[ranked[0].index].name} (${ranked[0].score}/100)`;

      document.getElementById("weakestArea").textContent =
        `${dimensions[ranked[ranked.length - 1].index].name} (${ranked[ranked.length - 1].score}/100)`;

      const recommendations =
        buildRecommendations(scores);

      document.getElementById("recommendations").innerHTML =
        recommendations.map((item, index) => `
          <div class="recommendation">
            <h4>${index + 1}. ${item.name} — ${item.score}/100</h4>
            <p>${item.text}</p>
          </div>
        `).join("");

      finalReport = buildPlainTextReport(
        overall,
        level,
        scores,
        ranked,
        recommendations
      );

      document.getElementById("audit")
        .classList.add("hidden");

      document.getElementById("results")
        .classList.remove("hidden");

      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    }

    async function copyReport() {
      try {
        await navigator.clipboard.writeText(finalReport);

        alert("Raportul a fost copiat cu succes.");

      } catch (error) {
        const textArea =
          document.createElement("textarea");

        textArea.value = finalReport;

        document.body.appendChild(textArea);

        textArea.select();

        document.execCommand("copy");

        textArea.remove();

        alert("Raportul a fost copiat.");
      }
    }

    function restartAudit() {
      answers = Array(questions.length).fill(null);
      currentQuestion = 0;
      finalReport = "";

      document.getElementById("results")
        .classList.add("hidden");

      document.getElementById("audit")
        .classList.remove("hidden");

      renderQuestion();

      document.getElementById("audit").scrollIntoView({
        behavior: "smooth",
        block: "start"
      });
    }

    nextBtn.addEventListener("click", () => {
      if (answers[currentQuestion] === null) {
        document.getElementById(
          "errorMessage"
        ).style.display = "block";

        return;
      }

      if (currentQuestion < questions.length - 1) {
        currentQuestion++;

        renderQuestion();

        document.getElementById("audit").scrollIntoView({
          behavior: "smooth",
          block: "start"
        });

      } else {
        generateResults();
      }
    });

    prevBtn.addEventListener("click", () => {
      if (currentQuestion > 0) {
        currentQuestion--;

        renderQuestion();
      }
    });

    document.getElementById("copyReportBtn")
      .addEventListener("click", copyReport);

    document.getElementById("pdfBtn")
      .addEventListener("click", () => window.print());

    document.getElementById("restartBtn")
      .addEventListener("click", restartAudit);

    renderQuestion();
  </script>

</body>
</html>
