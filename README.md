[Uploading index.html…]()
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>小明 - 前端开发者</title>
<meta name="description" content="小明,前端开发者。作品集与联系方式。">
<style>
:root{
  --paper:#F2F4F1;
  --ink:#12202E;
  --muted:#556270;
  --line:#C9D0D6;
  --blue:#2B4CFF;
  --tint:#DDE4FF;
  --tint2:#E7EBF1;
  --font:"PingFang SC","Hiragino Sans GB","Microsoft YaHei","Noto Sans SC","Source Han Sans SC",system-ui,sans-serif;
  --mono:ui-monospace,"SF Mono",Consolas,"Liberation Mono",monospace;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--paper);color:var(--ink);font-family:var(--font);line-height:1.75;-webkit-font-smoothing:antialiased}
a{color:inherit}
a:focus-visible{outline:3px solid var(--blue);outline-offset:3px;border-radius:2px}
.wrap{max-width:1080px;margin:0 auto;padding:0 24px}

/* header */
header .wrap{display:flex;justify-content:space-between;align-items:center;height:72px}
.brand{font-weight:800;font-size:18px;text-decoration:none;letter-spacing:.02em}
nav{display:flex;gap:28px}
nav a{text-decoration:none;color:var(--muted);font-size:15px;padding:4px 0;border-bottom:2px solid transparent}
nav a:hover{color:var(--ink);border-bottom-color:var(--blue)}

/* hero: box model */
.bm{margin-top:16px;border:2px dashed #8A96A3;background:var(--tint2);padding:44px 28px 28px;position:relative}
.bm .border{border:2px solid var(--ink);background:var(--tint);padding:44px 28px 36px;position:relative}
.bm .pad{border:1px dashed var(--blue);background:var(--paper);padding:40px 28px 32px;position:relative}
.tag{position:absolute;top:10px;left:14px;font-family:var(--mono);font-size:12px;color:var(--muted);letter-spacing:.02em}
.bm .border>.tag{color:var(--ink)}
.bm .pad>.tag{color:var(--blue)}
.val{position:absolute;font-family:var(--mono);font-size:12px;color:var(--muted)}
.bm>.val{top:10px;right:14px}
h1{font-size:clamp(64px,14vw,168px);line-height:1.02;font-weight:900;letter-spacing:-.02em}
.role{font-size:clamp(22px,3.4vw,36px);font-weight:700;margin-top:6px}
.size{margin-top:20px;font-family:var(--mono);font-size:12px;color:var(--blue)}

.intro{display:grid;grid-template-columns:1.4fr 1fr;gap:48px;padding:48px 0 72px;align-items:start}
.intro p{font-size:19px;max-width:30em}
.actions{display:flex;flex-direction:column;gap:12px;align-items:flex-start}
.btn{display:inline-block;padding:12px 24px;background:var(--blue);color:#fff;text-decoration:none;font-weight:700;border-radius:4px}
.btn:hover{background:var(--ink)}
.plain{color:var(--ink);font-weight:600;text-underline-offset:4px;text-decoration-thickness:2px;text-decoration-color:var(--blue)}

/* sections */
section{padding:72px 0;border-top:1px solid var(--line)}
h2{font-size:28px;font-weight:800;margin-bottom:32px}

.rows{list-style:none}
.rows li{display:grid;grid-template-columns:200px 1fr 220px 64px;gap:24px;padding:24px 0;border-top:1px solid var(--line);align-items:baseline}
.rows li:last-child{border-bottom:1px solid var(--line)}
.rows h3{font-size:20px;font-weight:800}
.rows p{color:var(--muted)}
.stack{font-size:14px;color:var(--ink)}
.rows a{font-weight:700;color:var(--blue);text-underline-offset:4px}

dl{display:grid;grid-template-columns:200px 1fr;gap:0 24px}
dt{font-weight:800;padding:20px 0;border-top:1px solid var(--line)}
dd{padding:20px 0;border-top:1px solid var(--line);color:var(--muted)}
dl dt:last-of-type,dl dd:last-of-type{border-bottom:1px solid var(--line)}

.mail{display:inline-block;font-size:clamp(24px,5vw,52px);font-weight:900;text-decoration:underline;text-decoration-color:var(--blue);text-decoration-thickness:4px;text-underline-offset:8px;word-break:break-all}
.mail:hover{color:var(--blue)}
.social{margin-top:28px;display:flex;gap:28px;flex-wrap:wrap}
footer{padding:32px 0 56px;color:var(--muted);font-size:14px;border-top:1px solid var(--line)}

/* one load sequence: layers nest in from outside */
@keyframes in{from{opacity:0;transform:scale(.97)}to{opacity:1;transform:none}}
.bm{animation:in .5s ease-out both}
.bm .border{animation:in .5s .25s ease-out both}
.bm .pad{animation:in .5s .5s ease-out both}
.bm .pad>*:not(.tag){animation:in .5s .75s ease-out both}
@media (prefers-reduced-motion:reduce){
  *{animation:none!important;scroll-behavior:auto!important}
}

@media (max-width:820px){
  .intro{grid-template-columns:1fr;gap:28px;padding:36px 0 56px}
  .rows li{grid-template-columns:1fr;gap:6px}
  dl{grid-template-columns:1fr}
  dt{padding-bottom:0;border-bottom:0}
  dd{border-top:0;padding-top:4px}
  dl dt:last-of-type{border-bottom:0}
  nav{gap:18px}
}
@media (max-width:520px){
  .wrap{padding:0 16px}
  .bm{padding:36px 10px 10px}
  .bm .border{padding:36px 10px 14px}
  .bm .pad{padding:34px 14px 20px}
  .val{display:none}
}
</style>
</head>
<body>

<header>
  <div class="wrap">
    <a class="brand" href="#top">小明</a>
    <nav aria-label="主导航">
      <a href="#projects">项目</a>
      <a href="#skills">技能</a>
      <a href="#contact">联系</a>
    </nav>
  </div>
</header>

<main id="top">
  <div class="wrap">
    <!-- 首屏:用浏览器开发者工具里的盒模型图,表达“前端开发者” -->
    <div class="bm" aria-hidden="false">
      <span class="val">margin 28</span>
      <span class="tag">margin</span>
      <div class="border">
        <span class="tag">border 2</span>
        <span class="val" style="top:10px;right:14px">padding 32</span>
        <div class="pad">
          <span class="tag">content</span>
          <h1>小明</h1>
          <div class="role">前端开发者</div>
          <div class="size">1080 x auto</div>
        </div>
      </div>
    </div>

    <div class="intro">
      <p>我做网页界面。把设计稿变成在手机和电脑上都清晰、好用、加载快的页面,也关心代码是否好维护。</p>
      <div class="actions">
        <a class="btn" href="#contact">联系我</a>
        <a class="plain" href="#projects">看看我的项目</a>
      </div>
    </div>
  </div>

  <section id="projects">
    <div class="wrap">
      <h2>项目</h2>
      <ul class="rows">
        <!-- 把下面三个项目换成你自己的:标题、简介、技术栈、链接 -->
        <li>
          <h3>在线课程平台</h3>
          <p>为培训机构做的学习网站,支持课程搜索、进度记录和移动端播放。</p>
          <span class="stack">Vue、Vite、Element Plus</span>
          <a href="#">查看</a>
        </li>
        <li>
          <h3>数据看板</h3>
          <p>把销售数据整理成可筛选的图表页面,首屏加载时间从 4 秒降到 1.2 秒。</p>
          <span class="stack">React、TypeScript、ECharts</span>
          <a href="#">查看</a>
        </li>
        <li>
          <h3>个人博客</h3>
          <p>记录学习笔记的静态站点,Markdown 写作,推送到 GitHub 后自动发布。</p>
          <span class="stack">HTML、CSS、Vercel</span>
          <a href="#">查看</a>
        </li>
      </ul>
    </div>
  </section>

  <section id="skills">
    <div class="wrap">
      <h2>技能</h2>
      <dl>
        <dt>页面与样式</dt>
        <dd>HTML、CSS、Flex 与 Grid 布局、响应式适配、无障碍基础</dd>
        <dt>框架与语言</dt>
        <dd>JavaScript、TypeScript、React、Vue、Vite</dd>
        <dt>工程与协作</dt>
        <dd>Git、GitHub、性能优化、与设计师和后端对接接口</dd>
      </dl>
    </div>
  </section>

  <section id="contact">
    <div class="wrap">
      <h2>联系</h2>
      <p style="color:var(--muted);margin-bottom:20px">有项目想聊,或者想一起做点东西,发邮件给我:</p>
      <a class="mail" href="mailto:hello@example.com">hello@example.com</a>
      <div class="social">
        <a class="plain" href="https://github.com/" target="_blank" rel="noopener">GitHub</a>
        <a class="plain" href="#">微信:请替换为你的微信号</a>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap">&copy; 2026 小明</div>
</footer>

</body>
</html>
