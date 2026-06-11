
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
.wrap { max-width: 860px; margin: 0 auto; padding: 1.5rem 1rem; font-family: var(--font-sans); }
.gh { background: #0d1117; border-radius: 12px; overflow: hidden; border: 0.5px solid #21262d; }
.gh-top { background: #0d1117; padding: 2rem 2rem 0; border-bottom: 0.5px solid #21262d; }
.avatar-row { display: flex; align-items: flex-end; gap: 1.5rem; padding-bottom: 1.5rem; }
.avatar { width: 96px; height: 96px; border-radius: 50%; background: #238636; border: 3px solid #30a14e; display: flex; align-items: center; justify-content: center; flex-shrink: 0; overflow: hidden; }
.avatar-inner { display: grid; grid-template-columns: 1fr 1fr; gap: 4px; width: 70px; height: 70px; }
.av-cell { border-radius: 2px; }
.av-g { background: #39d353; }
.av-w { background: #161b22; }
.name-col { flex: 1; }
.disp { font-size: 22px; font-weight: 500; color: #e6edf3; letter-spacing: -0.3px; }
.uname { font-size: 15px; color: #8b949e; margin-top: 2px; font-family: var(--font-mono); }
.badge-row { display: flex; gap: 6px; margin-top: 8px; flex-wrap: wrap; }
.badge { font-size: 11px; padding: 3px 10px; border-radius: 99px; border: 1px solid; font-family: var(--font-mono); }
.b-green { background: rgba(35,134,54,0.15); color: #3fb950; border-color: rgba(35,134,54,0.4); }
.b-blue { background: rgba(56,139,253,0.12); color: #58a6ff; border-color: rgba(56,139,253,0.35); }
.b-purple { background: rgba(163,113,247,0.12); color: #a371f7; border-color: rgba(163,113,247,0.35); }
.nav-tabs { display: flex; gap: 0; border-top: 0.5px solid #21262d; margin: 0 -2rem; padding: 0 2rem; }
.tab { font-size: 13px; color: #8b949e; padding: 10px 14px; border-bottom: 2px solid transparent; cursor: pointer; white-space: nowrap; }
.tab.active { color: #e6edf3; border-bottom-color: #f78166; font-weight: 500; }
.gh-body { padding: 1.5rem 2rem; background: #0d1117; }
.bio { font-size: 14px; color: #c9d1d9; line-height: 1.7; margin-bottom: 1.25rem; }
.bio .hl { color: #58a6ff; font-weight: 500; }
.bio .hl2 { color: #3fb950; font-weight: 500; }
.sec-label { font-size: 11px; color: #6e7681; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 8px; margin-top: 1.25rem; }
.skill-grid { display: flex; flex-wrap: wrap; gap: 6px; }
.skill { font-size: 12px; padding: 4px 10px; border-radius: 6px; background: #161b22; border: 0.5px solid #30363d; color: #c9d1d9; font-family: var(--font-mono); display: flex; align-items: center; gap: 5px; }
.skill-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
.stats-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 8px; margin-top: 1rem; }
.stat-card { background: #161b22; border: 0.5px solid #21262d; border-radius: 8px; padding: 12px; text-align: center; }
.snum { font-size: 20px; font-weight: 500; color: #e6edf3; display: block; }
.slbl { font-size: 11px; color: #6e7681; display: block; margin-top: 2px; }
.streak-bar { display: flex; justify-content: space-around; background: #161b22; border: 0.5px solid #21262d; border-radius: 8px; padding: 14px; margin-top: 10px; }
.streak-item { text-align: center; }
.sval { font-size: 22px; font-weight: 500; display: block; }
.ssub { font-size: 11px; color: #6e7681; margin-top: 2px; }
.sdiv { width: 0.5px; background: #21262d; }
.graph-wrap { margin-top: 1rem; }
.graph-header { display: flex; justify-content: space-between; font-size: 12px; color: #6e7681; margin-bottom: 8px; align-items: center; }
.legend { display: flex; align-items: center; gap: 4px; font-size: 11px; color: #6e7681; }
.lc { width: 11px; height: 11px; border-radius: 2px; display: inline-block; }
.cg { overflow-x: auto; }
.cgrid { display: grid; grid-template-rows: repeat(7, 11px); grid-auto-flow: column; gap: 3px; width: max-content; }
.cell { width: 11px; height: 11px; border-radius: 2px; }
.c0 { background: #161b22; }
.c1 { background: #0e4429; }
.c2 { background: #006d32; }
.c3 { background: #26a641; }
.c4 { background: #39d353; }
.repo-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 10px; margin-top: 1rem; }
.repo { background: #161b22; border: 0.5px solid #30363d; border-radius: 8px; padding: 14px; cursor: pointer; transition: border-color 0.15s; }
.repo:hover { border-color: #58a6ff; }
.rname { font-size: 13px; font-weight: 500; color: #58a6ff; margin-bottom: 5px; display: flex; align-items: center; gap: 5px; }
.rdesc { font-size: 12px; color: #8b949e; line-height: 1.5; margin-bottom: 10px; }
.rmeta { display: flex; gap: 10px; font-size: 12px; color: #6e7681; align-items: center; }
.ldot { width: 10px; height: 10px; border-radius: 50%; display: inline-block; }
.social-row { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 1rem; }
.soc { display: flex; align-items: center; gap: 6px; font-size: 12px; color: #8b949e; background: #161b22; border: 0.5px solid #30363d; border-radius: 6px; padding: 6px 12px; cursor: pointer; transition: color 0.12s; text-decoration: none; }
.soc:hover { color: #58a6ff; border-color: #58a6ff; }
.follow-row { display: flex; gap: 16px; font-size: 13px; color: #8b949e; margin-top: 10px; }
.follow-row span { color: #e6edf3; font-weight: 500; }
.gh-footer { background: #161b22; border-top: 0.5px solid #21262d; padding: 12px 2rem; display: flex; justify-content: space-between; align-items: center; }
.ft { font-size: 11px; color: #6e7681; }
.ft span { color: #3fb950; }
.copy-btn { font-size: 12px; color: #58a6ff; background: rgba(56,139,253,0.1); border: 0.5px solid rgba(56,139,253,0.35); border-radius: 6px; padding: 5px 14px; cursor: pointer; }
.copy-btn:hover { background: rgba(56,139,253,0.2); }
.copied { text-align: center; font-size: 12px; color: #3fb950; margin-top: 8px; display: none; }
</style>

<h2 style="position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0,0,0,0)">GitHub README profile for Krish_Parashar — AI/ML engineer with Python, C, C++ skills</h2>

<div class="wrap">
<div class="gh">

  <div class="gh-top">
    <div class="avatar-row">
      <div class="avatar">
        <div class="avatar-inner">
          <div class="av-cell av-w"></div><div class="av-cell av-g"></div>
          <div class="av-cell av-g"></div><div class="av-cell av-w"></div>
        </div>
      </div>
      <div class="name-col">
        <div class="disp">Krish Parashar</div>
        <div class="uname">@KrishParashar37</div>
        <div class="badge-row">
          <span class="badge b-green">Aspiring AI/ML Engineer</span>
          <span class="badge b-blue">Open Source</span>
          <span class="badge b-purple">DSA Practitioner</span>
        </div>
        <div class="follow-row">
          <div><span>6</span> followers</div>
          <div><span>14</span> following</div>
        </div>
      </div>
    </div>
    <div class="nav-tabs">
      <div class="tab active">Overview</div>
      <div class="tab">Repositories</div>
      <div class="tab">Projects</div>
      <div class="tab">Stars</div>
    </div>
  </div>

  <div class="gh-body">

    <div class="bio">
      <span class="hl2">Hi there!</span> I'm <span class="hl">Krish Parashar</span> — an <span class="hl">Aspiring AI/ML Engineer</span> from India.<br>
      Proficient in <span class="hl2">C &amp; C++</span> · Practicing <span class="hl2">Data Structures &amp; Algorithms</span> in Python<br>
      Focused on matrix logic, array manipulation &amp; terminal-based projects.
    </div>

    <div class="sec-label">Languages &amp; tools</div>
    <div class="skill-grid">
      <span class="skill"><span class="skill-dot" style="background:#3572A5;"></span>Python</span>
      <span class="skill"><span class="skill-dot" style="background:#f34b7d;"></span>C++</span>
      <span class="skill"><span class="skill-dot" style="background:#555555;"></span>C</span>
      <span class="skill"><span class="skill-dot" style="background:#e34c26;"></span>HTML</span>
      <span class="skill"><span class="skill-dot" style="background:#563d7c;"></span>CSS</span>
      <span class="skill"><span class="skill-dot" style="background:#3178c6;"></span>TypeScript</span>
      <span class="skill"><span class="skill-dot" style="background:#41b883;"></span>Machine Learning</span>
      <span class="skill"><span class="skill-dot" style="background:#FF6F00;"></span>NumPy / Pandas</span>
      <span class="skill"><span class="skill-dot" style="background:#30363d;"></span>Git</span>
    </div>

    <div class="stats-grid">
      <div class="stat-card">
        <span class="snum">2</span>
        <span class="slbl">Repos</span>
      </div>
      <div class="stat-card">
        <span class="snum" style="color:#39d353;">62</span>
        <span class="slbl">Contributions</span>
      </div>
      <div class="stat-card">
        <span class="snum" style="color:#f0883e;">9</span>
        <span class="slbl">Commits this month</span>
      </div>
      <div class="stat-card">
        <span class="snum" style="color:#a371f7;">6</span>
        <span class="slbl">Followers</span>
      </div>
    </div>

    <div class="streak-bar">
      <div class="streak-item">
        <span class="sval" style="color:#e6edf3;">62</span>
        <span class="ssub">Total contributions</span>
      </div>
      <div class="sdiv"></div>
      <div class="streak-item">
        <span class="sval" style="color:#39d353;">Active</span>
        <span class="ssub">Current status</span>
      </div>
      <div class="sdiv"></div>
      <div class="streak-item">
        <span class="sval" style="color:#f0883e;">Jun 2026</span>
        <span class="ssub">Latest activity</span>
      </div>
    </div>

    <div class="graph-wrap">
      <div class="graph-header">
        <span>62 contributions in the last year</span>
        <div class="legend">
          Less <span class="lc c0"></span><span class="lc c1"></span><span class="lc c2"></span><span class="lc c3"></span><span class="lc c4"></span> More
        </div>
      </div>
      <div class="cg"><div class="cgrid" id="cgrid"></div></div>
    </div>

    <div class="sec-label" style="margin-top:1.25rem;">Pinned repositories</div>
    <div class="repo-grid">
      <div class="repo">
        <div class="rname"><i class="ti ti-brand-python" style="font-size:14px;" aria-hidden="true"></i> Trading-app</div>
        <div class="rdesc">Python-based trading application. Explores market logic, data handling, and terminal-based UI patterns.</div>
        <div class="rmeta">
          <span><span class="ldot" style="background:#3572A5;"></span> Python</span>
          <span style="color:#6e7681;">Public</span>
        </div>
      </div>
      <div class="repo">
        <div class="rname"><i class="ti ti-plane" style="font-size:14px;" aria-hidden="true"></i> Flight-booking-web-site</div>
        <div class="rdesc">Web app for flight booking with a clean UI. Demonstrates HTML/CSS frontend with dynamic routing logic.</div>
        <div class="rmeta">
          <span><span class="ldot" style="background:#e34c26;"></span> HTML</span>
          <span>6 commits</span>
        </div>
      </div>
      <div class="repo">
        <div class="rname"><i class="ti ti-map" style="font-size:14px;" aria-hidden="true"></i> Trip-mat</div>
        <div class="rdesc">Trip planning and itinerary manager. Focuses on array manipulation and data organisation in Python.</div>
        <div class="rmeta">
          <span><span class="ldot" style="background:#3572A5;"></span> Python</span>
          <span>3 commits</span>
        </div>
      </div>
    </div>

    <div class="sec-label" style="margin-top:1.25rem;">Current focus</div>
    <div style="background:#161b22; border:0.5px solid #21262d; border-radius:8px; padding:14px; font-size:13px; color:#8b949e; line-height:1.8;">
      <div style="color:#e6edf3; font-weight:500; margin-bottom:6px;">Learning roadmap 2026</div>
      <div style="display:flex; flex-direction:column; gap:6px;">
        <div style="display:flex; align-items:center; gap:8px;"><span style="color:#39d353; font-size:12px;">✓</span> <span>Data Structures &amp; Algorithms (Python)</span></div>
        <div style="display:flex; align-items:center; gap:8px;"><span style="color:#39d353; font-size:12px;">✓</span> <span>Matrix logic &amp; array manipulation</span></div>
        <div style="display:flex; align-items:center; gap:8px;"><span style="color:#58a6ff; font-size:12px;">→</span> <span>Machine Learning fundamentals (scikit-learn)</span></div>
        <div style="display:flex; align-items:center; gap:8px;"><span style="color:#6e7681; font-size:12px;">○</span> <span>Deep Learning with TensorFlow / PyTorch</span></div>
        <div style="display:flex; align-items:center; gap:8px;"><span style="color:#6e7681; font-size:12px;">○</span> <span>Full-stack ML deployment</span></div>
      </div>
    </div>

    <div class="sec-label" style="margin-top:1.25rem;">Connect with me</div>
    <div class="social-row">
      <a class="soc" href="#"><i class="ti ti-brand-github" style="font-size:15px;" aria-hidden="true"></i> KrishParashar37</a>
      <a class="soc" href="#"><i class="ti ti-brand-linkedin" style="font-size:15px;" aria-hidden="true"></i> LinkedIn</a>
      <a class="soc" href="#"><i class="ti ti-mail" style="font-size:15px;" aria-hidden="true"></i> Email me</a>
    </div>

  </div>

  <div class="gh-footer">
    <div class="ft">Profile · <span>KrishParashar37</span> · Updated June 2026</div>
    <button class="copy-btn" onclick="doCopy()">Copy README.md</button>
  </div>
</div>
<div class="copied" id="copied-msg">✓ Copied! Paste into KrishParashar37/KrishParashar37/README.md</div>
</div>

<script>
const weights = [0,0,0,0,1,0,1,0,1,1,2,1,2,3,2,3,4,3,2,3,4,3,2,1,2,3,2,1,0,1,0,1,2,1,2,0,1,0,1,0,0,1,0,1,0,1,0,0,0,0,0,1];
const grid = document.getElementById('cgrid');
weights.forEach((w,wi) => {
  for(let d=0;d<7;d++){
    const c=document.createElement('div');
    const v=Math.max(0,Math.min(4,w + (Math.random()<0.4?Math.floor(Math.random()*2)-1:0)));
    c.className='cell c'+v;
    grid.appendChild(c);
  }
});

const readme = `# Hi there, I'm Krish Parashar! 👋

![Profile Views](https://komarev.com/ghpvc/?username=KrishParashar37&color=green)

## 🚀 About Me

🔭 **Aspiring AI/ML Engineer** from India  
💡 Proficient in **C & C++** | Practicing **Data Structures & Algorithms** in Python  
🧠 Focused on matrix logic, array manipulation, and terminal-based projects  
📈 Currently exploring **Machine Learning fundamentals**

---

## 🛠 Tech Stack

\`Python\` \`C++\` \`C\` \`HTML\` \`CSS\` \`NumPy\` \`Pandas\` \`Git\`

---

## 📊 GitHub Stats

![Krish's GitHub Stats](https://github-readme-stats.vercel.app/api?username=KrishParashar37&show_icons=true&theme=github_dark&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=KrishParashar37&layout=compact&theme=github_dark&hide_border=true)

![GitHub Streak](https://streak-stats.demolab.com/?user=KrishParashar37&theme=github-dark-blue&hide_border=true)

---

## 🗺 Learning Roadmap 2026

- [x] Data Structures & Algorithms (Python)
- [x] Matrix logic & array manipulation  
- [ ] Machine Learning fundamentals (scikit-learn)
- [ ] Deep Learning with TensorFlow / PyTorch
- [ ] Full-stack ML deployment

---

## 📌 Pinned Projects

| Project | Description | Language |
|---|---|---|
| [Trading-app](https://github.com/KrishParashar37/Trading-app) | Terminal trading app | Python |
| [Flight-booking-web-site](https://github.com/KrishParashar37/Flight-booking-web-site) | Flight booking UI | HTML/CSS |
| [Trip-mat](https://github.com/KrishParashar37/Trip-mat) | Trip planner | Python |

---

## 🤝 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin)](https://linkedin.com/in/krishparashar37)
[![GitHub](https://img.shields.io/badge/GitHub-black?style=flat&logo=github)](https://github.com/KrishParashar37)

---

*Last updated: June 2026*`;

function doCopy(){
  navigator.clipboard.writeText(readme).then(()=>{
    const m=document.getElementById('copied-msg');
    m.style.display='block';
    setTimeout(()=>m.style.display='none',3500);
  });
}
</script>
