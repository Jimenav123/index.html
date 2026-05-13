# Eightsleep-index.html[8sleep-index.html](https://github.com/user-attachments/files/27727304/8sleep-index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Night Shift — Jimena Vázquez for Eight Sleep</title>
<meta name="description" content="A creative brand strategy pitch for Eight Sleep's Marketing Intern position by Jimena Vázquez.">
<link href="https://fonts.googleapis.com/css2?family=Instrument+Sans:wght@400;500;600;700&family=Instrument+Serif:ital@0;1&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *{margin:0;padding:0;box-sizing:border-box}
  body{background:#fff;font-family:'Instrument Sans','Helvetica Neue',sans-serif;color:#1a1a1a;min-height:100vh;display:flex;align-items:center;justify-content:center;padding:16px}
  .wrap{width:100%;max-width:460px;min-height:720px;position:relative;display:flex;flex-direction:column}
  .dots{display:flex;gap:8px;justify-content:center;margin-bottom:32px}
  .dot{height:6px;border-radius:3px;cursor:pointer;transition:all 0.4s}
  .dot.active{width:24px;background:#1a1a1a}
  .dot.inactive{width:6px;background:#ddd}
  .slide{display:none;opacity:0;transform:translateX(25px);transition:all 0.5s cubic-bezier(.4,0,.2,1)}
  .slide.active{display:block;opacity:1;transform:translateX(0)}
  .label{display:inline-block;font-size:10px;letter-spacing:3px;text-transform:uppercase;font-family:'DM Mono',monospace;border-bottom:1.5px solid;padding-bottom:2px}
  .label-gray{color:#999;border-color:#999}
  .label-warm{color:#c49a6c;border-color:#c49a6c}
  .serif{font-family:'Instrument Serif',Georgia,serif}
  .mono{font-family:'DM Mono',monospace}
  h1{font-size:56px;font-weight:400;letter-spacing:-3px;line-height:1;margin:20px 0 16px;color:#1a1a1a}
  h2.section-title{font-size:34px;font-weight:400;letter-spacing:-1px;margin:12px 0 0;color:#1a1a1a}
  .nav{display:flex;justify-content:space-between;align-items:center;margin-top:auto;padding-top:36px}
  .nav span{font-size:13px;font-family:'DM Mono',monospace;cursor:pointer;user-select:none}
  .nav .disabled{color:#ddd;cursor:default}
  .nav .counter{font-size:11px;color:#ccc}

  /* Cover */
  .cover{text-align:center}
  .logo-wrap{margin-bottom:48px;display:flex;justify-content:center}

  /* About */
  .avatar{width:88px;height:88px;border-radius:50%;margin:0 auto 16px;background:linear-gradient(135deg,#e8e8e8,#d0d0d0);display:flex;align-items:center;justify-content:center;font-size:32px;color:#999}
  .about-name{font-size:30px;font-weight:400;letter-spacing:-1px}
  .about-item{display:flex;gap:16px;margin-bottom:18px}
  .about-num{font-size:12px;color:#888;font-family:'DM Mono',monospace;min-width:22px;padding-top:3px}
  .about-title{font-size:15px;font-weight:600;color:#1a1a1a}
  .about-desc{font-size:13px;color:#555;margin-top:2px}

  /* Audit */
  .audit-item{margin-bottom:22px;padding-bottom:22px;border-bottom:1px solid #e8e8e8}
  .audit-item:last-child{border-bottom:none}
  .audit-title{font-size:16px;font-weight:600;color:#1a1a1a;margin-bottom:8px}
  .audit-text{font-size:13px;color:#555;line-height:1.7}

  /* Opportunities */
  .opp-item{padding:16px 0;border-bottom:1px solid #e8e8e8;cursor:pointer}
  .opp-header{display:flex;justify-content:space-between;align-items:center}
  .opp-title{font-size:15px;font-weight:600;color:#1a1a1a}
  .opp-toggle{font-size:20px;color:#888;transition:transform 0.3s;font-weight:300}
  .opp-toggle.open{transform:rotate(45deg)}
  .opp-body{display:none;margin-top:14px}
  .opp-body.open{display:block}
  .opp-insight{font-size:13px;color:#555;line-height:1.7;margin-bottom:12px}
  .opp-action{font-size:13px;color:#8B6914;line-height:1.6;padding-left:16px;border-left:2px solid rgba(196,168,130,0.27)}
  .opp-action strong{color:#c49a6c}

  /* Campaign */
  .tab-bar{display:flex;gap:4px;margin-bottom:20px}
  .tab-btn{flex:1;padding:10px 6px;border:none;border-radius:0;border-bottom:2px solid transparent;background:transparent;font-size:11px;font-weight:600;color:#888;cursor:pointer;font-family:'DM Mono',monospace;letter-spacing:0.5px;transition:all 0.3s}
  .tab-btn.active{border-bottom-color:#1a1a1a;color:#1a1a1a}
  .tab-content{display:none}
  .tab-content.active{display:block}
  .demo-card{background:#0a0a0c;border-radius:16px;padding:28px 24px;margin-bottom:14px;color:#fff;position:relative;overflow:hidden}
  .demo-label{font-size:10px;font-family:'DM Mono',monospace;letter-spacing:2px;margin-bottom:16px}
  .demo-headline{font-family:'Instrument Serif',serif;color:#f0f0f0;line-height:1.2;margin-bottom:6px}
  .stat-row{display:flex;align-items:baseline;gap:14px;margin-bottom:12px}
  .stat-num{font-size:24px;font-family:'Instrument Serif',serif;color:#c8d4e0;min-width:76px}
  .stat-label{font-size:12px;color:#667}
  .script-label{color:#c49a6c;font-family:'DM Mono',monospace;font-size:10px}
  .series-row{display:flex;gap:10px;margin-bottom:12px;align-items:baseline}
  .series-num{font-size:11px;color:#445;font-family:'DM Mono',monospace}
  .series-who{color:#ccc;font-weight:600;font-size:13px}
  .series-desc{color:#777;font-size:13px}

  /* Why Me */
  .why-lead{font-size:22px;font-family:'Instrument Serif',serif;color:#1a1a1a;line-height:1.4;margin-bottom:28px;letter-spacing:-0.5px}
  .why-item{margin-bottom:20px}
  .why-title{font-size:15px;font-weight:700;color:#1a1a1a;margin-bottom:4px}
  .why-text{font-size:14px;color:#555;line-height:1.65}

  /* Close */
  .close-slide{text-align:center;padding-top:48px}
  .close-heading{font-size:38px;font-weight:400;line-height:1.25;margin:20px 0;letter-spacing:-1.5px}
  .close-sub{font-size:15px;color:#555;line-height:1.6;max-width:300px;margin:0 auto 40px}
  .close-info{display:inline-block;text-align:left;font-size:14px;color:#555;font-family:'DM Mono',monospace;line-height:2.2}
  .close-buttons{margin-top:36px;display:flex;gap:12px;justify-content:center;flex-wrap:wrap}
  .btn-primary{display:inline-block;padding:12px 24px;border-radius:6px;font-size:13px;font-weight:600;background:#1a1a1a;color:#fff;text-decoration:none;font-family:'DM Mono',monospace}
  .btn-secondary{display:inline-block;padding:12px 24px;border-radius:6px;font-size:13px;font-weight:600;background:transparent;color:#1a1a1a;text-decoration:none;font-family:'DM Mono',monospace;border:1.5px solid #e8e8e8}
  .link-small{font-size:12px;color:#888;font-family:'DM Mono',monospace;text-decoration:none;margin-top:12px;display:inline-block}

  .hint{font-size:11px;color:#888;font-family:'DM Mono',monospace;margin-top:8px}
  .sub-text{font-size:13px;color:#555;line-height:1.5}
</style>
</head>
<body>

<div class="wrap">
  <div class="dots" id="dots"></div>

  <!-- SLIDE 0: COVER -->
  <div class="slide cover" data-slide="0">
    <div class="logo-wrap">
      <svg width="160" height="32" viewBox="0 0 400 80" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="0" y="0" width="56" height="80" rx="8" fill="#000"/>
        <rect x="8" y="8" width="40" height="26" rx="6" fill="#fff"/>
        <rect x="8" y="46" width="40" height="26" rx="6" fill="#fff"/>
        <text x="76" y="58" font-family="'Instrument Sans','Helvetica Neue',sans-serif" font-size="48" font-weight="700" fill="#000" letter-spacing="-1">EIGHT SLEEP</text>
      </svg>
    </div>
    <span class="label label-gray">brand strategy pitch</span>
    <h1 class="serif">The Night<br>Shift</h1>
    <p style="font-size:16px;color:#555;line-height:1.6;max-width:300px;margin:0 auto 36px">
      A creative application for<br><span style="color:#1a1a1a;font-weight:600">Marketing Intern, Brand</span>
    </p>
    <div class="mono" style="font-size:14px;color:#888">Jimena Vázquez · Miami</div>
  </div>

  <!-- SLIDE 1: WHO I AM -->
  <div class="slide" data-slide="1">
    <div style="text-align:center;margin-bottom:28px">
      <div class="avatar">JV</div>
      <div class="serif about-name">Jimena Vázquez</div>
      <div style="margin-top:6px"><span class="label label-gray">who i am</span></div>
    </div>
    <div class="about-item"><div class="about-num">01</div><div><div class="about-title">Northeastern '26</div><div class="about-desc">BS Business Admin & Health Science</div></div></div>
    <div class="about-item"><div class="about-num">02</div><div><div class="about-title">2BalanceU (Forbes Family)</div><div class="about-desc">Researched wearables & longevity with a PhD-level expert</div></div></div>
    <div class="about-item"><div class="about-num">03</div><div><div class="about-title">Built @wellness4her</div><div class="about-desc">Women's health brand, grown from zero</div></div></div>
    <div class="about-item"><div class="about-num">04</div><div><div class="about-title">Harvard Chan School</div><div class="about-desc">Managed social channels reaching 600K+ followers</div></div></div>
    <div class="about-item"><div class="about-num">05</div><div><div class="about-title">Trilingual</div><div class="about-desc">Native English & Spanish, learning Portuguese</div></div></div>
    <div class="about-item"><div class="about-num">06</div><div><div class="about-title">MBG Health Coach</div><div class="about-desc">Certified in health & wellness coaching</div></div></div>
    <a href="https://www.linkedin.com/in/jimena-v%C3%A1zquez/" target="_blank" rel="noopener noreferrer" class="link-small">→ view full resume on linkedin</a>
  </div>

  <!-- SLIDE 2: BRAND AUDIT -->
  <div class="slide" data-slide="2">
    <div style="margin-bottom:28px">
      <span class="label label-gray">brand audit</span>
      <h2 class="serif section-title">Where Eight Sleep wins.</h2>
    </div>
    <div class="audit-item">
      <div class="audit-title">Aspirational Positioning</div>
      <p class="audit-text">The whole 'Tesla of Sleep' thing? It works. Partnering with Hamilton, Huberman, Attia, and Zuckerberg doesn't just build credibility, it makes the Pod feel like a status symbol. People don't just buy it for better sleep, they buy it because of who else sleeps on one.</p>
    </div>
    <div class="audit-item">
      <div class="audit-title">Product-Led Storytelling</div>
      <p class="audit-text">1 billion hours of sleep data is a stat that stops you mid-scroll. And the peer-reviewed studies (like a 56% reduction in menopausal hot flashes) give Eight Sleep something most DTC brands would kill for: real clinical proof.</p>
    </div>
    <div class="audit-item">
      <div class="audit-title">Influencer Strategy</div>
      <p class="audit-text">Alexandra Zatarain's partnership playbook is genuinely best in class. Long term, authentic collabs over one off sponsored posts. You can tell the brand cares about relationships, not just reach, and that shows in the content quality.</p>
    </div>
  </div>

  <!-- SLIDE 3: WHITE SPACE -->
  <div class="slide" data-slide="3">
    <div style="margin-bottom:24px">
      <span class="label label-warm">where i see white space</span>
      <h2 class="serif section-title">Opportunities.</h2>
    </div>
    <div class="opp-item" onclick="toggleOpp(this)">
      <div class="opp-header"><span class="opp-title">Women's Health Angle</span><span class="opp-toggle">+</span></div>
      <div class="opp-body">
        <p class="opp-insight">The menopause study is massive. 56% reduction in hot flashes. But right now, most Eight Sleep content features male biohackers and tech founders. There's a huge audience of women 30 to 55 dealing with hormonal shifts, perimenopause, and disrupted sleep who would connect deeply with this product if they saw themselves in the brand.</p>
        <div class="opp-action"><strong>My move:</strong> Launch a 'Sleep Fitness for Her' content series targeting women experiencing hormonal changes. I've been creating women's health content for years through Wellness for Her, covering PCOS, insulin sensitivity, and hormonal balance. This is literally my lane.</div>
      </div>
    </div>
    <div class="opp-item" onclick="toggleOpp(this)">
      <div class="opp-header"><span class="opp-title">TikTok Organic Growth</span><span class="opp-toggle">+</span></div>
      <div class="opp-body">
        <p class="opp-insight">43.8K followers is solid, but WHOOP has over 1M. Eight Sleep's TikTok currently leans on influencer reposts rather than original brand storytelling. There's room for recurring, ownable formats that build community, not just impressions.</p>
        <div class="opp-action"><strong>My move:</strong> Create a recurring series called '8 Hours with Eight Sleep' showing real members and their sleep data transformations. I've grown @wellness4her from zero and managed Harvard's social channels at 600K+ followers. I know what it takes to build organic traction.</div>
      </div>
    </div>
    <div class="opp-item" onclick="toggleOpp(this)">
      <div class="opp-header"><span class="opp-title">Bilingual + LatAm Expansion</span><span class="opp-toggle">+</span></div>
      <div class="opp-body">
        <p class="opp-insight">Eight Sleep just launched in China, its biggest market expansion ever. Latin America is wide open. High net worth consumers in Mexico City, São Paulo, and Buenos Aires are wellness obsessed and completely untapped.</p>
        <div class="opp-action"><strong>My move:</strong> Develop Spanish language social content and influencer partnerships targeting LatAm wellness communities. I'm a native English and Spanish speaker, currently learning Portuguese. I can create content for these markets starting day one.</div>
      </div>
    </div>
    <div class="hint">tap to expand each</div>
  </div>

  <!-- SLIDE 4: CAMPAIGN -->
  <div class="slide" data-slide="4">
    <div style="margin-bottom:20px">
      <span class="label label-gray">campaign concept</span>
      <h2 class="serif" style="font-size:30px;font-weight:400;letter-spacing:-1px;margin:10px 0 4px;color:#1a1a1a">The Night Shift</h2>
      <p style="font-size:14px;color:#555;font-style:italic">What happens while you sleep determines who you are when you're awake.</p>
    </div>
    <div class="tab-bar">
      <button class="tab-btn active" onclick="switchTab(0)">The Data Drop</button>
      <button class="tab-btn" onclick="switchTab(1)">Sleep Confessions</button>
      <button class="tab-btn" onclick="switchTab(2)">Pod Diaries</button>
    </div>

    <div class="tab-content active" data-tab="0">
      <div class="demo-card">
        <div style="position:absolute;top:-30px;right:-30px;width:120px;height:120px;border-radius:50%;background:radial-gradient(circle,rgba(180,200,220,0.06),transparent 70%)"></div>
        <div class="demo-label" style="color:#556">EXAMPLE POST · CAROUSEL</div>
        <div class="demo-headline" style="font-size:24px">We analyzed 10M nights.</div>
        <div style="font-size:14px;color:#8899aa;margin-bottom:22px">Here's what the top 1% of sleepers do differently.</div>
        <div class="stat-row"><span class="stat-num">68°F</span><span class="stat-label">Avg room temp of top performers</span></div>
        <div class="stat-row"><span class="stat-num">10:47pm</span><span class="stat-label">Most common bedtime</span></div>
        <div class="stat-row"><span class="stat-num">2.1×</span><span class="stat-label">More deep sleep than average</span></div>
      </div>
      <p class="sub-text">Weekly carousel pulling one insight from Eight Sleep's billion-hour dataset. Designed to be saved and shared.</p>
    </div>

    <div class="tab-content" data-tab="1">
      <div class="demo-card">
        <div class="demo-label" style="color:#6b5a42">EXAMPLE · SHORT-FORM VIDEO</div>
        <div style="font-size:14px;color:#ccc;line-height:1.9">
          <span class="script-label">HOOK</span><br>"I used to wake up 4 times a night."<br><br>
          <span class="script-label">STORY</span><br>Member shares their before: scrolling at 2am, dragging through mornings, relying on caffeine.<br><br>
          <span class="script-label">DATA</span><br>Cut to their Eight Sleep app: sleep score 62 → 89 in three weeks.<br><br>
          <span class="script-label">CLOSE</span><br>"I didn't change my mattress. I changed my temperature."
        </div>
      </div>
      <p class="sub-text">Raw, UGC-style 30 to 60 second videos. Real members, real data, real transformation stories.</p>
    </div>

    <div class="tab-content" data-tab="2">
      <div class="demo-card">
        <div class="demo-label" style="color:#556">SERIES · STORY/REEL</div>
        <div class="serif" style="font-size:18px;color:#eee;margin-bottom:20px">5 people. 5 lives. 1 Pod. 7 nights.</div>
        <div class="series-row"><span class="series-num">01</span><span><span class="series-who">The Founder</span><span class="series-desc"> — Series A CEO. 5 hrs/night. Watch what changes.</span></span></div>
        <div class="series-row"><span class="series-num">02</span><span><span class="series-who">The New Mom</span><span class="series-desc"> — 3-month-old, zero routine. Can the Pod help recovery?</span></span></div>
        <div class="series-row"><span class="series-num">03</span><span><span class="series-who">The Athlete</span><span class="series-desc"> — D1 swimmer. Recovery is everything.</span></span></div>
        <div class="series-row"><span class="series-num">04</span><span><span class="series-who">The Night Nurse</span><span class="series-desc"> — 12hr shifts. Circadian chaos.</span></span></div>
        <div class="series-row"><span class="series-num">05</span><span><span class="series-who">The Woman in Perimenopause</span><span class="series-desc"> — Hot flashes, disrupted sleep. The 56% study, lived.</span></span></div>
      </div>
      <p class="sub-text">Weekly docuseries-style Reels. Each episode follows one person for 7 nights.</p>
    </div>
  </div>

  <!-- SLIDE 5: WHY ME -->
  <div class="slide" data-slide="5">
    <span class="label label-gray">why me</span>
    <p class="why-lead serif" style="margin-top:24px">I'm a recent grad applying to an internship on purpose. I'm that eager to get my foot in the door at a health tech company I actually believe in.</p>
    <div class="why-item"><div class="why-title">I have real marketing experience</div><div class="why-text">I managed Harvard's social channels at 600K+ followers. I built Wellness for Her from zero. I led content strategy for a Swedish startup entering the U.S. market and drove 25% growth in 3 months. This isn't hypothetical.</div></div>
    <div class="why-item"><div class="why-title">I've done the research</div><div class="why-text">I worked alongside a PhD on wearable devices and longevity at 2BalanceU. I didn't just study this category. I researched it, wrote about it, and shaped content strategy around it.</div></div>
    <div class="why-item"><div class="why-title">I'm constantly in healthtech rooms</div><div class="why-text">Networking events, conferences, founder meetups. I show up because I know this space is the future and I want to be part of it, one way or another.</div></div>
    <div class="why-item"><div class="why-title">I'm eager to learn and grow</div><div class="why-text">I know what I bring. I also know what I still need to learn. That's exactly why I want to be at Eight Sleep: to grow alongside a team that's redefining what a health tech brand looks like.</div></div>
  </div>

  <!-- SLIDE 6: CLOSE -->
  <div class="slide close-slide" data-slide="6">
    <span class="label label-gray">let's talk</span>
    <h2 class="serif close-heading">I didn't send a<br>cover letter.<br>I sent a campaign.</h2>
    <p class="close-sub">Because the best way to show you I can do this job is to start doing it.</p>
    <div class="close-info">
      Jimena Vázquez<br>Jimenav02@icloud.com<br>(305) 562-0663<br><span style="color:#888">Miami → NYC ready</span>
    </div>
    <div class="close-buttons">
      <a href="https://jimena-port.vercel.app" target="_blank" rel="noopener noreferrer" class="btn-primary">view my portfolio →</a>
      <a href="https://www.linkedin.com/in/jimena-v%C3%A1zquez/" target="_blank" rel="noopener noreferrer" class="btn-secondary">linkedin →</a>
    </div>
  </div>

  <!-- NAV -->
  <div class="nav">
    <span id="prev" onclick="go(current-1)">← back</span>
    <span class="counter" id="counter">1/7</span>
    <span id="next" onclick="go(current+1)">next →</span>
  </div>
</div>

<script>
let current = 0;
const TOTAL = 7;

function go(n) {
  if (n < 0 || n >= TOTAL) return;
  const oldSlide = document.querySelector('.slide.active');
  if (oldSlide) { oldSlide.style.opacity = '0'; oldSlide.style.transform = `translateX(${n > current ? -25 : 25}px)`; }
  setTimeout(() => {
    document.querySelectorAll('.slide').forEach(s => s.classList.remove('active'));
    const newSlide = document.querySelector(`[data-slide="${n}"]`);
    newSlide.style.transform = `translateX(${n > current ? 25 : -25}px)`;
    newSlide.classList.add('active');
    requestAnimationFrame(() => { newSlide.style.opacity = '1'; newSlide.style.transform = 'translateX(0)'; });
    current = n;
    updateNav();
  }, 260);
}

function updateNav() {
  document.getElementById('counter').textContent = `${current+1}/${TOTAL}`;
  document.getElementById('prev').style.color = current === 0 ? '#ddd' : '#555';
  document.getElementById('prev').style.cursor = current === 0 ? 'default' : 'pointer';
  document.getElementById('next').style.color = current === TOTAL-1 ? '#ddd' : '#1a1a1a';
  document.getElementById('next').style.cursor = current === TOTAL-1 ? 'default' : 'pointer';
  document.querySelectorAll('.dot').forEach((d, i) => {
    d.className = 'dot ' + (i === current ? 'active' : 'inactive');
  });
}

function toggleOpp(el) {
  const body = el.querySelector('.opp-body');
  const toggle = el.querySelector('.opp-toggle');
  const isOpen = body.classList.contains('open');
  document.querySelectorAll('.opp-body').forEach(b => b.classList.remove('open'));
  document.querySelectorAll('.opp-toggle').forEach(t => t.classList.remove('open'));
  if (!isOpen) { body.classList.add('open'); toggle.classList.add('open'); }
}

function switchTab(idx) {
  document.querySelectorAll('.tab-btn').forEach((b, i) => b.classList.toggle('active', i === idx));
  document.querySelectorAll('.tab-content').forEach((c, i) => c.classList.toggle('active', i === idx));
}

// Init dots
const dotsEl = document.getElementById('dots');
for (let i = 0; i < TOTAL; i++) {
  const d = document.createElement('div');
  d.className = 'dot ' + (i === 0 ? 'active' : 'inactive');
  d.onclick = () => go(i);
  dotsEl.appendChild(d);
}

// Show first slide
document.querySelector('[data-slide="0"]').classList.add('active');
document.querySelector('[data-slide="0"]').style.opacity = '1';
document.querySelector('[data-slide="0"]').style.transform = 'translateX(0)';
updateNav();
</script>

</body>
</html>
