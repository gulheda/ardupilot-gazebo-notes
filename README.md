<div align="center">

<!-- TOP BAR -->
<div style="max-width:980px;width:100%;background:#0b0f19;border:1px solid #151b2c;border-radius:18px;padding:22px 22px 16px;box-shadow:0 20px 60px rgba(0,0,0,.55);">
  <div style="display:flex;align-items:center;justify-content:space-between;gap:14px;flex-wrap:wrap;">
    <div style="display:flex;align-items:center;gap:10px;">
      <span style="display:inline-block;width:10px;height:10px;border-radius:999px;background:#ff5f56;"></span>
      <span style="display:inline-block;width:10px;height:10px;border-radius:999px;background:#ffbd2e;"></span>
      <span style="display:inline-block;width:10px;height:10px;border-radius:999px;background:#27c93f;"></span>
      <span style="color:#8b93a7;font-family:ui-monospace,SFMono-Regular,Menlo,Monaco,Consolas,monospace;font-size:12px;margin-left:10px;">
        /system/uav/vtol/autonomy
      </span>
    </div>
    <div style="display:flex;gap:8px;flex-wrap:wrap;justify-content:center;">
      <span style="padding:6px 10px;border:1px solid #1c2440;border-radius:999px;background:#0f1526;color:#d7dcef;font-size:12px;">ArduPilot SITL</span>
      <span style="padding:6px 10px;border:1px solid #1c2440;border-radius:999px;background:#0f1526;color:#d7dcef;font-size:12px;">Gazebo 11</span>
      <span style="padding:6px 10px;border:1px solid #1c2440;border-radius:999px;background:#0f1526;color:#d7dcef;font-size:12px;">MAVProxy</span>
      <span style="padding:6px 10px;border:1px solid #1c2440;border-radius:999px;background:#0f1526;color:#d7dcef;font-size:12px;">Ubuntu 20.04</span>
    </div>
  </div>

  <!-- HERO -->
  <div style="margin-top:18px;padding:18px;border-radius:14px;border:1px solid #141a2e;background:radial-gradient(1200px 220px at 50% 0%, rgba(0,245,212,.12), transparent 70%), linear-gradient(180deg, rgba(124,58,237,.10), transparent 60%), #0b0f19;">
    <div style="display:flex;align-items:flex-start;justify-content:space-between;gap:18px;flex-wrap:wrap;">
      <div style="text-align:left;flex:1;min-width:260px;">
        <div style="font-family:ui-monospace,SFMono-Regular,Menlo,Monaco,Consolas,monospace;color:#7c86a5;font-size:12px;margin-bottom:8px;">
          MISSION-ORIENTED SIMULATION STACK
        </div>
        <div style="font-weight:800;letter-spacing:.2px;color:#e9edff;font-size:28px;line-height:1.15;">
          Otonom VTOL İHA Simülasyon Sistemi
        </div>
        <div style="margin-top:10px;color:#b7bfd8;font-size:14px;line-height:1.55;">
          Bu repo, “drone uçurma” değil; <b>otonomi altyapısı</b> kurma işidir.
          ArduPilot tabanlı uçuş kontrolü + Gazebo fizik simülasyonu + MAVProxy komut mimarisi ile
          görev senaryolarına hazır bir sistem tasarlanır.
        </div>

        <div style="margin-top:14px;display:flex;gap:10px;flex-wrap:wrap;">
          <span style="padding:8px 12px;border-radius:12px;background:#0f1526;border:1px solid #1c2440;color:#00f5d4;font-weight:700;font-size:12px;">
            AUTONOMY READY
          </span>
          <span style="padding:8px 12px;border-radius:12px;background:#0f1526;border:1px solid #1c2440;color:#7c3aed;font-weight:700;font-size:12px;">
            AI INTEGRATION PATH
          </span>
          <span style="padding:8px 12px;border-radius:12px;background:#0f1526;border:1px solid #1c2440;color:#e9edff;font-weight:700;font-size:12px;">
            STABILITY & TUNING
          </span>
        </div>
      </div>

      <!-- SVG "VTOL" DARK ICON -->
      <div style="flex:0 0 260px;min-width:260px;">
        <div style="border-radius:14px;border:1px solid #141a2e;background:#0f1526;padding:14px;position:relative;overflow:hidden;">
          <div style="position:absolute;inset:-60px -60px auto auto;width:140px;height:140px;background:radial-gradient(circle, rgba(0,245,212,.18), transparent 65%);filter:blur(2px);"></div>
          <div style="position:absolute;inset:auto auto -60px -60px;width:180px;height:180px;background:radial-gradient(circle, rgba(124,58,237,.18), transparent 65%);filter:blur(2px);"></div>

          <svg viewBox="0 0 420 220" width="100%" height="140" xmlns="http://www.w3.org/2000/svg">
            <defs>
              <linearGradient id="g1" x1="0" y1="0" x2="1" y2="1">
                <stop offset="0" stop-color="#00f5d4"/>
                <stop offset="1" stop-color="#7c3aed"/>
              </linearGradient>
              <filter id="glow">
                <feGaussianBlur stdDeviation="3" result="blur"/>
                <feMerge>
                  <feMergeNode in="blur"/>
                  <feMergeNode in="SourceGraphic"/>
                </feMerge>
              </filter>
            </defs>

            <!-- horizon grid -->
            <g opacity="0.35">
              <path d="M0 150 H420" stroke="#1c2440" stroke-width="2"/>
              <path d="M0 170 H420" stroke="#121a33" stroke-width="2"/>
              <path d="M0 190 H420" stroke="#121a33" stroke-width="2"/>
              <path d="M60 120 V220" stroke="#121a33" stroke-width="2"/>
              <path d="M140 110 V220" stroke="#121a33" stroke-width="2"/>
              <path d="M220 105 V220" stroke="#121a33" stroke-width="2"/>
              <path d="M300 110 V220" stroke="#121a33" stroke-width="2"/>
              <path d="M380 120 V220" stroke="#121a33" stroke-width="2"/>
            </g>

            <!-- VTOL silhouette -->
            <g filter="url(#glow)">
              <path d="M60 95 L140 95 L165 75 L255 75 L280 95 L360 95" stroke="url(#g1)" stroke-width="6" fill="none" stroke-linecap="round"/>
              <path d="M205 75 L205 45" stroke="url(#g1)" stroke-width="6" stroke-linecap="round"/>
              <path d="M185 45 L225 45" stroke="url(#g1)" stroke-width="6" stroke-linecap="round"/>
              <path d="M170 95 L130 130" stroke="url(#g1)" stroke-width="6" stroke-linecap="round"/>
              <path d="M250 95 L290 130" stroke="url(#g1)" stroke-width="6" stroke-linecap="round"/>
              <circle cx="130" cy="132" r="10" fill="#00f5d4"/>
              <circle cx="290" cy="132" r="10" fill="#7c3aed"/>
              <path d="M165 75 L165 105" stroke="#e9edff" stroke-width="3" opacity="0.9"/>
              <path d="M255 75 L255 105" stroke="#e9edff" stroke-width="3" opacity="0.9"/>
            </g>

            <!-- HUD text -->
            <text x="18" y="28" fill="#8b93a7" font-family="ui-monospace, monospace" font-size="12">VTOL / AUTONOMY STACK</text>
            <text x="18" y="48" fill="#00f5d4" font-family="ui-monospace, monospace" font-size="12">STATUS: ONLINE</text>
          </svg>

          <div style="display:flex;gap:10px;flex-wrap:wrap;margin-top:8px;">
            <span style="padding:6px 10px;border-radius:999px;background:#0b0f19;border:1px solid #1c2440;color:#b7bfd8;font-size:12px;">
              stability-first
            </span>
            <span style="padding:6px 10px;border-radius:999px;background:#0b0f19;border:1px solid #1c2440;color:#b7bfd8;font-size:12px;">
              mission-driven
            </span>
            <span style="padding:6px 10px;border-radius:999px;background:#0b0f19;border:1px solid #1c2440;color:#b7bfd8;font-size:12px;">
              ai-ready
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- PANELS -->
  <div style="margin-top:16px;display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:12px;text-align:left;">
    <div style="border-radius:14px;border:1px solid #141a2e;background:#0f1526;padding:14px;">
      <div style="color:#00f5d4;font-weight:800;font-size:12px;letter-spacing:.4px;">MISSION</div>
      <div style="margin-top:8px;color:#d7dcef;font-size:14px;line-height:1.6;">
        • Otonom kalkış / iniş<br/>
        • Waypoint görev uçuşu<br/>
        • Stabilite + kontrol sürekliliği<br/>
        • Gerçekçi motor/servo davranışı
      </div>
    </div>

    <div style="border-radius:14px;border:1px solid #141a2e;background:#0f1526;padding:14px;">
      <div style="color:#7c3aed;font-weight:800;font-size:12px;letter-spacing:.4px;">WHAT I DO</div>
      <div style="margin-top:8px;color:#d7dcef;font-size:14px;line-height:1.6;">
        • SITL parametre & mod yönetimi<br/>
        • Gazebo world/model/plugin uyumu<br/>
        • SERVO & motor mapping optimizasyonu<br/>
        • MAVProxy komut mimarisi
      </div>
    </div>

    <div style="border-radius:14px;border:1px solid #141a2e;background:#0f1526;padding:14px;">
      <div style="color:#e9edff;font-weight:800;font-size:12px;letter-spacing:.4px;">SYSTEM HUD</div>
      <div style="margin-top:10px;font-family:ui-monospace,SFMono-Regular,Menlo,Monaco,Consolas,monospace;font-size:12px;line-height:1.7;">
        <span style="color:#00f5d4;">SIMULATION</span>: <span style="color:#d7dcef;">ONLINE</span><br/>
        <span style="color:#00f5d4;">SPAWN</span>: <span style="color:#d7dcef;">OK</span><br/>
        <span style="color:#00f5d4;">GUIDED/ARM</span>: <span style="color:#d7dcef;">STABLE</span><br/>
        <span style="color:#00f5d4;">TAKEOFF</span>: <span style="color:#d7dcef;">OK</span><br/>
        <span style="color:#7c3aed;">AUTONOMY</span>: <span style="color:#d7dcef;">IN PROGRESS</span><br/>
        <span style="color:#7c3aed;">AI VISION</span>: <span style="color:#d7dcef;">PLANNED</span>
      </div>
    </div>
  </div>

  <!-- ARCH -->
  <div style="margin-top:12px;border-radius:14px;border:1px solid #141a2e;background:#0f1526;padding:14px;text-align:left;">
    <div style="display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap;">
      <div style="color:#8b93a7;font-family:ui-monospace,monospace;font-size:12px;">
        ARCHITECTURE
      </div>
      <div style="display:flex;gap:8px;flex-wrap:wrap;">
        <span style="padding:6px 10px;border-radius:999px;background:#0b0f19;border:1px solid #1c2440;color:#00f5d4;font-size:12px;">SITL</span>
        <span style="padding:6px 10px;border-radius:999px;background:#0b0f19;border:1px solid #1c2440;color:#00f5d4;font-size:12px;">CMD</span>
        <span style="padding:6px 10px;border-radius:999px;background:#0b0f19;border:1px solid #1c2440;color:#00f5d4;font-size:12px;">PHYSICS</span>
      </div>
    </div>

```text
ArduPilot (SITL)  →  MAVProxy (Control)  →  Gazebo 11 (World)
     │                 │                      │
     ├─ params/tuning   ├─ commands/telemetry  ├─ physics/models/plugins
     └─ flight modes    └─ mission control     └─ visualization
</div> <!-- FOOT --> <div style="margin-top:14px;color:#8b93a7;font-size:12px;text-align:center;"> dark UI • mission driven • autonomy first </div> </div> </div> ```
