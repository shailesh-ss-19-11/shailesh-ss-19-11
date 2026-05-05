  Shailesh Gokhale | Full Stack Developer  \*, \*::before, \*::after { margin: 0; padding: 0; box-sizing: border-box; } :root { --cyan: #00d4ff; --purple: #7c3aed; --purple-light: #a78bfa; --green: #34d399; --yellow: #fbbf24; --orange: #fb923c; --bg: #080c14; --bg2: #0d1221; --bg3: #111827; --border: rgba(255,255,255,0.06); --border-cyan: rgba(0,212,255,0.2); --text: #e2e8f0; --text-muted: #64748b; --text-dim: #374151; } html { scroll-behavior: smooth; } body { background: var(--bg); color: var(--text); font-family: 'Rajdhani', sans-serif; overflow-x: hidden; min-height: 100vh; } /\* ANIMATED GRID BACKGROUND \*/ body::before { content: ''; position: fixed; inset: 0; background-image: linear-gradient(rgba(0,212,255,0.035) 1px, transparent 1px), linear-gradient(90deg, rgba(0,212,255,0.035) 1px, transparent 1px); background-size: 44px 44px; animation: gridPulse 5s ease-in-out infinite; pointer-events: none; z-index: 0; } @keyframes gridPulse { 0%,100% { opacity:.4; } 50% { opacity:1; } } /\* SCANLINE \*/ body::after { content: ''; position: fixed; top: -100%; left: 0; right: 0; height: 3px; background: linear-gradient(90deg, transparent, rgba(0,212,255,.35), transparent); animation: scanDown 7s linear infinite; pointer-events: none; z-index: 9999; } @keyframes scanDown { to { top: 110%; } } /\* PARTICLES \*/ #particles { position: fixed; inset: 0; pointer-events: none; z-index: 0; } .particle { position: absolute; width: 2px; height: 2px; border-radius: 50%; opacity: 0; animation: floatUp linear infinite; } @keyframes floatUp { 0% { transform: translateY(100vh); opacity: 0; } 10% { opacity: 1; } 90% { opacity: .8; } 100% { transform: translateY(-120px); opacity: 0; } } .wrapper { position: relative; z-index: 1; max-width: 920px; margin: 0 auto; padding: 32px 20px 80px; } /\* ── HERO ── \*/ .hero { text-align: center; padding: 50px 0 36px; position: relative; } .hero-glow { position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); width: 560px; height: 320px; background: radial-gradient(ellipse, rgba(0,212,255,.07) 0%, transparent 70%); pointer-events: none; animation: heroGlow 3.5s ease-in-out infinite; } @keyframes heroGlow { 0%,100% { opacity:.5; transform:translate(-50%,-50%) scale(1); } 50% { opacity:1; transform:translate(-50%,-50%) scale(1.1); } } .avatar-wrap { display: inline-block; position: relative; margin-bottom: 22px; } .ring1, .ring2 { position: absolute; border-radius: 50%; border: 2px solid transparent; } .ring1 { inset: -8px; border-top-color: var(--cyan); border-right-color: var(--cyan); animation: spin 3s linear infinite; } .ring2 { inset: -16px; border-bottom-color: var(--purple); border-left-color: var(--purple); animation: spin 4.5s linear infinite reverse; } @keyframes spin { to { transform: rotate(360deg); } } .avatar { width: 96px; height: 96px; border-radius: 50%; background: linear-gradient(135deg, #0f2027, #203a43, #2c5364); border: 3px solid #1a2a3a; display: flex; align-items: center; justify-content: center; font-family: 'JetBrains Mono', monospace; font-size: 30px; font-weight: 800; color: var(--cyan); position: relative; z-index: 1; box-shadow: 0 0 30px rgba(0,212,255,.15); } .hero-name { font-family: 'JetBrains Mono', monospace; font-size: clamp(32px, 6vw, 54px); font-weight: 800; background: linear-gradient(90deg, var(--cyan), var(--purple-light), var(--cyan)); background-size: 200% auto; -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; animation: shine 3s linear infinite; margin-bottom: 8px; line-height: 1.1; } @keyframes shine { to { background-position: 200% center; } } .hero-sub { font-size: 14px; color: var(--text-muted); letter-spacing: 4px; text-transform: uppercase; font-family: 'JetBrains Mono', monospace; margin-bottom: 18px; } .typer-wrap { height: 30px; margin-bottom: 28px; display: flex; align-items: center; justify-content: center; } #typer { font-family: 'JetBrains Mono', monospace; font-size: 15px; color: var(--cyan); } #typer::after { content: '|'; color: var(--purple-light); animation: blink .7s step-end infinite; margin-left: 2px; } @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} } .badges { display: flex; flex-wrap: wrap; justify-content: center; gap: 8px; } .badge { display: inline-flex; align-items: center; gap: 5px; padding: 5px 14px; border-radius: 20px; font-size: 12px; font-family: 'JetBrains Mono', monospace; font-weight: 700; border: 1px solid; transition: transform .25s, box-shadow .25s; opacity: 0; animation: fadeSlideUp .5s ease forwards; cursor: default; } .badge:hover { transform: translateY(-3px) scale(1.05); box-shadow: 0 0 18px currentColor; } .b-cyan { color:var(--cyan); border-color:rgba(0,212,255,.4); background:rgba(0,212,255,.08); } .b-purple { color:var(--purple-light); border-color:rgba(124,58,237,.4); background:rgba(124,58,237,.08); } .b-green { color:var(--green); border-color:rgba(52,211,153,.4); background:rgba(52,211,153,.08); } .b-orange { color:var(--orange); border-color:rgba(251,146,60,.4); background:rgba(251,146,60,.08); } @keyframes fadeSlideUp { from { opacity:0; transform:translateY(12px); } to { opacity:1; transform:translateY(0); } } /\* ── DIVIDER ── \*/ .divider { height: 1px; background: linear-gradient(90deg, transparent, rgba(0,212,255,.2), rgba(124,58,237,.2), transparent); margin: 10px 0; } /\* ── SECTION HEADER ── \*/ .sec { display: flex; align-items: center; gap: 12px; margin: 40px 0 18px; } .sec-icon { width: 38px; height: 38px; border-radius: 9px; background: rgba(0,212,255,.09); border: 1px solid rgba(0,212,255,.28); display: flex; align-items: center; justify-content: center; font-size: 17px; animation: iconPulse 2.5s ease-in-out infinite; flex-shrink: 0; } @keyframes iconPulse { 0%,100% { box-shadow: 0 0 0 0 rgba(0,212,255,.3); } 50% { box-shadow: 0 0 0 7px rgba(0,212,255,0); } } .sec-title { font-family: 'JetBrains Mono', monospace; font-size: 17px; font-weight: 700; color: var(--text); letter-spacing: 1px; } .sec-line { flex: 1; height: 1px; background: linear-gradient(90deg, rgba(0,212,255,.25), transparent); } /\* ── ABOUT CARD ── \*/ .about-card { background: rgba(255,255,255,.018); border: 1px solid rgba(0,212,255,.14); border-radius: 13px; padding: 22px 24px; font-family: 'JetBrains Mono', monospace; font-size: 13px; position: relative; overflow: hidden; } .about-card::before { content: ''; position: absolute; top:0; left:0; width:3px; height:100%; background: linear-gradient(180deg, var(--cyan), var(--purple)); border-radius: 3px 0 0 3px; } .yl { line-height: 2.1; } .yk { color: #a78bfa; } .yv { color: #a8dadc; } .ys { color: #34d399; } .yc { color: var(--text-dim); } .yi { padding-left: 22px; display: block; } /\* ── TIMELINE ── \*/ .timeline { position: relative; padding-left: 30px; } .timeline::before { content: ''; position: absolute; left: 11px; top:0; bottom:0; width:1px; background: linear-gradient(180deg, var(--cyan), var(--purple), rgba(124,58,237,.08)); } .exp { position: relative; background: rgba(255,255,255,.018); border: 1px solid var(--border); border-radius: 13px; padding: 18px 20px 15px; margin-bottom: 16px; transition: background .3s, border-color .3s, transform .3s, box-shadow .3s; opacity: 0; animation: expIn .5s ease forwards; } .exp:hover { background: rgba(0,212,255,.04); border-color: rgba(0,212,255,.24); transform: translateX(5px); box-shadow: -4px 0 24px rgba(0,212,255,.08); } @keyframes expIn { from { opacity:0; transform:translateX(-16px); } to { opacity:1; transform:translateX(0); } } .exp-dot { position: absolute; left: -26px; top: 21px; width: 13px; height: 13px; border-radius: 50%; border: 2px solid; background: var(--bg); animation: dotPulse 2.2s ease-in-out infinite; } @keyframes dotPulse { 0%,100% { box-shadow: 0 0 0 0 currentColor; } 50% { box-shadow: 0 0 0 5px transparent; } } .dc { color:var(--cyan); border-color:var(--cyan); } .dg { color:var(--green); border-color:var(--green); } .dy { color:var(--yellow); border-color:var(--yellow); } .do { color:var(--orange); border-color:var(--orange); } .dm { color:#6b7280; border-color:#6b7280; } .exp-head { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: 6px; margin-bottom: 5px; } .exp-role { font-size:15px; font-weight:700; color:var(--text); } .exp-co { font-size:13px; color:var(--cyan); font-weight:600; margin-top:2px; } .exp-meta { font-size:11px; color:var(--text-dim); font-family:'JetBrains Mono',monospace; white-space:nowrap; } .exp-desc { font-size:13px; color:var(--text-muted); line-height:1.75; margin:9px 0; } .current-pill { display:inline-flex; align-items:center; gap:4px; padding:2px 10px; border-radius:20px; background:rgba(52,211,153,.1); border:1px solid rgba(52,211,153,.3); color:var(--green); font-size:10px; font-family:'JetBrains Mono',monospace; margin-left:8px; vertical-align:middle; } .live { width:6px; height:6px; border-radius:50%; background:var(--green); display:inline-block; animation:livePulse 1s ease-in-out infinite; } @keyframes livePulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:.4;transform:scale(.7)} } .tags { display:flex; flex-wrap:wrap; gap:5px; margin-top:10px; } .tag { font-size:10px; font-family:'JetBrains Mono',monospace; padding:2px 9px; border-radius:4px; background:rgba(124,58,237,.12); color:#a78bfa; border:1px solid rgba(124,58,237,.2); transition:background .2s; } .tag:hover { background:rgba(124,58,237,.25); } /\* ── EDUCATION ── \*/ .edu { display:flex; align-items:center; gap:14px; background:rgba(255,255,255,.018); border:1px solid rgba(124,58,237,.2); border-radius:12px; padding:15px 18px; margin-bottom:10px; transition:background .3s,border-color .3s; } .edu:hover { background:rgba(124,58,237,.06); border-color:rgba(124,58,237,.4); } .edu-icon { width:42px; height:42px; border-radius:10px; flex-shrink:0; background:rgba(124,58,237,.14); border:1px solid rgba(124,58,237,.28); display:flex; align-items:center; justify-content:center; font-size:19px; } .edu-deg { font-size:14px; font-weight:700; color:var(--text); margin-bottom:2px; } .edu-sch { font-size:12px; color:var(--text-muted); font-family:'JetBrains Mono',monospace; } .edu-yr { font-size:11px; color:var(--purple-light); font-family:'JetBrains Mono',monospace; margin-top:3px; } /\* ── SKILLS ── \*/ .skills-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(130px,1fr)); gap: 10px; } .skill { background:rgba(255,255,255,.018); border:1px solid var(--border); border-radius:11px; padding:13px 10px; text-align:center; font-family:'JetBrains Mono',monospace; font-size:11px; color:#94a3b8; transition:all .3s; cursor:default; position:relative; overflow:hidden; opacity:0; animation:skillPop .4s ease forwards; } .skill::before { content:''; position:absolute; inset:0; background:linear-gradient(135deg,rgba(0,212,255,.05),transparent); opacity:0; transition:opacity .3s; } .skill:hover { border-color:rgba(0,212,255,.3); color:var(--text); transform:translateY(-4px); box-shadow:0 10px 24px rgba(0,0,0,.35), 0 0 20px rgba(0,212,255,.08); } .skill:hover::before { opacity:1; } @keyframes skillPop { from { opacity:0; transform:scale(.82); } to { opacity:1; transform:scale(1); } } .sk-icon { font-size:22px; margin-bottom:6px; display:block; } .sk-name { display:block; margin-bottom:6px; } .sk-dots { display:flex; gap:3px; justify-content:center; } .sd { width:5px; height:5px; border-radius:50%; background:rgba(255,255,255,.1); transition:background .3s; } .sd.on { background:var(--cyan); } /\* ── STATS ── \*/ .stats-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(160px,1fr)); gap:12px; } .stat { background:rgba(255,255,255,.018); border:1px solid var(--border); border-radius:13px; padding:18px; text-align:center; position:relative; overflow:hidden; transition:transform .3s, border-color .3s; opacity:0; animation:statRise .6s ease forwards; } .stat::after { content:''; position:absolute; bottom:0; left:0; right:0; height:2px; background:var(--ac); transform:scaleX(0); transition:transform .35s; transform-origin:left; } .stat:hover { transform:translateY(-4px); border-color:rgba(255,255,255,.1); } .stat:hover::after { transform:scaleX(1); } @keyframes statRise { from { opacity:0; transform:translateY(22px); } to { opacity:1; transform:translateY(0); } } .stat-num { font-family:'JetBrains Mono',monospace; font-size:30px; font-weight:800; display:block; margin-bottom:4px; } .stat-lbl { font-size:11px; color:var(--text-dim); font-family:'JetBrains Mono',monospace; letter-spacing:1.5px; text-transform:uppercase; } /\* ── CONTACT ── \*/ .contact-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:10px; } .cl { display:flex; align-items:center; gap:11px; background:rgba(255,255,255,.018); border:1px solid var(--border); border-radius:11px; padding:13px 15px; text-decoration:none; color:#94a3b8; font-size:13px; font-family:'JetBrains Mono',monospace; transition:all .3s; cursor:pointer; } .cl:hover { transform:translateY(-3px); color:var(--text); } .cl-icon { width:34px; height:34px; border-radius:8px; display:flex; align-items:center; justify-content:center; font-size:15px; flex-shrink:0; font-weight:700; } .cl-label { font-size:12px; color:var(--text); display:block; margin-bottom:1px; } .cl-val { font-size:11px; display:block; } /\* ── FOOTER ── \*/ footer { text-align:center; padding:50px 0 24px; font-family:'JetBrains Mono',monospace; font-size:12px; animation:footerPulse 2.5s ease-in-out infinite; } @keyframes footerPulse { 0%,100% { color:#1e293b; } 50% { color:#374151; } } /\* SCROLLBAR \*/ ::-webkit-scrollbar { width:5px; } ::-webkit-scrollbar-track { background:var(--bg); } ::-webkit-scrollbar-thumb { background:rgba(0,212,255,.3); border-radius:3px; }

SG

Shailesh Gokhale

Software Engineer & Full Stack Developer

📍 Nagpur / Mumbai, India ⚡ 4+ Years Experience 🏢 Pinnacle Teleservices 📞 +91 8208671941

👤

about\_me.yaml

name: "Shailesh Gokhale"

role: "Full Stack Developer"

company: "Pinnacle Teleservices Pvt Ltd" \# Current

email: saileshgokhale81@gmail.com

linkedin: linkedin.com/in/shailesh-gokhale-react-dev

education: "B.E. Information Technology"

specialties:

\- React.js · Java · Spring Boot · Node.js \- AdonisJS · TypeScript · PostgreSQL · Hibernate \- Docker · AWS · CI/CD · Apache Kafka

passion: "Clean code & scalable architecture"

💼

experience.log

Software Engineer CURRENT

🔷 Pinnacle Teleservices Pvt Ltd

📍 Nagpur  |  Feb 2026 – Present

Building scalable backend services with Java, Spring Boot & Hibernate. Designing RESTful APIs for system integrations, working with PostgreSQL for database optimization, and collaborating with React.js frontend teams.

JavaSpring BootHibernate React.jsPostgreSQLREST APIsGit

Full Stack Developer

🟢 Prevoyance IT Solutions Pvt Ltd

📍 Nagpur  |  Feb 2024 – Jan 2026 · 2 yrs

Specialized in scalable web apps using AdonisJS, TypeScript & PostgreSQL. Focused on backend–database integration, performance optimization, and full-stack delivery.

AdonisJSTypeScriptJavaScript PostgreSQLSQLReact.jsNode.js

Front-end Developer

🟡 Leo Coders Private Limited

📍 Nagpur  |  Nov 2022 – Dec 2023 · 1y 2m

Crafted responsive, pixel-perfect UI components in React.js with Redux state management. Built mobile-first layouts and integrated REST APIs seamlessly.

React.jsReduxJavaScript HTML5CSS3Bootstrap

Associate Software Engineer

🟠 Accrualify, Inc.

📍 Nagpur  |  Dec 2021 – May 2022 · 6m

Developed and maintained web application features, participated in code reviews and testing, building a strong software engineering foundation.

JavaScriptReact.jsHTMLCSSGit

Business Development Executive

⚪ Pixel Values Technolabs

📍 Nagpur  |  Oct 2020 – Oct 2021 · 1 yr

Managed client relationships, coordinated with technical teams, and drove company growth through strategic client acquisition.

Business DevClient RelationsStrategy

Market Research Analyst

⚪ The Lead Market

📍 Nagpur  |  Oct 2019 – Oct 2020 · 1 yr

Conducted competitive analysis and market research, prepared strategic reports and identified growth opportunities.

Market ResearchAnalysisReporting

🎓

education.json

🎓

B.E. – Information Technology

Tulsiramji Gaikwad Patil College of Engineering & Technology

Sep 2016 – Aug 2019

📜

Diploma – Computer Science & Engineering

Abha College of Engineering, Wardha Road

Jul 2013 – Aug 2016

⚙️

skills.config

📊

stats.live

0 years exp

0 companies

0 technologies

0 roles held

🌐

connect.sh

[

in

LinkedInshailesh-gokhale-react-dev

](https://linkedin.com/in/shailesh-gokhale-react-dev)[

⌨

GitHubshailesh-ss-19-11

](https://github.com/shailesh-ss-19-11)[

✉

Gmailsaileshgokhale81@gmail.com

](mailto:saileshgokhale81@gmail.com)[

✍

Dev.toshaileshss1911

](https://dev.to/shaileshss1911)[

◈

StackOverflowShailesh Gokhale

](https://stackoverflow.com/users/18943522/shailesh-gokhale)[

☎

Phone+91 8208671941

](tel:+918208671941)

// designed & built with passion · shailesh gokhale · 2026

// PARTICLES const pc = document.getElementById('particles'); for(let i=0;i<22;i++){ const p = document.createElement('div'); p.className='particle'; p.style.cssText=\` left:${Math.random()\*100}%; animation-duration:${9+Math.random()\*13}s; animation-delay:${Math.random()\*11}s; width:${Math.random()>.5?2:3}px; height:${Math.random()>.5?2:3}px; background:${Math.random()>.6?'#a78bfa':'#00d4ff'}; \`; pc.appendChild(p); } // TYPING const phrases = \[ 'React.js | Java | Spring Boot', 'Full Stack Developer @ Pinnacle', 'Building scalable web systems ⚡', 'PostgreSQL | AdonisJS | TypeScript', 'Open to exciting opportunities 🚀', \]; let pi=0,ci=0,del=false; const te=document.getElementById('typer'); function type(){ const cur=phrases\[pi\]; if(!del){ te.textContent=cur.slice(0,++ci); if(ci===cur.length){del=true;setTimeout(type,1900);return;} setTimeout(type,62); } else { te.textContent=cur.slice(0,--ci); if(ci===0){del=false;pi=(pi+1)%phrases.length;setTimeout(type,320);return;} setTimeout(type,32); } } type(); // SKILLS const skills=\[ {i:'⚛',n:'React.js',l:5},{i:'☕',n:'Java',l:4},{i:'🍃',n:'Spring Boot',l:4}, {i:'🟦',n:'TypeScript',l:4},{i:'🟨',n:'JavaScript',l:5},{i:'🌿',n:'Node.js',l:4}, {i:'🐘',n:'PostgreSQL',l:4},{i:'🍃',n:'MongoDB',l:3},{i:'🐬',n:'MySQL',l:3}, {i:'🎨',n:'CSS3',l:5},{i:'🔴',n:'Redux',l:4},{i:'🐳',n:'Docker',l:3}, {i:'☁',n:'AWS',l:3},{i:'🐙',n:'Git',l:5},{i:'🔥',n:'Firebase',l:3}, {i:'🌀',n:'Tailwind',l:4},{i:'⚡',n:'Kafka',l:3},{i:'🅰',n:'Angular',l:3}, \]; const sg=document.getElementById('skillsGrid'); skills.forEach((s,i)=>{ const c=document.createElement('div'); c.className='skill'; c.style.animationDelay=(i\*.04)+'s'; const dots=Array(5).fill(0).map((\_,d)=>\`<div class="sd${d<s.l?' on':''}"></div>\`).join(''); c.innerHTML=\`<span class="sk-icon">${s.i}</span><span class="sk-name">${s.n}</span><div class="sk-dots">${dots}</div>\`; sg.appendChild(c); }); // COUNTERS function count(id,target){ const el=document.getElementById(id); let n=0,step=target/55; const t=setInterval(()=>{ n+=step; if(n>=target){el.textContent=target;clearInterval(t);return;} el.textContent=Math.floor(n); },18); } setTimeout(()=>{count('c1',4);count('c2',5);count('c3',18);count('c4',6);},500);
