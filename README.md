
<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#302044">
<meta name="description" content="ARVANA Brand & Marketing Audit – descoperă cât de clar și coerent este construit brandul și marketingul businessului tău.">
<title>ARVANA | Brand & Marketing Audit</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@400;500;600;700;800&family=Playfair+Display:wght@400;500;600&display=swap" rel="stylesheet">

<style>
:root{
  --dark:#2D1D40;
  --purple:#49316F;
  --medium:#67478E;
  --light:#9478B8;
  --violet:#B9A3D7;
  --lavender:#E2D7EF;
  --pale:#F8F5FB;
  --white:#fff;
  --ink:#382C44;
  --muted:#857B90;
  --line:#E9E1F0;
  --serif:"Playfair Display",Georgia,serif;
  --sans:"Manrope",sans-serif;
  --body:"DM Sans",sans-serif;
  --shadow:0 22px 65px rgba(48,32,68,.10);
}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;
  color:var(--ink);
  background:#FCFAFD;
  font-family:var(--body);
  line-height:1.7;
  overflow-x:hidden;
}
button{font:inherit}
a{color:inherit;text-decoration:none}
button:focus-visible,a:focus-visible{outline:3px solid var(--violet);outline-offset:4px}

/* GLOBAL ATMOSPHERE */

.ambient{
  position:fixed;
  z-index:-2;
  pointer-events:none;
  border-radius:50%;
  filter:blur(100px);
  opacity:.34;
}
.ambient.a{width:420px;height:420px;background:#D8C5EC;top:10%;left:-260px;animation:ambientA 18s ease-in-out infinite alternate}
.ambient.b{width:380px;height:380px;background:#C5B0DF;top:58%;right:-240px;animation:ambientB 21s ease-in-out infinite alternate}
.ambient.c{width:300px;height:300px;background:#E8DDF2;bottom:0;left:35%;animation:ambientA 24s ease-in-out infinite alternate-reverse}

@keyframes ambientA{
  from{transform:translate(0,0) scale(1)}
  to{transform:translate(70px,60px) scale(1.18)}
}
@keyframes ambientB{
  from{transform:translate(0,0) scale(1)}
  to{transform:translate(-60px,80px) scale(1.15)}
}
@keyframes float{
  0%,100%{transform:translate3d(0,0,0) rotate(0)}
  50%{transform:translate3d(0,-18px,0) rotate(5deg)}
}
@keyframes floatReverse{
  0%,100%{transform:translate3d(0,0,0) rotate(0)}
  50%{transform:translate3d(12px,17px,0) rotate(-8deg)}
}
@keyframes rotateSlow{to{transform:rotate(360deg)}}
@keyframes pulse{
  0%,100%{opacity:.25;transform:scale(.94)}
  50%{opacity:.65;transform:scale(1.06)}
}
@keyframes fadeUp{
  from{opacity:0;transform:translateY(35px)}
  to{opacity:1;transform:translateY(0)}
}
@keyframes fadeIn{
  from{opacity:0}
  to{opacity:1}
}
@keyframes revealLine{
  from{transform:scaleX(0)}
  to{transform:scaleX(1)}
}
@keyframes shimmer{
  0%{background-position:-200% center}
  100%{background-position:200% center}
}
@keyframes barIn{
  from{width:0}
}
@keyframes scoreIn{
  from{opacity:0;transform:scale(.7) rotate(-20deg)}
  to{opacity:1;transform:scale(1) rotate(0)}
}

/* ABSTRACT DECORATIONS */

.orb{
  position:absolute;
  pointer-events:none;
  border-radius:50%;
  border:1px solid rgba(255,255,255,.32);
}
.orb:after{
  content:"";
  position:absolute;
  inset:14px;
  border:1px solid rgba(255,255,255,.20);
  border-radius:50%;
}
.orb-one{width:125px;height:125px;top:18%;right:9%;animation:float 9s ease-in-out infinite}
.orb-two{width:75px;height:75px;bottom:17%;left:7%;animation:floatReverse 8s ease-in-out infinite}
.orb-three{width:180px;height:180px;top:42%;right:-80px;animation:rotateSlow 55s linear infinite}
.orb-three:after{inset:28px}
.decor-ring{
  position:absolute;
  width:210px;height:210px;
  border:1px solid rgba(177,154,210,.35);
  border-radius:50%;
  pointer-events:none;
  animation:rotateSlow 65s linear infinite;
}
.decor-ring:before,.decor-ring:after{
  content:"";
  position:absolute;
  border:1px solid rgba(177,154,210,.25);
  border-radius:50%;
}
.decor-ring:before{inset:17px}
.decor-ring:after{inset:35px}

/* HEADER */

.header{
  position:relative;
  z-index:10;
  background:rgba(255,255,255,.91);
  backdrop-filter:blur(20px);
  border-bottom:1px solid rgba(73,49,111,.10);
}
.header-inner{
  max-width:1280px;
  min-height:116px;
  padding:12px 38px;
  margin:auto;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
}
.logo{
  display:block;
  width:275px;
  max-height:92px;
  object-fit:contain;
  object-position:left center;
  transition:transform .5s ease;
}
.brand-link:hover .logo{transform:scale(1.035)}
.logo-fallback{
  display:none;
  color:var(--purple);
  font-family:var(--sans);
  font-size:31px;
  font-weight:800;
  letter-spacing:5px;
}
.header-note{
  text-align:right;
  color:var(--purple);
  font-size:10px;
  font-weight:800;
  letter-spacing:2.3px;
  text-transform:uppercase;
}
.header-note span{
  display:block;
  margin-top:5px;
  color:var(--light);
  font-size:9px;
  letter-spacing:1.5px;
}

/* HERO */

.hero{
  position:relative;
  overflow:hidden;
  padding:105px 24px 105px;
  background:
    radial-gradient(ellipse at 80% 20%,rgba(177,154,210,.42),transparent 35%),
    radial-gradient(ellipse at 10% 85%,rgba(220,208,237,.5),transparent 35%),
    linear-gradient(135deg,#F3EDF9,#FCFAFD 55%,#EFE7F6);
}
.hero-inner{
  position:relative;
  z-index:2;
  max-width:970px;
  margin:auto;
  text-align:center;
  animation:fadeUp 1s ease both;
}
.eyebrow{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:12px;
  color:var(--medium);
  font-size:10px;
  font-weight:800;
  letter-spacing:2.8px;
  text-transform:uppercase;
}
.eyebrow:before,.eyebrow:after{
  content:"";
  width:28px;height:1px;
  background:var(--violet);
}
.hero h1{
  margin:26px 0 23px;
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(45px,7vw,82px);
  font-weight:400;
  line-height:1.08;
  letter-spacing:-2px;
}
.hero h1 em{color:var(--medium);font-weight:400}
.hero-description{
  max-width:760px;
  margin:auto;
  color:#766C83;
  font-size:15px;
  line-height:2;
}
.hero-description strong{color:var(--purple)}
.hero-divider{
  width:65px;height:2px;
  margin:34px auto;
  background:linear-gradient(90deg,var(--purple),var(--violet));
  transform-origin:center;
  animation:revealLine 1.2s .4s ease both;
}
.hero-statement{
  max-width:680px;
  margin:auto;
  color:var(--purple);
  font-family:var(--serif);
  font-size:clamp(21px,3vw,28px);
  line-height:1.5;
}
.hero-meta{
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:14px 29px;
  margin-top:38px;
}
.meta-item{
  display:flex;
  align-items:center;
  gap:9px;
  color:var(--medium);
  font-size:11px;
  font-weight:700;
}
.meta-dot{
  width:7px;height:7px;
  border-radius:50%;
  background:var(--violet);
  box-shadow:0 0 0 4px rgba(177,154,210,.18);
}

/* MAIN */

.main{
  position:relative;
  max-width:1040px;
  margin:auto;
  padding:0 25px 100px;
}

/* CENTERED PURPLE INTRO BOX */

.intro-panel{
  position:relative;
  overflow:hidden;
  margin:-34px auto 0;
  max-width:950px;
  min-height:245px;
  padding:53px 65px;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  color:white;
  background:
    radial-gradient(circle at 90% 10%,rgba(194,172,223,.25),transparent 32%),
    radial-gradient(circle at 8% 95%,rgba(177,154,210,.20),transparent 36%),
    linear-gradient(125deg,#302044,#49316F 62%,#5D417F);
  border:1px solid rgba(255,255,255,.18);
  border-radius:4px;
  box-shadow:0 25px 65px rgba(48,32,68,.19);
  animation:fadeUp .9s .2s ease both;
}
.intro-panel:before,.intro-panel:after{
  content:"";
  position:absolute;
  border:1px solid rgba(229,217,243,.18);
  border-radius:50%;
  pointer-events:none;
}
.intro-panel:before{
  width:240px;height:240px;
  right:-90px;top:-130px;
  animation:rotateSlow 50s linear infinite;
}
.intro-panel:after{
  width:175px;height:175px;
  left:-80px;bottom:-110px;
  animation:floatReverse 12s ease-in-out infinite;
}
.intro-panel .decor-ring{
  width:125px;height:125px;
  top:50%;right:8%;
  transform:translateY(-50%);
  opacity:.55;
}
.intro-content{position:relative;z-index:2;max-width:710px}
.intro-panel .eyebrow{color:#DCCFED}
.intro-panel .eyebrow:before,.intro-panel .eyebrow:after{background:#BCA8D5}
.intro-panel h2{
  color:#fff;
  font-family:var(--serif);
  font-size:clamp(31px,4.5vw,45px);
  line-height:1.2;
  font-weight:400;
  margin:17px 0 15px;
}
.intro-panel p{
  max-width:660px;
  margin:auto;
  color:#E4DCEB;
  font-size:14px;
  line-height:1.9;
}

/* SIX EDITORIAL BOXES */

.understanding{margin-top:95px}
.section-heading{text-align:center;margin-bottom:38px}
.section-heading h2{
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(31px,4vw,42px);
  line-height:1.25;
  font-weight:400;
  margin:14px 0 10px;
}
.section-heading p{color:var(--muted);font-size:13px;margin:0}
.feature-list{display:flex;flex-direction:column;gap:15px}
.feature-box{
  position:relative;
  min-height:150px;
  padding:30px 38px;
  display:grid;
  grid-template-columns:1fr 105px;
  align-items:center;
  gap:25px;
  overflow:hidden;
  border:1px solid var(--line);
  border-radius:3px;
  box-shadow:0 9px 30px rgba(48,32,68,.035);
  opacity:0;
  transform:translateY(38px);
  transition:transform .65s cubic-bezier(.2,.8,.2,1),opacity .65s,box-shadow .4s;
}
.feature-box.revealed{opacity:1;transform:translateY(0)}
.feature-box:hover{
  transform:translateX(7px) translateY(-3px);
  box-shadow:0 20px 42px rgba(48,32,68,.12);
}
.feature-box:before{
  content:"";
  position:absolute;
  left:0;top:0;
  width:4px;height:100%;
  transform:scaleY(0);
  transform-origin:bottom;
  transition:transform .45s ease;
}
.feature-box:hover:before{transform:scaleY(1)}
.feature-box.light{background:#fff;color:var(--dark)}
.feature-box.light:before{background:var(--violet)}
.feature-box.dark{
  color:white;
  background:linear-gradient(115deg,#302044,#49316F 70%,#5A407A);
  border-color:#49316F;
}
.feature-box.dark:before{background:#DCD0ED}
.feature-copy{position:relative;z-index:2}
.feature-kicker{
  display:block;
  font-size:9px;
  font-weight:800;
  letter-spacing:2px;
  text-transform:uppercase;
  margin-bottom:8px;
}
.light .feature-kicker{color:var(--light)}
.dark .feature-kicker{color:#CDBBE5}
.feature-box h3{
  font-family:var(--serif);
  font-size:clamp(25px,3vw,33px);
  font-weight:400;
  line-height:1.25;
  margin:0 0 8px;
}
.feature-box p{max-width:740px;font-size:12px;line-height:1.9;margin:0}
.light p{color:var(--muted)}
.dark p{color:#E0D7EA}
.feature-number{
  justify-self:end;
  font-family:var(--serif);
  font-size:clamp(58px,7vw,79px);
  line-height:1;
  transition:transform .5s ease;
}
.light .feature-number{color:#DCCFED}
.dark .feature-number{color:rgba(224,211,241,.58)}
.feature-box:hover .feature-number{transform:scale(1.12) rotate(-5deg)}

/* AUDIT */

.audit-area{margin-top:105px}
.audit-heading{text-align:center;margin-bottom:30px}
.audit-heading h2{
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(31px,4vw,42px);
  font-weight:400;
  margin:13px 0 7px;
}
.audit-heading p{color:var(--muted);font-size:13px;margin:0}
.progress-panel{
  padding:19px 23px;
  margin-bottom:17px;
  background:white;
  border:1px solid var(--line);
  border-radius:5px;
}
.progress-top{display:flex;justify-content:space-between;gap:12px;margin-bottom:11px}
.progress-label{color:var(--purple);font-size:11px;font-weight:800}
.progress-percent{color:var(--muted);font-size:11px}
.progress-track{height:5px;background:var(--pale);border-radius:20px;overflow:hidden}
.progress-fill{
  width:0;height:100%;
  background:linear-gradient(90deg,var(--purple),var(--violet));
  border-radius:20px;
  transition:width .6s cubic-bezier(.2,.8,.2,1);
}
.question-card{
  position:relative;
  overflow:hidden;
  min-height:360px;
  padding:39px 43px;
  background:white;
  border:1px solid rgba(104,73,149,.15);
  border-radius:5px;
  box-shadow:var(--shadow);
  animation:fadeUp .5s ease both;
}
.question-card:after{
  content:"";
  position:absolute;
  width:200px;height:200px;
  right:-110px;bottom:-110px;
  border:1px solid rgba(177,154,210,.35);
  border-radius:50%;
  box-shadow:0 0 0 22px rgba(177,154,210,.06),0 0 0 45px rgba(177,154,210,.035);
  animation:float 10s ease-in-out infinite;
  pointer-events:none;
}
.question-top{display:flex;justify-content:space-between;align-items:center;margin-bottom:26px}
.dimension-tag{
  padding:7px 14px;
  background:var(--pale);
  color:var(--purple);
  border-radius:30px;
  font-size:9px;
  font-weight:800;
  letter-spacing:1.5px;
  text-transform:uppercase;
}
.question-index{color:var(--violet);font-family:var(--serif);font-size:20px}
.question-title{
  max-width:690px;
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(25px,4vw,34px);
  line-height:1.35;
  font-weight:400;
  margin:0 0 11px;
}
.question-description{max-width:640px;color:var(--muted);font-size:13px;margin:0 0 30px}
.scale{position:relative;z-index:1;display:grid;grid-template-columns:repeat(5,1fr);gap:10px}
.scale-option{
  min-height:84px;
  padding:12px 5px;
  background:#FDFCFE;
  color:var(--purple);
  border:1px solid var(--line);
  border-radius:5px;
  cursor:pointer;
  transition:transform .3s,border .3s,background .3s,box-shadow .3s;
}
.scale-option:hover{
  transform:translateY(-5px);
  border-color:var(--violet);
  box-shadow:0 10px 24px rgba(73,49,111,.10);
}
.scale-option.selected{
  color:white;
  background:linear-gradient(145deg,var(--dark),var(--medium));
  border-color:var(--purple);
  box-shadow:0 9px 23px rgba(73,49,111,.2);
  transform:translateY(-3px);
}
.scale-option strong{display:block;font-family:var(--serif);font-size:26px;font-weight:400}
.scale-option span{display:block;font-size:9px;line-height:1.4}
.scale-hint{display:flex;justify-content:space-between;gap:10px;color:#A39AAA;font-size:10px;margin-top:12px}
.error{display:none;color:#A64C58;font-size:11px;margin-top:13px}
.navigation{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-top:20px}

/* BUTTONS */

.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:9px;
  padding:14px 25px;
  border:0;
  border-radius:40px;
  cursor:pointer;
  font-size:11px;
  font-weight:800;
  letter-spacing:.4px;
  transition:transform .3s,box-shadow .3s,background .3s;
}
.btn:hover:not(:disabled){transform:translateY(-3px);box-shadow:0 12px 25px rgba(48,32,68,.17)}
.btn:disabled{opacity:.35;cursor:not-allowed}
.btn-primary{color:white;background:linear-gradient(120deg,var(--dark),var(--medium))}
.btn-light{color:var(--purple);background:var(--pale);border:1px solid var(--line)}

/* RESULTS */

.results{animation:fadeUp .7s ease both}
.result-card{
  padding:42px;
  background:white;
  border:1px solid var(--line);
  border-radius:6px;
  box-shadow:var(--shadow);
}
.result-heading{text-align:center}
.result-heading h2{
  color:var(--dark);
  font-family:var(--serif);
  font-size:39px;
  font-weight:400;
  margin:10px 0 4px;
}
.result-heading p{color:var(--muted);font-size:12px;margin:0}
.score-circle{
  position:relative;
  display:grid;
  place-items:center;
  width:190px;height:190px;
  margin:32px auto 20px;
  border-radius:50%;
  background:conic-gradient(var(--medium) var(--score),var(--pale) var(--score));
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
.score-out-of{display:block;color:var(--muted);font-size:10px;margin-top:6px}
.result-level-wrap{text-align:center}
.result-level{
  display:inline-block;
  padding:9px 18px;
  background:var(--pale);
  color:var(--purple);
  border:1px solid var(--lavender);
  border-radius:30px;
  font-size:11px;
  font-weight:800;
}
.result-summary{max-width:650px;color:var(--muted);text-align:center;font-size:13px;margin:18px auto 0}
.section-title{
  color:var(--dark);
  font-family:var(--serif);
  font-size:27px;
  font-weight:400;
  margin:38px 0 18px;
}
.dimension-result{margin-bottom:19px}
.dimension-top{display:flex;justify-content:space-between;gap:12px;font-size:12px;margin-bottom:7px}
.dimension-top strong{color:var(--purple)}
.dimension-top span{color:var(--medium);font-weight:800}
.dimension-track{height:7px;background:var(--pale);border-radius:20px;overflow:hidden}
.dimension-fill{
  height:100%;
  background:linear-gradient(90deg,var(--purple),var(--violet));
  border-radius:20px;
  animation:barIn 1s ease both;
}
.insight-grid{display:grid;grid-template-columns:1fr 1fr;gap:13px;margin-top:25px}
.insight{padding:20px;background:var(--pale);border:1px solid var(--line);border-radius:5px}
.insight small{display:block;color:var(--muted);font-size:9px;font-weight:800;letter-spacing:1.3px;text-transform:uppercase;margin-bottom:7px}
.insight strong{color:var(--purple);font-size:13px}
.recommendation{
  padding:18px 20px;
  margin-bottom:11px;
  background:#FAF8FC;
  border-left:3px solid var(--violet);
  border-radius:0 5px 5px 0;
}
.recommendation h4{color:var(--purple);font-size:12px;margin:0 0 6px}
.recommendation p{color:var(--muted);font-size:12px;margin:0}
.disclaimer{max-width:660px;color:#9991A0;text-align:center;font-size:10px;margin:25px auto 0}
.result-actions{display:flex;justify-content:center;flex-wrap:wrap;gap:10px;margin-top:25px}

/* PROFESSIONAL ADVICE */

.professional-section{
  position:relative;
  overflow:hidden;
  margin-top:25px;
  padding:47px 45px;
  background:
    radial-gradient(circle at 100% 0%,rgba(177,154,210,.28),transparent 35%),
    linear-gradient(130deg,#F0EAF7,#FCFAFD);
  border:1px solid #E4D8F0;
  border-radius:5px;
}
.professional-section:after{
  content:"";
  position:absolute;
  width:250px;height:250px;
  right:-130px;bottom:-150px;
  border:1px solid rgba(104,73,149,.18);
  border-radius:50%;
  box-shadow:0 0 0 25px rgba(104,73,149,.035);
  animation:rotateSlow 55s linear infinite;
  pointer-events:none;
}
.professional-content{position:relative;z-index:1;max-width:750px}
.professional-section h3{
  color:var(--dark);
  font-family:var(--serif);
  font-size:clamp(29px,4vw,39px);
  line-height:1.25;
  font-weight:400;
  margin:15px 0;
}
.professional-section p{color:#70677D;font-size:13px;line-height:1.95;margin:0 0 14px}
.professional-section p strong{color:var(--purple)}
.professional-note{
  padding-left:18px;
  border-left:2px solid var(--violet);
  color:var(--purple)!important;
  font-family:var(--serif);
  font-size:20px!important;
  line-height:1.6!important;
  margin:24px 0!important;
}

/* FINAL CTA */

.cta{
  position:relative;
  overflow:hidden;
  margin-top:24px;
  padding:49px 30px;
  background:
    radial-gradient(circle at 90% 0%,rgba(177,154,210,.28),transparent 35%),
    linear-gradient(130deg,#302044,#49316F 65%,#65488E);
  border-radius:5px;
  color:white;
  text-align:center;
}
.cta:before{
  content:"";
  position:absolute;
  width:190px;height:190px;
  left:-95px;bottom:-120px;
  border:1px solid rgba(255,255,255,.2);
  border-radius:50%;
  box-shadow:0 0 0 20px rgba(255,255,255,.04);
  animation:float 10s ease-in-out infinite;
}
.cta .eyebrow{color:#DCCFED}
.cta .eyebrow:before,.cta .eyebrow:after{background:#BDA9D7}
.cta h3{
  font-family:var(--serif);
  font-size:clamp(29px,4vw,38px);
  font-weight:400;
  margin:15px 0;
}
.cta p{max-width:560px;color:#E0D8E9;font-size:12px;margin:0 auto 24px}
.cta .btn{color:var(--purple);background:white}
.cta .btn:hover{background:var(--pale)}

/* FOOTER */

.footer{
  padding:33px 20px;
  text-align:center;
  background:white;
  border-top:1px solid var(--line);
}
.footer img{width:190px;max-height:65px;object-fit:contain;margin-bottom:8px}
.footer p{color:var(--muted);font-size:10px;margin:0}
.hidden{display:none!important}

/* RESPONSIVE */

@media(max-width:650px){
  .header-inner{min-height:85px;padding:9px 16px;gap:10px}
  .logo{width:185px;max-height:67px}
  .header-note{font-size:7px;letter-spacing:.8px}
  .header-note span{font-size:7px;letter-spacing:.6px}
  .hero{padding:70px 18px 65px}
  .hero h1{letter-spacing:-1px}
  .hero-description{font-size:13px}
  .hero-meta{gap:13px 18px}
  .meta-item{font-size:10px}
  .orb-one{right:-35px}
  .orb-two{left:-30px}
  .main{padding:0 14px 60px}
  .intro-panel{
    min-height:240px;
    padding:38px 23px;
    margin-top:-22px;
  }
  .intro-panel h2{font-size:32px}
  .intro-panel p{font-size:12px}
  .intro-panel .decor-ring{right:-35px;opacity:.35}
  .understanding{margin-top:65px}
  .section-heading{margin-bottom:25px}
  .section-heading p{font-size:12px}
  .feature-list{gap:10px}
  .feature-box{
    min-height:135px;
    padding:23px 19px;
    grid-template-columns:1fr 57px;
    gap:10px;
  }
  .feature-box h3{font-size:24px}
  .feature-box p{font-size:11px;line-height:1.7}
  .feature-number{font-size:48px}
  .audit-area{margin-top:75px}
  .audit-heading h2{font-size:30px}
  .question-card{min-height:auto;padding:26px 19px}
  .question-title{font-size:25px}
  .scale{gap:5px}
  .scale-option{min-height:73px;padding:8px 2px}
  .scale-option strong{font-size:20px}
  .scale-option span{font-size:8px}
  .scale-hint{font-size:8px}
  .navigation .btn{padding:12px 15px;font-size:10px}
  .result-card{padding:25px 19px}
  .result-heading h2{font-size:30px}
  .insight-grid{grid-template-columns:1fr}
  .result-actions .btn{width:100%}
  .professional-section{padding:32px 23px}
  .professional-section h3{font-size:29px}
  .cta{padding:38px 21px}
  .cta h3{font-size:28px}
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
  .header,.hero,.intro-panel,.understanding,.audit-area,.footer,.result-actions{display:none!important}
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

<div class="ambient a"></div>
<div class="ambient b"></div>
<div class="ambient c"></div>

<header class="header">
  <div class="header-inner">
    <a class="brand-link" href="https://marianapastean.my.canva.site/mariana-pastean-portfolio" aria-label="ARVANA Digital Marketing">
      <img class="logo"
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
  <div class="orb orb-one"></div>
  <div class="orb orb-two"></div>
  <div class="orb orb-three"></div>

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

  <!-- INTRO BOX -->
  <section class="intro-panel">
    <div class="decor-ring"></div>
    <div class="intro-content">
      <div class="eyebrow">Primul pas către o direcție mai bună</div>
      <h2>Începe cu o perspectivă mai clară.</h2>
      <p>
        Evaluează fundația brandului și a activităților tale de marketing.
        Răspunde sincer, în funcție de situația actuală a businessului.
        Înțelege ce funcționează, unde există oportunități și ce merită
        să devină prioritatea ta.
      </p>
    </div>
  </section>

  <!-- SIX EDITORIAL BOXES -->
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

  <!-- AUDIT -->
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
/* CONFIGURARE AUDIT */

const dimensions=[
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
      "Pornește de la întrebările și preocupările publicului. Comunică beneficii, soluții și perspective relevante."
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

const questions=[
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

/* ANIMAȚII LA SCROLL */

const revealObserver=new IntersectionObserver((entries,observer)=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add("revealed");
      observer.unobserve(entry.target);
    }
  });
},{threshold:.12});

document.querySelectorAll(".feature-box").forEach(box=>revealObserver.observe(box));

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
