<div align="center">

<!-- ============================================================ -->
<!--             MAXIMUM ANIMATION HACKER SVG BANNER               -->
<!-- ============================================================ -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 260" width="100%" height="260">
  <defs>
    <!-- Green Glow Filter -->
    <filter id="greenGlow">
      <feGaussianBlur stdDeviation="4" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>
    <filter id="redGlow">
      <feGaussianBlur stdDeviation="3" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>
    <!-- For glitch clipping -->
    <clipPath id="glitchClip1">
      <rect x="0" y="60" width="1000" height="30" />
    </clipPath>
    <clipPath id="glitchClip2">
      <rect x="0" y="110" width="1000" height="25" />
    </clipPath>
  </defs>

  <!-- BACKGROUND -->
  <rect width="1000" height="260" fill="#0A0A0A" />

  <!-- CRT FLICKER (Subtle opacity oscillation) -->
  <rect width="1000" height="260" fill="#00FF41" opacity="0.02">
    <animate attributeName="opacity" values="0.02;0.06;0.01;0.04;0.02" dur="0.8s" repeatCount="indefinite" />
  </rect>

  <!-- HORIZONTAL SCANLINE 1 (Moving down) -->
  <rect x="0" y="0" width="1000" height="2" fill="#00FF41" opacity="0.6">
    <animate attributeName="y" from="0" to="260" dur="3s" repeatCount="indefinite" />
    <animate attributeName="opacity" values="0.8;0.1;0.8" dur="3s" repeatCount="indefinite" />
  </rect>

  <!-- HORIZONTAL SCANLINE 2 (Faster, smaller) -->
  <rect x="0" y="0" width="1000" height="1" fill="#00FF41" opacity="0.4">
    <animate attributeName="y" from="-20" to="280" dur="1.5s" repeatCount="indefinite" />
  </rect>

  <!-- MATRIX DIGITAL RAIN (Column 1) -->
  <g font-family="'Courier New', monospace" font-size="18" fill="#00FF41" font-weight="bold" opacity="0.7">
    <text x="120" y="0">0</text><text x="135" y="0">1</text><text x="150" y="0">0</text>
    <animateTransform attributeName="transform" type="translate" from="0 -200" to="0 280" dur="2.8s" repeatCount="indefinite" />
  </g>
  <!-- MATRIX DIGITAL RAIN (Column 2) -->
  <g font-family="'Courier New', monospace" font-size="18" fill="#00FF41" opacity="0.5">
    <text x="380" y="0">1</text><text x="395" y="0">0</text><text x="410" y="0">1</text>
    <animateTransform attributeName="transform" type="translate" from="0 -180" to="0 280" dur="3.5s" repeatCount="indefinite" />
  </g>
  <!-- MATRIX DIGITAL RAIN (Column 3) -->
  <g font-family="'Courier New', monospace" font-size="18" fill="#00FF41" opacity="0.6">
    <text x="650" y="0">1</text><text x="665" y="0">0</text><text x="680" y="0">1</text>
    <animateTransform attributeName="transform" type="translate" from="0 -220" to="0 280" dur="2.5s" repeatCount="indefinite" />
  </g>
  <!-- MATRIX DIGITAL RAIN (Column 4) -->
  <g font-family="'Courier New', monospace" font-size="18" fill="#00FF41" opacity="0.4">
    <text x="880" y="0">0</text><text x="895" y="0">0</text><text x="910" y="0">1</text>
    <animateTransform attributeName="transform" type="translate" from="0 -150" to="0 280" dur="4s" repeatCount="indefinite" />
  </g>

  <!-- PULSING RADAR RINGS (Center-left) -->
  <g transform="translate(80, 130)">
    <circle cx="0" cy="0" r="10" fill="none" stroke="#00FF41" stroke-width="2" opacity="0">
      <animate attributeName="r" from="10" to="60" dur="2.5s" repeatCount="indefinite" />
      <animate attributeName="opacity" from="0.8" to="0" dur="2.5s" repeatCount="indefinite" />
    </circle>
    <circle cx="0" cy="0" r="10" fill="none" stroke="#00FF41" stroke-width="2" opacity="0">
      <animate attributeName="r" from="10" to="60" dur="2.5s" begin="1.25s" repeatCount="indefinite" />
      <animate attributeName="opacity" from="0.8" to="0" dur="2.5s" begin="1.25s" repeatCount="indefinite" />
    </circle>
    <circle cx="0" cy="0" r="4" fill="#00FF41" filter="url(#greenGlow)" />
  </g>

  <!-- GLITCH TEXT: "S. JAY SURYA" -->
  <!-- Base White Text -->
  <text x="500" y="105" font-family="'Courier New', monospace" font-size="52" font-weight="900" fill="#FFFFFF" text-anchor="middle" letter-spacing="5">S. JAY SURYA</text>
  
  <!-- Cyan Glitch (Offset Left) -->
  <text x="500" y="105" font-family="'Courier New', monospace" font-size="52" font-weight="900" fill="#00FFFF" text-anchor="middle" letter-spacing="5" clip-path="url(#glitchClip1)" opacity="0">
    S. JAY SURYA
    <animate attributeName="x" values="500;495;505;500" dur="0.15s" repeatCount="indefinite" />
    <animate attributeName="opacity" values="0;1;1;0;0;0" dur="2s" repeatCount="indefinite" />
  </text>
  
  <!-- Red Glitch (Offset Right) -->
  <text x="500" y="105" font-family="'Courier New', monospace" font-size="52" font-weight="900" fill="#FF0000" text-anchor="middle" letter-spacing="5" clip-path="url(#glitchClip2)" opacity="0">
    S. JAY SURYA
    <animate attributeName="x" values="500;508;492;500" dur="0.18s" repeatCount="indefinite" />
    <animate attributeName="opacity" values="0;0;0;1;1;0" dur="2.3s" repeatCount="indefinite" />
  </text>

  <!-- GLITCH HORIZONTAL BAR (Screen Tear Effect) -->
  <rect x="0" y="80" width="1000" height="4" fill="#00FF41" opacity="0" filter="url(#greenGlow)">
    <animate attributeName="opacity" values="0;0.9;0;0;0.9;0" dur="0.3s" repeatCount="indefinite" />
    <animate attributeName="y" values="80;120;80;150;80" dur="0.5s" repeatCount="indefinite" />
  </rect>

  <!-- Subtitle: Full-Stack · AI · Secure -->
  <text x="500" y="155" font-family="'Courier New', monospace" font-size="24" font-weight="600" fill="#00FF41" text-anchor="middle" filter="url(#greenGlow)" opacity="0.9">
    &lt; FULL-STACK · AI · SECURE_SYSTEMS &gt;
    <animate attributeName="opacity" values="0.9;0.5;0.9" dur="1.2s" repeatCount="indefinite" />
  </text>

  <!-- BLINKING TERMINAL CURSOR -->
  <text x="320" y="195" font-family="'Courier New', monospace" font-size="20" fill="#00FF41">root@surya:~$</text>
  <text x="495" y="195" font-family="'Courier New', monospace" font-size="20" fill="#FFFFFF">Building the future...</text>
  <rect x="685" y="180" width="12" height="18" fill="#00FF41" filter="url(#greenGlow)">
    <animate attributeName="opacity" values="1;0;1" dur="0.8s" repeatCount="indefinite" />
  </rect>

  <!-- PULSING BRACKETS (Bottom Left) -->
  <text x="30" y="235" font-family="'Courier New', monospace" font-size="24" fill="#00FF41" opacity="0.4">[</text>
  <text x="45" y="235" font-family="'Courier New', monospace" font-size="24" fill="#00FF41" opacity="0.4">
    <animate attributeName="opacity" values="0.4;0.8;0.4" dur="1.5s" repeatCount="indefinite" />
    SYSTEM_STATUS: ONLINE
  </text>
  <text x="280" y="235" font-family="'Courier New', monospace" font-size="24" fill="#00FF41" opacity="0.4">]</text>

  <!-- PULSING BRACKETS (Bottom Right) -->
  <text x="700" y="235" font-family="'Courier New', monospace" font-size="24" fill="#00FF41" opacity="0.4">{</text>
  <text x="715" y="235" font-family="'Courier New', monospace" font-size="24" fill="#00FF41" opacity="0.4">
    <animate attributeName="opacity" values="0.4;0.8;0.4" dur="1.8s" repeatCount="indefinite" />
    CONNECTION: SECURE
  </text>
  <text x="940" y="235" font-family="'Courier New', monospace" font-size="24" fill="#00FF41" opacity="0.4">}</text>

  <!-- DASHED BORDER (Animated perimeter) -->
  <rect x="6" y="6" width="988" height="248" rx="8" fill="none" stroke="#00FF41" stroke-width="2" stroke-dasharray="20 15" opacity="0.4">
    <animate attributeName="stroke-dashoffset" from="2000" to="0" dur="8s" repeatCount="indefinite" />
  </rect>
</svg>

<br>

<!-- Typing Animation (Matrix style) -->
<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&duration=2000&pause=800&color=00FF41&center=true&vCenter=true&width=900&height=50&lines=INITIALIZING+PROFILE...;LOADING+SKILLSET...;ACCESS+GRANTED.;WELCOME+TO+THE+MATRIX." alt="Typing SVG" />

<br>

<img src="https://komarev.com/ghpvc/?username=surya-hash-coder&label=TERMINAL+VIEWS&color=00FF41&style=for-the-badge" alt="Profile Views" />

</div>

---

## 🖥️ `> whoami`

<table align="center" style="border: 1px solid #00FF41; background: #0D0D0D;">
<tr>
<td width="50%" style="padding: 15px; color: #00FF41; font-family: 'Courier New', monospace;">

```bash
root@surya:~$ whoami
➜ S. JAY SURYA
➜ B.Sc IT Graduate
➜ Ex-Intern @ Jestech
➜ Location: Madurai, IN
