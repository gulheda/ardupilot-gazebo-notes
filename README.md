<!-- =========================
     DARK • PREMIUM • NO GIF
     ========================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=venom&height=220&color=0:000000,100:0b0f19&text=OTONOM%20VTOL%20IHA%20SISTEMI&fontColor=00F5D4&fontSize=44&animation=twinkling&stroke=00F5D4&strokeWidth=1" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=16&pause=900&color=00F5D4&center=true&vCenter=true&width=900&lines=ArduPilot+SITL+%E2%86%92+MAVProxy+%E2%86%92+Gazebo+11;Mission-Oriented+Autonomy+Infrastructure;Stability+%7C+Parameter+Tuning+%7C+AI-Ready+Design" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ARdupilot-SITL-0b0f19?style=for-the-badge&logo=apache&logoColor=00F5D4&labelColor=000000">
  <img src="https://img.shields.io/badge/Gazebo-11-0b0f19?style=for-the-badge&logo=linux&logoColor=00F5D4&labelColor=000000">
  <img src="https://img.shields.io/badge/MAVProxy-Control-0b0f19?style=for-the-badge&labelColor=000000&logoColor=00F5D4">
  <img src="https://img.shields.io/badge/Ubuntu-20.04-0b0f19?style=for-the-badge&logo=ubuntu&logoColor=00F5D4&labelColor=000000">
</p>

---

<!-- HUD PANEL (PURE SVG, INLINE) -->
<p align="center">
<svg width="980" height="220" viewBox="0 0 980 220" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Mission HUD">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#05070d"/>
      <stop offset="1" stop-color="#0b0f19"/>
    </linearGradient>
    <linearGradient id="neon" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0" stop-color="#00F5D4"/>
      <stop offset="1" stop-color="#7C3AED"/>
    </linearGradient>
    <filter id="softGlow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="3" result="b"/>
      <feMerge>
        <feMergeNode in="b"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <!-- frame -->
  <rect x="10" y="10" rx="18" ry="18" width="960" height="200" fill="url(#bg)" stroke="#151b2c" stroke-width="2"/>
  <path d="M40 54 H940" stroke="#141a2e" stroke-width="2"/>

  <!-- top left dots -->
  <circle cx="40" cy="35" r="6" fill="#ff5f56"/>
  <circle cx="62" cy="35" r="6" fill="#ffbd2e"/>
  <circle cx="84" cy="35" r="6" fill="#27c93f"/>

  <!-- title -->
  <text x="120" y="41" fill="#8b93a7" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">
    /system/uav/vtol/autonomy
  </text>
  <text x="40" y="82" fill="#E9EDFF" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="16" font-weight="700">
    MISSION HUD
  </text>

  <!-- neon line -->
  <path d="M40 96 H940" stroke="url(#neon)" stroke-width="3" opacity="0.9"/>

  <!-- VTOL silhouette -->
  <g filter="url(#softGlow)" opacity="0.95">
    <path d="M650 110 L740 110 L765 92 L855 92 L880 110 L940 110" stroke="url(#neon)" stroke-width="5" fill="none" stroke-linecap="round"/>
    <path d="M810 92 L810 62" stroke="url(#neon)" stroke-width="5" stroke-linecap="round"/>
    <path d="M790 62 L830 62" stroke="url(#neon)" stroke-width="5" stroke-linecap="round"/>
    <path d="M760 110 L730 140" stroke="url(#neon)" stroke-width="5" stroke-linecap="round"/>
    <path d="M865 110 L895 140" stroke="url(#neon)" stroke-width="5" stroke-linecap="round"/>
    <circle cx="730" cy="142" r="8" fill="#00F5D4"/>
    <circle cx="895" cy="142" r="8" fill="#7C3AED"/>
  </g>

  <!-- left status -->
  <text x="40" y="120" fill="#00F5D4" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">SIMULATION:</text>
  <text x="170" y="120" fill="#D7DCEF" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">ONLINE</text>

  <text x="40" y="142" fill="#00F5D4" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">CONTROL:</text>
  <text x="170" y="142" fill="#D7DCEF" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">GUIDED / ARM / TAKEOFF</text>

  <text x="40" y="164" fill="#7C3AED" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">AUTONOMY:</text>
  <text x="170" y="164" fill="#D7DCEF" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">IN PROGRESS</text>

  <text x="40" y="186" fill="#7C3AED" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">AI LAYER:</text>
  <text x="170" y="186" fill="#D7DCEF" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace" font-size="12">PLANNED</text>
</svg>
</p>

---

## 🎯 KISA TANIM

Bu repo, **otonom VTOL İHA simülasyon altyapısını** kurar ve geliştirir.  
Hedef: uçuşu göstermekten öte **görev mantığı + stabilite + parametre optimizasyonu + AI entegrasyon zemini** oluşturmaktır.

---

## 🛰 GÖREV

- Otonom kalkış / iniş  
- Waypoint görev uçuşu  
- Stabil uçuş kontrolü  
- Motor–SERVO parametre optimizasyonu  
- İleri faz: görüntü işleme + karar + koordinasyon altyapısı  

---

## 🛠 BENİM ODAĞIM

- ArduPilot SITL yapılandırma & mod yönetimi  
- Gazebo world/model/plugin uyumluluğu  
- SERVO / motor mapping ve tuning  
- MAVProxy komut akışı ve kontrol mantığı  
- Otonom görev test senaryoları (kararlılık odaklı)

---

## 🧩 MİMARİ

```text
ArduPilot (SITL)  →  MAVProxy (Control)  →  Gazebo 11 (World)
     │                 │                      │
     ├─ params/tuning   ├─ commands/telemetry  ├─ physics/models/plugins
     └─ flight modes    └─ mission control     └─ visualization
