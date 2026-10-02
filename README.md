from pathlib import Path
from textwrap import dedent

base = Path("/mnt/data/rahul_github_profile")
(base / "assets").mkdir(parents=True, exist_ok=True)

svg = dedent(r'''<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
     width="1600" height="900" viewBox="0 0 1600 900">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#050a10"/>
      <stop offset="0.5" stop-color="#07121b"/>
      <stop offset="1" stop-color="#02070c"/>
    </linearGradient>
    <linearGradient id="cyan" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#00e5ff"/>
      <stop offset="1" stop-color="#587cff"/>
    </linearGradient>
    <linearGradient id="purple" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#8b5cf6"/>
      <stop offset="1" stop-color="#00d9ff"/>
    </linearGradient>
    <filter id="glow">
      <feGaussianBlur stdDeviation="5" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <clipPath id="avatarClip">
      <circle cx="225" cy="190" r="125"/>
    </clipPath>
    <pattern id="grid" width="28" height="28" patternUnits="userSpaceOnUse">
      <path d="M28 0H0V28" fill="none" stroke="#0e2532" stroke-width="1"/>
    </pattern>
    <style>
      .mono{font-family:'DejaVu Sans Mono',monospace}
      .sans{font-family:Arial,Helvetica,sans-serif}
      .muted{fill:#7f96a5}
      .white{fill:#edf7ff}
      .cyanText{fill:#00e5ff}
      .green{fill:#00f5a0}
      .purple{fill:#b78cff}
      .line{stroke:#173544;stroke-width:1}
      .small{font-size:18px}
      .label{font-size:20px;fill:#8ea5b5}
      .value{font-size:20px;fill:#dff7ff}
    </style>
  </defs>

  <!-- Background -->
  <rect width="1600" height="900" rx="28" fill="url(#bg)"/>
  <rect x="1" y="1" width="1598" height="898" rx="27" fill="none" stroke="#17384a" stroke-width="2"/>
  <rect x="0" y="0" width="1600" height="900" fill="url(#grid)" opacity=".22"/>

  <!-- LEFT PROFILE CARD -->
  <rect x="28" y="28" width="430" height="844" rx="24" fill="#071018" stroke="#173b4e" stroke-width="2"/>
  <circle cx="225" cy="190" r="137" fill="none" stroke="url(#purple)" stroke-width="5" filter="url(#glow)"/>
  <image href="profile.jpg" x="100" y="65" width="250" height="250"
         preserveAspectRatio="xMidYMid slice" clip-path="url(#avatarClip)"/>
  <circle cx="225" cy="190" r="125" fill="none" stroke="#00d9ff" stroke-width="3"/>

  <!-- online dot -->
  <circle cx="350" cy="300" r="15" fill="#00e676" stroke="#071018" stroke-width="7"/>
  <circle cx="350" cy="300" r="7" fill="#9affcb"/>

  <text x="225" y="365" text-anchor="middle" class="sans white" font-size="35" font-weight="700">Rahul Kirtoniya</text>
  <text x="225" y="402" text-anchor="middle" class="mono cyanText" font-size="17">FULL STACK ENGINEER</text>
  <text x="225" y="428" text-anchor="middle" class="mono muted" font-size="16">TECHNICAL LEAD  •  AI &amp; AUTOMATION</text>

  <line x1="65" y1="456" x2="395" y2="456" class="line"/>

  <text x="65" y="493" class="mono label">⌖</text>
  <text x="95" y="493" class="mono value">Kolkata, India</text>

  <text x="65" y="530" class="mono label">✉</text>
  <text x="95" y="530" class="mono value">rahulkirtoniya@gmail.com</text>

  <text x="65" y="567" class="mono label">↗</text>
  <text x="95" y="567" class="mono value">rahul-kirtoniya.vercel.app</text>

  <text x="65" y="604" class="mono label">in</text>
  <text x="95" y="604" class="mono value">linkedin.com/in/rahulkirtoniya</text>

  <rect x="65" y="638" width="330" height="48" rx="10" fill="#0b1720" stroke="#2a5369"/>
  <text x="230" y="670" text-anchor="middle" class="mono white" font-size="19">◉  FOLLOW  @RahulKirtoniya</text>

  <line x1="65" y1="715" x2="395" y2="715" class="line"/>

  <text x="115" y="754" text-anchor="middle" class="sans cyanText" font-size="25" font-weight="700">50+</text>
  <text x="115" y="779" text-anchor="middle" class="mono muted" font-size="13">REPOSITORIES</text>

  <text x="230" y="754" text-anchor="middle" class="sans purple" font-size="25" font-weight="700">★</text>
  <text x="230" y="779" text-anchor="middle" class="mono muted" font-size="13">OPEN SOURCE</text>

  <text x="345" y="754" text-anchor="middle" class="sans green" font-size="25" font-weight="700">AI</text>
  <text x="345" y="779" text-anchor="middle" class="mono muted" font-size="13">FOCUS</text>

  <!-- CENTER TERMINAL -->
  <rect x="478" y="28" width="560" height="844" rx="24" fill="#04090e" stroke="#173b4e" stroke-width="2"/>
  <rect x="478" y="28" width="560" height="55" rx="24" fill="#08141c"/>
  <circle cx="510" cy="55" r="8" fill="#ff4d5a"/>
  <circle cx="535" cy="55" r="8" fill="#ffc43d"/>
  <circle cx="560" cy="55" r="8" fill="#26d96f"/>
  <text x="590" y="62" class="mono white" font-size="18">rahul@github: ~/profile</text>

  <text x="505" y="115" class="mono green" font-size="18">&gt; whoami</text>
  <line x1="505" y1="127" x2="1010" y2="127" class="line"/>

  <!-- Stylized ASCII portrait -->
  <g class="mono" fill="#55dfff" opacity=".92" font-size="11">
    <text x="535" y="160">                 .::::::::::::.</text>
    <text x="535" y="175">             .::#@@@@@@@@@@@@#::.</text>
    <text x="535" y="190">          .:#@@@@@@@########@@@@@@#:.</text>
    <text x="535" y="205">        .#@@@@@###::::::::::###@@@@@#.</text>
    <text x="535" y="220">      .#@@@@##::::::::::::::::::##@@@@#.</text>
    <text x="535" y="235">     #@@@##:::::::::..:::::::::::##@@@#</text>
    <text x="535" y="250">    @@@##::::::..:::::::::::..::::##@@@</text>
    <text x="535" y="265">   @@@#::::::..::::::....::::::..::::#@@@</text>
    <text x="535" y="280">  @@@#:::::::.::::.      .::::.:::::::#@@@</text>
    <text x="535" y="295">  @@#:::::::..:::.  .--.  .::..:::::::#@@</text>
    <text x="535" y="310">  @@#:::::::::::   .@@@@.   ::::::::::#@@</text>
    <text x="535" y="325">  @@#:::::::::    .@@@@@@.    ::::::::#@@</text>
    <text x="535" y="340">  @@@#::::::::     @@@@@@     :::::::#@@@</text>
    <text x="535" y="355">   @@@#::::::::     .--.     :::::::#@@@</text>
    <text x="535" y="370">    @@@##::::::::           ::::::##@@@</text>
    <text x="535" y="385">     #@@@##:::::::.........:::::##@@@#</text>
    <text x="535" y="400">       #@@@@##:::::::::::::::##@@@@#</text>
    <text x="535" y="415">         #@@@@@@###:::::###@@@@@@#</text>
    <text x="535" y="430">            ##@@@@@@@@@@@@@@@##</text>
    <text x="535" y="445">          .:::::::::::::::::::::.</text>
    <text x="535" y="460">       .:::::::::::::::::::::::::::.</text>
    <text x="535" y="475">     .::::::###:::::::::::###::::::.</text>
    <text x="535" y="490">    :::::::#####:::::::::#####:::::::</text>
    <text x="535" y="505">   :::::::#######:::::::#######:::::::</text>
    <text x="535" y="520">  :::::::#########:::::#########:::::::</text>
    <text x="535" y="535"> :::::::###########:::###########:::::::</text>
    <text x="535" y="550">:::::::#############@#############:::::::</text>
    <text x="535" y="565">::::::###########################:::::::</text>
    <text x="535" y="580">:::::#############################::::::</text>
    <text x="535" y="595">::::###############################:::::</text>
    <text x="535" y="610">:::#################################::::</text>
    <text x="535" y="625">::###################################:::</text>
    <text x="535" y="640">:#####################################::</text>
    <text x="535" y="655">#######################################:</text>
    <text x="535" y="670">#######################################</text>
    <text x="535" y="685">#######################################</text>
    <text x="535" y="700">#######################################</text>
  </g>

  <text x="758" y="765" text-anchor="middle" class="mono cyanText" font-size="18" letter-spacing="8">
    R A H U L   K I R T O N I Y A
  </text>
  <text x="758" y="800" text-anchor="middle" class="mono muted" font-size="13">
    BUILD • AUTOMATE • SCALE
  </text>

  <!-- RIGHT PANEL -->
  <rect x="1058" y="28" width="514" height="844" rx="24" fill="#071018" stroke="#173b4e" stroke-width="2"/>

  <!-- nav -->
  <text x="1090" y="62" class="mono cyanText" font-size="15">ABOUT</text>
  <text x="1155" y="62" class="mono muted" font-size="15">│</text>
  <text x="1180" y="62" class="mono muted" font-size="15">SKILLS</text>
  <text x="1250" y="62" class="mono muted" font-size="15">│</text>
  <text x="1275" y="62" class="mono muted" font-size="15">PROJECTS</text>
  <text x="1360" y="62" class="mono muted" font-size="15">│</text>
  <text x="1385" y="62" class="mono muted" font-size="15">STATS</text>
  <text x="1440" y="62" class="mono muted" font-size="15">│</text>
  <text x="1465" y="62" class="mono muted" font-size="15">CONTACT</text>

  <!-- about -->
  <rect x="1080" y="90" width="470" height="230" rx="15" fill="#050c12" stroke="#173b4e"/>
  <text x="1100" y="120" class="mono green" font-size="18">&gt; identity</text>
  <line x1="1100" y1="130" x2="1530" y2="130" class="line"/>

  <text x="1100" y="160" class="mono label">NAME</text>
  <text x="1210" y="160" class="mono cyanText" font-size="18">Rahul Kirtoniya</text>

  <text x="1100" y="190" class="mono label">ROLE</text>
  <text x="1210" y="190" class="mono value" font-size="17">Full Stack Engineer</text>

  <text x="1100" y="220" class="mono label">TITLE</text>
  <text x="1210" y="220" class="mono value" font-size="17">Technical Lead</text>

  <text x="1100" y="250" class="mono label">FOCUS</text>
  <text x="1210" y="250" class="mono value" font-size="16">AI + Automation</text>

  <text x="1100" y="280" class="mono label">LOCATION</text>
  <text x="1210" y="280" class="mono value" font-size="16">Kolkata, India</text>

  <text x="1100" y="305" class="mono purple" font-size="13">
    "Build useful software that solves real business problems."
  </text>

  <!-- stack -->
  <rect x="1080" y="340" width="470" height="205" rx="15" fill="#050c12" stroke="#173b4e"/>
  <text x="1100" y="370" class="mono green" font-size="18">&gt; tech-stack</text>
  <line x1="1100" y1="380" x2="1530" y2="380" class="line"/>

  <text x="1100" y="415" class="mono cyanText" font-size="16">PHP</text>
  <text x="1190" y="415" class="mono cyanText" font-size="16">Laravel</text>
  <text x="1300" y="415" class="mono cyanText" font-size="16">React</text>
  <text x="1385" y="415" class="mono cyanText" font-size="16">Next.js</text>
  <text x="1480" y="415" class="mono cyanText" font-size="16">Node.js</text>

  <text x="1100" y="455" class="mono purple" font-size="16">TypeScript</text>
  <text x="1215" y="455" class="mono purple" font-size="16">Python</text>
  <text x="1310" y="455" class="mono purple" font-size="16">MySQL</text>
  <text x="1400" y="455" class="mono purple" font-size="16">AWS</text>
  <text x="1470" y="455" class="mono purple" font-size="16">Git</text>

  <text x="1100" y="495" class="mono green" font-size="16">OpenAI</text>
  <text x="1195" y="495" class="mono green" font-size="16">Claude</text>
  <text x="1285" y="495" class="mono green" font-size="16">LLM</text>
  <text x="1360" y="495" class="mono green" font-size="16">RAG</text>
  <text x="1435" y="495" class="mono green" font-size="16">CI/CD</text>

  <text x="1100" y="525" class="mono muted" font-size="13">
    WEB • AI • CLOUD • AUTOMATION • SAAS
  </text>

  <!-- expertise -->
  <rect x="1080" y="565" width="470" height="125" rx="15" fill="#050c12" stroke="#173b4e"/>
  <text x="1100" y="595" class="mono green" font-size="18">&gt; expertise</text>
  <line x1="1100" y1="605" x2="1530" y2="605" class="line"/>

  <text x="1100" y="635" class="mono white" font-size="15">AI Integration</text>
  <text x="1215" y="635" class="mono white" font-size="15">LLM &amp; RAG</text>
  <text x="1320" y="635" class="mono white" font-size="15">Automation</text>
  <text x="1435" y="635" class="mono white" font-size="15">SaaS</text>

  <text x="1100" y="665" class="mono muted" font-size="14">
    Architecture • APIs • Cloud • Product Engineering
  </text>

  <!-- stats -->
  <rect x="1080" y="710" width="470" height="140" rx="15" fill="#050c12" stroke="#173b4e"/>
  <text x="1100" y="740" class="mono green" font-size="18">&gt; github-stats</text>
  <line x1="1100" y1="750" x2="1530" y2="750" class="line"/>

  <text x="1120" y="790" class="sans cyanText" font-size="25" font-weight="700">50+</text>
  <text x="1120" y="815" class="mono muted" font-size="12">REPOS</text>

  <text x="1225" y="790" class="sans purple" font-size="25" font-weight="700">342</text>
  <text x="1225" y="815" class="mono muted" font-size="12">STARS</text>

  <text x="1330" y="790" class="sans green" font-size="25" font-weight="700">420</text>
  <text x="1330" y="815" class="mono muted" font-size="12">FOLLOWERS</text>

  <text x="1450" y="790" class="sans" fill="#ff69d4" font-size="25" font-weight="700">95</text>
  <text x="1450" y="815" class="mono muted" font-size="12">CONTRIBUTIONS</text>
</svg>
''')

readme = dedent(r'''# Rahul Kirtoniya

<div align="center">

<img src="./assets/github-profile.svg" alt="Rahul Kirtoniya GitHub Profile" width="100%">

</div>

<br>

<div align="center">

### Full Stack Engineer • Technical Lead • AI & Automation

Building web applications, AI integrations, business automation systems and SaaS products.

[Portfolio](https://rahul-kirtoniya.vercel.app/) •
[LinkedIn](https://linkedin.com/in/rahulkirtoniya) •
[GitHub](https://github.com/RahulKirtoniya)

</div>

---

## What I Build

```text
AI Integrations       → OpenAI • Claude • LLM • RAG
Business Automation   → Workflow • WhatsApp • Operations
Web Applications      → Laravel • React • Next.js
Backend Systems       → PHP • Node.js • Python
Cloud & DevOps        → AWS • Git • CI/CD
SaaS Products         → Architecture • APIs • Product Engineering
```

## Core Stack

<p align="center">
<img src="https://skillicons.dev/icons?i=php,laravel,react,nextjs,nodejs,ts,python,mysql,aws,js,html,css,git,github" />
</p>

## Selected Work

- **Expat Management System**  
  Enterprise client management, workflows, bulk operations, filtering and AI-powered automation.

- **WhatsApp Marketing Automation**  
  Customer segmentation, campaigns, message tracking and automated engagement.

- **Government & Compliance Systems**  
  Registration, immigration, renewal, document and compliance workflow systems.

- **AI Business Automation**  
  LLM-powered workflows, intelligent classification, recommendations and business process automation.

---

## Current Direction

```text
$ ./rahul --current-focus

AI-powered SaaS
LLM & RAG applications
AI agents
Business automation
Scalable web applications
Cloud architecture
Product engineering
```

---

<div align="center">

### Build useful software. Automate the repetitive. Ship what matters.

</div>
''')

(base / "README.md").write_text(readme, encoding="utf-8")
(base / "assets" / "github-profile.svg").write_text(svg, encoding="utf-8")

print(f"Created:\n{base/'README.md'}\n{base/'assets/github-profile.svg'}")
