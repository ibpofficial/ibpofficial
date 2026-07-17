<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- SEO Meta Tags -->
  <title>IBP Official · Web Developer & Creator</title>
  <meta name="description" content="IBP Official – Web Developer, Creator, and lifelong learner. Explore modern web projects, GitHub stats, and connect." />
  <meta name="keywords" content="IBP Official, web developer, GitHub, portfolio, coding, creator" />
  <meta name="author" content="IBP Official" />
  <link rel="canonical" href="https://ibpofficial.dev" />
  <!-- Open Graph -->
  <meta property="og:title" content="IBP Official · Web Developer & Creator" />
  <meta property="og:description" content="Building cool things with code. Always learning, always building." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://ibpofficial.dev" />
  <meta name="theme-color" content="#2E86DE" />

  <!-- Fonts & Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0d0e1a;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
      color: #eef2ff;
      display: flex;
      justify-content: center;
      padding: 2rem 1rem;
      line-height: 1.6;
    }

    .profile-card {
      max-width: 1000px;
      width: 100%;
      background: rgba(18, 20, 35, 0.7);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-radius: 3.5rem 3.5rem 2.5rem 2.5rem;
      padding: 2rem 2rem 2.5rem;
      box-shadow: 0 25px 50px -8px rgba(0,0,0,0.8), 0 0 0 1px rgba(255,255,255,0.03);
      border: 1px solid rgba(255,255,255,0.02);
      transition: all 0.2s;
    }

    /* ===== HEADER with animated wave ===== */
    .header-wave {
      position: relative;
      margin: -2rem -2rem 2rem -2rem;
      border-radius: 3.5rem 3.5rem 0 0;
      overflow: hidden;
      background: linear-gradient(135deg, #1a1c2e, #0d0e1a);
    }

    .header-wave svg {
      display: block;
      width: 100%;
      height: auto;
      min-height: 180px;
    }

    .header-content {
      position: relative;
      text-align: center;
      padding: 1.5rem 1rem 2rem;
    }

    .header-content h1 {
      font-size: 3.2rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      background: linear-gradient(135deg, #f0f4ff, #a78bfa, #7dd3fc);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-shadow: 0 0 30px rgba(167, 139, 250, 0.2);
      animation: glowPulse 4s ease-in-out infinite alternate;
    }

    .header-content .sub {
      font-size: 1.1rem;
      color: #a5b4fc;
      letter-spacing: 0.3px;
      margin-top: 0.2rem;
      font-weight: 400;
      background: rgba(255,255,255,0.02);
      display: inline-block;
      padding: 0.2rem 1.2rem;
      border-radius: 40px;
      backdrop-filter: blur(4px);
    }

    @keyframes glowPulse {
      0% { text-shadow: 0 0 15px rgba(167, 139, 250, 0.1); }
      100% { text-shadow: 0 0 40px rgba(167, 139, 250, 0.5), 0 0 80px rgba(59, 130, 246, 0.2); }
    }

    /* ===== Typing SVG ===== */
    .typing-wrapper {
      margin: 0.5rem 0 1.8rem;
      display: flex;
      justify-content: center;
    }

    .typing-wrapper img {
      max-width: 100%;
      height: auto;
      filter: drop-shadow(0 0 12px rgba(167, 139, 250, 0.2));
      transition: transform 0.3s;
    }

    .typing-wrapper img:hover {
      transform: scale(1.01);
    }

    /* badges */
    .badge-row {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.8rem 1.2rem;
      margin-top: 0.5rem;
    }

    .badge-row img {
      transition: transform 0.2s ease, box-shadow 0.2s;
    }

    .badge-row img:hover {
      transform: translateY(-3px) scale(1.02);
      filter: brightness(1.1);
    }

    /* about */
    .about-section {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1.8rem;
      background: rgba(30, 34, 55, 0.4);
      border-radius: 2.5rem;
      padding: 1.8rem 2rem;
      margin: 2rem 0 2.2rem;
      border: 1px solid rgba(255,255,255,0.03);
      backdrop-filter: blur(4px);
    }

    .about-text {
      flex: 2;
      min-width: 220px;
    }

    .about-text h2 {
      font-size: 1.8rem;
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      color: #c4b5fd;
    }

    .about-text p {
      color: #d1d5f0;
      margin: 0.6rem 0 0.3rem;
      font-size: 1rem;
      line-height: 1.7;
    }

    .about-text .fun-fact {
      color: #93c5fd;
      font-size: 0.95rem;
      background: rgba(46, 134, 222, 0.08);
      padding: 0.3rem 1rem;
      border-radius: 40px;
      display: inline-block;
      border: 1px solid rgba(46, 134, 222, 0.15);
    }

    .about-gif {
      flex: 0 0 180px;
      display: flex;
      justify-content: center;
    }

    .about-gif img {
      max-width: 100%;
      border-radius: 30px;
      filter: drop-shadow(0 10px 18px rgba(0,0,0,0.6));
      border: 1px solid rgba(255,255,255,0.04);
      transition: transform 0.3s ease;
    }

    .about-gif img:hover {
      transform: scale(1.02) rotate(1deg);
    }

    /* tech stack */
    .tech-stack {
      display: flex;
      justify-content: center;
      margin: 1.8rem 0 2rem;
    }

    .tech-stack img {
      max-width: 100%;
      transition: filter 0.3s;
    }

    .tech-stack img:hover {
      filter: drop-shadow(0 0 20px rgba(167, 139, 250, 0.3));
    }

    /* stats grid */
    .stats-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem;
      justify-content: center;
      margin: 2rem 0 1.2rem;
    }

    .stats-grid > * {
      flex: 1 1 240px;
      min-width: 180px;
      transition: transform 0.25s ease, box-shadow 0.3s;
      border-radius: 28px;
      overflow: hidden;
      background: rgba(22, 25, 45, 0.5);
      backdrop-filter: blur(4px);
      border: 1px solid rgba(255,255,255,0.02);
    }

    .stats-grid > *:hover {
      transform: translateY(-6px) scale(1.01);
      box-shadow: 0 20px 30px -10px rgba(0,0,0,0.7);
      border-color: rgba(167, 139, 250, 0.15);
    }

    .stats-grid img {
      display: block;
      width: 100%;
      height: auto;
    }

    .lang-chart {
      display: flex;
      justify-content: center;
      margin: 1.2rem 0 0.5rem;
    }

    .lang-chart img {
      max-width: 70%;
      border-radius: 30px;
      transition: transform 0.3s;
      background: rgba(0,0,0,0.1);
    }

    .lang-chart img:hover {
      transform: scale(1.02);
    }

    /* trophies */
    .trophy-row {
      display: flex;
      justify-content: center;
      margin: 2rem 0 1.5rem;
    }

    .trophy-row img {
      max-width: 100%;
      border-radius: 30px;
      transition: filter 0.3s;
    }

    .trophy-row img:hover {
      filter: drop-shadow(0 0 25px rgba(167, 139, 250, 0.2));
    }

    /* activity graph */
    .activity-graph {
      display: flex;
      justify-content: center;
      margin: 1.8rem 0 2rem;
    }

    .activity-graph img {
      width: 100%;
      max-width: 900px;
      border-radius: 30px;
      background: rgba(0,0,0,0.2);
      transition: all 0.3s;
      border: 1px solid rgba(255,255,255,0.02);
    }

    .activity-graph img:hover {
      box-shadow: 0 0 40px rgba(167, 139, 250, 0.05);
    }

    /* social */
    .social-links {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.9rem 1.2rem;
      margin: 2rem 0 1rem;
    }

    .social-links a {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: rgba(30, 34, 60, 0.6);
      padding: 0.6rem 1.5rem;
      border-radius: 60px;
      color: #eef2ff;
      text-decoration: none;
      font-weight: 500;
      font-size: 0.95rem;
      backdrop-filter: blur(4px);
      border: 1px solid rgba(255,255,255,0.02);
      transition: all 0.25s ease;
      letter-spacing: 0.2px;
    }

    .social-links a i {
      font-size: 1.2rem;
      color: #a5b4fc;
    }

    .social-links a:hover {
      background: rgba(167, 139, 250, 0.12);
      border-color: rgba(167, 139, 250, 0.2);
      transform: translateY(-4px);
      box-shadow: 0 12px 20px -12px rgba(0,0,0,0.6);
    }

    .footer-wave {
      margin: 2.5rem -2rem -2.5rem -2rem;
      border-radius: 0 0 2.5rem 2.5rem;
      overflow: hidden;
      line-height: 0;
    }

    .footer-wave svg {
      display: block;
      width: 100%;
      height: 80px;
    }

    .credit {
      text-align: center;
      color: #7986b0;
      font-size: 0.9rem;
      margin-top: 0.5rem;
      letter-spacing: 0.2px;
      opacity: 0.7;
    }

    .credit i {
      color: #a78bfa;
    }

    /* responsiveness */
    @media (max-width: 680px) {
      .profile-card { padding: 1.2rem; }
      .header-wave { margin: -1.2rem -1.2rem 1.2rem -1.2rem; }
      .about-section { flex-direction: column; text-align: center; padding: 1.5rem; }
      .about-gif { flex: 0 0 140px; }
      .header-content h1 { font-size: 2.5rem; }
      .stats-grid > * { flex: 1 1 100%; }
      .lang-chart img { max-width: 95%; }
      .social-links a { padding: 0.5rem 1.2rem; font-size: 0.9rem; }
    }

    @media (max-width: 480px) {
      .header-content h1 { font-size: 2rem; }
      .badge-row { gap: 0.4rem; }
    }
  </style>
</head>
<body>
  <div class="profile-card">

    <!-- ========== HEADER WAVE ========== -->
    <div class="header-wave">
      <svg viewBox="0 0 1200 200" preserveAspectRatio="none" style="background: linear-gradient(135deg, #1a1c2e, #0d0e1a);">
        <defs>
          <linearGradient id="waveGrad" x1="0%" y1="0%" x2="100%" y2="0%">
            <stop offset="0%" style="stop-color:#2E86DE;stop-opacity:0.9" />
            <stop offset="100%" style="stop-color:#9B59B6;stop-opacity:0.9" />
          </linearGradient>
          <filter id="glowFilter">
            <feGaussianBlur stdDeviation="3" result="blur" />
            <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
          </filter>
        </defs>
        <path d="M0,120 C300,40 600,160 900,80 C1050,40 1150,60 1200,80 L1200,200 L0,200 Z" fill="url(#waveGrad)" opacity="0.25" />
        <path d="M0,140 C200,80 400,180 700,100 C900,60 1050,120 1200,90 L1200,200 L0,200 Z" fill="url(#waveGrad)" opacity="0.4" />
        <path d="M0,160 C250,120 500,200 750,130 C950,90 1100,130 1200,110 L1200,200 L0,200 Z" fill="url(#waveGrad)" opacity="0.6" />
        <text x="50%" y="48%" dominant-baseline="middle" text-anchor="middle" font-family="'Inter', sans-serif" font-weight="700" font-size="48" fill="white" filter="url(#glowFilter)" letter-spacing="1">IBP OFFICIAL</text>
        <text x="50%" y="68%" dominant-baseline="middle" text-anchor="middle" font-family="'Inter', sans-serif" font-weight="400" font-size="16" fill="#c4b5fd" opacity="0.9">Web Developer · Creator · Learner</text>
      </svg>
    </div>

    <!-- ========== TYPING SVG ========== -->
    <div class="typing-wrapper">
      <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=2800&pause=800&color=9B59B6&center=true&vCenter=true&width=600&lines=Welcome+to+my+GitHub+%F0%9F%91%8B;Building+cool+things+with+code;Always+learning%2C+always+building;Check+out+my+pinned+repos+below" alt="Typing SVG" />
    </div>

    <!-- ========== BADGES ========== -->
    <div class="badge-row">
      <img src="https://komarev.com/ghpvc/?username=ibpofficial&label=Profile+Views&color=9B59B6&style=for-the-badge" alt="views" />
      <img src="https://img.shields.io/github/followers/ibpofficial?label=Followers&style=for-the-badge&color=2E86DE" alt="followers" />
    </div>

    <!-- ========== ABOUT ========== -->
    <div class="about-section">
      <div class="about-text">
        <h2><i class="fas fa-code" style="color:#a78bfa;"></i> About Me</h2>
        <p>🔭 Currently building and improving web projects<br />
        🌱 Learning new tools and modern frameworks<br />
        🎯 Goal: write clean, useful, and creative code</p>
        <span class="fun-fact"><i class="fas fa-bolt" style="margin-right:6px;"></i> Fun fact: I enjoy turning simple ideas into working projects</span>
        <p style="margin-top:0.8rem; font-size:0.95rem;"><i class="fas fa-envelope" style="color:#93c5fd;"></i> ishantpbupadhyay@gmaol.com</p>
      </div>
      <div class="about-gif">
        <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/gifs/Coding.gif" alt="Coding" />
      </div>
    </div>

    <!-- ========== TECH STACK ========== -->
    <div class="tech-stack">
      <img src="https://skillicons.dev/icons?i=html,css,js,git,github,vscode,figma&theme=dark" alt="tech skills" />
    </div>

    <!-- ========== STATS GRID ========== -->
    <div class="stats-grid">
      <img src="https://github-readme-stats.vercel.app/api?username=ibpofficial&show_icons=true&theme=radical&hide_border=true&count_private=true&bg_color=0d0e1a&title_color=c4b5fd&icon_color=9B59B6" alt="GitHub Stats" />
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=ibpofficial&theme=radical&hide_border=true&background=0d0e1a&stroke=2E86DE&ring=9B59B6&fire=9B59B6&currStreakLabel=c4b5fd" alt="streak" />
    </div>

    <!-- ========== TOP LANGUAGES ========== -->
    <div class="lang-chart">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ibpofficial&layout=compact&theme=radical&hide_border=true&bg_color=0d0e1a&title_color=c4b5fd" alt="top languages" />
    </div>

    <!-- ========== TROPHIES ========== -->
    <div class="trophy-row">
      <img src="https://github-profile-trophy.vercel.app/?username=ibpofficial&theme=radical&no-frame=true&row=1&column=6&margin-w=6&margin-h=6" alt="trophies" />
    </div>

    <!-- ========== ACTIVITY GRAPH ========== -->
    <div class="activity-graph">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=ibpofficial&theme=redical-red&hide_border=true&bg_color=0d0e1a&color=c4b5fd&line=9B59B6&point=2E86DE" alt="activity graph" />
    </div>

    <!-- ========== SOCIAL LINKS ========== -->
    <div class="social-links">
      <a href="#"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
      <a href="#"><i class="fab fa-twitter"></i> Twitter</a>
      <a href="#"><i class="fab fa-instagram"></i> Instagram</a>
      <a href="mailto:ishantpbupadhyay@gmaol.com"><i class="fas fa-envelope"></i> Email</a>
    </div>

    <!-- ========== FOOTER WAVE ========== -->
    <div class="footer-wave">
      <svg viewBox="0 0 1200 120" preserveAspectRatio="none" style="display:block;">
        <path d="M0,60 C300,20 600,100 900,50 C1050,25 1150,40 1200,30 L1200,120 L0,120 Z" fill="url(#waveGrad)" opacity="0.3" />
        <path d="M0,80 C250,50 500,110 750,70 C950,45 1100,70 1200,60 L1200,120 L0,120 Z" fill="url(#waveGrad)" opacity="0.5" />
        <path d="M0,100 C200,80 400,120 700,95 C950,80 1100,100 1200,90 L1200,120 L0,120 Z" fill="url(#waveGrad)" opacity="0.7" />
      </svg>
    </div>

    <div class="credit">
      <i class="fas fa-star"></i> Thanks for stopping by — feel free to explore my repos!
    </div>
  </div>
</body>
</html>
