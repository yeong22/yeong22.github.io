<!-- !DOCTYPE html --> 
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Yewon Choi | Yonsei University</title>
<meta name="description" content="Yewon Choi — Integrated MS-PhD student at Yonsei University working on trustworthy and auditable medical AI." />
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Crimson+Pro:ital,wght@0,400;0,500;0,600;1,500;1,600&family=Ubuntu+Mono&display=swap" rel="stylesheet" />
<style>
  :root{
    --accent:#1f6f78; --accent-dark:#155057; --accent-soft:#e7f1f1;
    --ink:#222; --body:#595959; --faint:#8a929c; --line:#e5e5e5;
    --serif:"Crimson Pro",Georgia,"Times New Roman",serif;
    --mono:"Ubuntu Mono",Menlo,Consolas,monospace;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{background:#fff;color:var(--body);margin:0;font:400 16px/1.5 var(--serif);-webkit-font-smoothing:antialiased;}
  a{color:var(--accent);text-decoration:none;}
  a:hover{color:var(--accent-dark);text-decoration:underline;text-underline-offset:2px;}
  strong,b{color:var(--ink);font-weight:600;}
  .wrapper{width:960px;margin:0 auto;}

  /* left fixed sidebar */
  header{width:232px;float:left;position:fixed;padding-top:4em;text-align:center;}
  .avatar{display:inline-block;margin:0 0 1.1em;width:200px;height:240px;border-radius:11px;overflow:hidden;
    background:linear-gradient(155deg,var(--accent),#2d8b94);color:#fff;font-family:var(--serif);font-weight:500;
    font-size:3.4rem;line-height:240px;box-shadow:0 8px 26px rgba(31,111,120,.20);}
  .avatar img{width:100%;height:100%;object-fit:cover;display:block;}
  header h1{font-weight:600;font-size:28px;line-height:1.15;color:var(--accent);margin:0 0 10px;}
  header .position{font-size:1.05rem;color:var(--ink);display:block;margin-bottom:2px;}
  header .affil{font-size:1.0rem;display:block;margin-bottom:8px;}
  header .email{font-family:var(--mono);font-size:14px;color:var(--body);display:block;margin-top:4px;}
  .social-icons{margin-top:18px;}
  .social-icons a{display:inline-block;width:2.4rem;height:2.4rem;line-height:2.4rem;border-radius:100%;
    text-align:center;color:var(--accent);margin:0 .35rem;transition:transform .2s,background-color .2s,color .2s;}
  .social-icons a:hover{background:#fff;color:var(--accent-dark);transform:scale(1.2);text-decoration:none;}
  .social-icons svg{width:21px;height:21px;fill:currentColor;vertical-align:middle;}
  .social-icons .lbl{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0);}

  /* right content */
  section{width:650px;float:right;padding-top:4em;padding-bottom:50px;}
  section > .block + .block{margin-top:40px;}
  h2{font-weight:500;font-size:157%;line-height:1.1;color:var(--accent);margin:2px 0 15px;}
  h2.sub{border-bottom:1px solid var(--line);padding-bottom:8px;}
  h3{font-weight:600;color:var(--accent);margin:0 0 16px;font-size:1.02rem;}
  p{margin:0 0 16px;}
  .lead{font-size:1.06rem;color:var(--ink);}
  .callout{border-left:3px solid var(--accent);background:#fafdfd;padding:12px 16px;border-radius:0 6px 6px 0;margin:4px 0 0;}
  .callout p{margin:0 0 6px;} .callout p:last-child{margin:0;}

  .interests{display:flex;flex-direction:column;gap:11px;}
  .interest{display:flex;gap:11px;}
  .interest .dot{flex:0 0 auto;margin-top:10px;width:7px;height:7px;border-radius:50%;background:var(--accent);}
  .interest .t{color:var(--ink);font-weight:600;}

  .tl{display:flex;flex-direction:column;gap:16px;}
  .tl .row{display:grid;grid-template-columns:1fr auto;gap:4px 18px;align-items:baseline;}
  .tl .org{color:var(--ink);font-weight:600;}
  .tl .desc{font-size:.98rem;}
  .tl .desc .pos{font-style:italic;}
  .tl .when{color:var(--faint);font-size:.86rem;font-family:var(--mono);white-space:nowrap;}

  .news{display:flex;flex-direction:column;gap:9px;}
  .news .n{display:grid;grid-template-columns:48px 1fr;gap:13px;align-items:baseline;}
  .news .date{color:var(--accent-dark);font-weight:600;font-family:var(--mono);font-size:.8rem;}

  .pubgroup + .pubgroup{margin-top:22px;}
  .pubgroup h3{text-transform:uppercase;letter-spacing:.07em;font-size:.78rem;color:var(--faint);}
  .pub{display:grid;grid-template-columns:132px 1fr;gap:16px;margin-bottom:20px;align-items:start;}
  .thumb .img{width:132px;height:84px;border-radius:7px;overflow:hidden;border:1px solid var(--line);
    background:var(--accent-soft);display:flex;align-items:center;justify-content:center;color:var(--accent-dark);
    font-weight:600;font-size:.74rem;letter-spacing:.05em;text-align:center;padding:6px;line-height:1.25;}
  .thumb .img img{width:100%;height:100%;object-fit:cover;display:block;}
  .pub .title{color:var(--ink);font-weight:600;line-height:1.35;}
  .pub .authors{font-size:.94rem;margin-top:2px;}
  .pub .authors .me{color:var(--ink);font-weight:600;}
  .pub .venue{font-size:.92rem;font-style:italic;color:var(--faint);margin-top:1px;}
  .pub .links{margin-top:8px;display:flex;flex-wrap:wrap;gap:7px;}
  .pub .links a{font-size:.74rem;font-weight:600;color:var(--accent-dark);border:1px solid var(--line);
    background:#fafdfd;border-radius:5px;padding:2px 10px;line-height:1.55;}
  .pub .links a:hover{background:var(--accent-soft);border-color:#d4e6e6;text-decoration:none;}

  .slist{display:flex;flex-direction:column;gap:13px;}
  .slist .h{color:var(--ink);font-weight:600;}
  .slist .m{font-size:.95rem;}

  footer{clear:both;width:650px;float:right;border-top:1px solid var(--line);margin-top:10px;padding:18px 0 40px;color:var(--faint);font-size:.85rem;}

  @media print, screen and (max-width:960px){
    .wrapper{width:auto;margin:0;}
    header,section,footer{float:none;position:static;width:auto;}
    header{padding:28px 0 0;}
    section{padding:24px 0 30px;border-top:1px solid var(--line);margin-top:18px;}
    body{padding:15px;word-wrap:break-word;}
    .avatar{width:150px;height:180px;font-size:2.6rem;line-height:180px;}
  }
  @media (max-width:520px){
    .tl .row{grid-template-columns:1fr;}
    .pub{grid-template-columns:1fr;gap:8px;}
    .thumb .img{width:160px;}
  }
  @media (prefers-reduced-motion:reduce){html{scroll-behavior:auto;}.social-icons a:hover{transform:none;}}
</style>
</head>
<body>
  <div class="wrapper">
    <header id="sidebar"></header>
    <section id="content"></section>
    <footer id="foot"></footer>
  </div>

<!-- ════════════════════════════════════════════════════════════════════
     ⬇️  YOU ONLY EDIT THIS SCRIPT BLOCK.  The design above never needs touching.
     ════════════════════════════════════════════════════════════════════

     HOW TO ADD AN IMAGE  → set  img: "assets/img/yourfile.png"   (or a full https URL)
     HOW TO ADD A PAPER   → copy one { ... } object and paste it into the list
     HOW TO ADD/REMOVE A LINK BUTTON → edit the  links: [ ... ]  array (PDF / Code / etc.)
     Leave a field as ""  to hide it. Your name is auto-bolded in author lists.
-->
<script>
const SITE = {

  /* ---------- 1. IDENTITY (left sidebar) ---------- */
  name:        "Yewon Choi",
  position:    "Integrated MS-PhD Student",
  affiliation: "Yonsei University",
  affiliationUrl: "https://www.yonsei.ac.kr/",
  subline:     "AI Researcher, IIDH · Severance Hospital",
  email:       "yewon0126@yonsei.ac.kr",

  // PROFILE PHOTO — paste the path here. Leave "" to show "YC" placeholder.
  photo: "",                      //  e.g.  "assets/img/profile.jpg"

  // SOCIAL LINKS — leave "" to hide that icon.
  links: {
    scholar:  "https://scholar.google.com/",
    cv:       "assets/files/CV_yewon.pdf",
    github:   "https://github.com/",
    linkedin: "https://www.linkedin.com/",
  },

  /* ---------- 2. INTRO ---------- */
  introHeading: "Hi, I'm Yewon",
  introLead: "I build medical AI that clinicians can actually trust and verify.",
  introParagraphs: [
    "I am an integrated MS-PhD student in the Department of Integrative Medicine at Yonsei University, advised by Prof. Sungjun Kim, and an AI Researcher at the Institute for Innovation in Digital Healthcare (Severance Hospital). My goal is to develop reliable and trustworthy medical AI models that hold up under the demands of real-world clinical deployment.",
    "My recent work centers on <strong>LLM alignment, auditability, and evaluation metrics</strong> for clinical use — asking not just whether a model is right, but whether its reasoning can be inspected and defended. Earlier, I developed explainable and interpretable methods for medical imaging and longitudinal EHR data using approaches such as SHAP and Cox modeling. I am also drawn to causal inference, epidemiology, clinical LLMs, and automated systematic reviews and meta-analysis.",
  ],
  introCallout: [
    "<strong>Interested in collaborating?</strong> I welcome collaborations on auditable medical AI, clinical NLP, and causal epidemiology — feel free to reach out.",
    "<strong>Want to chat?</strong> Send me a short email with some context, and we'll find a time.",
  ],

  /* ---------- 3. RESEARCH INTERESTS ---------- */
  interests: [
    { t:"Trustworthy & Auditable Medical AI", d:"LLM alignment, auditability, and evaluation metrics built for clinical deployment." },
    { t:"Explainable AI for Imaging & EHR",    d:"interpretable models for medical images and longitudinal health data using SHAP and Cox modeling." },
    { t:"Causal Inference & Epidemiology",     d:"DAG-based causal analysis applied to large national health cohorts." },
    { t:"Clinical LLMs & Evidence Synthesis",  d:"automated systematic reviews, meta-analysis, and span-grounded reasoning pipelines." },
  ],

  /* ---------- 4. WORK EXPERIENCE ---------- */
  experience: [
    { org:"Severance Hospital — IIDH", pos:"AI Researcher", desc:", Institute for Innovation in Digital Healthcare", when:"Mar 2025 – Present" },
    { org:"VATA Co., Ltd.", pos:"Co-Founder & Co-CEO", desc:" — Clonefit, 3D body-avatar app from 2D images; secured $90K (Naver D2SF, MSS, Yonsei AI).", when:"Apr 2024 – Present" },
    { org:"Korea AI Medical Healthcare Research Institute", pos:"Researcher", desc:" — 3D body-shape analysis for chronic-disease prognosis; AI medical-device consulting.", when:"Aug 2021 – Apr 2023" },
    { org:"Gangnam CHA Hospital", pos:"Intern", desc:", Infection Control Office — public-health materials, COVID-19 support, facility statistics.", when:"Jan 2020 – Mar 2020" },
  ],

  /* ---------- 5. EDUCATION ---------- */
  education: [
    { org:"Yonsei University", desc:"Integrated MS-PhD, Dept. of Integrative Medicine · Advisor: Prof. Sungjun Kim", when:"Mar 2022 – Present" },
    { org:"CHA University", desc:"B.S. in AI Healthcare · Double major in Data Science & Management", when:"Mar 2018 – Feb 2022" },
  ],

  /* ---------- 6. NEWS ---------- */
  news: [
    { date:"2026", text:"📄 Paper on an interpretable radiomics model for bladder cancer grading accepted to <i>European Urology Open Science</i>." },
    { date:"2026", text:"📄 Liver cancer risk-stratification study accepted to <i>BMC Medical Informatics and Decision Making</i>." },
    { date:"2026", text:"🎤 Abstract accepted for presentation at the <i>EAU Congress 2026</i>." },
    { date:"2025", text:"🏆 Best Poster Presentation Award (LLM & Agent Track) at <i>KOSAIM 2025</i>." },
    { date:"2025", text:"📝 Filed a Korean patent on visual explanation of bladder cancer grade prediction." },
    { date:"2025", text:"🎓 Joined the Institute for Innovation in Digital Healthcare (Severance Hospital)." },
  ],

  /* ---------- 7. PUBLICATIONS ----------
     Each paper:
       img:    "assets/img/xxx.png"   ← THE IMAGE. Leave "" to show the `thumb` text instead.
       thumb:  "PLACEHOLDER TEXT"      ← shown only while img is empty
       title / authors / venue
       links:  [{label, url}, ...]     ← PDF / Code / BibTex buttons (omit array to show none)
  */
  publications: [
    { group:"Journal Articles", items:[
      {
        img:"", thumb:"CYSTOSCOPY RADIOMICS",
        title:"A Novel Radiomics-based Interpretable Model for Bladder Cancer Grade Prediction Using White-Light Cystoscopy Images",
        authors:"Yewon Choi, Sang Wouk Cho, Junho Hong, Jongsoo Lee, Hwiyoung Kim*, Kwang Suk Lee*",
        venue:"European Urology Open Science, 87, 71–79, 2026",
        links:[{label:"PDF",url:"#"},{label:"Code",url:"#"}],
      },
      {
        img:"", thumb:"LIVER DEEP LEARNING",
        title:"Liver Cancer Risk Stratification Using Deep Learning on Nationwide Longitudinal Health Screening Data: A Retrospective Cohort Study",
        authors:"Yewon Choi, Sungmin Cho, Changdai Gu, Chungho Kim, Bomi Park*, Hwiyoung Kim*",
        venue:"BMC Medical Informatics and Decision Making, 26:44, 2026",
        links:[{label:"PDF",url:"#"},{label:"Code",url:"#"}],
      },
      {
        img:"", thumb:"3D BODY SCANNER",
        title:"An Analysis of Healthcare Application Research and Standardization Trends on 3D Body Scanner",
        authors:"Yewon Choi, Jisu Hong, Jungwon Kim, Jongsoo Han*, Young Huh*",
        venue:"Society for Standards Certification and Safety, 13(4), 1–18, 2023",
        links:[{label:"PDF",url:"#"}],
      },
    ]},
    { group:"Conference · International", items:[
      {
        img:"", thumb:"BLADDER GRADING",
        title:"P0630 — A Visually Interpretable Radiomics Model for Bladder Cancer Grading Using White-Light Cystoscopy Images",
        authors:"Yewon Choi, Sang Wouk Cho, Junho Hong, Jongsoo Lee, Hwiyoung Kim*, Kwang Suk Lee*",
        venue:"European Urology — EAU Congress 2026 Abstract",
        links:[{label:"PDF",url:"#"}],
      },
      {
        img:"", thumb:"SPINE BALANCE",
        title:"A Comparative Study of the Sagittal and Coronal Plane Balance of the Spine Measured Using a 3D Full Body Scanner and Spine X-Ray",
        authors:"Tae Hoon Kang, Minseok Choi, Yewon Choi, Jungwon Kim, Jae Hyup Lee*, Yohan Lee*, Minjoon Cho*",
        venue:"3DBODY.TECH, 2023",
        links:[{label:"PDF",url:"#"}],
      },
    ]},
    { group:"Conference · Domestic", items:[
      {
        img:"", thumb:"ICU LLM MORTALITY",
        title:"Developing an Early Mortality Prediction Model for ICU Patients Using LLM-Based Approaches",
        authors:"Soojung Choi, Sungmin Cho, Yewon Choi, Minsun Kim, Hwiyoung Kim",
        venue:"Korean Society of Artificial Intelligence in Medicine (KOSAIM), 2025",
        links:[{label:"PDF",url:"#"}],
      },
      {
        img:"", thumb:"LIVER RISK",
        title:"Liver Cancer Risk Stratification via Deep Learning on Longitudinal Nationwide Health Screening Data",
        authors:"Yewon Choi, Sungmin Cho, Changdai Gu, Chungho Kim, Bomi Park*, Hwiyoung Kim*",
        venue:"Korean Society of Artificial Intelligence in Medicine (KOSAIM), 2025",
        links:[{label:"PDF",url:"#"}],
      },
      {
        img:"", thumb:"SCANNER STANDARDS",
        title:"A Study on Standardization Trends for 3D Full-Body Scanner Utilization in Healthcare",
        authors:"Yewon Choi, Jungwon Kim, Jisu Hong",
        venue:"ICS 2023 Symposium on Information and Control, 2023",
        links:[{label:"PDF",url:"#"}],
      },
    ]},
  ],

  /* ---------- 8. BOOKS & PATENTS ---------- */
  booksPatents: [
    { h:"📘 Everything About Medical Imaging AI, Part I: From Development Environment Setup to ML Model Development",
      m:'Sang Wouk Cho, <strong>Yewon Choi</strong>, Junho Hong, Hyundo Jung · WikiDocs (e-book), 2025 · <a href="https://wikidocs.net/book/10449" target="_blank" rel="noopener">wikidocs.net/book/10449</a>' },
    { h:"📄 Apparatus, Method, and Computer-Readable Medium for the Visual Explanation of Bladder Cancer Grade Prediction",
      m:"Kwang Suk Lee, Sang Wouk Cho, Jongsoo Lee, Hwiyoung Kim, <strong>Yewon Choi</strong> · Application No. 10-2025-0130194, Republic of Korea, 2025" },
  ],

  /* ---------- 9. HONORS & AWARDS ---------- */
  honors: [
    { h:"🏆 Best Poster Presentation Award — LLM & Agent Track, KOSAIM 2025",
      m:'"Developing an Early Mortality Prediction Model for ICU Patients Using LLM-Based Approaches."' },
    { h:"🥇 10th Place — AOCR2024 AI Challenge (Second Stage)",
      m:"Kaggle competition on acute appendicitis classification from contrast-enhanced CT scans." },
  ],

  footer: "© 2026 Yewon Choi · Built with a single HTML file · Hosted on GitHub Pages",
};

/* ════════════════════════════════════════════════════════════════════
   RENDERER — you normally never need to touch anything below this line.
   ════════════════════════════════════════════════════════════════════ */
const ICONS = {
  scholar:'<path d="M5.242 13.769L0 9.5 12 0l12 9.5-5.242 4.269C17.548 11.249 14.978 9.5 12 9.5c-2.977 0-5.548 1.748-6.758 4.269zM12 10a7 7 0 1 0 0 14 7 7 0 0 0 0-14z"/>',
  cv:'<path d="M6 2a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8l-6-6H6zm7 1.5L18.5 9H13V3.5zM8 12.5h8V14H8v-1.5zm0 3.5h8v1.5H8V16z"/>',
  github:'<path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.5 11.5 0 0 1 12 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222 0 1.606-.014 2.898-.014 3.293 0 .322.216.694.825.576C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>',
  linkedin:'<path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>',
};
const ICON_TITLES = { scholar:"Google Scholar", cv:"CV", github:"GitHub", linkedin:"LinkedIn" };

const esc = s => String(s);
const boldName = s => SITE.name ? esc(s).split(SITE.name).join(`<span class="me">${SITE.name}</span>`) : esc(s);

function renderSidebar(){
  const avatar = SITE.photo
    ? `<a class="avatar"><img src="${SITE.photo}" alt="${SITE.name}"></a>`
    : `<a class="avatar">${SITE.name.split(' ').map(w=>w[0]).join('').slice(0,2).toUpperCase()}</a>`;
  const affil = SITE.affiliation
    ? `<a class="affil" href="${SITE.affiliationUrl||'#'}" target="_blank" rel="noopener">${SITE.affiliation}</a>` : '';
  const sub = SITE.subline ? `<span class="affil" style="color:var(--body)">${SITE.subline}</span>` : '';
  const email = SITE.email ? `<span class="email">${SITE.email}</span>` : '';
  const icons = Object.keys(ICONS).map(k=>{
    const url = SITE.links[k]; if(!url) return '';
    return `<a href="${url}" target="_blank" rel="noopener" title="${ICON_TITLES[k]}">
      <span class="lbl">${ICON_TITLES[k]}</span>
      <svg viewBox="0 0 24 24" aria-hidden="true">${ICONS[k]}</svg></a>`;
  }).join('');
  return `${avatar}
    <h1>${SITE.name}</h1>
    <span class="position">${SITE.position}</span>
    ${affil}${sub}${email}
    <div class="social-icons">${icons}</div>`;
}

function block(id, heading, inner, sub=true){
  return `<div class="block" id="${id}"><h2${sub?' class="sub"':''}>${heading}</h2>${inner}</div>`;
}

function renderContent(){
  let html = '';

  // intro
  html += `<div class="block" id="about">
    <h2>${SITE.introHeading}</h2>
    <p class="lead">${SITE.introLead}</p>
    ${SITE.introParagraphs.map(p=>`<p>${p}</p>`).join('')}
    <div class="callout">${SITE.introCallout.map(p=>`<p>${p}</p>`).join('')}</div>
  </div>`;

  // interests
  html += block('interests','Research Interests',
    `<div class="interests">${SITE.interests.map(i=>
      `<div class="interest"><span class="dot"></span><div><span class="t">${i.t}</span> — ${i.d}</div></div>`).join('')}</div>`);

  // experience
  html += block('experience','Work Experience',
    `<div class="tl">${SITE.experience.map(e=>
      `<div class="row"><div><div class="org">${e.org}</div><div class="desc"><span class="pos">${e.pos||''}</span>${e.desc||''}</div></div><div class="when">${e.when||''}</div></div>`).join('')}</div>`);

  // education
  html += block('education','Education',
    `<div class="tl">${SITE.education.map(e=>
      `<div class="row"><div><div class="org">${e.org}</div><div class="desc">${e.desc||''}</div></div><div class="when">${e.when||''}</div></div>`).join('')}</div>`);

  // news
  html += block('news','News',
    `<div class="news">${SITE.news.map(n=>
      `<div class="n"><span class="date">${n.date}</span><span>${n.text}</span></div>`).join('')}</div>`);

  // publications
  const pubInner = SITE.publications.map(g=>
    `<div class="pubgroup"><h3>${g.group}</h3>${g.items.map(p=>{
      const thumb = p.img ? `<img src="${p.img}" alt="">` : (p.thumb||'');
      const links = (p.links&&p.links.length)
        ? `<div class="links">${p.links.map(l=>`<a href="${l.url||'#'}" target="_blank" rel="noopener">${l.label}</a>`).join('')}</div>` : '';
      return `<div class="pub">
        <div class="thumb"><div class="img">${thumb}</div></div>
        <div class="body">
          <div class="title">${p.title}</div>
          <div class="authors">${boldName(p.authors)}</div>
          <div class="venue">${p.venue}</div>
          ${links}
        </div></div>`;
    }).join('')}</div>`).join('');
  html += `<div class="block" id="publications"><h2 class="sub">Publications</h2>
    <p style="font-size:.9rem;margin:-6px 0 18px">* Equal contribution · <strong>bold</strong> = me</p>${pubInner}</div>`;

  // books & patents
  html += block('other','Books & Patents',
    `<div class="slist">${SITE.booksPatents.map(x=>`<div><div class="h">${x.h}</div><div class="m">${x.m}</div></div>`).join('')}</div>`);

  // honors
  html += block('honors','Honors & Awards',
    `<div class="slist">${SITE.honors.map(x=>`<div><div class="h">${x.h}</div><div class="m">${x.m}</div></div>`).join('')}</div>`);

  return html;
}

document.getElementById('sidebar').innerHTML = renderSidebar();
document.getElementById('content').innerHTML = renderContent();
document.getElementById('foot').innerHTML = SITE.footer;
document.title = SITE.name + " | " + SITE.affiliation;
</script>
</body>
</html>
