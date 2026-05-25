<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>TechLearn AI｜新世代技職學習平台</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700;900&display=swap" rel="stylesheet">

<style>

:root{
  --primary:#2563eb;
  --primary2:#60a5fa;
  --bg:#f8fbff;
  --card:#ffffff;
  --text:#0f172a;
  --muted:#64748b;
  --border:#e2e8f0;
  --success:#10b981;
  --purple:#7c3aed;
}

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  font-family:'Noto Sans TC',sans-serif;
  background:var(--bg);
  color:var(--text);
  overflow-x:hidden;
}

/* NAV */

nav{
  position:fixed;
  width:100%;
  top:0;
  z-index:999;
  padding:18px 7%;
  display:flex;
  justify-content:space-between;
  align-items:center;
  backdrop-filter:blur(20px);
  background:rgba(255,255,255,.75);
  border-bottom:1px solid rgba(255,255,255,.4);
}

.logo{
  font-size:26px;
  font-weight:900;
  background:linear-gradient(90deg,var(--primary),var(--purple));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

nav ul{
  display:flex;
  list-style:none;
  gap:34px;
}

nav a{
  text-decoration:none;
  color:var(--muted);
  font-weight:600;
  transition:.3s;
}

nav a:hover{
  color:var(--primary);
}

.nav-btn{
  background:linear-gradient(135deg,var(--primary),var(--primary2));
  color:white;
  border:none;
  padding:12px 20px;
  border-radius:14px;
  font-weight:700;
  cursor:pointer;
  box-shadow:0 10px 30px rgba(37,99,235,.25);
}

/* HERO */

.hero{
  padding:150px 7% 100px;
  display:grid;
  grid-template-columns:1.1fr 1fr;
  gap:60px;
  align-items:center;
  position:relative;
}

.hero::before{
  content:'';
  position:absolute;
  right:-200px;
  top:-200px;
  width:600px;
  height:600px;
  background:radial-gradient(circle,var(--primary2),transparent 70%);
  opacity:.15;
  z-index:-1;
}

.hero-text h1{
  font-size:64px;
  line-height:1.1;
  font-weight:900;
  margin-bottom:24px;
}

.hero-text h1 span{
  background:linear-gradient(90deg,var(--primary),var(--purple));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

.hero-text p{
  color:var(--muted);
  font-size:18px;
  line-height:1.8;
  max-width:650px;
}

.hero-buttons{
  display:flex;
  gap:16px;
  margin-top:34px;
}

.primary-btn{
  background:linear-gradient(135deg,var(--primary),var(--primary2));
  color:white;
  padding:16px 26px;
  border:none;
  border-radius:16px;
  font-weight:800;
  cursor:pointer;
  box-shadow:0 15px 40px rgba(37,99,235,.25);
}

.secondary-btn{
  background:white;
  border:1px solid var(--border);
  padding:16px 26px;
  border-radius:16px;
  font-weight:700;
  cursor:pointer;
}

/* HERO UI */

.hero-ui{
  position:relative;
}

.dashboard{
  background:rgba(255,255,255,.75);
  backdrop-filter:blur(25px);
  border:1px solid rgba(255,255,255,.5);
  border-radius:32px;
  padding:28px;
  box-shadow:
    0 20px 60px rgba(15,23,42,.08),
    inset 0 1px rgba(255,255,255,.8);
}

.topbar{
  display:flex;
  justify-content:space-between;
  margin-bottom:24px;
}

.pill{
  background:#eef4ff;
  color:var(--primary);
  padding:10px 16px;
  border-radius:999px;
  font-size:13px;
  font-weight:700;
}

.progress-card{
  background:linear-gradient(135deg,#2563eb,#7c3aed);
  border-radius:26px;
  padding:28px;
  color:white;
  margin-bottom:22px;
}

.progress-card h3{
  font-size:28px;
  margin-bottom:10px;
}

.progress-bar{
  height:10px;
  background:rgba(255,255,255,.25);
  border-radius:999px;
  overflow:hidden;
  margin-top:18px;
}

.progress-fill{
  width:76%;
  height:100%;
  background:white;
  border-radius:999px;
}

.course-list{
  display:flex;
  flex-direction:column;
  gap:16px;
}

.course-item{
  background:white;
  border-radius:20px;
  padding:18px;
  display:flex;
  align-items:center;
  gap:16px;
  border:1px solid var(--border);
  transition:.3s;
}

.course-item:hover{
  transform:translateY(-4px);
  box-shadow:0 12px 30px rgba(15,23,42,.08);
}

.icon{
  width:56px;
  height:56px;
  border-radius:18px;
  display:flex;
  justify-content:center;
  align-items:center;
  font-size:24px;
  color:white;
  font-weight:700;
}

.blue{background:linear-gradient(135deg,#2563eb,#60a5fa);}
.green{background:linear-gradient(135deg,#10b981,#34d399);}
.purple{background:linear-gradient(135deg,#7c3aed,#a78bfa);}

.course-info{
  flex:1;
}

.course-info h4{
  margin-bottom:6px;
}

.course-info p{
  color:var(--muted);
  font-size:14px;
}

.percent{
  font-weight:800;
  color:var(--primary);
}

/* SECTION */

section{
  padding:90px 7%;
}

.section-title{
  font-size:42px;
  font-weight:900;
  margin-bottom:14px;
}

.section-sub{
  color:var(--muted);
  margin-bottom:40px;
  line-height:1.8;
}

/* CARDS */

.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:26px;
}

.card{
  background:white;
  border-radius:28px;
  overflow:hidden;
  border:1px solid var(--border);
  transition:.35s;
  position:relative;
}

.card:hover{
  transform:translateY(-10px);
  box-shadow:0 20px 60px rgba(15,23,42,.1);
}

.card img{
  width:100%;
  height:220px;
  object-fit:cover;
}

.card-body{
  padding:24px;
}

.tag{
  display:inline-block;
  padding:8px 14px;
  border-radius:999px;
  background:#eef4ff;
  color:var(--primary);
  font-size:12px;
  font-weight:800;
  margin-bottom:16px;
}

.card h3{
  font-size:24px;
  margin-bottom:10px;
}

.card p{
  color:var(--muted);
  line-height:1.8;
}

.price{
  margin-top:18px;
  font-size:24px;
  font-weight:900;
  color:var(--success);
}

/* FEATURES */

.features{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:24px;
}

.feature{
  background:white;
  padding:32px;
  border-radius:28px;
  border:1px solid var(--border);
}

.feature-icon{
  width:70px;
  height:70px;
  border-radius:22px;
  background:linear-gradient(135deg,#2563eb,#7c3aed);
  color:white;
  display:flex;
  justify-content:center;
  align-items:center;
  font-size:30px;
  margin-bottom:20px;
}

.feature h3{
  margin-bottom:12px;
}

.feature p{
  color:var(--muted);
  line-height:1.8;
}

/* CTA */

.cta{
  background:linear-gradient(135deg,#2563eb,#7c3aed);
  border-radius:40px;
  color:white;
  padding:80px;
  text-align:center;
  margin:80px 7%;
}

.cta h2{
  font-size:52px;
  margin-bottom:20px;
}

.cta p{
  opacity:.9;
  max-width:700px;
  margin:auto;
  line-height:1.8;
}

.cta button{
  margin-top:30px;
  background:white;
  color:var(--primary);
  border:none;
  padding:18px 30px;
  border-radius:18px;
  font-weight:900;
  font-size:17px;
  cursor:pointer;
}

/* FOOTER */

footer{
  padding:80px 7%;
  background:white;
  border-top:1px solid var(--border);
}

.footer-grid{
  display:grid;
  grid-template-columns:2fr 1fr 1fr 1fr;
  gap:40px;
}

.footer-logo{
  font-size:32px;
  font-weight:900;
  margin-bottom:16px;
  background:linear-gradient(90deg,var(--primary),var(--purple));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

footer p{
  color:var(--muted);
  line-height:1.8;
}

footer h4{
  margin-bottom:16px;
}

footer a{
  display:block;
  margin-bottom:12px;
  color:var(--muted);
  text-decoration:none;
}

footer a:hover{
  color:var(--primary);
}

/* MOBILE */

@media(max-width:1100px){

.hero{
  grid-template-columns:1fr;
}

.features{
  grid-template-columns:1fr 1fr;
}

.footer-grid{
  grid-template-columns:1fr 1fr;
}

.hero-text h1{
  font-size:52px;
}

}

@media(max-width:768px){

nav ul{
  display:none;
}

.features{
  grid-template-columns:1fr;
}

.footer-grid{
  grid-template-columns:1fr;
}

.hero-text h1{
  font-size:42px;
}

.hero-buttons{
  flex-direction:column;
}

.cta{
  padding:50px 30px;
}

.cta h2{
  font-size:38px;
}

}

</style>
</head>

<body>

<nav>

<div class="logo">TechLearn AI</div>

<ul>
<li><a href="#">課程</a></li>
<li><a href="#">技能證照</a></li>
<li><a href="#">AI學習</a></li>
<li><a href="#">技職升學</a></li>
<li><a href="#">企業合作</a></li>
</ul>

<button class="nav-btn">免費開始</button>

</nav>

<!-- HERO -->

<div class="hero">

<div class="hero-text">

<h1>
讓技職教育<br>
進入 <span>AI 時代</span>
</h1>

<p>
專為高職生與科技大學生打造的智慧學習平台，
整合 AI 學習分析、技能證照、統測備考與業界實作，
真正接軌升學與未來職場。
</p>

<div class="hero-buttons">
<button class="primary-btn">立即開始學習</button>
<button class="secondary-btn">觀看平台介紹</button>
</div>

</div>

<div class="hero-ui">

<div class="dashboard">

<div class="topbar">
<div class="pill">AI 學習分析</div>
<div class="pill">Lv.12 技術新星</div>
</div>

<div class="progress-card">

<h3>本週學習進度</h3>

<p>你的 Python 與統測英文進步超越 82% 學員</p>

<div class="progress-bar">
<div class="progress-fill"></div>
</div>

</div>

<div class="course-list">

<div class="course-item">

<div class="icon blue">💻</div>

<div class="course-info">
<h4>Python 全端開發</h4>
<p>HTML / CSS / JavaScript / Flask</p>
</div>

<div class="percent">78%</div>

</div>

<div class="course-item">

<div class="icon green">📊</div>

<div class="course-info">
<h4>Excel 商業分析</h4>
<p>商管群 × AI 數據應用</p>
</div>

<div class="percent">91%</div>

</div>

<div class="course-item">

<div class="icon purple">⚡</div>

<div class="course-info">
<h4>乙級電器修護</h4>
<p>術科模擬與題庫</p>
</div>

<div class="percent">62%</div>

</div>

</div>

</div>

</div>

</div>

<!-- COURSES -->

<section>

<h2 class="section-title">熱門學習領域</h2>

<p class="section-sub">
結合技職教育、AI 與產業能力，
打造真正能接軌未來的學習內容。
</p>

<div class="grid">

<div class="card">

<img src="https://images.unsplash.com/photo-1515879218367-8466d910aaa4?q=80&w=1200&auto=format&fit=crop">

<div class="card-body">

<div class="tag">資訊科技</div>

<h3>AI × 程式開發</h3>

<p>
從 Python 到 AI 應用開發，
完整學習未來科技技能。
</p>

<div class="price">120+ 課程</div>

</div>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1581092921461-eab62e97a780?q=80&w=1200&auto=format&fit=crop">

<div class="card-body">

<div class="tag">工程技術</div>

<h3>電機與工業控制</h3>

<p>
PLC、自動控制與乙級檢定，
對接智慧工廠產業需求。
</p>

<div class="price">85 種證照</div>

</div>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1554224155-8d04cb21cd6c?q=80&w=1200&auto=format&fit=crop">

<div class="card-body">

<div class="tag">商業管理</div>

<h3>數據分析 × 商業技能</h3>

<p>
Excel、會計、AI 商業分析，
打造新世代商管能力。
</p>

<div class="price">30,000+ 學生</div>

</div>

</div>

</div>

</section>

<!-- FEATURES -->

<section>

<h2 class="section-title">為什麼學生都在用</h2>

<p class="section-sub">
不是單純影片平台，而是真正會幫你學習成長的系統。
</p>

<div class="features">

<div class="feature">

<div class="feature-icon">🤖</div>

<h3>AI 智慧助教</h3>

<p>
24 小時 AI 即時解題與學習分析，
幫助學生快速突破盲點。
</p>

</div>

<div class="feature">

<div class="feature-icon">📈</div>

<h3>學習數據分析</h3>

<p>
自動分析弱點與進度，
建立個人化學習路線。
</p>

</div>

<div class="feature">

<div class="feature-icon">🏆</div>

<h3>技能證照系統</h3>

<p>
完整技術士與統測題庫，
對應真正考場規格。
</p>

</div>

<div class="feature">

<div class="feature-icon">🚀</div>

<h3>產業接軌課程</h3>

<p>
與科技大學與企業合作，
打造真正職場所需技能。
</p>

</div>

</div>

</section>

<!-- CTA -->

<div class="cta">

<h2>現在開始你的 AI 學習旅程</h2>

<p>
加入新世代技職教育平台，
從技能學習到未來職涯，
一次完成。
</p>

<button>免費開始學習</button>

</div>

<!-- FOOTER -->

<footer>

<div class="footer-grid">

<div>

<div class="footer-logo">TechLearn AI</div>

<p>
打造下一代技職教育平台，
讓每位學生都能找到屬於自己的未來技能。
</p>

</div>

<div>

<h4>學習領域</h4>

<a href="#">資訊科技</a>
<a href="#">商業管理</a>
<a href="#">電機電子</a>
<a href="#">設計群</a>

</div>

<div>

<h4>平台功能</h4>

<a href="#">AI 助教</a>
<a href="#">技能檢定</a>
<a href="#">模擬考試</a>
<a href="#">學習分析</a>

</div>

<div>

<h4>支援</h4>

<a href="#">聯絡客服</a>
<a href="#">企業合作</a>
<a href="#">學校合作</a>
<a href="#">隱私政策</a>

</div>

</div>

</footer>

</body>
</html>
