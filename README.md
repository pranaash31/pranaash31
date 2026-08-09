<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 340" width="100%">
  <defs>
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@700');
      @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500');

      .title-text {
        font-family: 'Space Grotesk', 'Segoe UI', system-ui, -apple-system, sans-serif;
        font-weight: 700;
        font-size: 62px;
        fill: url(#titleGradient);
      }
      .subtitle-text {
        font-family: 'JetBrains Mono', 'Consolas', monospace;
        font-weight: 500;
        font-size: 14px;
        fill: #7b8db8;
        letter-spacing: 6px;
      }
      .label-text {
        font-family: 'JetBrains Mono', 'Consolas', monospace;
        font-size: 10px;
        fill: #2d3560;
        letter-spacing: 1.5px;
      }
      .status-text {
        font-family: 'JetBrains Mono', 'Consolas', monospace;
        font-size: 11px;
        fill: #00E5A0;
        letter-spacing: 2px;
      }
      .grid { stroke: #111630; stroke-width: 0.5; }
      .corner { stroke: #1e2650; stroke-width: 1.5; fill: none; }

      @keyframes glow {
        0%, 100% {
          filter: drop-shadow(0 0 8px rgba(0,217,255,0.5)) drop-shadow(0 0 22px rgba(106,0,255,0.3));
        }
        50% {
          filter: drop-shadow(0 0 18px rgba(0,217,255,0.85)) drop-shadow(0 0 45px rgba(106,0,255,0.5));
        }
      }
      .title-group { animation: glow 4s ease-in-out infinite; }

      @keyframes p1 { 0%,100% { opacity:.12 } 50% { opacity:.75 } }
      @keyframes p2 { 0%,100% { opacity:.55 } 50% { opacity:.08 } }
      @keyframes p3 { 0%,100% { opacity:.08 } 50% { opacity:.9 } }
      @keyframes statusPulse { 0%,100% { opacity:.35 } 50% { opacity:1 } }
      .d1 { animation: p1 3.5s ease-in-out infinite }
      .d2 { animation: p2 4.5s ease-in-out infinite }
      .d3 { animation: p3 5.5s ease-in-out infinite }
      .status-dot { animation: statusPulse 2s ease-in-out infinite }
    </style>

    <linearGradient id="bgGrad" x1="0" y1="0" x2="1200" y2="340" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#070a14"/>
      <stop offset="50%" stop-color="#0b0e1c"/>
      <stop offset="100%" stop-color="#090c18"/>
    </linearGradient>

    <linearGradient id="titleGradient" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#FFFFFF">
        <animate attributeName="stop-color" values="#FFFFFF;#E0E7FF;#FFFFFF" dur="5s" repeatCount="indefinite"/>
      </stop>
      <stop offset="30%" stop-color="#C4B5FD">
        <animate attributeName="stop-color" values="#C4B5FD;#00D9FF;#C4B5FD" dur="5s" repeatCount="indefinite"/>
      </stop>
      <stop offset="65%" stop-color="#00D9FF">
        <animate attributeName="stop-color" values="#00D9FF;#8A2BE2;#00D9FF" dur="5s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#6A00FF">
        <animate attributeName="stop-color" values="#6A00FF;#FF3CAC;#6A00FF" dur="5s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <linearGradient id="accentLine" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#6A00FF" stop-opacity="0"/>
      <stop offset="30%" stop-color="#00D9FF" stop-opacity="0.5"/>
      <stop offset="70%" stop-color="#8A2BE2" stop-opacity="0.5"/>
      <stop offset="100%" stop-color="#FF3CAC" stop-opacity="0"/>
    </linearGradient>

    <linearGradient id="bottomStripe" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#6A00FF"/>
      <stop offset="20%" stop-color="#8A2BE2"/>
      <stop offset="40%" stop-color="#00BFFF"/>
      <stop offset="60%" stop-color="#00E5A0"/>
      <stop offset="80%" stop-color="#FFD166"/>
      <stop offset="100%" stop-color="#FF3CAC"/>
    </linearGradient>

    <linearGradient id="waveGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#6A00FF" stop-opacity="0.08"/>
      <stop offset="50%" stop-color="#00BFFF" stop-opacity="0.12"/>
      <stop offset="100%" stop-color="#FF3CAC" stop-opacity="0.08"/>
    </linearGradient>

    <filter id="softGlow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="3.5" result="blur"/>
      <feColorMatrix in="blur" type="matrix" values="0 0 0 0 0  0 0 0 0 0.65  0 0 0 0 1  0 0 0 0.6 0" result="glow"/>
      <feMerge>
        <feMergeNode in="glow"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <!-- BACKGROUND -->
  <rect width="1200" height="340" fill="url(#bgGrad)"/>

  <!-- GRID -->
  <line x1="0" y1="68" x2="1200" y2="68" class="grid"/>
  <line x1="0" y1="136" x2="1200" y2="136" class="grid"/>
  <line x1="0" y1="204" x2="1200" y2="204" class="grid"/>
  <line x1="0" y1="272" x2="1200" y2="272" class="grid"/>
  <line x1="240" y1="0" x2="240" y2="340" class="grid"/>
  <line x1="480" y1="0" x2="480" y2="340" class="grid"/>
  <line x1="720" y1="0" x2="720" y2="340" class="grid"/>
  <line x1="960" y1="0" x2="960" y2="340" class="grid"/>

  <!-- ANIMATED DOTS -->
  <circle cx="95" cy="52" r="2.5" fill="#00D9FF" class="d1"/>
  <circle cx="320" cy="35" r="1.5" fill="#8A2BE2" class="d2"/>
  <circle cx="520" cy="48" r="1" fill="#FFD166" class="d3"/>
  <circle cx="880" cy="42" r="2" fill="#FF3CAC" class="d1"/>
  <circle cx="1060" cy="58" r="1.5" fill="#00E5A0" class="d2"/>
  <circle cx="155" cy="285" r="1.5" fill="#FFD166" class="d3"/>
  <circle cx="420" cy="295" r="2" fill="#8A2BE2" class="d1"/>
  <circle cx="780" cy="280" r="1" fill="#00D9FF" class="d2"/>
  <circle cx="1100" cy="290" r="2" fill="#FF3CAC" class="d3"/>
  <circle cx="40" cy="170" r="1" fill="#00BFFF" class="d1"/>
  <circle cx="1160" cy="155" r="1" fill="#00E5A0" class="d2"/>

  <!-- CORNER BRACKETS -->
  <polyline points="24,45 24,22 47,22" class="corner"/>
  <polyline points="1153,22 1176,22 1176,45" class="corner"/>
  <polyline points="24,295 24,318 47,318" class="corner"/>
  <polyline points="1153,318 1176,318 1176,295" class="corner"/>

  <!-- CORNER LABELS -->
  <text x="32" y="16" class="label-text">SYS.PROFILE</text>
  <text x="1095" y="16" class="label-text">REV.2026.08</text>
  <text x="32" y="334" class="label-text">NODE.ACTIVE</text>
  <text x="1108" y="334" class="label-text">BUILD.01</text>

  <!-- STATUS INDICATOR -->
  <circle cx="505" cy="86" r="4" fill="#00E5A0" class="status-dot"/>
  <text x="516" y="90" class="status-text">ONLINE // READY TO BUILD</text>

  <!-- ACCENT LINE ABOVE NAME -->
  <line x1="250" y1="106" x2="950" y2="106" stroke="url(#accentLine)" stroke-width="1"/>

  <!-- MAIN NAME WITH GLOW -->
  <g class="title-group">
    <text x="600" y="172" text-anchor="middle" class="title-text" filter="url(#softGlow)">SAKTHI PRANAASH V</text>
  </g>

  <!-- ACCENT LINE BELOW NAME -->
  <line x1="250" y1="193" x2="950" y2="193" stroke="url(#accentLine)" stroke-width="1"/>

  <!-- SUBTITLE -->
  <text x="600" y="228" text-anchor="middle" class="subtitle-text">ENGINEERING IDEAS INTO REALITY</text>

  <!-- ANIMATED HEXAGON -->
  <polygon points="600,254 608,258 608,266 600,270 592,266 592,258" fill="none" stroke="#1e2650" stroke-width="1">
    <animate attributeName="stroke" values="#1e2650;#00D9FF;#1e2650" dur="4s" repeatCount="indefinite"/>
  </polygon>

  <!-- SCANNING LINE -->
  <line x1="0" y1="0" x2="1200" y2="0" stroke="#00D9FF" stroke-width="0.5" opacity="0">
    <animate attributeName="y1" values="0;340;0" dur="10s" repeatCount="indefinite"/>
    <animate attributeName="y2" values="0;340;0" dur="10s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0;0.18;0" dur="10s" repeatCount="indefinite"/>
  </line>

  <!-- BOTTOM WAVE SHAPES -->
  <path d="M0,300 C200,275 400,315 600,295 S1000,270 1200,300 L1200,335 L0,335 Z" fill="url(#waveGrad)"/>
  <path d="M0,310 C300,290 500,320 700,305 S1000,285 1200,310 L1200,335 L0,335 Z" fill="url(#waveGrad)"/>

  <!-- BOTTOM GRADIENT STRIPE -->
  <rect x="0" y="335" width="1200" height="5" fill="url(#bottomStripe)"/>
</svg>
</div>

<br>

<p align="center">
I'm an engineering student who believes that the most interesting part of<br>
technology is not what already exists, but <b>what can be built next</b>.
</p>

<p align="center">
I enjoy taking ideas from a blank page, understanding the problem beneath them,<br>
exploring different possibilities, and turning the strongest ideas into something real.<br>
I learn through experimentation, build through iteration, and treat every challenge<br>
as an opportunity to sharpen the way I think.
</p>

<div align="center">
<table>
<tr><td>
<br>
<p align="center">
<i>"For me, engineering is a continuous process of<br>
<b>questioning, creating, failing, understanding, and building better.</b>"</i>
</p>
<br>
</td></tr>
</table>
</div>

<br>

<!-- Engineering Process Flow -->
<div align="center">

<img src="https://img.shields.io/badge/QUESTION-00D9FF?style=flat-square&labelColor=0d1117" alt="Question"/>
&nbsp;
<sub><b>&gt;&gt;</b></sub>
&nbsp;
<img src="https://img.shields.io/badge/CREATE-8A2BE2?style=flat-square&labelColor=0d1117" alt="Create"/>
&nbsp;
<sub><b>&gt;&gt;</b></sub>
&nbsp;
<img src="https://img.shields.io/badge/TEST%20%26%20FAIL-FF3CAC?style=flat-square&labelColor=0d1117" alt="Fail"/>
&nbsp;
<sub><b>&gt;&gt;</b></sub>
&nbsp;
<img src="https://img.shields.io/badge/UNDERSTAND-FFD166?style=flat-square&labelColor=0d1117" alt="Understand"/>
&nbsp;
<sub><b>&gt;&gt;</b></sub>
&nbsp;
<img src="https://img.shields.io/badge/BUILD%20BETTER-00E5A0?style=flat-square&labelColor=0d1117" alt="Build Better"/>

</div>

<br>

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FF3CAC,50:00BFFF,100:6A00FF&height=2&section=header" width="100%"/>
</div>

<br>

<!-- ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀  THREE PILLARS  ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=transparent&text=THE%20THREE%20PILLARS&fontColor=A855F7&fontSize=30&fontAlignY=65&height=52&animation=fadeIn" alt="Section: Pillars"/>

<br>

<sub>A systematic framework for tackling complex technical problems.</sub>

<br><br>

<table>
<tr>

<td align="center" width="33%">
<br>
<img src="https://img.shields.io/badge/_%E2%96%8C_01__%E2%96%90-00D9FF?style=for-the-badge&labelColor=0d1117" alt="01"/>
<br><br>
<h3>THINK</h3>
<sub>
Question the problem.<br>
Understand the system.<br>
Map every constraint.
</sub>
<br><br>
<img src="https://img.shields.io/badge/PHASE__01-0d1117?style=flat-square&labelColor=0d1117" alt="Phase 01"/>
<br><br>
</td>

<td align="center" width="33%">
<br>
<img src="https://img.shields.io/badge/_%E2%96%8C_02__%E2%96%90-B14CFF?style=for-the-badge&labelColor=0d1117" alt="02"/>
<br><br>
<h3>BUILD</h3>
<sub>
Turn ideas into<br>
working solutions.<br>
Ship real code.
</sub>
<br><br>
<img src="https://img.shields.io/badge/PHASE__02-0d1117?style=flat-square&labelColor=0d1117" alt="Phase 02"/>
<br><br>
</td>

<td align="center" width="33%">
<br>
<img src="https://img.shields.io/badge/_%E2%96%8C_03__%E2%96%90-00E5A0?style=for-the-badge&labelColor=0d1117" alt="03"/>
<br><br>
<h3>EVOLVE</h3>
<sub>
Learn from every<br>
iteration.<br>
Never stop improving.
</sub>
<br><br>
<img src="https://img.shields.io/badge/PHASE__03-0d1117?style=flat-square&labelColor=0d1117" alt="Phase 03"/>
<br><br>
</td>

</tr>
</table>

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:6A00FF,50:00E5A0,100:FFD166&height=2&section=header" width="100%"/>

<br><br>

<!-- ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀  WHAT I BRING  ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ -->

<img src="https://capsule-render.vercel.app/api?type=transparent&text=WHAT%20I%20BRING&fontColor=FF3CAC&fontSize=30&fontAlignY=65&height=52&animation=fadeIn" alt="Section: Traits"/>

<br>

<sub>Key attributes that drive my engineering approach and execution.</sub>

<br><br>

<table>
<tr>

<td align="center" width="25%">
<br>
<img src="https://img.shields.io/badge/CURIOUS-00D9FF?style=for-the-badge&labelColor=0d1117" alt="Curious"/>
<br><br>
Always exploring<br>
what lies beyond<br>
the obvious.
<br><br>
<img src="https://img.shields.io/badge/%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%91-92%25-00D9FF?style=flat-square&labelColor=0d1117" alt="92%"/>
<br><br>
</td>

<td align="center" width="25%">
<br>
<img src="https://img.shields.io/badge/ADAPTIVE-FF3CAC?style=for-the-badge&labelColor=0d1117" alt="Adaptive"/>
<br><br>
Learning quickly<br>
and embracing<br>
new challenges.
<br><br>
<img src="https://img.shields.io/badge/%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%91-95%25-FF3CAC?style=flat-square&labelColor=0d1117" alt="95%"/>
<br><br>
</td>

<td align="center" width="25%">
<br>
<img src="https://img.shields.io/badge/CREATIVE-00E5A0?style=for-the-badge&labelColor=0d1117" alt="Creative"/>
<br><br>
Finding different<br>
ways to approach<br>
a problem.
<br><br>
<img src="https://img.shields.io/badge/%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%91%E2%96%91-88%25-00E5A0?style=flat-square&labelColor=0d1117" alt="88%"/>
<br><br>
</td>

<td align="center" width="25%">
<br>
<img src="https://img.shields.io/badge/DRIVEN-FFD166?style=for-the-badge&labelColor=0d1117" alt="Driven"/>
<br><br>
Focused on turning<br>
ideas into<br>
results.
<br><br>
<img src="https://img.shields.io/badge/%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93%E2%96%93-96%25-FFD166?style=flat-square&labelColor=0d1117" alt="96%"/>
<br><br>
</td>

</tr>
</table>

<br>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FFD166,50:FF3CAC,100:8A2BE2&height=2&section=header" width="100%"/>

<br><br>

<!-- ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀  CONNECT  ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ -->

<img src="https://capsule-render.vercel.app/api?type=transparent&text=LET'S%20BUILD%20SOMETHING%20WORTHWHILE&fontColor=FFD166&fontSize=26&fontAlignY=65&height=52&animation=fadeIn" alt="Section: Connect"/>

<br><br>

I'm open to **internships, collaborations, ambitious projects, and opportunities**
<br>where I can contribute, learn from exceptional people, and grow through meaningful engineering work.

<br>

If you have an interesting problem, an idea worth exploring, or an opportunity
<br>where I could contribute, **I'd genuinely love to hear from you.**

<br><br>

<a href="mailto:sakthipranaash31@gmail.com">
<img src="https://img.shields.io/badge/LET'S%20CONNECT-sakthipranaash31%40gmail.com-6A00FF?style=for-the-badge&logo=gmail&logoColor=white&labelColor=111827" alt="Email"/>
</a>

<br><br><br>

<!-- Mantra Footer Badges -->
<img src="https://img.shields.io/badge/BUILD_WITH_PURPOSE-00E5A0?style=flat-square&labelColor=0d1117" alt="Build With Purpose"/>
&nbsp;&nbsp;
<img src="https://img.shields.io/badge/%E2%97%86-00D9FF?style=flat-square&labelColor=0d1117" alt="*"/>
&nbsp;&nbsp;
<img src="https://img.shields.io/badge/LEARN_WITH_CURIOSITY-B14CFF?style=flat-square&labelColor=0d1117" alt="Learn With Curiosity"/>
&nbsp;&nbsp;
<img src="https://img.shields.io/badge/%E2%97%86-00D9FF?style=flat-square&labelColor=0d1117" alt="*"/>
&nbsp;&nbsp;
<img src="https://img.shields.io/badge/CREATE_WITH_IMPACT-FF3CAC?style=flat-square&labelColor=0d1117" alt="Create With Impact"/>

<br><br>

<!-- ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀  FOOTER WAVE  ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀ -->

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FF3CAC,25:FFD166,50:00E5A0,75:00BFFF,100:6A00FF&height=150&section=footer" width="100%"/>

</div>
