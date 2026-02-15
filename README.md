<!-- ===========================
      DARK / PREMIUM README
     =========================== -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=venom&height=240&color=0:000000,100:0b0f19&text=OTONOM%20VTOL%20IHA%20SISTEMI&fontColor=00F5D4&fontSize=46&animation=twinkling&stroke=00F5D4&strokeWidth=1" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=18&pause=800&color=00F5D4&center=true&vCenter=true&width=900&lines=Mission-Oriented+Autonomous+UAV+Simulation+Stack;ArduPilot+SITL+%E2%86%92+MAVProxy+%E2%86%92+Gazebo+11;Stability+%7C+Parameter+Tuning+%7C+Autonomy+Infrastructure;AI-Ready+Architecture+for+Vision+and+Coordination" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ARdupilot-SITL-0b0f19?style=for-the-badge&logo=apache&logoColor=00F5D4&labelColor=000000">
  <img src="https://img.shields.io/badge/Gazebo-11-0b0f19?style=for-the-badge&logo=linux&logoColor=00F5D4&labelColor=000000">
  <img src="https://img.shields.io/badge/MAVProxy-Control-0b0f19?style=for-the-badge&logoColor=00F5D4&labelColor=000000">
  <img src="https://img.shields.io/badge/Ubuntu-20.04-0b0f19?style=for-the-badge&logo=ubuntu&logoColor=00F5D4&labelColor=000000">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/74038190/212750093-1eac6f2f-6b21-4c24-a7c0-1b546f79a5d8.gif" width="900"/>
</p>

---

### 🧠 SYSTEM BRIEF (KISA AMA NET)

> Bu depo, **otonom VTOL İHA simülasyon mimarisini** görev odaklı şekilde kurar ve geliştirir.  
> Amaç “uçurmak” değil; **otonomi + görev altyapısı + AI entegrasyon zemini** oluşturmaktır.

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&height=4&color=0:00F5D4,100:7C3AED&section=header" width="900"/>
</p>

## 🎯 MISSION PROFILE

- **Otonom kalkış / iniş**
- **Waypoint / görev navigasyonu**
- **Stabilite ve kontrol**
- **Motor–SERVO parametre optimizasyonu**
- **İleri faz: Vision + karar + koordinasyon altyapısı**

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&height=4&color=0:7C3AED,100:00F5D4&section=header" width="900"/>
</p>

## 🛠 DEVELOPMENT FOCUS (BEN NE YAPIYORUM)

**Simülasyonun uçması → tek hedef değil.**  
Benim odağım:

- Uçuş kontrol yapılandırması (SITL / params)
- Gazebo model–plugin / world uyumu
- Motor davranışı (SERVOx, spin parametreleri, mapping)
- MAVProxy komut akışı ve kontrol paneli mantığı
- Otonom görev altyapısı (test senaryoları & kararlılık)

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&height=4&color=0:00F5D4,100:0b0f19&section=header" width="900"/>
</p>

## 🧩 ARCHITECTURE

```text
[ArduPilot SITL]  →  [MAVProxy Control]  →  [Gazebo 11 World]
        │                    │                 │
        ├── params/tuning    ├── commands      ├── physics + visuals
        └── flight modes     └── telemetry     └── models/plugins

<p align="center"> <img src="https://capsule-render.vercel.app/api?type=rect&height=4&color=0:0b0f19,100:7C3AED&section=header" width="900"/> </p>

🛰️ MISSION STATUS (HUD)

+ SIMULATION:   ONLINE
+ SPAWN:        OK
+ GUIDED/ARM:   STABLE
+ TAKEOFF:      OK
! AUTONOMY:     IN PROGRESS
! AI VISION:    PLANNED
