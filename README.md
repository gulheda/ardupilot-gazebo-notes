<!-- ===================== -->
<!--  VTOL UAV SIM LAB     -->
<!-- ===================== -->

<h1 align="center">
🚀 VTOL İHA SİMÜLASYON SİSTEMİ
</h1>

<p align="center">
<b>ArduPilot + Gazebo Tabanlı Hibrit Uçuş Kontrol ve Görev Altyapısı</b>
</p>

<p align="center">
<img src="https://img.shields.io/badge/System-VTOL-red?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Simulation-SITL-blue?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Physics-Hybrid-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge"/>
</p>

---

# 🛰 BU REPO NEDİR?

Bu bir demo klasörü değil.

Bu repository, VTOL (Vertical Take-Off and Landing) hibrit bir İHA'nın:

- 🔵 Dikey uçuş kontrol sistemi  
- 🔴 Sabit kanat aerodinamik modeli  
- 🔁 Transition dinamikleri  
- 🛰 Otonom görev altyapısı  
- ⚙ Parametre tabanlı davranış kontrolü  
- 🚨 Failsafe zincirleri  
- 🌪 Çevresel stres testleri  

için kurulmuş tam kapsamlı bir simülasyon laboratuvarıdır.

> Bu repoda VTOL İHA simülasyonuna dair **tüm dosyalar mevcuttur.**  
> Uçuş kontrolünden görev sistemine kadar her şey burada yapılandırılmıştır.

---

# 🧠 HİBRİT UÇUŞ MİMARİSİ

                ┌────────────────────┐
                │   Flight Control   │
                │   (ArduPilot)      │
                └──────────┬─────────┘
                           │
      ┌────────────────────┴────────────────────┐
      │                                         │
🔵 Multicopter Stack                      🔴 Fixed Wing Stack
   (Q Modları)                               (Plane Modları)



Transition =  
➡ Kontrol algoritması değişir  
➡ Lift üretim mekanizması değişir  
➡ Motor dağılımı değişir  
➡ Enerji modeli değişir  

Bu sadece mod değil, **fizik katmanı değişimidir.**

---

Tüm altyapı bu repoda mevcuttur.

