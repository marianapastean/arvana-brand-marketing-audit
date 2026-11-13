
<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#302044">
<meta name="description" content="ARVANA Brand & Marketing Audit — evaluează fundația brandului și a activităților tale de marketing.">
<title>ARVANA | Brand & Marketing Audit</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&family=Lora:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500&display=swap" rel="stylesheet">

<style>
:root{
  --plum:#302044;
  --deep:#241532;
  --purple:#49316F;
  --violet:#67478E;
  --medium:#8064A5;
  --lavender:#B9A3D7;
  --pale:#F1EAF7;
  --pale2:#F9F6FB;
  --gold:#C5A46D;
  --gold-light:#E5D5B5;
  --white:#FFFFFF;
  --ink:#382C44;
  --muted:#71677D;
  --line:#E9E1F0;
  --serif:"Lora",Georgia,serif;
  --sans:"DM Sans",Arial,sans-serif;
  --shadow:0 22px 65px rgba(48,32,68,.10);
}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;
  font-family:var(--sans);
  color:var(--ink);
  background:#FCFAFD;
  overflow-x:hidden;
  font-size:17px;
  line-height:1.7;
}
button,input{font:inherit}
button{cursor:pointer}
a{color:inherit}
::selection{background:var(--lavender);color:var(--deep)}

.background-effects{
  position:fixed;
  inset:0;
  overflow:hidden;
  pointer-events:none;
  z-index:-1;
}
.orb{
  position:absolute;
  border-radius:50%;
  filter:blur(2px);
  opacity:.20;
  animation:float 13s ease-in-out infinite;
}
.orb.one{
  width:280px;height:280px;
  background:radial-gradient(circle,#B9A3D7,transparent 70%);
  top:12%;left:-130px;
}
.orb.two{
  width:340px;height:340px;
  background:radial-gradient(circle,#D9C8E8,transparent 70%);
  top:48%;right:-170px;
  animation-delay:-5s;
}
.orb.three{
  width:220px;height:220px;
  background:radial-gradient(circle,#C5A46D,transparent 70%);
  bottom:0;left:20%;
  opacity:.10;
  animation-delay:-8s;
}

@keyframes float{
  0%,100%{transform:translate3d(0,0,0) scale(1)}
  50%{transform:translate3d(18px,-28px,0) scale(1.08)}
}
@keyframes rotate{
  from{transform:rotate(0deg)}
  to{transform:rotate(360deg)}
}
@keyframes fadeUp{
  from{opacity:0;transform:translateY(24px)}
  to{opacity:1;transform:translateY(0)}
}
@keyframes fadeIn{
  from{opacity:0}
  to{opacity:1}
}
@keyframes scoreIn{
  from{opacity:0;transform:scale(.88)}
  to{opacity:1;transform:scale(1)}
}

/* HEADER */

.header{
  width:100%;
  min-height:112px;
  padding:12px 6%;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
  position:relative;
  z-index:5;
  background:rgba(255,255,255,.92);
  backdrop-filter:blur(18px);
  border-bottom:1px solid rgba(197,164,109,.30);
}
.brand{
  display:flex;
  align-items:center;
  text-decoration:none;
  min-width:0;
}
.logo-image{
  display:block;
  width:145px;
  height:100px;
  object-fit:contain;
  object-position:center;
  filter:drop-shadow(0 5px 10px rgba(48,32,68,.08));
  transition:transform .45s ease,filter .45s ease;
}
.brand:hover .logo-image{
  transform:scale(1.035);
  filter:drop-shadow(0 8px 14px rgba(48,32,68,.16));
}
.header-label{
  color:var(--muted);
  font-size:12px;
  line-height:1.7;
  letter-spacing:1.5px;
  text-transform:uppercase;
  text-align:right;
}

/* HOME / HERO MOV */

.hero{
  min-height:650px;
  position:relative;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:100px 24px 110px;
  overflow:hidden;
  background:
    radial-gradient(ellipse at 50% 110%,rgba(185,163,215,.23),transparent 48%),
    radial-gradient(circle at 90% 15%,rgba(197,164,109,.12),transparent 28%),
    linear-gradient(135deg,#241532 0%,#302044 48%,#49316F 100%);
}
.hero:before{
  content:"";
  position:absolute;
  width:510px;height:510px;
  border:1px solid rgba(229,213,181,.24);
  border-radius:50%;
  top:50%;left:50%;
  transform:translate(-50%,-50%);
  animation:rotate 65s linear infinite;
}
.hero:after{
  content:"";
  position:absolute;
  width:365px;height:365px;
  border:1px solid rgba(185,163,215,.24);
  border-radius:50%;
  top:50%;left:50%;
  transform:translate(-50%,-50%);
  animation:rotate 45s linear infinite reverse;
}
.hero-inner{
  position:relative;
  z-index:2;
  max-width:920px;
  text-align:center;
  animation:fadeUp 1s ease both;
}
.eyebrow{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:14px;
  width:100%;
  max-width:100%;
  margin:0 auto 25px;
  text-align:center;
  color:var(--violet);
  text-transform:uppercase;
  letter-spacing:2px;
  font-size:13px;
  font-weight:800;
  line-height:1.5;
}
.eyebrow:before,.eyebrow:after{
  content:"";
  display:block;
  width:38px;
  height:1px;
  flex:0 0 38px;
  background:var(--gold);
}
.hero .eyebrow{color:var(--gold-light)}
.hero h1{
  font-family:var(--serif);
  font-size:clamp(48px,7vw,84px);
  line-height:1.15;
  font-weight:400;
  color:white;
  margin:0 auto 25px;
  letter-spacing:-1.5px;
}
.hero h1 span{color:#D7C3ED;font-style:italic}
.hero-description{
  max-width:720px;
  margin:0 auto;
  color:rgba(255,255,255,.87);
  font-size:18px;
  line-height:1.9;
}
.hero-note{
  margin:38px auto 0;
  font-size:13px;
  color:var(--gold-light);
  letter-spacing:1.7px;
  text-transform:uppercase;
  text-align:center;
}

/* GENERAL SECTIONS */

.container{width:min(1120px,90%);margin:0 auto}
.section{padding:90px 0}
.section-heading{
  max-width:760px;
  margin:0 auto 50px;
  text-align:center;
}
.section-heading h2{
  font-family:var(--serif);
  font-weight:400;
  color:var(--plum);
  font-size:clamp(38px,5vw,56px);
  line-height:1.25;
  margin:0 0 19px;
}
.section-heading p{
  color:var(--muted);
  font-size:17px;
  line-height:1.9;
  margin:0;
}

/* INTRO PANEL MOV */

.intro-wrap{padding:10px 0 80px}
.intro-panel{
  position:relative;
  overflow:hidden;
  padding:70px 55px;
  border-radius:32px;
  color:white;
  text-align:center;
  background:
    radial-gradient(circle at 90% 15%,rgba(197,164,109,.18),transparent 28%),
    radial-gradient(circle at 8% 100%,rgba(185,163,215,.18),transparent 35%),
    linear-gradient(130deg,#302044,#49316F 65%,#5A407A);
  border:1px solid rgba(229,213,181,.65);
  box-shadow:0 25px 65px rgba(48,32,68,.17);
}
.intro-panel:before{
  content:"";
  position:absolute;
  width:240px;height:240px;
  border:1px solid rgba(229,213,181,.25);
  border-radius:50%;
  right:-100px;top:-115px;
  animation:rotate 45s linear infinite;
}
.intro-panel:after{
  content:"";
  position:absolute;
  width:150px;height:150px;
  border:1px solid rgba(229,213,181,.22);
  border-radius:50%;
  left:-65px;bottom:-65px;
  animation:rotate 35s linear infinite reverse;
}
.intro-content{position:relative;z-index:1;max-width:800px;margin:auto}
.intro-panel .eyebrow{color:var(--gold-light)}
.intro-panel h2{
  font-family:var(--serif);
  font-weight:400;
  font-size:clamp(38px,5vw,59px);
  line-height:1.25;
  margin:0 0 24px;
}
.intro-panel p{
  font-size:17px;
  line-height:1.95;
  color:rgba(255,255,255,.90);
  margin:0;
}

/* FEATURE BOXES */

.features{
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:24px;
}
.feature-box{
  min-height:255px;
  padding:38px;
  position:relative;
  overflow:hidden;
  border-radius:27px;
  border:1px solid rgba(197,164,109,.62);
  transition:transform .45s ease,box-shadow .45s ease,border-color .45s ease;
  will-change:transform;
}
.feature-box:hover{
  transform:translateY(-7px);
  box-shadow:0 22px 45px rgba(48,32,68,.14);
  border-color:var(--gold);
}
.feature-box.light{
  background:linear-gradient(145deg,#FFFFFF,#FBF8FD);
  color:var(--plum);
}
.feature-box.dark{
  background:
    radial-gradient(circle at 90% 10%,rgba(197,164,109,.14),transparent 35%),
    linear-gradient(125deg,#302044,#49316F 70%,#5A407A);
  color:white;
  border-color:rgba(229,213,181,.58);
}
.feature-icon{
  width:56px;height:56px;
  display:grid;place-items:center;
  border:1px solid var(--gold);
  border-radius:18px;
  color:var(--violet);
  font-family:var(--serif);
  font-size:25px;
  margin-bottom:24px;
  transition:transform .4s ease,background .4s ease;
}
.feature-box:hover .feature-icon{
  transform:translateY(-3px) rotate(-5deg);
  background:rgba(197,164,109,.08);
}
.dark .feature-icon{color:var(--gold-light);border-color:rgba(229,213,181,.7)}
.feature-box h3{
  font-family:var(--serif);
  font-size:31px;
  font-weight:500;
  margin:0 0 14px;
}
.feature-box p{
  font-size:16px;
  line-height:1.85;
  opacity:.88;
  margin:0;
  max-width:460px;
}
.feature-decoration{
  position:absolute;
  width:100px;height:100px;
  right:-35px;bottom:-42px;
  border:1px solid rgba(197,164,109,.38);
  border-radius:50%;
  animation:rotate 35s linear infinite;
}
.feature-decoration:after{
  content:"";
  position:absolute;
  inset:12px;
  border:1px solid rgba(197,164,109,.25);
  border-radius:50%;
}

/* AUDIT INTRO */

.audit-intro{
  background:linear-gradient(180deg,transparent,#F5F0F9 100%);
  padding:75px 0;
}
.audit-intro-card{
  background:white;
  border:1px solid rgba(197,164,109,.58);
  border-radius:30px;
  padding:55px 48px;
  box-shadow:var(--shadow);
  text-align:center;
}
.audit-intro-card h2{
  font-family:var(--serif);
  font-size:clamp(37px,5vw,53px);
  font-weight:400;
  color:var(--plum);
  margin:0 0 20px;
  line-height:1.25;
}
.audit-intro-card p{
  max-width:760px;
  margin:0 auto;
  color:var(--muted);
  line-height:1.9;
  font-size:17px;
}

/* BUTTONS */

.primary-btn,.secondary-btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:12px;
  padding:18px 32px;
  border-radius:50px;
  border:1px solid var(--gold);
  font-size:13px;
  letter-spacing:1.2px;
  font-weight:800;
  text-transform:uppercase;
  text-decoration:none;
  transition:all .35s ease;
}
.primary-btn{
  color:white;
  background:linear-gradient(110deg,#49316F,#67478E,#49316F);
  background-size:200% auto;
  box-shadow:0 10px 30px rgba(73,49,111,.20);
}
.primary-btn:hover{
  background-position:right center;
  transform:translateY(-3px);
  box-shadow:0 15px 35px rgba(73,49,111,.28);
}
.secondary-btn{color:var(--purple);background:white}
.secondary-btn:hover{background:var(--pale);transform:translateY(-2px)}

/* AUDIT AREA */

.audit-area{padding:85px 0 100px;display:none}
.audit-area.active{display:block;animation:fadeIn .6s ease}
.progress-panel{
  background:white;
  border:1px solid rgba(197,164,109,.55);
  border-radius:25px;
  padding:28px 32px;
  margin-bottom:28px;
  box-shadow:0 12px 35px rgba(48,32,68,.05);
}
.progress-top{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
  margin-bottom:15px;
  font-size:13px;
  color:var(--muted);
  letter-spacing:1px;
  text-transform:uppercase;
}
.progress-track{height:9px;border-radius:20px;background:#EEE8F3;overflow:hidden}
.progress-fill{
  height:100%;width:0;
  border-radius:20px;
  background:linear-gradient(90deg,var(--purple),var(--lavender),var(--gold));
  transition:width .5s ease;
}
.audit-heading{text-align:center;margin:58px auto 38px}
.audit-heading .eyebrow{margin-bottom:16px}
.audit-heading h2{
  font-family:var(--serif);
  font-size:clamp(38px,5vw,53px);
  color:var(--plum);
  font-weight:400;
  margin:0 0 14px;
}
.audit-heading p{color:var(--muted);font-size:17px;line-height:1.8}

/* QUESTION CARDS */

.question-card{
  display:none;
  position:relative;
  background:white;
  padding:48px;
  border-radius:29px;
  border:1px solid rgba(197,164,109,.62);
  box-shadow:var(--shadow);
  overflow:hidden;
}
.question-card.active{display:block;animation:fadeUp .45s ease}
.question-category{
  color:var(--violet);
  text-transform:uppercase;
  letter-spacing:1.8px;
  font-size:13px;
  font-weight:800;
  margin-bottom:20px;
}
.question-card h3{
  font-family:var(--serif);
  color:var(--plum);
  font-size:clamp(30px,3.5vw,39px);
  line-height:1.4;
  font-weight:500;
  margin:0 0 34px;
}
.answer-options{display:grid;gap:14px}
.answer-option{
  display:flex;
  align-items:center;
  gap:17px;
  width:100%;
  text-align:left;
  padding:19px 21px;
  border:1px solid var(--line);
  border-radius:17px;
  color:var(--ink);
  background:#FEFCFF;
  transition:background .25s ease,border-color .25s ease,box-shadow .25s ease;
  font-size:16px;
  line-height:1.65;
}
.answer-option:hover{
  border-color:var(--gold);
  background:#FBF8FD;
}
.answer-option.selected{
  border-color:var(--violet);
  background:#F2ECF8;
  box-shadow:inset 0 0 0 1px var(--violet);
}
.answer-dot{
  width:25px;height:25px;
  min-width:25px;
  border:1px solid #C8BBD5;
  border-radius:50%;
  display:grid;
  place-items:center;
  font-size:12px;
  color:transparent;
}
.selected .answer-dot{
  background:var(--violet);
  color:white;
  border-color:var(--violet);
}
.question-navigation{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:15px;
  margin-top:35px;
}
.nav-button{
  border:1px solid var(--gold);
  border-radius:40px;
  padding:15px 25px;
  background:white;
  color:var(--purple);
  font-size:12px;
  letter-spacing:1px;
  font-weight:800;
  text-transform:uppercase;
  transition:.3s;
}
.nav-button.next{background:var(--purple);color:white}
.nav-button:hover:not(:disabled){transform:translateY(-2px)}
.nav-button:disabled{opacity:.35;cursor:not-allowed}

/* RESULTS */

.results{display:none;padding:80px 0 100px}
.results.active{display:block;animation:fadeIn .7s ease}
.results-header{text-align:center;margin-bottom:48px}
.results-header h2{
  font-family:var(--serif);
  color:var(--plum);
  font-size:clamp(40px,6vw,63px);
  font-weight:400;
  line-height:1.2;
  margin:0 0 17px;
}
.results-header p{color:var(--muted);font-size:17px;line-height:1.8}
.result-card{
  background:white;
  border:1px solid rgba(197,164,109,.60);
  border-radius:30px;
  padding:45px;
  box-shadow:var(--shadow);
  margin-bottom:27px;
  transition:transform .4s ease,box-shadow .4s ease;
}
.result-card:hover{box-shadow:0 25px 60px rgba(48,32,68,.12)}
.score-layout{
  display:grid;
  grid-template-columns:260px 1fr;
  align-items:center;
  gap:40px;
}
.score-circle{
  position:relative;
  display:grid;
  place-items:center;
  width:220px;height:220px;
  margin:auto;
  animation:scoreIn .9s ease both;
}
.score-svg{
  position:absolute;
  inset:0;
  width:100%;height:100%;
  transform:rotate(-90deg);
  overflow:visible;
}
.score-track{fill:none;stroke:#EAE2F1;stroke-width:9}
.score-progress{
  fill:none;
  stroke:var(--violet);
  stroke-width:9;
  stroke-linecap:round;
  stroke-dasharray:490.09;
  stroke-dashoffset:490.09;
  transition:stroke-dashoffset 1.5s ease;
}
.score-content{position:relative;z-index:2;text-align:center}
.score-number{
  display:block;
  font-family:var(--serif);
  font-size:72px;
  line-height:1.1;
  color:var(--plum);
}
.score-out-of{
  display:block;
  color:var(--muted);
  font-size:14px;
  letter-spacing:1px;
  margin-top:8px;
}
.score-summary h3{
  font-family:var(--serif);
  color:var(--plum);
  font-size:39px;
  font-weight:500;
  line-height:1.3;
  margin:0 0 14px;
}
.score-summary p{font-size:16px;color:var(--muted);line-height:1.9;margin:0}
.score-level{
  display:inline-block;
  margin-top:19px;
  padding:10px 18px;
  background:#F1EAF7;
  color:var(--violet);
  border-radius:40px;
  font-size:12px;
  letter-spacing:1px;
  font-weight:800;
  text-transform:uppercase;
}

/* DIMENSIONS */

.result-section-title{
  font-family:var(--serif);
  font-weight:400;
  color:var(--plum);
  font-size:clamp(32px,4vw,40px);
  line-height:1.3;
  margin:0 0 28px;
}
.dimension-list{display:grid;gap:27px}
.dimension-item{break-inside:avoid}
.dimension-top{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:12px;
  margin-bottom:11px;
}
.dimension-name{font-size:16px;font-weight:800;color:var(--ink)}
.dimension-score{color:var(--violet);font-size:15px;font-weight:800}
.dimension-track{
  height:12px;
  border-radius:30px;
  background:#EEE8F3;
  overflow:hidden;
}
.dimension-fill{
  height:100%;width:0;
  border-radius:30px;
  background:linear-gradient(90deg,#49316F,#9478B8,#C5A46D);
  transition:width 1.3s ease;
}
.dimension-description{margin-top:9px;color:var(--muted);font-size:14px;line-height:1.7}

/* INSIGHTS */

.insights-grid{
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:20px;
  margin-top:25px;
}
.insight{
  padding:28px;
  border-radius:23px;
  border:1px solid rgba(197,164,109,.55);
  background:#FBF9FD;
  break-inside:avoid;
  transition:transform .35s ease,box-shadow .35s ease;
}
.insight:hover,.recommendation:hover{
  transform:translateY(-4px);
  box-shadow:0 15px 32px rgba(48,32,68,.09);
}
.insight-label{
  font-size:12px;
  letter-spacing:1.8px;
  text-transform:uppercase;
  font-weight:800;
  color:var(--violet);
  margin-bottom:12px;
}
.insight h4{
  font-family:var(--serif);
  font-size:29px;
  line-height:1.3;
  font-weight:500;
  color:var(--plum);
  margin:0 0 10px;
}
.insight p{font-size:15px;line-height:1.8;color:var(--muted);margin:0}

/* RECOMMENDATIONS */

.recommendations{display:grid;gap:17px}
.recommendation{
  padding:27px;
  border-radius:22px;
  background:#FBF9FD;
  border:1px solid rgba(197,164,109,.52);
  break-inside:avoid;
  transition:transform .35s ease,box-shadow .35s ease;
}
.recommendation h4{
  font-family:var(--serif);
  font-size:28px;
  line-height:1.3;
  color:var(--plum);
  font-weight:500;
  margin:0 0 11px;
}
.recommendation p{font-size:15px;color:var(--muted);line-height:1.85;margin:0}

/* PROFESSIONAL SECTION */

.professional-section{
  position:relative;
  overflow:hidden;
  padding:60px;
  margin:30px 0;
  border-radius:30px;
  border:1px solid rgba(197,164,109,.68);
  background:
    radial-gradient(circle at 90% 10%,rgba(197,164,109,.15),transparent 35%),
    linear-gradient(135deg,#F5F0F9,#FFFFFF);
  text-align:center;
}
.professional-section .eyebrow{margin-bottom:20px}
.professional-section h3{
  font-family:var(--serif);
  font-weight:400;
  font-size:clamp(37px,5vw,52px);
  line-height:1.3;
  color:var(--plum);
  margin:0 auto 21px;
  max-width:760px;
}
.professional-section p{
  max-width:800px;
  margin:0 auto 22px;
  color:#6D6378;
  font-size:16px;
  line-height:1.95;
}
.professional-highlight{color:var(--violet);font-weight:800}

/* ACTIONS AND DISCLAIMER */

.result-actions{
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:15px;
  margin:32px auto;
}
.disclaimer{
  max-width:850px;
  text-align:center;
  margin:38px auto 0;
  font-size:13px;
  color:#766D80;
  line-height:1.8;
}

/* FOOTER */

.footer{
  background:var(--deep);
  color:white;
  padding:60px 6% 32px;
  text-align:center;
  position:relative;
  overflow:hidden;
}
.footer:before{
  content:"";
  position:absolute;
  width:300px;height:300px;
  border:1px solid rgba(197,164,109,.2);
  border-radius:50%;
  left:-170px;top:-170px;
  animation:rotate 55s linear infinite;
}
.footer-brand{
  font-family:var(--serif);
  font-size:38px;
  letter-spacing:4px;
  color:white;
  margin-bottom:8px;
}
.footer-subtitle{color:var(--gold-light);letter-spacing:3px;font-size:12px;margin-bottom:22px}
.footer-slogan{
  color:rgba(255,255,255,.82);
  font-family:var(--serif);
  font-size:27px;
  font-style:italic;
  margin-bottom:27px;
}
.footer-copy{font-size:13px;color:rgba(255,255,255,.62);margin-top:32px;line-height:1.8}
.footer-link{
  display:inline-block;
  color:var(--gold-light);
  font-size:13px;
  letter-spacing:1px;
  text-decoration:none;
  border-bottom:1px solid rgba(229,213,181,.5);
  padding-bottom:5px;
}

/* SCROLL ANIMATIONS */

.reveal{
  opacity:0;
  transform:translateY(28px) scale(.99);
  transition:opacity .8s ease,transform .8s cubic-bezier(.2,.7,.2,1);
}
.reveal.visible{opacity:1;transform:translateY(0) scale(1)}
.feature-box.reveal:nth-child(even){transition-delay:.08s}
.feature-box.reveal:nth-child(3n){transition-delay:.14s}
.result-card.reveal:nth-child(even){transition-delay:.08s}

/* MOBILE */

@media(max-width:760px){
  body{font-size:16px}
  .header{min-height:90px;padding:9px 5%}
  .logo-image{width:112px;height:80px}
  .header-label{font-size:10px;letter-spacing:1px}
  .hero{min-height:590px;padding:85px 21px}
  .hero:before{width:340px;height:340px}
  .hero:after{width:255px;height:255px}
  .hero h1{font-size:clamp(43px,11vw,64px);letter-spacing:-.7px}
  .hero-description{font-size:16px;line-height:1.9}
  .hero-note{font-size:12px;line-height:1.7}
  .eyebrow{
    width:100%;
    max-width:100%;
    gap:9px;
    font-size:11px;
    letter-spacing:1.2px;
    text-align:center;
    justify-content:center;
    line-height:1.55;
    margin-left:auto;
    margin-right:auto;
  }
  .eyebrow:before,.eyebrow:after{
    width:21px;
    flex:0 0 21px;
    min-width:21px;
  }
  .section{padding:68px 0}
  .section-heading{margin-bottom:35px}
  .section-heading h2{font-size:clamp(35px,9vw,45px)}
  .section-heading p{font-size:16px}
  .intro-wrap{padding-bottom:58px}
  .intro-panel{padding:50px 24px;border-radius:26px}
  .intro-panel h2{font-size:clamp(35px,9vw,45px)}
  .intro-panel p{font-size:16px;line-height:1.9}
  .features{grid-template-columns:1fr;gap:18px}
  .feature-box{min-height:220px;padding:30px;border-radius:24px}
  .feature-box h3{font-size:29px}
  .feature-box p{font-size:16px;line-height:1.85}
  .audit-intro{padding:58px 0}
  .audit-intro-card{padding:42px 24px;border-radius:25px}
  .audit-intro-card h2{font-size:clamp(35px,9vw,45px)}
  .audit-intro-card p{font-size:16px}
  .primary-btn,.secondary-btn{font-size:12px;padding:17px 23px}
  .audit-area{padding:58px 0 75px}
  .progress-panel{padding:22px;border-radius:21px}
  .progress-top{font-size:11px}
  .audit-heading{margin:45px auto 30px}
  .audit-heading h2{font-size:clamp(35px,9vw,45px)}
  .audit-heading p{font-size:16px}
  .question-card{padding:31px 22px;border-radius:23px}
  .question-category{font-size:12px;line-height:1.7}
  .question-card h3{font-size:29px;line-height:1.4}
  .answer-option{padding:16px;font-size:15px;line-height:1.65;gap:13px}
  .answer-dot{width:24px;height:24px;min-width:24px}
  .question-navigation{gap:10px;margin-top:27px}
  .nav-button{padding:14px 16px;font-size:11px}
  .results{padding:58px 0 75px}
  .results-header h2{font-size:clamp(36px,9vw,48px)}
  .results-header p{font-size:16px}
  .result-card{padding:30px 22px;border-radius:24px}
  .score-layout{grid-template-columns:1fr;gap:25px;text-align:center}
  .score-circle{width:190px;height:190px}
  .score-number{font-size:65px}
  .score-summary h3{font-size:33px}
  .score-summary p{font-size:15px}
  .result-section-title{font-size:32px}
  .dimension-name{font-size:15px}
  .dimension-score{font-size:14px}
  .dimension-description{font-size:14px}
  .insights-grid{grid-template-columns:1fr}
  .insight{padding:25px}
  .insight h4{font-size:27px}
  .insight p{font-size:15px}
  .recommendation{padding:24px}
  .recommendation h4{font-size:26px}
  .recommendation p{font-size:15px}
  .professional-section{padding:45px 23px;border-radius:25px}
  .professional-section h3{font-size:clamp(34px,9vw,43px)}
  .professional-section p{font-size:15px;line-height:1.9}
  .result-actions{flex-direction:column;align-items:stretch}
  .result-actions a,.result-actions button{width:100%}
  .disclaimer{font-size:12px}
  .footer{padding:50px 20px 27px}
  .footer-slogan{font-size:24px}
  .footer-copy{font-size:12px}

  /* Animatiile raman vizibile si pe mobil */
  .reveal{
    transform:translateY(22px) scale(.99);
    transition:opacity .75s ease,transform .75s ease;
  }
}

@media(max-width:390px){
  .logo-image{width:98px;height:72px}
  .header-label{font-size:9px}
  .hero h1{font-size:41px}
  .hero-description{font-size:15px}
  .question-card h3{font-size:26px}
  .answer-option{font-size:14px;padding:14px}
  .nav-button{padding:13px 12px;font-size:10px}
  .feature-box{padding:26px}
}

/* PRINT / PDF */

@page{size:A4;margin:14mm}

@media print{
  html,body{
    background:#FFFFFF!important;
    color:#382C44!important;
    print-color-adjust:exact!important;
    -webkit-print-color-adjust:exact!important;
  }
  body{font-size:10pt}
  .background-effects,.header,.hero,.intro-wrap,.section,
  .audit-intro,.audit-area,.footer,.result-actions{
    display:none!important;
  }
  .container{width:100%;max-width:100%}
  .results{display:block!important;padding:0!important}
  .results-header{margin-bottom:22px}
  .results-header h2{font-size:31pt}
  .results-header p{font-size:9pt}
  .result-card{
    display:block!important;
    background:#FFFFFF!important;
    border:1px solid #D8C59F!important;
    border-radius:13px!important;
    padding:22px!important;
    margin-bottom:16px!important;
    box-shadow:none!important;
    break-inside:auto;
    opacity:1!important;
    transform:none!important;
  }
  .score-layout{grid-template-columns:190px 1fr!important;gap:20px!important}
  .score-circle{
    display:grid!important;
    width:170px!important;height:170px!important;
    margin:10px auto!important;
    break-inside:avoid;
    opacity:1!important;
    transform:none!important;
  }
  .score-svg{
    display:block!important;
    overflow:visible!important;
    print-color-adjust:exact!important;
    -webkit-print-color-adjust:exact!important;
  }
  .score-track{stroke:#EAE2F1!important}
  .score-progress{stroke:#67478E!important}
  .score-number{font-size:48pt!important}
  .score-summary h3{font-size:24pt!important}
  .score-summary p,.dimension-description,.insight p,.recommendation p{font-size:8.5pt!important}
  .dimension-item,.insight,.recommendation,.professional-section{break-inside:avoid!important}
  .dimension-track,.dimension-fill{
    print-color-adjust:exact!important;
    -webkit-print-color-adjust:exact!important;
  }
  .dimension-track{background:#EEE8F3!important}
  .dimension-fill{
    background:linear-gradient(90deg,#49316F,#9478B8,#C5A46D)!important;
  }
  .professional-section{
    margin-top:15px!important;
    padding:25px!important;
    background:#F5F0F9!important;
    border:1px solid #D8C59F!important;
    border-radius:13px!important;
    print-color-adjust:exact!important;
    -webkit-print-color-adjust:exact!important;
  }
  .professional-section h3{font-size:25pt!important}
  .professional-section p{font-size:9pt!important}
  .insight,.recommendation{
    background:#FBF9FD!important;
    print-color-adjust:exact!important;
    -webkit-print-color-adjust:exact!important;
  }
  .disclaimer{font-size:7.5pt!important;color:#857B90!important}
  .eyebrow{font-size:7pt!important}
  .reveal,.reveal.visible{opacity:1!important;transform:none!important}
}

@media(prefers-reduced-motion:reduce){
  *,*:before,*:after{
    animation-duration:.01ms!important;
    animation-iteration-count:1!important;
    transition-duration:.01ms!important;
    scroll-behavior:auto!important;
  }
}
</style>
</head>

<body>

<div class="background-effects" aria-hidden="true">
  <div class="orb one"></div>
  <div class="orb two"></div>
  <div class="orb three"></div>
</div>

<header class="header">
  <a class="brand" href="#" aria-label="ARVANA Digital Marketing">
    <img
      class="logo-image"
      src="https://raw.githubusercontent.com/marianapastean/arvana-brand-marketing-audit/main/Logo%20-%20ARVANA%20Digital%20Marketing%20%281%29.png"
      alt="ARVANA Digital Marketing"
      fetchpriority="high"
    >
  </a>
  <div class="header-label">
    Strategic Marketing<br>& Brand Development
  </div>
</header>

<!-- HOME PAGE MOV -->

<section class="hero">
  <div class="hero-inner">
    <div class="eyebrow">ARVANA · BRAND & MARKETING AUDIT</div>
    <h1>
      Înțelege-ți<br>
      businessul.<br>
      <span>Construiește cu direcție.</span>
    </h1>
    <p class="hero-description">
      Un brand puternic începe cu o înțelegere clară a propriei activități.
      Atunci când știi ce oferi, cui te adresezi și ce te diferențiază,
      poți lua decizii mai bune și poți construi o comunicare care are sens.
      Descoperă cât de bine este conturată fundația brandului și a marketingului tău.
    </p>
    <div class="hero-note">Un instrument gratuit pentru businessul tău</div>
  </div>
</section>

<!-- INTRO PANEL -->

<section class="intro-wrap">
  <div class="container">
    <div class="intro-panel reveal">
      <div class="intro-content">
        <div class="eyebrow">O perspectivă mai clară</div>
        <h2>Începe cu o perspectivă mai clară.</h2>
        <p>
          Evaluează fundația brandului și a activităților tale de marketing.
          Răspunde sincer, în funcție de situația actuală a businessului.
          Nu există răspunsuri corecte sau greșite. Important este să privești
          obiectiv modul în care funcționează astăzi activitatea ta.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- FEATURE BOXES -->

<section class="section">
  <div class="container">
    <div class="section-heading reveal">
      <div class="eyebrow">Ce vei descoperi</div>
      <h2>O imagine de ansamblu asupra brandului tău.</h2>
      <p>
        Evaluarea analizează șase perspective esențiale ale dezvoltării
        unui business, reunite în cinci dimensiuni de evaluare.
      </p>
    </div>

    <div class="features">
      <article class="feature-box light reveal">
        <div class="feature-icon">01</div>
        <h3>Poziționare</h3>
        <p>Cât de bine îți cunoști publicul, oferta, valoarea pe care o aduci și diferențele care te fac relevant în piață?</p>
        <div class="feature-decoration"></div>
      </article>

      <article class="feature-box dark reveal">
        <div class="feature-icon">02</div>
        <h3>Identitate de brand</h3>
        <p>Identitatea vizuală, personalitatea și experiența oferită transmit aceeași imagine și aceleași valori?</p>
        <div class="feature-decoration"></div>
      </article>

      <article class="feature-box light reveal">
        <div class="feature-icon">03</div>
        <h3>Comunicare</h3>
        <p>Mesajele tale sunt clare, consecvente și relevante pentru oamenii cărora dorești să te adresezi?</p>
        <div class="feature-decoration"></div>
      </article>

      <article class="feature-box dark reveal">
        <div class="feature-icon">04</div>
        <h3>Strategie de conținut</h3>
        <p>Conținutul este construit în jurul unor obiective și direcții clare sau publici fără un plan bine definit?</p>
        <div class="feature-decoration"></div>
      </article>

      <article class="feature-box light reveal">
        <div class="feature-icon">05</div>
        <h3>Strategie de marketing</h3>
        <p>Ai obiective măsurabile, alegi canalele potrivite și urmărești rezultatele acțiunilor tale?</p>
        <div class="feature-decoration"></div>
      </article>

      <article class="feature-box dark reveal">
        <div class="feature-icon">06</div>
        <h3>Direcție și dezvoltare</h3>
        <p>Deciziile de marketing sunt conectate la obiectivele businessului și susțin dezvoltarea sa pe termen lung?</p>
        <div class="feature-decoration"></div>
      </article>
    </div>
  </div>
</section>

<!-- AUDIT INTRODUCTION -->

<section class="audit-intro">
  <div class="container">
    <div class="audit-intro-card reveal">
      <div class="eyebrow">Primul pas către o direcție mai bună</div>
      <h2>Descoperă unde te afli acum.</h2>
      <p>
        Răspunde la 15 întrebări despre modul în care îți construiești
        brandul și îți desfășori activitățile de marketing.
        La final vei primi un scor orientativ, o evaluare pe fiecare
        dimensiune și recomandări pentru zonele care merită atenția ta.
      </p>
      <div style="margin-top:32px">
        <button class="primary-btn" id="startBtn" type="button" onclick="startAudit()">
          Începe evaluarea <span>→</span>
        </button>
      </div>
      <p style="margin-top:20px;font-size:14px;letter-spacing:.5px">
        15 întrebări · Aproximativ 5–7 minute · Gratuit
      </p>
    </div>
  </div>
</section>

<!-- AUDIT QUESTIONS -->

<section class="audit-area" id="auditArea">
  <div class="container">
    <div class="progress-panel">
      <div class="progress-top">
        <span>Progresul evaluării</span>
        <span id="progressText">0 din 15</span>
      </div>
      <div class="progress-track">
        <div class="progress-fill" id="progressFill"></div>
      </div>
    </div>

    <div class="audit-heading">
      <div class="eyebrow">Evaluarea ARVANA</div>
      <h2>Răspunde cu sinceritate.</h2>
      <p>Alege varianta care descrie cel mai bine situația actuală a businessului tău.</p>
    </div>

    <div id="questionContainer"></div>
  </div>
</section>

<!-- RESULTS -->

<section class="results" id="results">
  <div class="container">
    <div class="results-header">
      <div class="eyebrow">ARVANA · Rezultatul evaluării</div>
      <h2>O perspectivă asupra brandului tău.</h2>
      <p>Acesta este punctul de plecare pentru decizii mai clare și o dezvoltare mai coerentă.</p>
    </div>

    <div class="result-card">
      <div class="score-layout">
        <div class="score-circle" id="scoreCircle">
          <svg class="score-svg" viewBox="0 0 180 180" role="img" aria-label="Graficul scorului general">
            <circle class="score-track" cx="90" cy="90" r="78"/>
            <circle class="score-progress" id="scoreArc" cx="90" cy="90" r="78"/>
          </svg>
          <div class="score-content">
            <span class="score-number" id="overallScore">0</span>
            <span class="score-out-of">din 100 puncte</span>
          </div>
        </div>

        <div class="score-summary">
          <h3 id="scoreTitle">Rezultatul tău</h3>
          <p id="scoreDescription"></p>
          <div class="score-level" id="scoreLevel"></div>
        </div>
      </div>
    </div>

    <div class="result-card">
      <h3 class="result-section-title">Evaluarea pe dimensiuni</h3>
      <div class="dimension-list" id="dimensionResults"></div>
    </div>

    <div class="result-card">
      <h3 class="result-section-title">Ce îți spune rezultatul?</h3>
      <div class="insights-grid" id="insights"></div>
    </div>

    <div class="result-card">
      <h3 class="result-section-title">Direcții de îmbunătățire</h3>
      <p style="color:var(--muted);font-size:15px;line-height:1.8;margin-top:-12px;margin-bottom:25px">
        Aceste recomandări sunt orientative și se bazează pe răspunsurile tale.
      </p>
      <div class="recommendations" id="recommendations"></div>
    </div>

    <section class="professional-section reveal">
      <div class="eyebrow">Dincolo de evaluare</div>
      <h3>Uneori, următorul pas este să privești businessul dintr-o perspectivă nouă.</h3>
      <p>
        Un instrument de autoevaluare te poate ajuta să identifici anumite
        aspecte ale activității tale. Totuși, un rezultat nu surprinde
        întotdeauna toate provocările, oportunitățile sau particularitățile
        unui business.
      </p>
      <p>
        <span class="professional-highlight">O discuție cu un profesionist în marketing</span>
        poate aduce claritate asupra poziționării, identității de brand,
        comunicării și direcției de dezvoltare. Împreună, aceste elemente
        pot fi analizate în contextul real al activității tale și transformate
        într-o direcție de acțiune adaptată obiectivelor businessului.
      </p>
      <p>
        La ARVANA, abordarea pornește de la înțelegerea businessului,
        continuă cu strategia și se concretizează în decizii de brand
        și comunicare cu un scop clar.
      </p>
      <div style="margin-top:30px">
        <a class="primary-btn" href="https://marianapastean.my.canva.site/mariana-pastean-portfolio" target="_blank" rel="noopener">
          Descoperă portofoliul ARVANA <span>→</span>
        </a>
      </div>
    </section>

    <div class="result-actions">
      <button class="primary-btn" type="button" onclick="downloadPDF()">Salvează raportul PDF</button>
      <button class="secondary-btn" type="button" onclick="copyReport()">Copiază rezultatul</button>
      <button class="secondary-btn" type="button" onclick="restartAudit()">Reia evaluarea</button>
    </div>

    <p class="disclaimer">
      ARVANA BRAND & MARKETING AUDIT este un instrument gratuit de
      autoevaluare orientativă. Rezultatul se bazează exclusiv pe
      răspunsurile oferite și nu reprezintă un audit profesional,
      o analiză de piață sau o garanție a performanței businessului.
      Recomandările au caracter informativ.
    </p>
  </div>
</section>

<footer class="footer">
  <div class="footer-brand">ARVANA</div>
  <div class="footer-subtitle">DIGITAL MARKETING</div>
  <div class="footer-slogan">Direcție clară. Branduri cu valoare.</div>
  <a class="footer-link" href="https://marianapastean.my.canva.site/mariana-pastean-portfolio" target="_blank" rel="noopener">
    Explorează portofoliul
  </a>
  <div class="footer-copy">
    ARVANA Digital Marketing · Strategic Marketing & Brand Development<br>
    © <span id="year"></span> ARVANA. Toate drepturile rezervate.
  </div>
</footer>

<script>
/* DATELE CHESTIONARULUI */

const questions = [
  {
    dimension:"Poziționare",
    text:"Cât de clar ai definit publicul căruia te adresezi?",
    options:[
      "Nu am definit încă un public specific.",
      "Am o idee generală despre clienții mei.",
      "Cunosc principalele caracteristici ale publicului meu.",
      "Am definit clar publicul și nevoile sale.",
      "Am o imagine detaliată și actualizată asupra publicului meu."
    ]
  },
  {
    dimension:"Poziționare",
    text:"Cât de clară este oferta ta și valoarea pe care o oferi?",
    options:[
      "Oferta mea nu este încă bine definită.",
      "Știu ce ofer, dar îmi este greu să explic valoarea.",
      "Pot descrie oferta și beneficiile principale.",
      "Oferta este clară și conectată la nevoile clienților.",
      "Oferta și valoarea sunt foarte bine definite și diferențiate."
    ]
  },
  {
    dimension:"Poziționare",
    text:"Cât de bine știi ce diferențiază businessul tău de alternativele din piață?",
    options:[
      "Nu am identificat diferențiatorii.",
      "Am câteva idei, dar nu sunt clar conturate.",
      "Cunosc câteva elemente care mă diferențiază.",
      "Am o diferențiere clară și relevantă.",
      "Diferențierea este bine definită și susținută prin activitatea mea."
    ]
  },
  {
    dimension:"Identitate de brand",
    text:"Cât de coerentă este identitatea vizuală în toate materialele tale?",
    options:[
      "Nu am o identitate vizuală stabilită.",
      "Folosesc elemente vizuale diferite, fără reguli clare.",
      "Există câteva elemente vizuale constante.",
      "Am o identitate vizuală coerentă.",
      "Identitatea este documentată și aplicată consecvent."
    ]
  },
  {
    dimension:"Identitate de brand",
    text:"Cât de clară este personalitatea brandului tău?",
    options:[
      "Nu am definit personalitatea brandului.",
      "Am câteva idei despre cum vreau să fie perceput.",
      "Am identificat câteva valori și trăsături.",
      "Personalitatea și valorile sunt clar definite.",
      "Personalitatea brandului este clară și se reflectă în toate interacțiunile."
    ]
  },
  {
    dimension:"Identitate de brand",
    text:"Cât de bine reflectă experiența oferită de business promisiunea brandului?",
    options:[
      "Nu am analizat această legătură.",
      "Există diferențe între ceea ce comunic și ceea ce ofer.",
      "În general, experiența este apropiată de promisiune.",
      "Experiența susține în mod consecvent promisiunea.",
      "Fiecare etapă a experienței este gândită în acord cu brandul."
    ]
  },
  {
    dimension:"Comunicare",
    text:"Cât de ușor înțelege publicul ce oferi și de ce ar trebui să te aleagă?",
    options:[
      "Mesajele mele nu transmit suficient de clar oferta.",
      "Uneori este nevoie de explicații suplimentare.",
      "Mesajele sunt relativ clare.",
      "Comunicarea explică bine oferta și beneficiile.",
      "Mesajele sunt clare, diferențiate și ușor de reținut."
    ]
  },
  {
    dimension:"Comunicare",
    text:"Cât de consecvent comunici pe canalele pe care ești prezent?",
    options:[
      "Comunic doar ocazional.",
      "Public fără un ritm sau o direcție constantă.",
      "Am o anumită regularitate.",
      "Am un stil și un ritm de comunicare consecvente.",
      "Comunicarea este planificată și coerentă pe toate canalele relevante."
    ]
  },
  {
    dimension:"Comunicare",
    text:"Cât de relevante sunt mesajele tale pentru nevoile publicului?",
    options:[
      "Nu cunosc suficient nevoile publicului.",
      "Comunic mai ales despre produsele sau serviciile mele.",
      "Abordez uneori problemele și interesele publicului.",
      "Mesajele sunt construite în jurul nevoilor publicului.",
      "Comunicarea pornește constant de la insight-uri despre public."
    ]
  },
  {
    dimension:"Strategie de conținut",
    text:"Ai stabilit piloni sau teme principale pentru conținutul publicat?",
    options:[
      "Nu am stabilit teme de conținut.",
      "Public în funcție de ideile care îmi vin pe moment.",
      "Am câteva teme recurente.",
      "Am piloni de conținut definiți și relevanți.",
      "Pilonii sunt documentați și conectați la obiectivele businessului."
    ]
  },
  {
    dimension:"Strategie de conținut",
    text:"Cât de mult este planificat conținutul în funcție de obiective?",
    options:[
      "Nu planific conținutul.",
      "Planific doar ocazional.",
      "Am un plan simplu de publicare.",
      "Conținutul este planificat în funcție de obiective.",
      "Fiecare tip de conținut are un rol clar în parcursul clientului."
    ]
  },
  {
    dimension:"Strategie de conținut",
    text:"Analizezi performanța conținutului publicat?",
    options:[
      "Nu urmăresc rezultatele.",
      "Mă uit ocazional la aprecieri și vizualizări.",
      "Urmăresc câțiva indicatori de bază.",
      "Analizez periodic indicatorii relevanți.",
      "Folosesc datele pentru a îmbunătăți constant strategia de conținut."
    ]
  },
  {
    dimension:"Strategie de marketing",
    text:"Ai obiective de marketing clare și măsurabile?",
    options:[
      "Nu am stabilit obiective de marketing.",
      "Am obiective generale, fără indicatori.",
      "Am câteva obiective și indicatori de bază.",
      "Obiectivele sunt clare și măsurabile.",
      "Obiectivele sunt prioritizate, măsurate și revizuite periodic."
    ]
  },
  {
    dimension:"Strategie de marketing",
    text:"Cât de bine alegi canalele de marketing potrivite businessului tău?",
    options:[
      "Nu am o strategie pentru alegerea canalelor.",
      "Folosesc canale doar pentru că sunt populare.",
      "Am ales câteva canale care par potrivite.",
      "Canalele sunt alese în funcție de public și obiective.",
      "Am o strategie clară de distribuție și folosesc eficient canalele relevante."
    ]
  },
  {
    dimension:"Strategie de marketing",
    text:"Cât de des analizezi și optimizezi activitățile de marketing?",
    options:[
      "Nu analizez activitățile de marketing.",
      "Fac schimbări doar când apar probleme.",
      "Revizuiesc ocazional rezultatele.",
      "Analizez periodic și ajustez acțiunile.",
      "Am un proces constant de analiză, învățare și optimizare."
    ]
  }
];

const dimensions = [
  {name:"Poziționare",start:0,end:3,description:"Claritatea publicului, a ofertei și a diferențierii."},
  {name:"Identitate de brand",start:3,end:6,description:"Coerența identității vizuale, a personalității și a experienței."},
  {name:"Comunicare",start:6,end:9,description:"Claritatea, consecvența și relevanța mesajelor."},
  {name:"Strategie de conținut",start:9,end:12,description:"Planificarea, obiectivele și evaluarea conținutului."},
  {name:"Strategie de marketing",start:12,end:15,description:"Obiectivele, canalele și optimizarea activităților."}
];

const recommendations = {
  "Poziționare":{
    low:"Începe prin a clarifica publicul căruia te adresezi, problema pe care o rezolvi și valoarea concretă pe care o aduci. Analizează alternativele din piață și identifică diferențiatorii reali ai businessului.",
    medium:"Revizuiește modul în care prezinți oferta și diferențierea. Testează dacă mesajele tale sunt înțelese corect de public și dacă reflectă beneficiile reale.",
    high:"Consolidează poziționarea printr-o comunicare consecventă și verifică periodic dacă oferta rămâne relevantă pentru publicul vizat."
  },
  "Identitate de brand":{
    low:"Definește elementele fundamentale ale brandului: valori, personalitate, direcție vizuală și reguli de utilizare. Construiește o identitate coerentă, care să susțină poziționarea.",
    medium:"Uniformizează elementele vizuale și mesajele pe toate punctele de contact. Documentează regulile de bază pentru a păstra coerența.",
    high:"Evaluează periodic experiența brandului și păstrează aceeași promisiune în toate interacțiunile cu publicul."
  },
  "Comunicare":{
    low:"Clarifică mesajul principal al businessului. Explică simplu ce oferi, cui te adresezi și ce valoare aduci. Construiește o direcție de comunicare adaptată publicului.",
    medium:"Lucrează la consecvența mesajelor și la adaptarea lor în funcție de canal și de etapa în care se află potențialul client.",
    high:"Dezvoltă comunicarea prin mesaje diferențiate și urmărește reacțiile publicului pentru a identifica subiectele cu cea mai mare relevanță."
  },
  "Strategie de conținut":{
    low:"Stabilește piloni de conținut și un calendar simplu. Fiecare material ar trebui să aibă un scop: informare, educare, încredere sau conversie.",
    medium:"Conectează mai bine temele publicate la obiectivele businessului și urmărește indicatori relevanți, nu doar numărul de aprecieri.",
    high:"Optimizează mixul de conținut în funcție de rezultate și dezvoltă formate care susțin diferitele etape ale parcursului clientului."
  },
  "Strategie de marketing":{
    low:"Stabilește obiective măsurabile și alege canalele în funcție de public, resurse și obiective. Evită activitățile fără un scop clar.",
    medium:"Introdu un proces periodic de analiză a rezultatelor și stabilește indicatori care te ajută să evaluezi eficiența acțiunilor.",
    high:"Consolidează procesul de optimizare și prioritizează investițiile în canalele și acțiunile care contribuie la obiectivele businessului."
  }
};

let answers = new Array(questions.length).fill(null);
let currentQuestion = 0;
let finalReport = null;
let revealObserver = null;

/* ANIMATII LA SCROLL */

function initRevealObserver(){
  if(!("IntersectionObserver" in window)){
    document.querySelectorAll(".reveal").forEach(el=>el.classList.add("visible"));
    return;
  }

  revealObserver = new IntersectionObserver(entries=>{
    entries.forEach(entry=>{
      if(entry.isIntersecting){
        entry.target.classList.add("visible");
        revealObserver.unobserve(entry.target);
      }
    });
  },{
    threshold:0.08,
    rootMargin:"0px 0px -25px 0px"
  });

  observeRevealElements(document);
}

function observeRevealElements(root){
  if(!revealObserver)return;
  root.querySelectorAll(".reveal").forEach(element=>{
    if(!element.classList.contains("visible")){
      revealObserver.observe(element);
    }
  });
}

/* AFISAREA INTREBARILOR */

function renderQuestions(){
  const container = document.getElementById("questionContainer");
  container.innerHTML = "";

  const question = questions[currentQuestion];
  const card = document.createElement("div");
  card.className = "question-card active";
  card.id = "question-" + currentQuestion;

  const category = document.createElement("div");
  category.className = "question-category";
  category.textContent = question.dimension + " · Întrebarea " + (currentQuestion+1) + " din 15";

  const title = document.createElement("h3");
  title.textContent = question.text;

  const options = document.createElement("div");
  options.className = "answer-options";

  question.options.forEach((option,optionIndex)=>{
    const button = document.createElement("button");
    button.type = "button";
    button.className = "answer-option" + (answers[currentQuestion]===optionIndex+1 ? " selected" : "");
    button.setAttribute("aria-pressed",answers[currentQuestion]===optionIndex+1 ? "true" : "false");

    const dot = document.createElement("span");
    dot.className = "answer-dot";
    dot.textContent = "✓";

    const label = document.createElement("span");
    label.textContent = option;

    button.appendChild(dot);
    button.appendChild(label);

    /* IMPORTANT:
       Actualizam doar selectia, fara reconstruirea paginii.
       Astfel, pozitia de scroll ramane neschimbata. */
    button.addEventListener("click",()=>{
      selectAnswer(currentQuestion,optionIndex+1);
    });

    options.appendChild(button);
  });

  const navigation = document.createElement("div");
  navigation.className = "question-navigation";

  const previous = document.createElement("button");
  previous.className = "nav-button";
  previous.type = "button";
  previous.textContent = "← Înapoi";
  previous.disabled = currentQuestion===0;
  previous.addEventListener("click",()=>goToQuestion(currentQuestion-1));

  const next = document.createElement("button");
  next.className = "nav-button next";
  next.type = "button";
  next.textContent = currentQuestion===questions.length-1 ? "Vezi rezultatul →" : "Continuă →";
  next.disabled = answers[currentQuestion]===null;
  next.addEventListener("click",()=>{
    if(currentQuestion===questions.length-1){
      generateResults();
    }else{
      goToQuestion(currentQuestion+1);
    }
  });

  navigation.appendChild(previous);
  navigation.appendChild(next);

  card.appendChild(category);
  card.appendChild(title);
  card.appendChild(options);
  card.appendChild(navigation);
  container.appendChild(card);

  updateProgress();
}

/* SELECTAREA RASPUNSULUI FARA SALT DE PAGINA */

function selectAnswer(questionIndex,value){
  answers[questionIndex] = value;

  const card = document.getElementById("question-" + questionIndex);
  if(!card)return;

  const buttons = card.querySelectorAll(".answer-option");

  buttons.forEach((button,index)=>{
    const selected = index+1===value;
    button.classList.toggle("selected",selected);
    button.setAttribute("aria-pressed",selected ? "true" : "false");
  });

  const nextButton = card.querySelector(".nav-button.next");
  if(nextButton)nextButton.disabled = false;

  updateProgress();
}

function updateProgress(){
  const completed = answers.filter(a=>a!==null).length;
  const percent = completed/questions.length*100;

  document.getElementById("progressText").textContent = completed + " din 15";
  document.getElementById("progressFill").style.width = percent + "%";
}

/* NAVIGAREA INTRE INTREBARI */

function goToQuestion(index){
  if(index<0 || index>=questions.length)return;

  /* Pastram exact pozitia paginii inainte de schimbarea intrebarii */
  const previousScrollPosition = window.scrollY;

  currentQuestion = index;
  renderQuestions();

  /* Nu trimitem utilizatorul la inceputul paginii.
     Noua intrebare apare in acelasi loc vizual. */
  requestAnimationFrame(()=>{
    window.scrollTo({
      top:previousScrollPosition,
      left:0,
      behavior:"instant"
    });
  });
}

function startAudit(){
  answers = new Array(questions.length).fill(null);
  currentQuestion = 0;
  finalReport = null;

  document.getElementById("results").classList.remove("active");
  document.getElementById("auditArea").classList.add("active");

  renderQuestions();

  setTimeout(()=>{
    document.getElementById("auditArea").scrollIntoView({
      behavior:"smooth",
      block:"start"
    });
  },100);
}

/* CALCUL SCOR */

function getLevel(score){
  if(score<40){
    return {
      label:"Are nevoie de claritate",
      title:"Este momentul să construiești fundația.",
      description:"Rezultatul indică mai multe zone în care este nevoie de claritate și structură. Înainte de a investi în mai multe acțiuni de marketing, merită să definești mai bine direcția brandului și obiectivele businessului."
    };
  }
  if(score<60){
    return {
      label:"Fundație în consolidare",
      title:"Ai început să construiești, dar există loc de structură.",
      description:"Businessul are deja câteva elemente de bază, însă unele direcții pot fi consolidate. O abordare mai coerentă te poate ajuta să conectezi mai bine brandul, comunicarea și obiectivele."
    };
  }
  if(score<80){
    return {
      label:"Direcție bună, cu oportunități",
      title:"Ai o fundație bună pe care poți construi.",
      description:"Rezultatul indică o bază relativ bine conturată. Următorul pas este să identifici zonele care pot fi optimizate și să transformi acțiunile existente într-o strategie mai integrată."
    };
  }
  return {
    label:"Fundație bine definită",
    title:"Ai construit o bază solidă.",
    description:"Răspunsurile indică o fundație bine conturată. Menținerea coerenței, analiza rezultatelor și adaptarea la schimbările pieței pot susține dezvoltarea în continuare."
  };
}

function getRecommendation(score,name){
  if(score<40)return recommendations[name].low;
  if(score<70)return recommendations[name].medium;
  return recommendations[name].high;
}

/* GENERARE REZULTATE */

function generateResults(){
  if(answers.some(a=>a===null)){
    alert("Te rugăm să răspunzi la toate întrebările înainte de a vedea rezultatul.");
    return;
  }

  const overall = Math.round(
    answers.reduce((sum,value)=>sum+value,0)/answers.length/5*100
  );

  const dimensionScores = dimensions.map(d=>{
    const selected = answers.slice(d.start,d.end);
    const average = selected.reduce((sum,value)=>sum+value,0)/selected.length;

    return {
      name:d.name,
      score:Math.round(average/5*100),
      description:d.description
    };
  });

  const sorted = [...dimensionScores].sort((a,b)=>a.score-b.score);
  const strongest = [...dimensionScores].sort((a,b)=>b.score-a.score)[0];
  const weakest = sorted[0];
  const level = getLevel(overall);

  finalReport = {
    overall,
    level,
    dimensions:dimensionScores,
    strongest,
    weakest,
    recommendations:sorted.slice(0,3)
  };

  document.getElementById("auditArea").classList.remove("active");
  document.getElementById("results").classList.add("active");

  document.getElementById("overallScore").textContent = overall;
  document.getElementById("scoreTitle").textContent = level.title;
  document.getElementById("scoreDescription").textContent = level.description;
  document.getElementById("scoreLevel").textContent = level.label;

  /* GRAFIC SCOR GENERAL - SVG */

  const scoreArc = document.getElementById("scoreArc");
  const circumference = 2*Math.PI*78;

  scoreArc.style.strokeDasharray = circumference;
  scoreArc.style.strokeDashoffset = circumference;

  requestAnimationFrame(()=>{
    scoreArc.style.strokeDashoffset = circumference*(1-overall/100);
  });

  /* SCORURI PE DIMENSIUNI */

  const dimensionContainer = document.getElementById("dimensionResults");
  dimensionContainer.innerHTML = "";

  dimensionScores.forEach(d=>{
    const item = document.createElement("div");
    item.className = "dimension-item";

    const top = document.createElement("div");
    top.className = "dimension-top";

    const name = document.createElement("span");
    name.className = "dimension-name";
    name.textContent = d.name;

    const score = document.createElement("span");
    score.className = "dimension-score";
    score.textContent = d.score + "/100";

    top.appendChild(name);
    top.appendChild(score);

    const track = document.createElement("div");
    track.className = "dimension-track";

    const fill = document.createElement("div");
    fill.className = "dimension-fill";
    fill.style.width = "0%";
    track.appendChild(fill);

    const description = document.createElement("div");
    description.className = "dimension-description";
    description.textContent = d.description;

    item.appendChild(top);
    item.appendChild(track);
    item.appendChild(description);
    dimensionContainer.appendChild(item);

    requestAnimationFrame(()=>{
      fill.style.width = d.score + "%";
    });
  });

  /* INSIGHTS */

  const insights = document.getElementById("insights");
  insights.innerHTML = "";

  const insightData = [
    {
      label:"Punctul tău forte",
      title:strongest.name,
      text:"Aceasta este dimensiunea cu cel mai bun rezultat: "+strongest.score+"/100. Păstrează această direcție și folosește-o ca punct de sprijin pentru dezvoltarea celorlalte zone."
    },
    {
      label:"Prioritate de dezvoltare",
      title:weakest.name,
      text:"Această dimensiune are cel mai mic scor: "+weakest.score+"/100. Merită să îi acorzi atenție și să identifici acțiunile concrete prin care o poți consolida."
    }
  ];

  insightData.forEach(data=>{
    const card = document.createElement("div");
    card.className = "insight";

    const label = document.createElement("div");
    label.className = "insight-label";
    label.textContent = data.label;

    const title = document.createElement("h4");
    title.textContent = data.title;

    const text = document.createElement("p");
    text.textContent = data.text;

    card.appendChild(label);
    card.appendChild(title);
    card.appendChild(text);
    insights.appendChild(card);
  });

  /* RECOMANDARI */

  const recommendationContainer = document.getElementById("recommendations");
  recommendationContainer.innerHTML = "";

  sorted.slice(0,3).forEach(d=>{
    const card = document.createElement("div");
    card.className = "recommendation";

    const title = document.createElement("h4");
    title.textContent = d.name + " · " + d.score + "/100";

    const text = document.createElement("p");
    text.textContent = getRecommendation(d.score,d.name);

    card.appendChild(title);
    card.appendChild(text);
    recommendationContainer.appendChild(card);
  });

  /* REACTIVEAZA ANIMATIILE PENTRU REZULTATE */

  document.querySelectorAll("#results .result-card").forEach(card=>{
    card.classList.add("reveal");
    card.classList.remove("visible");
  });

  document.querySelectorAll("#results .insight, #results .recommendation").forEach(card=>{
    card.classList.add("reveal");
    card.classList.remove("visible");
  });

  const professional = document.querySelector("#results .professional-section");
  professional.classList.add("reveal");
  professional.classList.remove("visible");

  observeRevealElements(document.getElementById("results"));

  document.getElementById("results").scrollIntoView({
    behavior:"smooth",
    block:"start"
  });
}

/* TEXTUL RAPORTULUI */

function buildReportText(){
  if(!finalReport)return "";

  let report = "ARVANA BRAND & MARKETING AUDIT\n";
  report += "Rezultatul evaluării\n\n";
  report += "Scor general: "+finalReport.overall+"/100\n";
  report += finalReport.level.label+"\n\n";

  report += "REZULTATE PE DIMENSIUNI\n";

  finalReport.dimensions.forEach(d=>{
    report += "\n"+d.name+": "+d.score+"/100\n";
    report += d.description+"\n";
  });

  report += "\nPUNCT FORTE\n";
  report += finalReport.strongest.name+" ("+finalReport.strongest.score+"/100)\n";

  report += "\nPRIORITATE DE DEZVOLTARE\n";
  report += finalReport.weakest.name+" ("+finalReport.weakest.score+"/100)\n";

  report += "\nRECOMANDĂRI\n";
  finalReport.recommendations.forEach(d=>{
    report += "\n"+d.name+"\n";
    report += getRecommendation(d.score,d.name)+"\n";
  });

  report += "\nARVANA Digital Marketing\n";
  report += "Direcție clară. Branduri cu valoare.\n";
  report += "Instrument de autoevaluare orientativă. Nu reprezintă un audit profesional.";

  return report;
}

/* PDF */

function downloadPDF(){
  if(!finalReport)return;

  /* Fortam afisarea tuturor elementelor raportului in PDF */
  document.querySelectorAll("#results .reveal").forEach(el=>{
    el.classList.add("visible");
  });

  const scoreArc = document.getElementById("scoreArc");
  const circumference = 2*Math.PI*78;

  scoreArc.style.strokeDasharray = circumference;
  scoreArc.style.strokeDashoffset = circumference*(1-finalReport.overall/100);

  document.querySelectorAll(".dimension-fill").forEach((fill,index)=>{
    fill.style.width = finalReport.dimensions[index].score + "%";
  });

  setTimeout(()=>window.print(),300);
}

/* COPIERE RAPORT */

async function copyReport(){
  const report = buildReportText();

  try{
    await navigator.clipboard.writeText(report);
    alert("Raportul a fost copiat. Îl poți lipi într-un document sau mesaj.");
  }catch(error){
    const textArea = document.createElement("textarea");
    textArea.value = report;
    document.body.appendChild(textArea);
    textArea.select();
    document.execCommand("copy");
    textArea.remove();
    alert("Raportul a fost copiat.");
  }
}

/* RESTART */

function restartAudit(){
  answers = new Array(questions.length).fill(null);
  currentQuestion = 0;
  finalReport = null;

  document.getElementById("results").classList.remove("active");
  startAudit();
}

/* ANUL DIN FOOTER */

document.getElementById("year").textContent = new Date().getFullYear();

/* INITIALIZARE ANIMATII */

initRevealObserver();
</script>

</body>
</html>
