# 🛰 VTOL İHA HİBRİT UÇUŞ SİSTEMİ LABORATUVARI
### ArduPilot + Gazebo Tabanlı Uçuş Kontrol, Görev Yönetimi ve Fizik Modelleme Ortamı

<p align="center">

![ArduPilot](https://img.shields.io/badge/ArduPilot-SITL-blue)
![Gazebo](https://img.shields.io/badge/Gazebo-Classic-orange)
![UAV](https://img.shields.io/badge/System-VTOL-red)
![Status](https://img.shields.io/badge/Simulation-Active-success)
![Research](https://img.shields.io/badge/Focus-FlightControl-purple)

</p>

---

## 🚀 PROJE TANIMI

Bu repository, hibrit VTOL (Vertical Take-Off and Landing) bir İHA'nın:

- Dikey uçuş kontrolünü  
- Sabit kanat aerodinamik davranışını  
- Transition (geçiş) dinamiklerini  
- Otonom görev sistemini  
- Failsafe zincirini  
- Parametre tabanlı kontrol karakteristiğini  

simülasyon ortamında mühendislik seviyesinde analiz etmek için oluşturulmuştur.

Bu bir "uçuş denemesi" değil,  
**hibrit uçuş mimarisinin çözümlemesidir.**

---

# 🧠 SİSTEM MİMARİSİ

                 ┌───────────────────────┐
                 │   Flight Controller   │
                 │   (ArduPilot SITL)    │
                 └───────────┬───────────┘
                             │
     ┌───────────────────────┼────────────────────────┐
     │                       │                        │
     Sensör Füzyonu Uçuş Kontrolü Görev Yönetimi
(EKF) (PID + Stabilizasyon) (Mission Logic)
│ │ │
└───────────────┬───────┴───────────────┬────────┘
│ │
🔵 Multicopter Katmanı 🔴 Sabit Kanat Katmanı
(Q Modları) (Plane Modları)


Mod değişimi yalnızca yazılım katmanı değil,  
**fizik modeli değişimidir.**

---

# 🔄 HİBRİT UÇUŞ DİNAMİĞİ

## 🔵 Multicopter Fazı

- Lift = Rotor itki
- Throttle = Yükseklik
- Hover mümkün
- Enerji tüketimi yüksek

## 🔴 Sabit Kanat Fazı

- Lift = Kanat aerodinamiği
- Throttle = İleri hız
- Hover mümkün değil
- Enerji verimliliği yüksek

## 🔁 Transition

- Airspeed eşik kontrolü
- Rotor kapanma zamanlaması
- Ön motor aktivasyonu
- PID yeniden yapılandırma

Transition bir mod değil,  
**kontrol mimarisi yeniden yapılandırmasıdır.**

---

# 🛰 GÖREV VE NAVİGASYON ANALİZİ

Bu laboratuvarda test edilenler:

- Waypoint kabul yarıçapı
- AUTO vs GUIDED davranışı
- RTL vs QRTL karşılaştırması
- Home reset doğrulaması
- L1 navigasyon hassasiyeti

---

# ⚙ PARAMETRE TABANLI DENEYLER

Aktif incelenen parametreler:

- `Q_LAND_FINAL_ALT`
- `NAVL1_PERIOD`
- `ARSPD_FBW_MIN`
- `SIM_WIND_SPD`
- Batarya failsafe aksiyonları

Parametre değiştirmek:
> Uçağın karakterini değiştirmektir.

---

# 🌪 STRES TEST ORTAMI

Simülasyon koşulları:

- Rüzgar enjeksiyonu
- Düşük batarya senaryosu
- GPS kaybı simülasyonu
- Transition sırasında yük değişimi
- Hover drift ölçümü

---

# 📊 KONTROL GÖZLEMLERİ

- Q modda throttle = yükseklik
- Plane modda throttle = hız
- Lift üretimi hız bağımlıdır
- Yanlış mod–komut kombinasyonu kararsızlık üretir
- Failsafe zinciri moddan bağımsız çalışır

---

# 🛠 TEKNOLOJİ YIĞINI

- ArduPilot SITL
- Gazebo Classic
- MAVProxy
- MAVLink
- Ubuntu 20.04

---

# 🔬 GELECEK AŞAMALAR

- EKF sensör füzyon derin analizi
- PID tuning optimizasyonu
- Görüntü işleme entegrasyonu
- ROS2 köprü katmanı
- Gerçek donanım adaptasyonu

---

# 👤 PROJE SAHİBİ

Bilgisayar Mühendisliği  
İHA Simülasyon ve Uçuş Kontrol Sistemleri Çalışmaları  

---




