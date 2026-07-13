<svg viewBox="0 0 1180 610" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice">
  <defs>
    <!-- Gradients -->
    <linearGradient id="bgGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0a0e27;stop-opacity:1" />
      <stop offset="50%" style="stop-color:#1a1f3a;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#0f1729;stop-opacity:1" />
    </linearGradient>

    <linearGradient id="asciiGradient" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#00ff88;stop-opacity:1">
        <animate attributeName="offset" values="0%;25%;50%;75%;100%;0%" dur="8s" repeatCount="indefinite" />
      </stop>
      <stop offset="33%" style="stop-color:#00ccff;stop-opacity:1">
        <animate attributeName="offset" values="33%;58%;83%;8%;33%;33%" dur="8s" repeatCount="indefinite" />
      </stop>
      <stop offset="66%" style="stop-color:#ff00ff;stop-opacity:1">
        <animate attributeName="offset" values="66%;91%;16%;41%;66%;66%" dur="8s" repeatCount="indefinite" />
      </stop>
      <stop offset="100%" style="stop-color:#00ff88;stop-opacity:1">
        <animate attributeName="offset" values="100%;125%;150%;175%;100%;100%" dur="8s" repeatCount="indefinite" />
      </stop>
    </linearGradient>

    <filter id="glowFilter">
      <feGaussianBlur stdDeviation="2" result="coloredBlur" />
      <feMerge>
        <feMergeNode in="coloredBlur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <filter id="strongGlow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur" />
      <feMerge>
        <feMergeNode in="coloredBlur" />
        <feMergeNode in="coloredBlur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <filter id="scanlines">
      <feTurbulence type="fractalNoise" baseFrequency="0.9" numOctaves="4" result="noise" seed="2" />
      <feDisplacementMap in="SourceGraphic" in2="noise" scale="1" />
    </filter>

    <!-- Animations -->
    <style>
      @keyframes float {
        0%, 100% { transform: translateY(0px); }
        50% { transform: translateY(-15px); }
      }

      @keyframes blink {
        0%, 49%, 100% { opacity: 1; }
        50%, 99% { opacity: 0; }
      }

      @keyframes pulse {
        0%, 100% { opacity: 0.8; }
        50% { opacity: 1; }
      }

      @keyframes glow-pulse {
        0%, 100% { filter: drop-shadow(0 0 8px rgba(0,255,136,0.5)); }
        50% { filter: drop-shadow(0 0 16px rgba(0,255,136,0.8)); }
      }

      @keyframes slideIn {
        from { opacity: 0; transform: translateX(-20px); }
        to { opacity: 1; transform: translateX(0); }
      }

      .ascii-text {
        animation: float 6s ease-in-out infinite;
      }

      .cursor {
        animation: blink 1s infinite;
      }

      .skill-pill {
        transition: all 0.3s ease;
      }

      .skill-pill:hover {
        r: 20px;
        filter: drop-shadow(0 0 12px rgba(0,255,136,0.8));
      }

      .social-icon {
        transition: all 0.3s ease;
      }

      .social-icon:hover {
        filter: drop-shadow(0 0 10px rgba(0,204,255,0.8));
        transform: scale(1.2);
      }

      .terminal-line {
        animation: slideIn 0.5s ease forwards;
      }

      .line-1 { animation-delay: 0s; }
      .line-2 { animation-delay: 0.3s; }
      .line-3 { animation-delay: 0.6s; }
      .line-4 { animation-delay: 0.9s; }
      .line-5 { animation-delay: 1.2s; }
      .line-6 { animation-delay: 1.5s; }
    </style>
  </defs>

  <!-- Background -->
  <rect width="1180" height="610" fill="url(#bgGradient)" />

  <!-- Animated grid background -->
  <defs>
    <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 0 0 40" fill="none" stroke="rgba(0,255,136,0.03)" stroke-width="1" />
    </pattern>
  </defs>
  <rect width="1180" height="610" fill="url(#grid)" />

  <!-- Glow orbs background -->
  <circle cx="150" cy="100" r="80" fill="rgba(0,255,136,0.05)" filter="url(#glowFilter)" />
  <circle cx="1050" cy="500" r="100" fill="rgba(0,204,255,0.05)" filter="url(#glowFilter)" />

  <!-- LEFT SIDE - ASCII Art with Gradient -->
  <g class="ascii-text">
    <!-- ASCII Portrait -->
    <text x="80" y="80" font-family="'Courier New', monospace" font-size="10" font-weight="bold" fill="url(#asciiGradient)" filter="url(#glowFilter)">
      ╔════════════════════╗
    </text>
    <text x="80" y="95" font-family="'Courier New', monospace" font-size="10" font-weight="bold" fill="url(#asciiGradient)" filter="url(#glowFilter)" opacity="0">
      ║  &gt;_ DEVELOPER _&lt;  ║
      <animate attributeName="opacity" values="0;1;1;1;1;1;1;0" dur="6s" repeatCount="indefinite" />
    </text>
    <text x="80" y="110" font-family="'Courier New', monospace" font-size="10" font-weight="bold" fill="url(#asciiGradient)" filter="url(#glowFilter)" opacity="0">
      ║  ▓░▓░▓░▓░▓░▓░▓░  ║
      <animate attributeName="opacity" values="0;0;1;1;1;1;0;0" dur="6s" repeatCount="indefinite" />
    </text>
    <text x="80" y="125" font-family="'Courier New', monospace" font-size="10" font-weight="bold" fill="url(#asciiGradient)" filter="url(#glowFilter)" opacity="0">
      ║   ◆  ◇  ◆  ◇   ║
      <animate attributeName="opacity" values="0;0;0;1;1;0;0;0" dur="6s" repeatCount="indefinite" />
    </text>
    <text x="80" y="140" font-family="'Courier New', monospace" font-size="10" font-weight="bold" fill="url(#asciiGradient)" filter="url(#glowFilter)" opacity="0">
      ║  BUILD_CREATE++  ║
      <animate attributeName="opacity" values="0;0;0;0;1;1;0;0" dur="6s" repeatCount="indefinite" />
    </text>
    <text x="80" y="155" font-family="'Courier New', monospace" font-size="10" font-weight="bold" fill="url(#asciiGradient)" filter="url(#glowFilter)" opacity="0">
      ║   @drag0nop_    ║
      <animate attributeName="opacity" values="0;0;0;0;0;1;1;0" dur="6s" repeatCount="indefinite" />
    </text>
    <text x="80" y="170" font-family="'Courier New', monospace" font-size="10" font-weight="bold" fill="url(#asciiGradient)" filter="url(#glowFilter)">
      ╚════════════════════╝
    </text>

    <!-- Decorative code blocks -->
    <text x="60" y="210" font-family="'Courier New', monospace" font-size="9" fill="rgba(0,255,136,0.6)" filter="url(#glowFilter)">
      &lt;code&gt;
    </text>
    <text x="60" y="230" font-family="'Courier New', monospace" font-size="9" fill="rgba(0,204,255,0.6)" filter="url(#glowFilter)">
      const passion = ∞
    </text>
    <text x="60" y="250" font-family="'Courier New', monospace" font-size="9" fill="rgba(255,0,255,0.6)" filter="url(#glowFilter)">
      const skills = [...]
    </text>
    <text x="60" y="270" font-family="'Courier New', monospace" font-size="9" fill="rgba(0,255,136,0.6)" filter="url(#glowFilter)">
      &lt;/code&gt;
    </text>
  </g>

  <!-- RIGHT SIDE - Terminal Window -->
  <g>
    <!-- Terminal background -->
    <rect x="450" y="50" width="700" height="520" rx="15" fill="rgba(10,14,39,0.8)" stroke="rgba(0,255,136,0.3)" stroke-width="2" />

    <!-- Terminal header -->
    <rect x="450" y="50" width="700" height="40" rx="15" fill="rgba(0,255,136,0.1)" stroke="rgba(0,255,136,0.3)" stroke-width="2" />
    <circle cx="475" cy="70" r="4" fill="#ff5f57" />
    <circle cx="495" cy="70" r="4" fill="#febc2e" />
    <circle cx="515" cy="70" r="4" fill="#28c940" />
    <text x="580" y="74" font-family="'Courier New', monospace" font-size="12" fill="rgba(0,255,136,0.7)">~/portfolio &gt;_</text>

    <!-- Greeting section -->
    <text x="480" y="110" font-family="'Segoe UI', Arial" font-size="18" font-weight="bold" fill="#00ff88" filter="url(#glowFilter)" class="terminal-line line-1">
      👋 Hi, I'm Drag0nop
    </text>

    <!-- Typing animation text -->
    <text x="480" y="145" font-family="'Courier New', monospace" font-size="14" fill="#00ccff" filter="url(#glowFilter)" class="terminal-line line-2">
      Full Stack Developer
    </text>

    <!-- Location and info -->
    <text x="480" y="175" font-family="'Courier New', monospace" font-size="12" fill="rgba(200,200,200,0.8)" class="terminal-line line-3">
      📍 Building digital experiences
    </text>

    <text x="480" y="200" font-family="'Courier New', monospace" font-size="12" fill="rgba(200,200,200,0.8)" class="terminal-line line-4">
      🎓 Computer Science Enthusiast
    </text>

    <text x="480" y="225" font-family="'Courier New', monospace" font-size="12" fill="rgba(200,200,200,0.8)" class="terminal-line line-5">
      💡 Open Source Contributor
    </text>

    <!-- Skills section -->
    <text x="480" y="265" font-family="'Segoe UI', Arial" font-size="13" font-weight="bold" fill="#00ff88" filter="url(#glowFilter)" class="terminal-line line-6">
      ⚡ Skills:
    </text>

    <!-- Skill Pills Row 1 -->
    <g class="skill-pill">
      <rect x="480" y="285" width="60" height="24" rx="12" fill="rgba(0,255,136,0.15)" stroke="rgba(0,255,136,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="510" y="302" font-family="'Segoe UI', Arial" font-size="11" font-weight="500" fill="#00ff88" text-anchor="middle">React</text>
    </g>

    <g class="skill-pill">
      <rect x="555" y="285" width="70" height="24" rx="12" fill="rgba(0,204,255,0.15)" stroke="rgba(0,204,255,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="590" y="302" font-family="'Segoe UI', Arial" font-size="11" font-weight="500" fill="#00ccff" text-anchor="middle">TypeScript</text>
    </g>

    <g class="skill-pill">
      <rect x="640" y="285" width="60" height="24" rx="12" fill="rgba(255,100,200,0.15)" stroke="rgba(255,100,200,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="670" y="302" font-family="'Segoe UI', Arial" font-size="11" font-weight="500" fill="#ff64c8" text-anchor="middle">Node.js</text>
    </g>

    <g class="skill-pill">
      <rect x="715" y="285" width="55" height="24" rx="12" fill="rgba(255,180,0,0.15)" stroke="rgba(255,180,0,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="742" y="302" font-family="'Segoe UI', Arial" font-size="11" font-weight="500" fill="#ffb400" text-anchor="middle">Python</text>
    </g>

    <!-- Skill Pills Row 2 -->
    <g class="skill-pill">
      <rect x="480" y="320" width="65" height="24" rx="12" fill="rgba(0,255,200,0.15)" stroke="rgba(0,255,200,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="512" y="337" font-family="'Segoe UI', Arial" font-size="11" font-weight="500" fill="#00ffc8" text-anchor="middle">Next.js</text>
    </g>

    <g class="skill-pill">
      <rect x="560" y="320" width="60" height="24" rx="12" fill="rgba(100,200,255,0.15)" stroke="rgba(100,200,255,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="590" y="337" font-family="'Segoe UI', Arial" font-size="11" font-weight="500" fill="#64c8ff" text-anchor="middle">Docker</text>
    </g>

    <g class="skill-pill">
      <rect x="635" y="320" width="60" height="24" rx="12" fill="rgba(150,100,255,0.15)" stroke="rgba(150,100,255,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="665" y="337" font-family="'Segoe UI', Arial" font-size="11" font-weight="500" fill="#9664ff" text-anchor="middle">AWS</text>
    </g>

    <g class="skill-pill">
      <rect x="710" y="320" width="60" height="24" rx="12" fill="rgba(0,255,136,0.15)" stroke="rgba(0,255,136,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="740" y="337" font-family="'Segoe UI', Arial" font-size="11" font-weight="500" fill="#00ff88" text-anchor="middle">Git</text>
    </g>

    <!-- Divider -->
    <line x1="480" y1="370" x2="1120" y2="370" stroke="rgba(0,255,136,0.2)" stroke-width="1" />

    <!-- Social and Contact section -->
    <text x="480" y="400" font-family="'Segoe UI', Arial" font-size="13" font-weight="bold" fill="#00ff88" filter="url(#glowFilter)">
      🔗 Connect:
    </text>

    <!-- Social Icons -->
    <!-- GitHub -->
    <g class="social-icon">
      <circle cx="510" cy="435" r="18" fill="rgba(0,255,136,0.15)" stroke="rgba(0,255,136,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="510" y="442" font-family="Arial" font-size="22" fill="#00ff88" text-anchor="middle">◊</text>
    </g>

    <!-- LinkedIn -->
    <g class="social-icon">
      <circle cx="570" cy="435" r="18" fill="rgba(0,204,255,0.15)" stroke="rgba(0,204,255,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="570" y="442" font-family="Arial" font-size="20" fill="#00ccff" text-anchor="middle">in</text>
    </g>

    <!-- Twitter -->
    <g class="social-icon">
      <circle cx="630" cy="435" r="18" fill="rgba(255,100,200,0.15)" stroke="rgba(255,100,200,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="630" y="442" font-family="Arial" font-size="20" fill="#ff64c8" text-anchor="middle">𝕏</text>
    </g>

    <!-- Portfolio -->
    <g class="social-icon">
      <circle cx="690" cy="435" r="18" fill="rgba(255,180,0,0.15)" stroke="rgba(255,180,0,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="690" y="442" font-family="Arial" font-size="20" fill="#ffb400" text-anchor="middle">⌘</text>
    </g>

    <!-- Email -->
    <g class="social-icon">
      <circle cx="750" cy="435" r="18" fill="rgba(150,100,255,0.15)" stroke="rgba(150,100,255,0.6)" stroke-width="1.5" filter="url(#glowFilter)" />
      <text x="750" y="442" font-family="Arial" font-size="20" fill="#9664ff" text-anchor="middle">✉</text>
    </g>

    <!-- Status line -->
    <text x="480" y="480" font-family="'Courier New', monospace" font-size="11" fill="rgba(0,255,136,0.8)" filter="url(#glowFilter)">
      $ Status: Open for collaboration
    </text>

    <text x="480" y="500" font-family="'Courier New', monospace" font-size="11" fill="rgba(0,255,136,0.6)">
      $ Last Update: 2026/07/13
    </text>

    <!-- Cursor -->
    <line x1="820" y1="500" x2="820" y2="512" stroke="#00ff88" stroke-width="2" class="cursor" filter="url(#glowFilter)" />
  </g>

  <!-- Top accent line -->
  <line x1="0" y1="0" x2="1180" y2="0" stroke="rgba(0,255,136,0.5)" stroke-width="2" />

  <!-- Bottom accent line -->
  <line x1="0" y1="610" x2="1180" y2="610" stroke="rgba(0,204,255,0.5)" stroke-width="2" />
</svg>
# 💫 About Me:
🔭 I’m currently working on projects and improving my problem-solving skills  <br>👯 I’m looking to collaborate on open-source and research-based projects  <br>🤝 I’m looking for help with model deployment and internships  <br>🌱 I’m currently learning Transformer Basics <br>💬 Ask me about Python, Machine Learning, and projects  <br>⚡ Fun fact: I enjoy turning raw data into useful (and sometimes fun) solutions


## 🌐 Socials:
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/_k_nagarkoti) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/krishna-singh-a84718316) [![X](https://img.shields.io/badge/X-black.svg?logo=X&logoColor=white)](https://x.com/_nagarkoti_k) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:nagarkotikrishna01@gmail.com) 

# 💻 Tech Stack:
![Python](https://img.shields.io/badge/python-3670A0?style=plastic&logo=python&logoColor=ffdd54) ![R](https://img.shields.io/badge/r-%23276DC3.svg?style=plastic&logo=r&logoColor=white) ![C](https://img.shields.io/badge/c-%2300599C.svg?style=plastic&logo=c&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=plastic&logo=c%2B%2B&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=plastic&logo=css3&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=plastic&logo=html5&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=plastic&logo=javascript&logoColor=%23F7DF1E) ![Render](https://img.shields.io/badge/Render-%46E3B7.svg?style=plastic&logo=render&logoColor=white) ![Netlify](https://img.shields.io/badge/netlify-%23000000.svg?style=plastic&logo=netlify&logoColor=#00C7B7) ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=plastic&logo=amazon-aws&logoColor=white) ![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=plastic&logo=vercel&logoColor=white) ![Chart.js](https://img.shields.io/badge/chart.js-F5788D.svg?style=plastic&logo=chart.js&logoColor=white) ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=plastic&logo=django&logoColor=white) ![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=plastic&logo=express&logoColor=%2361DAFB) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=plastic&logo=fastapi) ![Flask](https://img.shields.io/badge/flask-%23000.svg?style=plastic&logo=flask&logoColor=white) ![Jinja](https://img.shields.io/badge/jinja-white.svg?style=plastic&logo=jinja&logoColor=black) ![JWT](https://img.shields.io/badge/JWT-black?style=plastic&logo=JSON%20web%20tokens) ![jQuery](https://img.shields.io/badge/jquery-%230769AD.svg?style=plastic&logo=jquery&logoColor=white) ![NPM](https://img.shields.io/badge/NPM-%23CB3837.svg?style=plastic&logo=npm&logoColor=white) ![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=plastic&logo=opencv&logoColor=white) ![Next JS](https://img.shields.io/badge/Next-black?style=plastic&logo=next.js&logoColor=white) ![React](https://img.shields.io/badge/react-%2320232a.svg?style=plastic&logo=react&logoColor=%2361DAFB) ![WordPress](https://img.shields.io/badge/WordPress-%23117AC9.svg?style=plastic&logo=WordPress&logoColor=white) ![Snowflake](https://img.shields.io/badge/snowflake-%2329B5E8.svg?style=plastic&logo=snowflake&logoColor=white) ![Streamlit](https://img.shields.io/badge/Streamlit-%23FE4B4B.svg?style=plastic&logo=streamlit&logoColor=white) ![Three js](https://img.shields.io/badge/threejs-black?style=plastic&logo=three.js&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=plastic&logo=tailwind-css&logoColor=white) ![Gunicorn](https://img.shields.io/badge/gunicorn-%298729.svg?style=plastic&logo=gunicorn&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=plastic&logo=mysql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=plastic&logo=mongodb&logoColor=white) ![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=plastic&logo=sqlite&logoColor=white) ![Appwrite](https://img.shields.io/badge/Appwrite-%23FD366E.svg?style=plastic&logo=appwrite&logoColor=white) ![Blender](https://img.shields.io/badge/blender-%23F5792A.svg?style=plastic&logo=blender&logoColor=white) ![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=plastic&logo=Canva&logoColor=white) ![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=plastic&logo=figma&logoColor=white) ![Dribbble](https://img.shields.io/badge/Dribbble-EA4C89?style=plastic&logo=dribbble&logoColor=white) ![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=plastic&logo=Keras&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=plastic&logo=Matplotlib&logoColor=black) ![mlflow](https://img.shields.io/badge/mlflow-%23d9ead3.svg?style=plastic&logo=numpy&logoColor=blue) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=plastic&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=plastic&logo=pandas&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=plastic&logo=TensorFlow&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=plastic&logo=plotly&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=plastic&logo=PyTorch&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=plastic&logo=scikit-learn&logoColor=white) ![Scipy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=plastic&logo=scipy&logoColor=%white) ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=plastic&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=plastic&logo=github&logoColor=white) ![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=plastic&logo=gitlab&logoColor=white) ![Unity](https://img.shields.io/badge/unity-%23000000.svg?style=plastic&logo=unity&logoColor=white) ![Unreal Engine](https://img.shields.io/badge/unrealengine-%23313131.svg?style=plastic&logo=unrealengine&logoColor=white) ![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=plastic&logo=powerbi&logoColor=black) ![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=plastic&logo=notion&logoColor=white) ![Cisco](https://img.shields.io/badge/cisco-%23049fd9.svg?style=plastic&logo=cisco&logoColor=black)
# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=Drag0nop&theme=dark&hide_border=false&include_all_commits=true&count_private=false)<br/>
![](https://nirzak-streak-stats.vercel.app/?user=Drag0nop&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Drag0nop&theme=dark&hide_border=false&include_all_commits=true&count_private=false&layout=compact)

## 🏆 GitHub Trophies
![](https://github-profile-trophy.vercel.app/?username=Drag0nop&theme=radical&no-frame=false&no-bg=true&margin-w=4)

### ✍️ Random Dev Quote
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=dark)

### 🔝 Top Contributed Repo
![](https://github-contributor-stats.vercel.app/api?username=Drag0nop&limit=5&theme=radical&combine_all_yearly_contributions=true)

---
[![](https://visitcount.itsvg.in/api?id=Drag0nop&icon=0&color=0)](https://visitcount.itsvg.in)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
