<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>宿舍111 | 计算机学院最具代表性的牛逼宿舍</title>
  <meta name="description" content="111宿舍是计算机学院最具代表性的牛逼宿舍。波哥、佑哥、航哥、骏哥、洋哥、宁哥——电竞、才艺、技术与财运齐飞！" />
  <style>
    :root{
      --bg: #0b1220;
      --panel: #ffffff;
      --text: #0f172a;
      --muted:#475569;
      --border:#e2e8f0;
      --primary:#2563eb;
      --accent:#7c3aed;
      --chip:#eef2ff;
      --chipText:#3730a3;
    }
    *{ box-sizing: border-box; }
    html,body{ margin:0; padding:0; scroll-behavior: smooth; }
    body{
      font-family: system-ui,-apple-system,Segoe UI,Roboto,Inter,"PingFang SC","Hiragino Sans GB","Microsoft YaHei",sans-serif;
      color: var(--text);
      background:
        radial-gradient(1200px 600px at 90% -10%, rgba(124,58,237,.12), transparent 60%),
        radial-gradient(900px 500px at -10% 10%, rgba(37,99,235,.12), transparent 60%),
        #f8fafc;
      line-height: 1.6;
    }
    .container{ max-width: 1080px; margin: 0 auto; padding: 0 20px; }

    /* Navigation */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border);
      z-index: 1000;
      padding: 12px 0;
    }
    .nav-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      font-weight: 700;
      font-size: 20px;
      color: var(--primary);
    }
    .nav-links {
      display: flex;
      gap: 24px;
    }
    .nav-links a {
      text-decoration: none;
      color: var(--text);
      font-weight: 500;
      transition: color 0.2s;
    }
    .nav-links a:hover {
      color: var(--primary);
    }
    .mobile-menu-btn {
      display: none;
      background: none;
      border: none;
      font-size: 24px;
      cursor: pointer;
    }

    /* Hero */
    .hero{
      background: linear-gradient(120deg, #1d4ed8, #7c3aed);
      color:#fff;
      position: relative;
      overflow: hidden;
      margin-top: 60px;
    }
    .hero .wrap{
      padding: 72px 0 64px;
      position: relative;
      z-index: 2;
    }
    .badge{
      display:inline-flex; align-items:center; gap:8px;
      padding:6px 10px; border-radius:999px;
      background: rgba(255,255,255,.14);
      backdrop-filter: blur(6px);
      font-size: 12px; letter-spacing:.2px;
    }
    .hero h1{
      margin:16px 0 8px;
      font-size: clamp(34px, 6vw, 56px);
      line-height: 1.05;
      letter-spacing: .4px;
    }
    .hero p{
      margin: 0 0 18px;
      font-size: clamp(14px, 2.5vw, 18px);
      opacity: .95;
      max-width: 600px;
    }
    .chips{ display:flex; flex-wrap:wrap; gap:8px; margin-top:10px; }
    .chip{
      background: rgba(255,255,255,.16);
      border:1px solid rgba(255,255,255,.22);
      color:#fff; padding:6px 10px; border-radius:999px; font-size:12px;
    }
    .cta-button {
      display: inline-block;
      margin-top: 20px;
      padding: 12px 24px;
      background: rgba(255,255,255,0.2);
      border: 1px solid rgba(255,255,255,0.3);
      color: white;
      border-radius: 8px;
      text-decoration: none;
      font-weight: 500;
      transition: all 0.3s;
    }
    .cta-button:hover {
      background: rgba(255,255,255,0.3);
      transform: translateY(-2px);
    }

    /* Section */
    .section{
      padding: 44px 0 60px;
    }
    .section h2{
      font-size: 24px; margin: 0 0 12px;
    }
    .section .sub{
      color: var(--muted); margin-bottom: 18px;
    }

    /* About Section */
    .about-section {
      background: white;
      border-radius: 16px;
      padding: 32px;
      margin: 24px 0;
      box-shadow: 0 8px 24px rgba(15, 23, 42, .06);
    }
    .about-content {
      display: flex;
      gap: 24px;
      align-items: center;
    }
    .about-text {
      flex: 1;
    }
    .about-image {
      flex: 1;
      height: 300px;
      background: linear-gradient(135deg, #e0e7ff, #ede9fe);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 60px;
    }

    /* Grid cards */
    .grid{
      display:grid; gap:16px;
      grid-template-columns: repeat(3, 1fr);
    }
    @media (max-width: 980px){
      .grid{ grid-template-columns: repeat(2, 1fr); }
    }
    @media (max-width: 640px){
      .grid{ grid-template-columns: 1fr; }
      .hero .wrap{ padding: 56px 0 40px; }
      .about-content { flex-direction: column; }
      .nav-links { display: none; }
      .mobile-menu-btn { display: block; }
    }
    .card{
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 18px;
      box-shadow: 0 8px 24px rgba(15, 23, 42, .06);
      transition: transform .15s ease, box-shadow .15s ease;
      cursor: pointer;
    }
    .card:hover{
      transform: translateY(-2px);
      box-shadow: 0 12px 28px rgba(15, 23, 42, .10);
    }
    .row{ display:flex; align-items:center; gap:14px; }
    .avatar{
      width:48px; height:48px; flex:0 0 48px;
      display:grid; place-items:center;
      border-radius: 12px;
      background: linear-gradient(135deg, #e0e7ff, #ede9fe);
      font-size: 24px;
    }
    .name{
      font-weight: 700; font-size: 18px; margin: 0 0 2px;
      display:flex; align-items:center; gap:8px;
    }
    .title{ color: var(--muted); font-size: 13px; }
    .desc{ margin: 10px 0 10px; }
    .taglist{ display:flex; flex-wrap:wrap; gap:6px; }
    .tag{
      background: var(--chip); color: var(--chipText);
      padding: 4px 8px; border-radius: 999px; font-size: 12px;
      border: 1px solid #c7d2fe;
    }

    /* Achievements */
    .achievements {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      margin-top: 32px;
    }
    .achievement-card {
      flex: 1;
      min-width: 200px;
      background: white;
      border-radius: 12px;
      padding: 20px;
      text-align: center;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    }
    .achievement-icon {
      font-size: 32px;
      margin-bottom: 12px;
    }
    .achievement-number {
      font-size: 28px;
      font-weight: 700;
      color: var(--primary);
      margin-bottom: 8px;
    }
    .achievement-text {
      font-size: 14px;
      color: var(--muted);
    }

    /* Footer */
    footer{
      padding: 28px 0 44px; color: #475569; text-align: center;
      background: white;
      border-top: 1px solid var(--border);
    }
    .small{ font-size: 12px; color:#64748b; }
    .social-links {
      display: flex;
      justify-content: center;
      gap: 16px;
      margin: 16px 0;
    }
    .social-link {
      width: 36px;
      height: 36px;
      border-radius: 50%;
      background: var(--chip);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--primary);
      text-decoration: none;
      transition: all 0.2s;
    }
    .social-link:hover {
      background: var(--primary);
      color: white;
      transform: translateY(-2px);
    }
  </style>
</head>
<body>

  <!-- 导航栏 -->
  <nav class="navbar">
    <div class="container nav-container">
      <div class="logo">宿舍111</div>
      <div class="nav-links">
        <a href="#home">首页</a>
        <a href="#about">关于我们</a>
        <a href="#members">宿舍成员</a>
        <a href="#achievements">荣誉成就</a>
      </div>
      <button class="mobile-menu-btn">☰</button>
    </div>
  </nav>

  <!-- 顶部 Hero -->
  <header class="hero" id="home">
    <div class="container wrap">
      <span class="badge">宿舍号 · 111</span>
      <h1>111 宿舍</h1>
      <p>111宿舍是计算机学院最具代表性的牛逼宿舍。波哥、佑哥、航哥、骏哥、洋哥、宁哥——电竞、才艺、技术与财运齐飞！</p>
      <div class="chips">
        <span class="chip">计算机学院</span>
        <span class="chip">电竞 · 才艺 · 技术 · 财运</span>
        <span class="chip">团结友爱</span>
      </div>
      <a href="#members" class="cta-button">认识宿舍成员</a>
    </div>
  </header>

  <!-- 关于我们 -->
  <section class="section" id="about">
    <div class="container">
      <h2>关于111宿舍</h2>
      <div class="sub">计算机学院的传奇聚集地</div>
      
      <div class="about-section">
        <div class="about-content">
          <div class="about-text">
            <p>111宿舍是计算机学院最具代表性的宿舍之一，汇聚了六位各具特色的技术精英。</p>
            <p>我们不仅在学术上追求卓越，在电竞、才艺和个人发展方面也都有出色表现。从火影忍者到Valorant，从篮球场到吉他演奏，从技术分享到财富积累，我们每个人都有自己的闪光点。</p>
            <p>宿舍文化以"团结、互助、创新、快乐"为核心，我们相信团队的力量，也尊重每个人的独特性。</p>
          </div>
          <div class="about-image">
            🏠
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- 成员卡片 -->
  <main class="section" id="members">
    <div class="container">
      <h2>宿舍成员</h2>
      <div class="sub">六边形战士齐聚 111 · 各有高光，各有传奇。</div>

      <div class="grid">

        <!-- 波哥 -->
        <article class="card">
          <div class="row">
            <div class="avatar">😎</div>
            <div>
              <div class="name">波哥 <span class="title">最帅的男人｜火影 & 瓦玩家</span></div>
            </div>
          </div>
          <p class="desc">爱打瓦但是没见过他叫妈妈；火影也玩得非常溜，一手"国家队"上超影，稳！</p>
          <div class="taglist">
            <span class="tag">国家队</span>
            <span class="tag">超影</span>
            <span class="tag">Valorant</span>
          </div>
        </article>

        <!-- 佑哥 -->
        <article class="card">
          <div class="row">
            <div class="avatar">⚡</div>
            <div>
              <div class="name">佑哥 <span class="title">最有反应之人｜技术忍者本忍</span></div>
            </div>
          </div>
          <p class="desc">爱玩火影，但玩的全是技术忍者，尤其是天道超；时空反应快到没边儿。</p>
          <div class="taglist">
            <span class="tag">技术流</span>
            <span class="tag">天道超</span>
            <span class="tag">手速拉满</span>
          </div>
        </article>

        <!-- 航哥 -->
        <article class="card">
          <div class="row">
            <div class="avatar">💸</div>
            <div>
              <div class="name">航哥 <span class="title">最会发财之人｜撤离达人</span></div>
            </div>
          </div>
          <p class="desc">就爱玩撤离，随手就是百万撤离，一不留神就发财，财运buff常驻。</p>
          <div class="taglist">
            <span class="tag">撤离高手</span>
            <span class="tag">欧气满格</span>
            <span class="tag">资源管理</span>
          </div>
        </article>

        <!-- 骏哥 -->
        <article class="card">
          <div class="row">
            <div class="avatar">🎸</div>
            <div>
              <div class="name">骏哥 <span class="title">最有才艺之人｜篮球 & 吉他</span></div>
            </div>
          </div>
          <p class="desc">会打篮球，得用乔丹级别去防；会唱会弹吉他，多才多艺，气场拿捏全场。</p>
          <div class="taglist">
            <span class="tag">篮球手感</span>
            <span class="tag">歌手/吉他手</span>
            <span class="tag">舞台魅力</span>
          </div>
        </article>

        <!-- 洋哥 -->
        <article class="card">
          <div class="row">
            <div class="avatar">🛠️</div>
            <div>
              <div class="name">洋哥 <span class="title">最有技术之人｜优质分享官</span></div>
            </div>
          </div>
          <p class="desc">经常给舍友分享优质视频，知识与快乐两手抓；王者也玩得贼溜，操作行云流水。</p>
          <div class="taglist">
            <span class="tag">技术担当</span>
            <span class="tag">优质分享</span>
            <span class="tag">王者操作</span>
          </div>
        </article>

        <!-- 宁哥 -->
        <article class="card">
          <div class="row">
            <div class="avatar">🍥</div>
            <div>
              <div class="name">宁哥 <span class="title">无差别模式最强｜课堂积极</span></div>
            </div>
          </div>
          <p class="desc">火影无差别模式最强之人，小豪对他三分都要畏惧；上课最积极，真·榜样的力量。</p>
          <div class="taglist">
            <span class="tag">无差别之王</span>
            <span class="tag">三分杀手</span>
            <span class="tag">课堂猛士</span>
          </div>
        </article>

      </div>
    </div>
  </main>

  <!-- 成就部分 -->
  <section class="section" id="achievements">
    <div class="container">
      <h2>宿舍荣誉</h2>
      <div class="sub">我们的成就与高光时刻</div>
      
      <div class="achievements">
        <div class="achievement-card">
          <div class="achievement-icon">🏆</div>
          <div class="achievement-number">6+</div>
          <div class="achievement-text">各类比赛获奖</div>
        </div>
        <div class="achievement-card">
          <div class="achievement-icon">🎮</div>
          <div class="achievement-number">3</div>
          <div class="achievement-text">电竞高手</div>
        </div>
        <div class="achievement-card">
          <div class="achievement-icon">🎵</div>
          <div class="achievement-number">2</div>
          <div class="achievement-text">才艺达人</div>
        </div>
        <div class="achievement-card">
          <div class="achievement-icon">💻</div>
          <div class="achievement-number">4</div>
          <div class="achievement-text">技术大神</div>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <div class="container">
      <div>一起住，一起卷，也一起开心。</div>
      <div class="social-links">
        <a href="#" class="social-link">📱</a>
        <a href="#" class="social-link">📘</a>
        <a href="#" class="social-link">🐦</a>
        <a href="#" class="social-link">📸</a>
      </div>
      <div class="small">© 宿舍111 · 计算机学院 · All vibes reserved.</div>
    </div>
  </footer>

  <script>
    // 简单的移动端菜单切换
    document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
      const navLinks = document.querySelector('.nav-links');
      navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
    });

    // 平滑滚动
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({
            behavior: 'smooth'
          });
          // 移动端点击后关闭菜单
          if (window.innerWidth <= 640) {
            document.querySelector('.nav-links').style.display = 'none';
          }
        }
      });
    });
  </script>
</body>
</html>
