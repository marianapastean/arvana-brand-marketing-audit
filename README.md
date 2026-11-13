
<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#302044">
<meta name="description" content="ARVANA Brand & Marketing Audit – un instrument gratuit de autoevaluare pentru brandul și marketingul businessului tău.">
<title>ARVANA | Brand & Marketing Audit</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@400;500;600;700;800&family=Playfair+Display:wght@400;500;600&display=swap" rel="stylesheet">

<style>
:root{
  --dark:#302044;
  --purple:#49316F;
  --medium:#684995;
  --light:#9274B8;
  --violet:#B19AD2;
  --lavender:#DCD0ED;
  --soft:#F0EAF7;
  --pale:#FAF8FC;
  --white:#FFFFFF;
  --ink:#34283F;
  --muted:#82798D;
  --line:#E9E1F0;
  --serif:"Playfair Display",Georgia,serif;
  --sans:"Manrope",sans-serif;
  --body:"DM Sans",sans-serif;
  --shadow:0 18px 55px rgba(48,32,68,.09);
}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;
  background:var(--pale);
  color:var(--ink);
  font-family:var(--body);
  line-height:1.65;
  overflow-x:hidden;
}
button{font:inherit}
a{color:inherit;text-decoration:none}
button:focus-visible,a:focus-visible{outline:3px solid var(--violet);outline-offset:4px}

.ambient{
  position:fixed;
  z-index:-1;
  pointer-events:none;
  border-radius:50%;
  filter:blur(95px);
  opacity:.38;
  animation:ambientMove 14s ease-in-out infinite alternate;
}
.ambient.one{width:390px;height:390px;background:#DCD0ED;top:130px;left:-230px}
.ambient.two{width:360px;height:360px;background:#C8B3E0;right:-220px;top:850px;animation-delay:2s}

@keyframes ambientMove{
  from{transform:translate(0,0) scale(1)}
  to{transform:translate(35px,45px) scale(1.12)}
}
@keyframes fadeUp{
  from{opacity:0;transform:translateY(28px)}
  to{opacity:1;transform:translateY(0)}
}
@keyframes fadeIn{
  from{opacity:0}
  to{opacity:1}
}
@keyframes float{
  0%,100%{transform:translateY(0)}
  50%{transform:translateY(-8px)}
}
@keyframes shimmer{
  0%{background-position:-200% center}
  100%{background-position:200% center}
}
@keyframes barIn{
  from{width:0}
}
@keyframes scoreIn{
  from{opacity:0;transform:scale(.75) rotate(-15deg)}
  to{opacity:1;transform:scale(1) rotate(0)}
}
@keyframes lineGrow{
  from{transform:scaleX(0)}
  to{transform:scaleX(1)}
}

/* HEADER */

.header{
  position:relative;
  z-index:5;
  background:rgba(255,255,255,.94);
  backdrop-filter:blur(18px);
  border-bottom:1px solid rgba(73,49,111,.12);
}
.header-inner{
  max-width:1240px;
  min-height:112px;
  padding:12px 34px;
  margin:auto;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
}
.logo{
  display:block;
  width:260px;
  max-height:90px;
  object-fit:contain;
  object-position:left center;
  transition:transform .35s ease;
}
.brand-link:hover .logo{transform:scale(1.035)}
.logo-fallback{
  display:none;
  color:var(--purple);
  font-family:var(--sans);
  font-size:30px;
  font-weight:800;
  letter-spacing:4px;
}
.header-note{
  color:var(--purple);
  font-size:10px;
  font-weight:800;
  letter-spacing:2px;
  text-transform:uppercase;
  text-align:right;
}
.header-note span{
  display:block;
  color:var(--light);
  font-size:9px;
  font-weight:600;
  letter-spacing:1.5px;
  margin-top:5px;
}

/* HERO */

.hero{
  position:relative;
  overflow:hidden;
  padding:100px 24px 92px;
  background:
    radial-gradient(ellipse at 82% 15%,rgba(177,154,210,.42),transparent 36%),
    radial-gradient(ellipse at 8% 90%,rgba(220,208,237,.48),transparent 35%),
    linear-gradient(135deg,#F5F0FA,#FCFAFD 55%,#EEE6F6);
}
.hero:before,.hero:after{
  content:"";
  position:absolute;
  border:1px solid rgba(104,73,149,.13);
  border-radius:50%;
  pointer-events:none;
  animation:float 8s ease-in-out infinite;
}
.hero:before{width:390px;height:390px;right:-190px;top:10px}
.hero:after{width:270px;height:270px;right:-130px;top:70px;animation-delay:1.5s}
.hero-inner{
  position:relative;
  z-index:1;
  max-width:960px;
  margin:auto;
  text-align:center;
  animation:fadeUp 1s ease both;
}
.eyebrow{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:11px;
  color:var(--medium);
  font-size:10px;
  font-weight:800;
  letter-spacing:2.8px;
  text-transform:uppercase;
}
.eyebrow:before,.eyebrow:after{
  content:"";
  width:25px;
  height:1px;
  background:var(--violet);
}
.hero h1{
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(43px,7vw,78px);
  font-weight:400;
  line-height:1.08;
  letter-spacing:-2px;
  margin:25px 0 22px;
}
.hero h1 em{color:var(--medium);font-weight:400}
.hero-description{
  max-width:750px;
  margin:auto;
  color:#71677E;
  font-size:15px;
  line-height:1.95;
}
.hero-description strong{color:var(--purple)}
.hero-divider{
  width:58px;
  height:2px;
  margin:32px auto;
  background:linear-gradient(90deg,var(--purple),var(--violet));
  transform-origin:center;
  animation:lineGrow 1s .4s ease both;
}
.hero-statement{
  max-width:650px;
  margin:auto;
  color:var(--purple);
  font-family:var(--serif);
  font-size:clamp(20px,3vw,27px);
  line-height:1.5;
}
.hero-meta{
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:15px 28px;
  margin-top:35px;
}
.meta-item{
  display:flex;
  align-items:center;
  gap:8px;
  color:var(--medium);
  font-size:11px;
  font-weight:700;
}
.meta-dot{
  width:7px;height:7px;
  border-radius:50%;
  background:var(--violet);
}

/* MAIN */

.main{
  max-width:1000px;
  margin:auto;
  padding:0 24px 90px;
}
.intro-panel{
  position:relative;
  margin-top:-23px;
  padding:32px 36px;
  background:white;
  border:1px solid var(--line);
  border-radius:16px;
  box-shadow:var(--shadow);
  display:grid;
  grid-template-columns:1fr auto;
  align-items:center;
  gap:20px;
  animation:fadeUp .8s .15s ease both;
}
.intro-panel h2{
  color:var(--dark);
  font-family:var(--serif);
  font-size:27px;
  font-weight:400;
  margin:0 0 5px;
}
.intro-panel p{color:var(--muted);font-size:12px;margin:0}
.intro-number{
  color:var(--lavender);
  font-family:var(--serif);
  font-size:62px;
  line-height:1;
}

/* SIX LARGE EDITORIAL BOXES */

.understanding{
  margin-top:76px;
}
.section-heading{
  text-align:center;
  margin-bottom:34px;
}
.section-heading h2{
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(30px,4vw,39px);
  font-weight:400;
  margin:12px 0 8px;
}
.section-heading p{
  color:var(--muted);
  font-size:13px;
  margin:0;
  line-height:1.8;
}
.feature-list{
  display:flex;
  flex-direction:column;
  gap:15px;
}
.feature-box{
  position:relative;
  min-height:142px;
  padding:28px 34px;
  display:grid;
  grid-template-columns:1fr 100px;
  align-items:center;
  gap:25px;
  border:1px solid var(--line);
  border-radius:3px;
  overflow:hidden;
  box-shadow:0 8px 28px rgba(48,32,68,.035);
  transition:transform .45s cubic-bezier(.2,.8,.2,1),box-shadow .45s,border-color .35s;
}
.feature-box:hover{
  transform:translateX(8px);
  box-shadow:0 18px 38px rgba(48,32,68,.11);
}
.feature-box:before{
  content:"";
  position:absolute;
  top:0;left:0;
  width:4px;height:100%;
  transform:scaleY(0);
  transform-origin:bottom;
  transition:transform .4s ease;
}
.feature-box:hover:before{transform:scaleY(1)}
.feature-box.light{
  background:#fff;
  color:var(--dark);
  border-color:#E9E1F0;
}
.feature-box.light:before{background:var(--purple-medium)}
.feature-box.dark{
  background:linear-gradient(115deg,#302044,#49316F 70%,#59417A);
  color:#fff;
  border-color:#49316F;
}
.feature-box.dark:before{background:#DCD0ED}
.feature-copy{position:relative;z-index:1}
.feature-kicker{
  display:block;
  font-size:9px;
  font-weight:800;
  letter-spacing:2px;
  text-transform:uppercase;
  margin-bottom:7px;
}
.light .feature-kicker{color:var(--light)}
.dark .feature-kicker{color:#CDBBE5}
.feature-box h3{
  font-family:var(--serif);
  font-size:clamp(24px,3vw,32px);
  font-weight:400;
  line-height:1.25;
  margin:0 0 7px;
}
.feature-box p{
  max-width:720px;
  font-size:12px;
  line-height:1.8;
  margin:0;
}
.light p{color:var(--muted)}
.dark p{color:#E0D7EA}
.feature-number{
  position:relative;
  z-index:1;
  justify-self:end;
  font-family:var(--serif);
  font-size:clamp(55px,7vw,75px);
  line-height:1;
  font-weight:400;
  transition:transform .5s ease,opacity .5s;
}
.light .feature-number{color:#DCCFED}
.dark .feature-number{color:rgba(224,211,241,.55)}
.feature-box:hover .feature-number{transform:scale(1.1) rotate(-4deg)}
.feature-box:nth-child(odd){transform:translateY(18px);opacity:0}
.feature-box:nth-child(even){transform:translateY(18px);opacity:0}
.feature-box.revealed{
  transform:translateY(0);
  opacity:1;
}
.feature-box:nth-child(odd).revealed{transition-delay:.05s}
.feature-box:nth-child(even).revealed{transition-delay:.13s}

/* AUDIT */

.audit-area{margin-top:95px}
.audit-heading{text-align:center;margin-bottom:28px}
.audit-heading h2{
  color:var(--dark);
  font-family:var(--serif);
  font-size:36px;
  font-weight:400;
  margin:10px 0 5px;
}
.audit-heading p{color:var(--muted);font-size:12px;margin:0}
.progress-panel{
  padding:19px 22px;
  margin-bottom:16px;
  background:rgba(255,255,255,.9);
  border:1px solid var(--line);
  border-radius:12px;
}
.progress-top{
  display:flex;
  justify-content:space-between;
  gap:12px;
  margin-bottom:11px;
}
.progress-label{color:var(--purple);font-size:11px;font-weight:800}
.progress-percent{color:var(--muted);font-size:11px}
.progress-track{height:5px;background:var(--soft);border-radius:20px;overflow:hidden}
.progress-fill{
  width:0;height:100%;
  background:linear-gradient(90deg,var(--purple),var(--violet));
  border-radius:20px;
  transition:width .55s cubic-bezier(.2,.8,.2,1);
}
.question-card{
  position:relative;
  overflow:hidden;
  min-height:355px;
  padding:38px 42px 35px;
  background:white;
  border:1px solid rgba(104,73,149,.15);
  border-radius:16px;
  box-shadow:var(--shadow);
  animation:fadeUp .45s ease both;
}
.question-card:after{
  content:"";
  position:absolute;
  width:190px;height:190px;
  right:-105px;bottom:-105px;
  border:1px solid rgba(177,154,210,.35);
  border-radius:50%;
  box-shadow:0 0 0 20px rgba(177,154,210,.06),0 0 0 42px rgba(177,154,210,.035);
  pointer-events:none;
}
.question-top{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:12px;
  margin-bottom:25px;
}
.dimension-tag{
  display:inline-block;
  padding:7px 13px;
  background:var(--soft);
  color:var(--purple);
  border-radius:30px;
  font-size:9px;
  font-weight:800;
  letter-spacing:1.5px;
  text-transform:uppercase;
}
.question-index{color:var(--violet);font-family:var(--serif);font-size:19px}
.question-title{
  max-width:660px;
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(24px,4vw,33px);
  font-weight:400;
  line-height:1.35;
  margin:0 0 10px;
}
.question-description{max-width:620px;color:var(--muted);font-size:13px;margin:0 0 29px}
.scale{
  position:relative;
  z-index:1;
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:10px;
}
.scale-option{
  min-height:83px;
  padding:12px 5px;
  background:#FDFCFE;
  color:var(--purple);
  border:1px solid var(--line);
  border-radius:10px;
  cursor:pointer;
  transition:transform .25s,border .25s,background .25s,box-shadow .25s;
}
.scale-option:hover{
  transform:translateY(-5px);
  border-color:var(--violet);
  box-shadow:0 9px 22px rgba(73,49,111,.1);
}
.scale-option.selected{
  color:white;
  background:linear-gradient(145deg,var(--dark),var(--medium));
  border-color:var(--purple);
  box-shadow:0 8px 22px rgba(73,49,111,.22);
  transform:translateY(-3px);
}
.scale-option strong{display:block;font-family:var(--serif);font-size:25px;font-weight:400}
.scale-option span{display:block;font-size:9px;line-height:1.35}
.scale-hint{display:flex;justify-content:space-between;gap:10px;color:#A39AAA;font-size:10px;margin-top:12px}
.error{display:none;color:#A64C58;font-size:11px;margin-top:13px}
.navigation{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-top:20px}

/* BUTTONS */

.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:9px;
  padding:14px 24px;
  border:0;
  border-radius:40px;
  cursor:pointer;
  font-size:11px;
  font-weight:800;
  letter-spacing:.5px;
  transition:transform .25s,box-shadow .25s,background .25s;
}
.btn:hover:not(:disabled){transform:translateY(-3px);box-shadow:0 10px 22px rgba(48,32,68,.15)}
.btn:disabled{opacity:.35;cursor:not-allowed}
.btn-primary{color:white;background:linear-gradient(120deg,var(--dark),var(--medium))}
.btn-light{color:var(--purple);background:var(--soft)}

/* RESULTS */

.results{animation:fadeUp .7s ease both}
.result-card{
  padding:39px;
  background:white;
  border:1px solid var(--line);
  border-radius:18px;
  box-shadow:var(--shadow);
}
.result-heading{text-align:center}
.result-heading h2{
  color:var(--dark);
  font-family:var(--serif);
  font-size:37px;
  font-weight:400;
  margin:9px 0 4px;
}
.result-heading p{color:var(--muted);font-size:12px;margin:0}
.score-circle{
  position:relative;
  display:grid;
  place-items:center;
  width:190px;height:190px;
  margin:30px auto 20px;
  border-radius:50%;
  background:conic-gradient(var(--medium) var(--score),var(--soft) var(--score));
  animation:scoreIn .9s ease both;
}
.score-circle:before{
  content:"";
  position:absolute;
  width:162px;height:162px;
  background:white;
  border-radius:50%;
}
.score-content{position:relative;z-index:1;text-align:center}
.score-number{display:block;color:var(--dark);font-family:var(--serif);font-size:57px;line-height:1}
.score-out-of{display:block;color:var(--muted);font-size:10px;margin-top:5px}
.result-level-wrap{text-align:center}
.result-level{
  display:inline-block;
  padding:9px 17px;
  background:var(--soft);
  color:var(--purple);
  border:1px solid var(--lavender);
  border-radius:30px;
  font-size:11px;
  font-weight:800;
}
.result-summary{max-width:620px;color:var(--muted);text-align:center;font-size:13px;margin:17px auto 0}
.section-title{
  color:var(--dark);
  font-family:var(--serif);
  font-size:26px;
  font-weight:400;
  margin:36px 0 18px;
}
.dimension-result{margin-bottom:19px}
.dimension-top{display:flex;justify-content:space-between;gap:12px;font-size:12px;margin-bottom:7px}
.dimension-top strong{color:var(--purple);font-weight:700}
.dimension-top span{color:var(--medium);font-weight:800}
.dimension-track{height:7px;background:var(--soft);border-radius:20px;overflow:hidden}
.dimension-fill{
  height:100%;
  background:linear-gradient(90deg,var(--purple),var(--violet));
  border-radius:20px;
  animation:barIn .9s ease both;
}
.insight-grid{display:grid;grid-template-columns:1fr 1fr;gap:13px;margin-top:25px}
.insight{padding:19px;background:var(--pale);border:1px solid var(--line);border-radius:12px}
.insight small{display:block;color:var(--muted);font-size:9px;font-weight:800;letter-spacing:1.3px;text-transform:uppercase;margin-bottom:7px}
.insight strong{color:var(--purple);font-size:13px}
.recommendation{
  padding:17px 19px;
  margin-bottom:11px;
  background:#FAF8FC;
  border-left:3px solid var(--violet);
  border-radius:0 12px 12px 0;
}
.recommendation h4{color:var(--purple);font-size:12px;margin:0 0 6px}
.recommendation p{color:var(--muted);font-size:12px;margin:0}
.disclaimer{max-width:650px;color:#9991A0;text-align:center;font-size:10px;margin:25px auto 0}
.result-actions{display:flex;justify-content:center;flex-wrap:wrap;gap:10px;margin-top:23px}

/* PROFESSIONAL SECTION */

.professional-section{
  position:relative;
  overflow:hidden;
  margin-top:24px;
  padding:43px 42px;
  background:radial-gradient(circle at 100% 0%,rgba(177,154,210,.27),transparent 35%),linear-gradient(135deg,#F1EAF8,#FAF7FC);
  border:1px solid #E4D8F0;
  border-radius:18px;
}
.professional-section:after{
  content:"";
  position:absolute;
  width:230px;height:230px;
  right:-130px;bottom:-140px;
  border:1px solid rgba(104,73,149,.18);
  border-radius:50%;
  box-shadow:0 0 0 25px rgba(104,73,149,.035);
  pointer-events:none;
}
.professional-content{position:relative;z-index:1;max-width:720px}
.professional-section h3{
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(27px,4vw,36px);
  line-height:1.25;
  font-weight:400;
  margin:14px 0 13px;
}
.professional-section p{color:#70677D;font-size:13px;line-height:1.9;margin:0 0 14px}
.professional-section p strong{color:var(--purple)}
.professional-note{
  padding-left:17px;
  border-left:2px solid var(--violet);
  color:var(--purple)!important;
  font-family:var(--serif);
  font-size:19px!important;
  line-height:1.55!important;
  margin:22px 0!important;
}

/* FINAL CTA */

.cta{
  position:relative;
  overflow:hidden;
  margin-top:23px;
  padding:43px 30px;
  background:radial-gradient(circle at 90% 0%,rgba(177,154,210,.26),transparent 36%),linear-gradient(130deg,#302044,#49316F 65%,#65488E);
  border-radius:18px;
  color:white;
  text-align:center;
}
.cta .eyebrow{color:#DCCFED}
.cta .eyebrow:before,.cta .eyebrow:after{background:#BDA9D7}
.cta h3{font-family:var(--serif);font-size:32px;font-weight:400;margin:13px 0}
.cta p{max-width:540px;color:#E0D8E9;font-size:12px;margin:0 auto 22px}
.cta .btn{color:var(--purple);background:white}
.cta .btn:hover{background:var(--soft)}

/* FOOTER */

.footer{
  padding:31px 20px;
  text-align:center;
  background:white;
  border-top:1px solid var(--line);
}
.footer img{width:180px;max-height:65px;object-fit:contain;margin-bottom:7px}
.footer p{color:var(--muted);font-size:10px;margin:0}
.hidden{display:none!important}

/* MOBILE */

@media(max-width:650px){
  .header-inner{min-height:85px;padding:9px 16px;gap:10px}
  .logo{width:185px;max-height:67px}
  .header-note{font-size:7px;letter-spacing:.8px}
  .header-note span{font-size:7px;letter-spacing:.6px}
  .hero{padding:67px 18px 57px}
  .hero h1{letter-spacing:-1px}
  .hero-description{font-size:13px}
  .hero-meta{gap:13px 18px}
  .meta-item{font-size:10px}
  .main{padding:0 14px 55px}
  .intro-panel{grid-template-columns:1fr;padding:23px;text-align:center}
  .intro-number{display:none}
  .understanding{margin-top:53px}
  .section-heading{margin-bottom:25px}
  .section-heading p{font-size:12px}
  .feature-list{gap:10px}
  .feature-box{
    min-height:130px;
    padding:23px 19px;
    grid-template-columns:1fr 58px;
    gap:10px;
  }
  .feature-box h3{font-size:24px}
  .feature-box p{font-size:11px;line-height:1.65}
  .feature-number{font-size:49px}
  .audit-area{margin-top:70px}
  .audit-heading h2{font-size:29px}
  .question-card{min-height:auto;padding:25px 19px}
  .question-title{font-size:25px}
  .scale{gap:5px}
  .scale-option{min-height:72px;padding:8px 2px}
  .scale-option strong{font-size:20px}
  .scale-option span{font-size:8px}
  .scale-hint{font-size:8px}
  .navigation .btn{padding:12px 15px;font-size:10px}
  .result-card{padding:25px 19px}
  .result-heading h2{font-size:30px}
  .insight-grid{grid-template-columns:1fr}
  .result-actions .btn{width:100%}
  .professional-section{padding:31px 23px}
  .professional-section h3{font-size:29px}
  .cta{padding:34px 21px}
  .cta h3{font-size:27px}
}

@media(prefers-reduced-motion:reduce){
  *,*:before,*:after{
    scroll-behavior:auto!important;
    animation-duration:.01ms!important;
    animation-iteration-count:1!important;
    transition-duration:.01ms!important;
  }
}

/* PRINT */

@media print{
  body{background:white}
  .header{background:white}
  .hero,.intro-panel,.understanding,.audit-area,.footer,.result-actions{display:none!important}
  .main{max-width:100%;padding:10px}
  .result-card{box-shadow:none;border:0}
  .professional-section,.cta{break-inside:avoid}
  .cta{background:white;border:1px solid #DDD;color:var(--dark)}
  .cta p{color:#555}
  .recommendation,.insight{break-inside:avoid}
}
</style>
</head>

<body>
<div class="ambient one"></div>
<div class="ambient two"></div>

<header class="header">
  <div class="header-inner">
    <a class="brand-link" href="https://marianapastean.my.canva.site/mariana-pastean-portfolio" aria-label="ARVANA Digital Marketing">
      <img
        class="logo"
        src="./Logo%20-%20ARVANA%20Digital%20Marketing%20(1).png"
        alt="ARVANA Digital Marketing"
        onerror="this.style.display='none';document.getElementById('logoFallback').style.display='block';">
      <span id="logoFallback" class="logo-fallback">ARVANA</span>
    </a>
    <div class="header-note">
      Strategic Marketing
      <span>&amp; Brand Development</span>
    </div>
  </div>
</header>

<section class="hero">
  <div class="hero-inner">
    <div class="eyebrow">Un instrument pentru businessul tău</div>
    <h1>Înainte de marketing,<br>ai nevoie de <em>claritate.</em></h1>
    <p class="hero-description">
      Un business se dezvoltă mai bine atunci când îi cunoști activitatea,
      publicul și valoarea pe care o oferă. Înainte să alegi cum comunici,
      unde investești sau cum îți promovezi brandul, este important să înțelegi
      <strong>ce reprezintă businessul tău și în ce direcție vrei să îl dezvolți.</strong>
    </p>
    <div class="hero-divider"></div>
    <p class="hero-statement">Claritatea este primul pas către un marketing construit cu sens.</p>
    <div class="hero-meta">
      <div class="meta-item"><span class="meta-dot"></span>15 întrebări</div>
      <div class="meta-item"><span class="meta-dot"></span>5 dimensiuni</div>
      <div class="meta-item"><span class="meta-dot"></span>Raport personalizat</div>
      <div class="meta-item"><span class="meta-dot"></span>Gratuit</div>
    </div>
  </div>
</section>

<main class="main">

  <section class="intro-panel">
    <div>
      <h2>Începe cu o perspectivă mai clară.</h2>
      <p>Evaluează fundația brandului și a activităților tale de marketing. Răspunde sincer, în funcție de situația actuală a businessului.</p>
    </div>
    <div class="intro-number">01</div>
  </section>

  <!-- SIX VISUAL BOXES -->
  <section class="understanding">
    <div class="section-heading">
      <div class="eyebrow">Înțelege înainte să acționezi</div>
      <h2>Un business cunoscut înseamnă un business mai bine construit.</h2>
      <p>Șase repere care te ajută să privești activitatea ta dintr-o perspectivă mai clară.</p>
    </div>

    <div class="feature-list">

      <article class="feature-box light">
        <div class="feature-copy">
          <span class="feature-kicker">Primul reper</span>
          <h3>Cunoaște-ți activitatea.</h3>
          <p>Înțelege ce faci, ce valoare aduci și care sunt obiectivele reale ale businessului tău. O direcție bună începe cu o imagine clară asupra prezentului.</p>
        </div>
        <div class="feature-number">01</div>
      </article>

      <article class="feature-box dark">
        <div class="feature-copy">
          <span class="feature-kicker">Al doilea reper</span>
          <h3>Înțelege-ți publicul.</h3>
          <p>Descoperă cui te adresezi, ce nevoi are și ce îl determină să aleagă un produs sau un serviciu. Comunicarea relevantă pornește de la oameni.</p>
        </div>
        <div class="feature-number">02</div>
      </article>

      <article class="feature-box light">
        <div class="feature-copy">
          <span class="feature-kicker">Al treilea reper</span>
          <h3>Clarifică-ți oferta.</h3>
          <p>Definește ce oferi, ce problemă rezolvi și de ce soluția ta contează. O ofertă bine înțeleasă este mai ușor de comunicat și de diferențiat.</p>
        </div>
        <div class="feature-number">03</div>
      </article>

      <article class="feature-box dark">
        <div class="feature-copy">
          <span class="feature-kicker">Al patrulea reper</span>
          <h3>Construiește un brand coerent.</h3>
          <p>Identitatea vizuală, personalitatea și valorile brandului trebuie să transmită aceeași idee. Coerența creează recunoaștere și încredere.</p>
        </div>
        <div class="feature-number">04</div>
      </article>

      <article class="feature-box light">
        <div class="feature-copy">
          <span class="feature-kicker">Al cincilea reper</span>
          <h3>Comunică cu intenție.</h3>
          <p>Fiecare mesaj și fiecare material de conținut ar trebui să aibă un rol. Nu este vorba doar despre a fi prezent, ci despre a transmite ceva relevant.</p>
        </div>
        <div class="feature-number">05</div>
      </article>

      <article class="feature-box dark">
        <div class="feature-copy">
          <span class="feature-kicker">Al șaselea reper</span>
          <h3>Alege o direcție strategică.</h3>
          <p>Conectează obiectivele, poziționarea, comunicarea și acțiunile de marketing într-un plan coerent. Astfel, deciziile au un scop și pot fi evaluate.</p>
        </div>
        <div class="feature-number">06</div>
      </article>

    </div>
  </section>

  <!-- AUDIT QUESTIONS -->
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
      <button class="btn btn-light" id="prevBtn" type="button" disabled>← Înapoi</button>
      <button class="btn btn-primary" id="nextBtn" type="button" disabled>Următoarea întrebare →</button>
    </div>
    <div class="error" id="errorMessage" role="alert">Selectează un răspuns pentru a continua.</div>
  </section>

  <!-- RESULTS -->
  <section id="results" class="results hidden">
    <div class="result-card">
      <div class="result-heading">
        <div class="eyebrow">Rezultatul evaluării</div>
        <h2>Imaginea de ansamblu.</h2>
        <p>ARVANA BRAND &amp; MARKETING AUDIT</p>
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
        Acest raport este generat pe baza răspunsurilor oferite și are scop orientativ.
        Reprezintă o autoevaluare, nu un audit profesional complet, o analiză de piață
        sau o evaluare comparativă cu alte businessuri.
      </p>

      <div class="result-actions">
        <button class="btn btn-primary" id="copyReportBtn" type="button">Copiază raportul</button>
        <button class="btn btn-light" id="pdfBtn" type="button">Salvează PDF</button>
        <button class="btn btn-light" id="restartBtn" type="button">Reia evaluarea</button>
      </div>
    </div>

    <section class="professional-section">
      <div class="professional-content">
        <div class="eyebrow">Dincolo de autoevaluare</div>
        <h3>Uneori, următorul pas nu este să faci mai mult. Este să înțelegi mai bine ce ai de făcut.</h3>
        <p>Rezultatele acestui audit îți oferă un prim reper. Însă fiecare business are propriul context: obiective, resurse, public, concurență și provocări.</p>
        <p><strong>O discuție cu un profesionist în marketing</strong> te poate ajuta să privești aceste elemente în ansamblu, să identifici cauzele din spatele problemelor și să stabilești ce merită prioritizat.</p>
        <p>Nu orice business are nevoie de mai mult conținut, de încă o platformă sau de o campanie nouă. Uneori, are nevoie de o poziționare mai clară, de o ofertă mai bine definită sau de o strategie care să conecteze toate acțiunile de marketing.</p>
        <p class="professional-note">O perspectivă profesionistă nu înlocuiește cunoașterea propriului business. Te ajută să o transformi într-o direcție mai clară și în decizii mai bine fundamentate.</p>
        <a class="btn btn-primary" href="https://marianapastean.my.canva.site/mariana-pastean-portfolio" target="_blank" rel="noopener noreferrer">Descoperă serviciile ARVANA →</a>
      </div>
    </section>

    <section class="cta">
      <div class="eyebrow">ARVANA Digital Marketing</div>
      <h3>Direcție clară. Branduri cu valoare.</h3>
      <p>Dacă simți că businessul tău are nevoie de mai multă claritate în strategie, branding sau comunicare, descoperă abordarea ARVANA.</p>
      <a class="btn" href="https://marianapastean.my.canva.site/mariana-pastean-portfolio" target="_blank" rel="noopener noreferrer">Descoperă ARVANA →</a>
    </section>
  </section>
</main>

<footer class="footer">
  <img src="./Logo%20-%20ARVANA%20Digital%20Marketing%20(1).png" alt="ARVANA Digital Marketing" onerror="this.style.display='none';">
  <p>Direcție clară. Branduri cu valoare.</p>
</footer>

<script>
/* DIMENSIUNI ȘI RECOMANDĂRI */

const dimensions = [
  {
    name:"Poziționare",
    recommendations:[
      "Definește cât mai precis publicul căruia i te adresezi. Identifică nevoile, provocările și motivațiile clienților potriviți.",
      "Clarifică oferta: ce problemă rezolvă, ce valoare oferă și de ce ar alege un client businessul tău.",
      "Identifică elementele care diferențiază businessul tău. Construiește un mesaj de poziționare simplu, relevant și ușor de înțeles."
    ]
  },
  {
    name:"Identitate de brand",
    recommendations:[
      "Stabilește un sistem vizual coerent: logo, paletă cromatică, tipografie și reguli de utilizare. Aplică-l consecvent în toate materialele.",
      "Definește personalitatea brandului și valorile pe care dorești să le transmită. Acestea trebuie să se reflecte în limbaj, design și comportament.",
      "Analizează experiența oferită clientului în toate punctele de contact: website, social media, comunicare și interacțiunea directă."
    ]
  },
  {
    name:"Comunicare",
    recommendations:[
      "Construiește un mesaj central care explică limpede cine ești, ce oferi și cui te adresezi. Elimină formulările care nu transmit valoare concretă.",
      "Creează reguli de comunicare și un ton al vocii recognoscibil. Asigură-te că mesajele sunt coerente pe toate canalele.",
      "Pornește de la întrebările și preocupările publicului. Comunică beneficii, soluții și perspective relevante, nu doar informații despre produse sau servicii."
    ]
  },
  {
    name:"Strategie de conținut",
    recommendations:[
      "Definește 3–5 piloni de conținut care susțin poziționarea brandului și răspund intereselor publicului tău.",
      "Planifică fiecare material în funcție de un obiectiv: vizibilitate, educare, încredere, interacțiune sau conversie.",
      "Urmărește performanța conținutului prin indicatori relevanți. Analizează ce funcționează și ajustează planul în consecință."
    ]
  },
  {
    name:"Strategie de marketing",
    recommendations:[
      "Stabilește obiective de marketing concrete și măsurabile. Leagă activitățile de marketing de obiectivele reale ale businessului.",
      "Alege canalele în funcție de public, resurse și obiective. Nu este necesar să fii prezent peste tot dacă nu poți susține o comunicare relevantă.",
      "Construiește un proces periodic de analiză. Evaluează rezultatele, identifică blocajele și ajustează acțiunile în funcție de date."
    ]
  }
];

/* CELE 15 ÎNTREBĂRI */

const questions = [
  {dimension:0,title:"Știi exact cui se adresează businessul tău?",description:"Ai definit publicul țintă prin nevoi, comportamente și caracteristici relevante?"},
  {dimension:0,title:"Poți explica simplu ce valoare oferă businessul tău?",description:"Este clar ce problemă rezolvi și de ce oferta ta este relevantă?"},
  {dimension:0,title:"Știi ce diferențiază brandul tău de alternativele existente?",description:"Poți identifica motive concrete pentru care un client ar trebui să te aleagă?"},
  {dimension:1,title:"Identitatea vizuală este consecventă pe toate canalele?",description:"Logo-ul, culorile, fonturile și materialele transmit aceeași direcție vizuală?"},
  {dimension:1,title:"Brandul tău are o personalitate și valori clar definite?",description:"Știi ce dorești să transmită brandul și cum vrei să fie perceput?"},
  {dimension:1,title:"Experiența oferită clienților este coerentă?",description:"Există continuitate între promisiunea brandului și experiența reală?"},
  {dimension:2,title:"Mesajele tale explică limpede ce oferi și cui te adresezi?",description:"Un potențial client poate înțelege rapid valoarea serviciilor sau produselor tale?"},
  {dimension:2,title:"Comunicarea brandului este consecventă?",description:"Tonul vocii și mesajele sunt recognoscibile pe canalele folosite?"},
  {dimension:2,title:"Conținutul tău răspunde nevoilor și întrebărilor publicului?",description:"Comunici subiecte relevante pentru potențialii clienți, nu doar despre businessul tău?"},
  {dimension:3,title:"Ai piloni de conținut bine definiți?",description:"Știi care sunt principalele teme pe care trebuie să le abordezi?"},
  {dimension:3,title:"Planifici conținutul în funcție de obiective?",description:"Fiecare material are un rol clar în comunicarea și marketingul businessului?"},
  {dimension:3,title:"Analizezi rezultatele conținutului publicat?",description:"Urmărești indicatori și folosești concluziile pentru a îmbunătăți conținutul?"},
  {dimension:4,title:"Ai obiective de marketing clare și măsurabile?",description:"Știi ce rezultate urmărești și cum vei evalua progresul?"},
  {dimension:4,title:"Ai ales canalele de marketing potrivite businessului tău?",description:"Canalele folosite sunt relevante pentru public și pentru obiectivele tale?"},
  {dimension:4,title:"Analizezi și optimizezi periodic activitățile de marketing?",description:"Evaluezi rezultatele și adaptezi acțiunile în funcție de ceea ce observi?"}
];

const scaleLabels=["Deloc","În mică măsură","Parțial","În mare măsură","Complet"];
let answers=Array(questions.length).fill(null);
let currentQuestion=0;
let finalReport="";

const questionContainer=document.getElementById("questionContainer");
const nextBtn=document.getElementById("nextBtn");
const prevBtn=document.getElementById("prevBtn");

/* ANIMAȚIA CASETELOR LA SCROLL */

const revealObserver=new IntersectionObserver((entries,observer)=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add("revealed");
      observer.unobserve(entry.target);
    }
  });
},{threshold:.14});

document.querySelectorAll(".feature-box").forEach(box=>{
  revealObserver.observe(box);
});

/* AFIȘARE ÎNTREBĂRI */

function renderQuestion(){
  const question=questions[currentQuestion];
  const dimension=dimensions[question.dimension];
  const completed=answers.filter(value=>value!==null).length;
  const percentage=Math.round(completed/questions.length*100);

  document.getElementById("progressText").textContent=
    `Întrebarea ${currentQuestion+1} din ${questions.length}`;
  document.getElementById("progressPercent").textContent=
    `${percentage}% completat`;
  document.getElementById("progressFill").style.width=`${percentage}%`;

  questionContainer.innerHTML=`
    <div class="question-card">
      <div class="question-top">
        <span class="dimension-tag">${dimension.name}</span>
        <span class="question-index">${String(currentQuestion+1).padStart(2,"0")} / 15</span>
      </div>
      <h3 class="question-title">${question.title}</h3>
      <p class="question-description">${question.description}</p>
      <div class="scale">
        ${scaleLabels.map((label,index)=>`
          <button
            type="button"
            class="scale-option ${answers[currentQuestion]===index+1?"selected":""}"
            data-value="${index+1}"
            aria-pressed="${answers[currentQuestion]===index+1}"
            aria-label="${index+1}: ${label}">
            <strong>${index+1}</strong>
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

  questionContainer.querySelectorAll(".scale-option").forEach(button=>{
    button.addEventListener("click",()=>{
      answers[currentQuestion]=Number(button.dataset.value);
      document.getElementById("errorMessage").style.display="none";
      renderQuestion();
    });
  });

  prevBtn.disabled=currentQuestion===0;
  nextBtn.disabled=answers[currentQuestion]===null;
  nextBtn.textContent=currentQuestion===questions.length-1
    ?"Vezi raportul →"
    :"Următoarea întrebare →";
}

/* CALCUL SCORURI */

function calculateScores(){
  return dimensions.map((dimension,index)=>{
    const values=questions
      .map((question,i)=>({dimension:question.dimension,answer:answers[i]}))
      .filter(item=>item.dimension===index)
      .map(item=>item.answer);

    const average=values.reduce((sum,value)=>sum+value,0)/values.length;
    return Math.round(average/5*100);
  });
}

function getScoreLevel(score){
  if(score<=39){
    return {
      title:"Este nevoie de mai multă claritate",
      summary:"Rezultatele indică mai multe zone care au nevoie de structură. Înainte de a intensifica activitățile de marketing, merită să clarifici fundația brandului și direcția businessului."
    };
  }
  if(score<=59){
    return {
      title:"Fundație în curs de consolidare",
      summary:"Există elemente deja conturate, însă unele dimensiuni au nevoie de mai multă coerență și consecvență. O abordare structurată te poate ajuta să construiești o direcție mai clară."
    };
  }
  if(score<=79){
    return {
      title:"Direcție bună, cu oportunități de optimizare",
      summary:"Businessul tău are o bază relativ bine definită. Următorul pas este să identifici punctele care pot fi îmbunătățite și să conectezi mai bine strategia, brandul și comunicarea."
    };
  }
  return {
    title:"Fundație bine definită",
    summary:"Răspunsurile indică un nivel ridicat de claritate și coerență. Menține această direcție prin analiză periodică, adaptare și optimizarea continuă a activităților."
  };
}

function buildRecommendations(scores){
  return scores
    .map((score,index)=>({score,index}))
    .sort((a,b)=>a.score-b.score)
    .slice(0,3)
    .map(item=>{
      let recommendationIndex=0;
      if(item.score>=60)recommendationIndex=1;
      if(item.score>=80)recommendationIndex=2;
      return {
        name:dimensions[item.index].name,
        score:item.score,
        text:dimensions[item.index].recommendations[recommendationIndex]
      };
    });
}

/* RAPORT TEXT */

function buildPlainTextReport(overall,level,scores,ranked,recommendations){
  let report="ARVANA BRAND & MARKETING AUDIT\n";
  report+="Direcție clară. Branduri cu valoare.\n\n";
  report+=`SCOR GENERAL: ${overall}/100\n${level.title}\n\n${level.summary}\n\n`;
  report+="SCOR PE DIMENSIUNI\n";
  scores.forEach((score,index)=>{
    report+=`${dimensions[index].name}: ${score}/100\n`;
  });
  report+="\nPUNCTUL FORTE\n";
  report+=`${dimensions[ranked[0].index].name} (${ranked[0].score}/100)\n`;
  report+="\nPRIORITATE DE ÎMBUNĂTĂȚIRE\n";
  report+=`${dimensions[ranked[ranked.length-1].index].name} (${ranked[ranked.length-1].score}/100)\n`;
  report+="\nRECOMANDĂRI\n";
  recommendations.forEach((item,index)=>{
    report+=`\n${index+1}. ${item.name} (${item.score}/100)\n${item.text}\n`;
  });
  report+="\nNotă: Acest raport este o autoevaluare orientativă, nu un audit profesional complet.\n";
  report+="ARVANA DIGITAL MARKETING\n";
  return report;
}

/* GENERARE REZULTATE */

function generateResults(){
  const scores=calculateScores();
  const overall=Math.round(
    answers.reduce((sum,value)=>sum+value,0)/answers.length/5*100
  );
  const level=getScoreLevel(overall);
  const ranked=scores.map((score,index)=>({score,index})).sort((a,b)=>b.score-a.score);

  document.getElementById("overallScore").textContent=overall;
  document.getElementById("scoreCircle").style.setProperty("--score",`${overall*3.6}deg`);
  document.getElementById("resultLevel").textContent=level.title;
  document.getElementById("resultSummary").textContent=level.summary;

  document.getElementById("dimensionResults").innerHTML=scores.map((score,index)=>`
    <div class="dimension-result">
      <div class="dimension-top">
        <strong>${dimensions[index].name}</strong>
        <span>${score}/100</span>
      </div>
      <div class="dimension-track">
        <div class="dimension-fill" style="width:${score}%"></div>
      </div>
    </div>
  `).join("");

  document.getElementById("strongestArea").textContent=
    `${dimensions[ranked[0].index].name} (${ranked[0].score}/100)`;
  document.getElementById("weakestArea").textContent=
    `${dimensions[ranked[ranked.length-1].index].name} (${ranked[ranked.length-1].score}/100)`;

  const recommendations=buildRecommendations(scores);
  document.getElementById("recommendations").innerHTML=recommendations.map((item,index)=>`
    <div class="recommendation">
      <h4>${index+1}. ${item.name} — ${item.score}/100</h4>
      <p>${item.text}</p>
    </div>
  `).join("");

  finalReport=buildPlainTextReport(overall,level,scores,ranked,recommendations);

  document.getElementById("audit").classList.add("hidden");
  document.getElementById("results").classList.remove("hidden");
  window.scrollTo({top:0,behavior:"smooth"});
}

/* COPIERE RAPORT */

async function copyReport(){
  try{
    await navigator.clipboard.writeText(finalReport);
    alert("Raportul a fost copiat cu succes.");
  }catch(error){
    const textArea=document.createElement("textarea");
    textArea.value=finalReport;
    document.body.appendChild(textArea);
    textArea.select();
    document.execCommand("copy");
    textArea.remove();
    alert("Raportul a fost copiat.");
  }
}

/* REIA TESTUL */

function restartAudit(){
  answers=Array(questions.length).fill(null);
  currentQuestion=0;
  finalReport="";
  document.getElementById("results").classList.add("hidden");
  document.getElementById("audit").classList.remove("hidden");
  renderQuestion();
  document.getElementById("audit").scrollIntoView({behavior:"smooth",block:"start"});
}

/* NAVIGARE */

nextBtn.addEventListener("click",()=>{
  if(answers[currentQuestion]===null){
    document.getElementById("errorMessage").style.display="block";
    return;
  }

  if(currentQuestion<questions.length-1){
    currentQuestion++;
    renderQuestion();
    document.getElementById("audit").scrollIntoView({behavior:"smooth",block:"start"});
  }else{
    generateResults();
  }
});

prevBtn.addEventListener("click",()=>{
  if(currentQuestion>0){
    currentQuestion--;
    renderQuestion();
  }
});

document.getElementById("copyReportBtn").addEventListener("click",copyReport);
document.getElementById("pdfBtn").addEventListener("click",()=>window.print());
document.getElementById("restartBtn").addEventListener("click",restartAudit);

/* INITIALIZARE */

renderQuestion();
</script>
</body>
</html>
