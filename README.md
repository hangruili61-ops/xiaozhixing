<div id="kzx-root">
<style>
  #kzx-root {
    --cream: #fff9ed; --cream-2: #fff3dd;
    --ink: #2a2540; --ink-soft: #5a5670; --ink-mute: #8a87a0;
    --sun: #ffc83d; --sun-deep: #f3a91a;
    --sky: #4ec3f0; --sky-deep: #2a9bcb;
    --leaf: #6dc26d; --leaf-deep: #4ea64e;
    --berry: #ff7a8a; --berry-deep: #e85a6e;
    --grape: #9b7ed4; --grape-deep: #7857b8;
    --rule: #f0e3c2;
    background: var(--cream);
    color: var(--ink);
    font-family: "PingFang SC", "Microsoft YaHei", "Noto Sans SC", system-ui, sans-serif;
    line-height: 1.7;
    border-radius: 16px;
    overflow: hidden;
    border: 1px solid #e8dec1;
  }
  #kzx-root *, #kzx-root *::before, #kzx-root *::after { box-sizing: border-box; }
  #kzx-root .container { max-width: 1100px; margin: 0 auto; padding: 0 20px; position: relative; z-index: 2; }

  #kzx-root .nav { background: rgba(255, 249, 237, 0.95); border-bottom: 2px dashed var(--rule); }
  #kzx-root .nav-inner {
    display: flex; align-items: center; justify-content: space-between;
    padding: 12px 20px; max-width: 1100px; margin: 0 auto;
  }
  #kzx-root .brand { display: flex; align-items: center; gap: 10px; font-weight: 700; font-size: 17px; color: var(--ink); }
  #kzx-root .brand-mark {
    width: 34px; height: 34px; background: var(--sun);
    border-radius: 10px; display: grid; place-items: center;
    box-shadow: 2px 2px 0 var(--ink); transform: rotate(-4deg);
  }
  #kzx-root .nav-links { display: flex; gap: 14px; font-size: 13px; }
  #kzx-root .nav-links a { color: var(--ink-soft); text-decoration: none; padding: 4px 10px; border-radius: 999px; transition: all .2s; }
  #kzx-root .nav-links a:hover { background: var(--sun); color: var(--ink); }

  #kzx-root .hero { padding: 50px 0 40px; text-align: center; position: relative; }
  #kzx-root .hero-greet {
    display: inline-flex; align-items: center; gap: 8px;
    background: white; border: 2px solid var(--ink);
    padding: 6px 16px; border-radius: 999px;
    font-size: 13px; font-weight: 500;
    box-shadow: 3px 3px 0 var(--ink); margin-bottom: 24px;
  }
  #kzx-root .hero h1 { font-size: 48px; margin: 0 0 18px; line-height: 1.05; color: var(--ink); font-weight: 900; }
  #kzx-root .hero h1 .accent { background: linear-gradient(180deg, transparent 60%, var(--sun) 60%); padding: 0 5px; }
  #kzx-root .hero-lede { max-width: 580px; margin: 0 auto 28px; font-size: 16px; color: var(--ink-soft); }
  #kzx-root .scenes { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; margin-bottom: 20px; }
  #kzx-root .scene-card {
    background: white; border: 2px solid var(--ink);
    border-radius: 16px; padding: 14px 18px;
    box-shadow: 4px 4px 0 var(--ink);
    cursor: pointer;
    display: flex; align-items: center; gap: 10px;
    min-width: 180px; text-align: left;
    transition: transform .15s, box-shadow .15s;
  }
  #kzx-root .scene-card:hover { transform: translate(-2px,-2px); box-shadow: 6px 6px 0 var(--ink); }
  #kzx-root .scene-emoji { font-size: 30px; line-height: 1; }
  #kzx-root .scene-text b { display: block; font-size: 14px; font-weight: 700; }
  #kzx-root .scene-text span { font-size: 12px; color: var(--ink-mute); }

  #kzx-root .hero-deco { position: absolute; pointer-events: none; font-size: 36px; }
  #kzx-root .hero-deco.d1 { top: 12%; left: 6%; }
  #kzx-root .hero-deco.d2 { top: 18%; right: 8%; font-size: 30px; }
  #kzx-root .hero-deco.d3 { bottom: 6%; left: 10%; font-size: 28px; }
  #kzx-root .hero-deco.d4 { bottom: 10%; right: 9%; font-size: 32px; }
  @keyframes kzxFloat { 0%,100% { transform: translateY(0) rotate(0); } 50% { transform: translateY(-10px) rotate(6deg); } }
  #kzx-root .hero-deco { animation: kzxFloat 4s ease-in-out infinite; }
  #kzx-root .hero-deco.d2 { animation-delay: 1s; }
  #kzx-root .hero-deco.d3 { animation-delay: 2s; }
  #kzx-root .hero-deco.d4 { animation-delay: 0.5s; }

  #kzx-root section { padding: 56px 0; position: relative; }
  #kzx-root .section-head { text-align: center; margin-bottom: 36px; }
  #kzx-root .section-eyebrow {
    display: inline-block; background: var(--ink); color: var(--cream);
    padding: 4px 14px; border-radius: 999px;
    font-size: 12px; font-weight: 500; margin-bottom: 14px;
  }
  #kzx-root .section-title { font-size: 32px; margin: 0 0 10px; font-weight: 800; }
  #kzx-root .section-lede { color: var(--ink-soft); font-size: 15px; max-width: 560px; margin: 0 auto; }

  #kzx-root .subjects { display: grid; grid-template-columns: repeat(4, 1fr); gap: 14px; }
  #kzx-root .subject {
    background: white; border: 2px solid var(--ink);
    border-radius: 18px; padding: 20px 14px;
    text-align: center; cursor: pointer;
    box-shadow: 4px 4px 0 var(--ink);
    position: relative;
    transition: transform .2s, box-shadow .2s;
  }
  #kzx-root .subject:hover { transform: translate(-3px,-3px); box-shadow: 7px 7px 0 var(--ink); }
  #kzx-root .subject.active { transform: translate(2px,2px); box-shadow: 2px 2px 0 var(--ink); }
  #kzx-root .subject-emoji { font-size: 38px; display: block; margin-bottom: 8px; }
  #kzx-root .subject-name { font-weight: 700; font-size: 16px; }
  #kzx-root .subject-en { font-size: 11px; color: var(--ink-mute); letter-spacing: 0.04em; margin-top: 2px; }
  #kzx-root .subject .badge {
    position: absolute; top: 8px; right: 8px;
    background: var(--berry); color: white;
    font-size: 10px; padding: 2px 7px; border-radius: 999px; font-weight: 500;
  }
  #kzx-root .subject[data-key="chinese"]   { background: linear-gradient(160deg, #fff3dd 0%, white 60%); }
  #kzx-root .subject[data-key="math"]      { background: linear-gradient(160deg, #e3f4ff 0%, white 60%); }
  #kzx-root .subject[data-key="english"]   { background: linear-gradient(160deg, #ffe7eb 0%, white 60%); }
  #kzx-root .subject[data-key="science"]   { background: linear-gradient(160deg, #e6f5e1 0%, white 60%); }
  #kzx-root .subject[data-key="history"]   { background: linear-gradient(160deg, #fce4cc 0%, white 60%); }
  #kzx-root .subject[data-key="geography"] { background: linear-gradient(160deg, #d8efe7 0%, white 60%); }
  #kzx-root .subject[data-key="art"]       { background: linear-gradient(160deg, #efe4ff 0%, white 60%); }
  #kzx-root .subject[data-key="info"]      { background: linear-gradient(160deg, #dceff5 0%, white 60%); }

  #kzx-root .subject-panel {
    margin-top: 24px; background: white;
    border: 2px solid var(--ink); border-radius: 18px;
    box-shadow: 5px 5px 0 var(--ink); padding: 22px;
    display: none;
  }
  #kzx-root .subject-panel.open { display: block; }
  #kzx-root .panel-head {
    display: flex; align-items: center; gap: 12px;
    margin-bottom: 16px; padding-bottom: 14px;
    border-bottom: 2px dashed var(--rule);
  }
  #kzx-root .panel-emoji {
    font-size: 32px; background: var(--cream-2);
    width: 50px; height: 50px;
    border-radius: 12px; border: 2px solid var(--ink);
    display: grid; place-items: center;
  }
  #kzx-root .panel-head h3 { margin: 0; font-size: 20px; font-weight: 800; }
  #kzx-root .panel-head p { margin: 0; font-size: 13px; color: var(--ink-mute); }
  #kzx-root .panel-close {
    margin-left: auto; width: 32px; height: 32px;
    border-radius: 50%; border: 2px solid var(--ink);
    background: white; cursor: pointer; font-size: 16px;
  }
  #kzx-root .resource-list {
    display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px;
    list-style: none; padding: 0; margin: 0;
  }
  #kzx-root .resource-item {
    display: flex; gap: 12px; align-items: flex-start;
    padding: 12px; border-radius: 12px;
    background: var(--cream);
    text-decoration: none; color: inherit;
    border: 1.5px solid transparent;
    transition: background .2s, transform .15s;
  }
  #kzx-root .resource-item:hover {
    background: white; border-color: var(--ink);
    transform: translateY(-2px);
  }
  #kzx-root .resource-icon {
    font-size: 22px; width: 38px; height: 38px;
    background: white; border-radius: 10px;
    display: grid; place-items: center; flex-shrink: 0;
  }
  #kzx-root .resource-info b { display: block; font-size: 14px; font-weight: 700; margin-bottom: 2px; }
  #kzx-root .resource-info span { font-size: 12px; color: var(--ink-mute); line-height: 1.5; }
  #kzx-root .resource-tag {
    display: inline-block; margin-top: 5px;
    font-size: 10px; padding: 2px 7px;
    border-radius: 4px; font-weight: 500;
  }
  #kzx-root .tag-official { background: #e3f4ff; color: var(--sky-deep); }
  #kzx-root .tag-fun      { background: #ffe7eb; color: var(--berry-deep); }
  #kzx-root .tag-deep     { background: #efe4ff; color: var(--grape-deep); }

  #kzx-root .method-section { background: var(--ink); color: var(--cream); }
  #kzx-root .method-section .section-eyebrow { background: var(--sun); color: var(--ink); }
  #kzx-root .method-section .section-title { color: var(--cream); }
  #kzx-root .method-section .section-lede { color: rgba(255,249,237,0.7); }
  #kzx-root .steps { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; }
  #kzx-root .step {
    background: rgba(255,249,237,0.06);
    border: 2px solid rgba(255,249,237,0.18);
    border-radius: 16px; padding: 20px 18px;
  }
  #kzx-root .step-num {
    width: 38px; height: 38px;
    background: var(--sun); color: var(--ink);
    border-radius: 12px;
    display: grid; place-items: center;
    font-weight: 800; font-size: 18px; margin-bottom: 12px;
  }
  #kzx-root .step:nth-child(2) .step-num { background: var(--sky); color: white; }
  #kzx-root .step:nth-child(3) .step-num { background: var(--berry); color: white; }
  #kzx-root .step:nth-child(4) .step-num { background: var(--leaf); color: white; }
  #kzx-root .step h3 { font-size: 16px; margin: 0 0 6px; color: var(--cream); }
  #kzx-root .step p { font-size: 13px; color: rgba(255,249,237,0.75); margin: 0; }

  #kzx-root .ai-section { background: linear-gradient(160deg, #fff9ed 0%, #ffe7eb 100%); }
  #kzx-root .ai-wrap { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; align-items: center; }
  #kzx-root .ai-text h2 { font-size: 34px; margin: 14px 0 16px; line-height: 1.1; font-weight: 900; }
  #kzx-root .ai-text h2 em {
    font-style: normal; background: var(--sun);
    padding: 0 6px; border-radius: 6px;
    display: inline-block; transform: rotate(-1deg);
  }
  #kzx-root .ai-text p { color: var(--ink-soft); font-size: 15px; margin-bottom: 20px; }
  #kzx-root .ai-bubbles { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 22px; }
  #kzx-root .ai-bubble {
    background: white; border: 2px solid var(--ink);
    padding: 6px 14px; border-radius: 999px;
    font-size: 13px; font-weight: 500;
    cursor: pointer; box-shadow: 2px 2px 0 var(--ink);
    transition: all .15s;
  }
  #kzx-root .ai-bubble:hover { background: var(--sun); transform: translate(-1px,-1px); box-shadow: 3px 3px 0 var(--ink); }
  #kzx-root .ai-cta {
    display: inline-flex; align-items: center; gap: 10px;
    background: var(--ink); color: var(--cream);
    padding: 12px 22px; border-radius: 999px;
    font-weight: 600; font-size: 15px;
    border: none; cursor: pointer;
    box-shadow: 4px 4px 0 var(--berry);
    transition: transform .15s, box-shadow .15s;
  }
  #kzx-root .ai-cta:hover { transform: translate(-2px,-2px); box-shadow: 6px 6px 0 var(--berry); }
  #kzx-root .ai-cta .pulse {
    width: 8px; height: 8px; background: var(--leaf);
    border-radius: 50%; animation: kzxPulse 1.8s infinite;
  }
  @keyframes kzxPulse {
    0% { box-shadow: 0 0 0 0 rgba(109,194,109,0.55); }
    70% { box-shadow: 0 0 0 10px rgba(109,194,109,0); }
    100% { box-shadow: 0 0 0 0 rgba(109,194,109,0); }
  }

  #kzx-root .ai-mascot {
    background: white; border: 3px solid var(--ink);
    border-radius: 22px; padding: 26px;
    box-shadow: 8px 8px 0 var(--ink);
    position: relative;
  }
  #kzx-root .ai-mascot-face {
    width: 100%; aspect-ratio: 1;
    background: var(--sun); border: 3px solid var(--ink);
    border-radius: 50%; position: relative;
    margin: 0 auto; max-width: 220px;
  }
  #kzx-root .ai-mascot-face::before, #kzx-root .ai-mascot-face::after {
    content: ""; position: absolute;
    width: 22px; height: 28px;
    background: var(--ink); border-radius: 50%;
    top: 32%;
    animation: kzxBlink 4s infinite;
  }
  #kzx-root .ai-mascot-face::before { left: 22%; }
  #kzx-root .ai-mascot-face::after { right: 22%; }
  @keyframes kzxBlink {
    0%, 92%, 100% { transform: scaleY(1); }
    96% { transform: scaleY(0.1); }
  }
  #kzx-root .mouth {
    position: absolute;
    width: 50px; height: 25px;
    border: 3px solid var(--ink);
    border-top: 0; border-radius: 0 0 50px 50px;
    bottom: 22%; left: 50%;
    transform: translateX(-50%);
    background: white;
  }
  #kzx-root .cheek {
    position: absolute;
    width: 22px; height: 14px;
    background: var(--berry);
    border-radius: 50%;
    top: 55%; opacity: 0.7;
  }
  #kzx-root .cheek.l { left: 12%; }
  #kzx-root .cheek.r { right: 12%; }
  #kzx-root .ai-mascot-label { text-align: center; margin-top: 16px; font-weight: 700; font-size: 16px; }
  #kzx-root .ai-mascot-label span { display: block; font-size: 12px; color: var(--ink-mute); font-weight: 400; margin-top: 2px; }
  #kzx-root .ai-decor { position: absolute; font-size: 22px; }
  #kzx-root .ai-decor.d1 { top: -12px; right: 16px; }
  #kzx-root .ai-decor.d2 { bottom: 16px; left: -12px; }

  #kzx-root .platforms { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; }
  #kzx-root .platform {
    background: white; border: 2px solid var(--ink);
    border-radius: 16px; padding: 18px;
    text-decoration: none; color: inherit;
    box-shadow: 4px 4px 0 var(--ink);
    transition: transform .15s, box-shadow .15s;
    display: block;
  }
  #kzx-root .platform:hover { transform: translate(-2px,-2px); box-shadow: 6px 6px 0 var(--ink); }
  #kzx-root .platform-head { display: flex; align-items: center; gap: 10px; margin-bottom: 10px; }
  #kzx-root .platform-logo {
    width: 42px; height: 42px;
    border-radius: 10px;
    display: grid; place-items: center;
    font-size: 22px; border: 2px solid var(--ink);
  }
  #kzx-root .platform-meta b { display: block; font-size: 14px; font-weight: 700; }
  #kzx-root .platform-meta span { font-size: 11px; color: var(--ink-mute); }
  #kzx-root .platform p { margin: 0; font-size: 13px; color: var(--ink-soft); }
  #kzx-root .platform-cta {
    display: inline-flex; align-items: center; gap: 4px;
    margin-top: 10px; font-size: 12px;
    font-weight: 600; color: var(--berry-deep);
  }

  #kzx-root .tip-box {
    background: var(--cream-2); border: 2px solid var(--ink);
    border-radius: 18px; padding: 24px;
    box-shadow: 5px 5px 0 var(--ink);
    display: flex; gap: 18px; align-items: flex-start;
  }
  #kzx-root .tip-emoji { font-size: 44px; line-height: 1; flex-shrink: 0; }
  #kzx-root .tip-box h3 { margin: 0 0 8px; font-size: 19px; font-weight: 800; }
  #kzx-root .tip-box p { margin: 0; color: var(--ink-soft); font-size: 14px; }
  #kzx-root .tip-box ul { margin: 12px 0 0; padding-left: 20px; color: var(--ink-soft); font-size: 13px; }
  #kzx-root .tip-box ul li { margin-bottom: 5px; }

  #kzx-root .footer {
    background: var(--ink); color: var(--cream);
    padding: 36px 0 22px; text-align: center;
    margin-top: 30px;
  }
  #kzx-root .footer h3 { font-size: 26px; color: var(--sun); margin: 0 0 10px; font-weight: 800; }
  #kzx-root .footer p { color: rgba(255,249,237,0.7); margin: 0 auto 14px; max-width: 380px; font-size: 13px; }
  #kzx-root .footer .links { display: flex; justify-content: center; gap: 18px; flex-wrap: wrap; font-size: 12px; }
  #kzx-root .footer .links a { color: var(--cream); text-decoration: none; opacity: 0.8; }
  #kzx-root .footer .copyright { margin-top: 18px; font-size: 11px; color: rgba(255,249,237,0.5); }
</style>

<nav class="nav">
  <div class="nav-inner">
    <div class="brand">
      <span class="brand-mark">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#2a2540" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
          <path d="M12 2l2.4 7.4H22l-6.2 4.5 2.4 7.4L12 16.8l-6.2 4.5 2.4-7.4L2 9.4h7.6z"/>
        </svg>
      </span>
      小知星
      <span style="font-weight:400;font-size:12px;color:var(--ink-mute);margin-left:4px;">学习资源站</span>
    </div>
    <div class="nav-links">
      <a href="#kzx-subjects">学科资源</a>
      <a href="#kzx-method">学习方法</a>
      <a href="#kzx-ai">AI 助手</a>
      <a href="#kzx-platforms">推荐平台</a>
      <a href="#kzx-tips">家长老师</a>
    </div>
  </div>
</nav>

<header class="hero">
  <span class="hero-deco d1">📚</span>
  <span class="hero-deco d2">✨</span>
  <span class="hero-deco d3">🚀</span>
  <span class="hero-deco d4">🌟</span>
  <div class="container">
    <div class="hero-greet"><span>👋</span> 嗨，欢迎来到小知星</div>
    <h1><span class="accent">课前预习</span>，<span class="accent">课后复习</span><br>都从这里开始 ✏️</h1>
    <p class="hero-lede">
      这是一个为小学和初中同学准备的 <strong>线上学习资源导航站</strong>。
      不知道学什么？怎么学？找不到好资源？没关系——选一个场景，开始今天的学习吧！
    </p>
    <div class="scenes">
      <div class="scene-card" data-jump="kzx-subjects">
        <span class="scene-emoji">🌅</span>
        <div class="scene-text"><b>课前预习</b><span>明天上什么课？先看一眼</span></div>
      </div>
      <div class="scene-card" data-jump="kzx-subjects">
        <span class="scene-emoji">🌙</span>
        <div class="scene-text"><b>课后复习</b><span>今天没听懂？再练练</span></div>
      </div>
      <div class="scene-card" data-jump="kzx-ai">
        <span class="scene-emoji">🎯</span>
        <div class="scene-text"><b>拓展学习</b><span>感兴趣？让 AI 推荐</span></div>
      </div>
    </div>
  </div>
</header>

<section id="kzx-subjects">
  <div class="container">
    <div class="section-head">
      <span class="section-eyebrow">第 1 步 · 选学科</span>
      <h2 class="section-title">今天想学什么？</h2>
      <p class="section-lede">点一下学科卡片，下面就会展开为你精选的学习资源。</p>
    </div>
    <div class="subjects" id="kzxSubjectsGrid">
      <div class="subject" data-key="chinese"><span class="subject-emoji">📖</span><div class="subject-name">语文</div><div class="subject-en">Chinese</div></div>
      <div class="subject" data-key="math"><span class="subject-emoji">🔢</span><div class="subject-name">数学</div><div class="subject-en">Math</div></div>
      <div class="subject" data-key="english"><span class="subject-emoji">🔤</span><div class="subject-name">英语</div><div class="subject-en">English</div></div>
      <div class="subject" data-key="science"><span class="subject-emoji">🔬</span><div class="subject-name">科学</div><div class="subject-en">Science</div><span class="badge">含理化生</span></div>
      <div class="subject" data-key="history"><span class="subject-emoji">🏛️</span><div class="subject-name">历史</div><div class="subject-en">History</div></div>
      <div class="subject" data-key="geography"><span class="subject-emoji">🌍</span><div class="subject-name">地理</div><div class="subject-en">Geography</div></div>
      <div class="subject" data-key="art"><span class="subject-emoji">🎨</span><div class="subject-name">艺术</div><div class="subject-en">Art &amp; Music</div></div>
      <div class="subject" data-key="info"><span class="subject-emoji">💻</span><div class="subject-name">信息科技</div><div class="subject-en">Tech</div></div>
    </div>
    <div class="subject-panel" id="kzxSubjectPanel">
      <div class="panel-head">
        <div class="panel-emoji" id="kzxPanelEmoji">📖</div>
        <div>
          <h3 id="kzxPanelTitle">语文</h3>
          <p id="kzxPanelSub">阅读、写作、古诗文 —— 精选资源</p>
        </div>
        <button class="panel-close" id="kzxPanelClose">✕</button>
      </div>
      <ul class="resource-list" id="kzxPanelList"></ul>
    </div>
  </div>
</section>

<section id="kzx-method" class="method-section">
  <div class="container">
    <div class="section-head">
      <span class="section-eyebrow">第 2 步 · 会学习</span>
      <h2 class="section-title">自主学习的小窍门 🍀</h2>
      <p class="section-lede">资源虽好，方法更要紧。试试这四步，比刷一晚上视频更有效。</p>
    </div>
    <div class="steps">
      <div class="step"><div class="step-num">1</div><h3>先有目标</h3><p>今天要学什么？是预习明天的课，还是把没听懂的再看一遍？目标越具体越好。</p></div>
      <div class="step"><div class="step-num">2</div><h3>找对资源</h3><p>不需要看十个视频，找一个讲得清楚的就够了。看不懂再换。</p></div>
      <div class="step"><div class="step-num">3</div><h3>专心 20 分钟</h3><p>把手机放远一点。番茄钟试试看：学 20 分钟，休息 5 分钟。</p></div>
      <div class="step"><div class="step-num">4</div><h3>动手检验</h3><p>合上视频，自己讲一遍 / 做两道题 / 写笔记。能讲出来才是真的会。</p></div>
    </div>
  </div>
</section>

<section id="kzx-ai" class="ai-section">
  <div class="container">
    <div class="ai-wrap">
      <div class="ai-text">
        <span class="section-eyebrow">第 3 步 · 问 AI</span>
        <h2>不知道学啥？问问<em>小知星</em>！</h2>
        <p>找不到合适资源？听不懂某个知识点？想知道这道题的解题思路？点右下角的小气泡，AI 学习小助手随时在线。</p>
        <div class="ai-bubbles">
          <span class="ai-bubble">📐 推荐预习资源</span>
          <span class="ai-bubble">🔁 帮我复习</span>
          <span class="ai-bubble">🌟 拓展学习</span>
          <span class="ai-bubble">💡 兴趣启蒙</span>
        </div>
        <button class="ai-cta">
          <span class="pulse"></span>
          打开 AI 小助手聊一聊 →
        </button>
      </div>
      <div class="ai-mascot">
        <span class="ai-decor d1">⭐</span>
        <span class="ai-decor d2">💡</span>
        <div class="ai-mascot-face">
          <div class="cheek l"></div>
          <div class="cheek r"></div>
          <div class="mouth"></div>
        </div>
        <div class="ai-mascot-label">小知星<span>你的学习小伙伴 · 24 小时在线</span></div>
      </div>
    </div>
  </div>
</section>

<section id="kzx-platforms">
  <div class="container">
    <div class="section-head">
      <span class="section-eyebrow">第 4 步 · 收藏好平台</span>
      <h2 class="section-title">这些官方学习平台，建议收藏 ⭐</h2>
      <p class="section-lede">免费、权威、安全 —— 适合中小学生长期使用。</p>
    </div>
    <div class="platforms">
      <a class="platform" href="https://basic.smartedu.cn/" target="_blank" rel="noopener">
        <div class="platform-head">
          <div class="platform-logo" style="background:#fff3dd;">🇨🇳</div>
          <div class="platform-meta"><b>国家中小学智慧教育平台</b><span>教育部 · 全学科</span></div>
        </div>
        <p>教育部官方平台，按教材版本提供同步课程视频、电子课本、作业习题，全部免费。</p>
        <span class="platform-cta">去看看 →</span>
      </a>
      <a class="platform" href="https://www.cdstm.cn/" target="_blank" rel="noopener">
        <div class="platform-head">
          <div class="platform-logo" style="background:#e6f5e1;">🔬</div>
          <div class="platform-meta"><b>中国数字科技馆</b><span>中国科协主办</span></div>
        </div>
        <p>科普视频、虚拟科技馆、动手实验，让科学课变得超有意思。</p>
        <span class="platform-cta">去看看 →</span>
      </a>
      <a class="platform" href="https://www.dpm.org.cn/" target="_blank" rel="noopener">
        <div class="platform-head">
          <div class="platform-logo" style="background:#fce4cc;">🏯</div>
          <div class="platform-meta"><b>故宫博物院</b><span>数字文物库 · 历史</span></div>
        </div>
        <p>在线逛故宫、看文物高清图，学历史的同时认识中华文明。</p>
        <span class="platform-cta">去看看 →</span>
      </a>
      <a class="platform" href="https://www.nlc.cn/" target="_blank" rel="noopener">
        <div class="platform-head">
          <div class="platform-logo" style="background:#e3f4ff;">📚</div>
          <div class="platform-meta"><b>国家图书馆</b><span>少儿馆 · 阅读资源</span></div>
        </div>
        <p>大量儿童电子书、有声故事、传统文化主题资源，免费阅读。</p>
        <span class="platform-cta">去看看 →</span>
      </a>
      <a class="platform" href="https://kids.cctv.com/" target="_blank" rel="noopener">
        <div class="platform-head">
          <div class="platform-logo" style="background:#ffe7eb;">📺</div>
          <div class="platform-meta"><b>央视少儿</b><span>CCTV · 综合</span></div>
        </div>
        <p>央视出品的少儿频道节目库，纪录片、科普栏目、动画都很优质。</p>
        <span class="platform-cta">去看看 →</span>
      </a>
      <a class="platform" href="https://www.xuexi.cn/" target="_blank" rel="noopener">
        <div class="platform-head">
          <div class="platform-logo" style="background:#efe4ff;">🇨🇳</div>
          <div class="platform-meta"><b>学习强国</b><span>综合学习平台</span></div>
        </div>
        <p>有专门的"教育"和"少年"频道，包含大量公开课、纪录片和文化内容。</p>
        <span class="platform-cta">去看看 →</span>
      </a>
    </div>
  </div>
</section>

<section id="kzx-tips">
  <div class="container">
    <div class="section-head">
      <span class="section-eyebrow">小提醒</span>
      <h2 class="section-title">给家长和老师的话 💌</h2>
    </div>
    <div class="tip-box">
      <div class="tip-emoji">🌱</div>
      <div>
        <h3>把"自主学习"还给孩子，但不是放手不管</h3>
        <p>这个网站希望成为孩子主动找资源、主动提问的入口，而不是又一个被动观看的"网课平台"。建议家长和老师注意：</p>
        <ul>
          <li>陪伴第一次使用，约定每次使用的时间（建议 25–40 分钟为一个学习段）</li>
          <li>鼓励孩子在 AI 助手提出"我哪里不懂"，而不是直接要答案</li>
          <li>所有跳转的外部平台都是公益/官方/权威机构，可放心使用</li>
          <li>定期问问孩子："今天学到了什么？""哪里还想再了解一下？"</li>
          <li>如发现孩子使用 AI 仅为完成作业，请及时引导：AI 是学习伙伴，不是答案机</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<div class="footer">
  <div class="container">
    <h3>小知星 · 一起去学习吧 ✨</h3>
    <p>为义务教育阶段同学准备的线上学习资源导航站，让自主学习更轻松、更有趣。</p>
    <div class="links">
      <a href="#kzx-subjects">学科资源</a>
      <a href="#kzx-method">学习方法</a>
      <a href="#kzx-ai">AI 小助手</a>
      <a href="#kzx-platforms">推荐平台</a>
      <a href="#kzx-tips">给家长老师</a>
    </div>
    <div class="copyright">© 2026 小知星学习资源站 · 公益教育项目</div>
  </div>
</div>

<script src="https://lf-cdn.coze.cn/obj/unpkg/flow-platform/chat-app-sdk/1.2.0-beta.19/libs/cn/index.js"></script>
<script>
  new CozeWebSDK.WebChatClient({
    config: {
      bot_id: '7623978712010244136',
    },
    componentProps: {
      title: 'Coze',
    },
    auth: {
      type: 'token',
      token: 'pat_DzSSoVHgxd99X6N1sYepfZbWM91BEEFPuJ4P1glNzHR5FsHJumhtPxvuLZ5eTf19',
      onRefreshToken: function () {
        return 'pat_DzSSoVHgxd99X6N1sYepfZbWM91BEEFPuJ4P1glNzHR5FsHJumhtPxvuLZ5eTf19'
      }
    }
  });
</script>

</div>
