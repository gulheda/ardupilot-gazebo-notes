
# 🚀 VTOL İHA SİMÜLASYON LABORATUVARI
### ArduPilot + Gazebo Tabanlı Hibrit Uçuş Kontrol ve Görev Sistemleri Araştırma Ortamı

---

<p align="center">
<b>Bu bir drone simülasyonu değildir.</b><br>
Bu, hibrit bir uçuş kontrol sisteminin mühendislik seviyesinde analiz edildiği deneysel bir laboratuvardır.
</p>

---

# 🧠 PROJE NEDİR?

Bu repository, VTOL (Vertical Take-Off and Landing) yapısına sahip hibrit bir İHA'nın:

- Dikey uçuş fiziğini
- Sabit kanat aerodinamiğini
- Geçiş (transition) dinamiklerini
- Otonom görev algoritmalarını
- Failsafe zincirlerini
- Parametre temelli kontrol davranışlarını

simülasyon ortamında sistematik olarak test etmek ve anlamak amacıyla oluşturulmuştur.

Bu proje bir “uçuş denemesi” değil,  
bir **uçuş kontrol sistemi çözümlemesidir.**

---

# 🛩 HİBRİT MİMARİ

Bir VTOL aracı aslında iki ayrı uçaktır:

            ┌────────────────────────┐
            │   Flight Controller    │
            └───────────┬────────────┘
                        │
    ┌───────────────────┴───────────────────┐
    │                                       │

🔵 Multicopter Katmanı 🔴 Sabit Kanat Katmanı
(Q Modları) (Plane Modları)

    

Mod değişimi sadece yazılımsal değildir.  
**Fizik modeli değişir.**

- Lift üretim mekanizması değişir
- Motor dağılımı değişir
- Kontrol algoritması değişir
- Enerji tüketim modeli değişir

---

# 🔬 BU LABORATUVARDA NELER TEST EDİLİYOR?

## 🔵 Dikey Uçuş (Q Modları)

- Hover stabilitesi
- Rüzgar altında pozisyon tutma
- Dikey iniş algoritması
- QRTL dönüş mantığı
- Batarya temelli zorunlu iniş

---

## 🔴 Sabit Kanat Uçuşu

- Hız – lift ilişkisi
- Stall eşiği gözlemi
- L1 navigasyon parametreleri
- Otonom seyir davranışı
- Glide performansı

---

## 🔄 Transition Dinamikleri

- Airspeed eşik değerleri
- Rotor kapanma zamanlaması
- Ön motor devreye girme süresi
- Hibrit görev akışı:
  - VTOL kalkış
  - Sabit kanat seyir
  - VTOL iniş

Transition bir mod değişimi değil,  
bir **fizik katmanı değişimidir.**

---

# 🛰 OTONOM GÖREV SİSTEMİ

Bu projede:

- Waypoint tolerans analizi
- AUTO ve GUIDED davranış karşılaştırması
- RTL vs QRTL rota farkı
- Home konum doğrulaması
- GPS bağımlılığı analizi

detaylı olarak incelenmektedir.

---

# ⚙ PARAMETRE TABANLI MÜHENDİSLİK

Uçak davranışı doğrudan parametrelerle şekillenir.

Bu laboratuvarda aktif olarak incelenen parametreler:

- `Q_LAND_FINAL_ALT`
- `NAVL1_PERIOD`
- `ARSPD_FBW_MIN`
- `SIM_WIND_SPD`
- Batarya failsafe aksiyonları

Parametre değiştirmek,  
uçağın karakterini değiştirmektir.

---

# 🌪 STRES TEST SENARYOLARI

Simülasyon ortamında:

- Rüzgar enjeksiyonu
- Düşük batarya senaryosu
- GPS kaybı
- Transition sırasında yük değişimi
- Hover drift analizi

gerçek sistem koşulları taklit edilmektedir.

---

# 🧠 KAZANIMLAR

Bu proje sayesinde:

- Hibrit uçuş sistem mimarisi anlaşılmıştır
- Uçuş modları arası fiziksel farklar gözlemlenmiştir
- Lift üretiminin hız bağımlılığı doğrulanmıştır
- Yanlış mod – yanlış komut kombinasyonunun etkileri analiz edilmiştir
- Failsafe zinciri test edilmiştir

---

# 🎯 PROJENİN AMACI

Amaç bir simülasyon uçurmak değil;

- Hibrit uçuş kontrol sistemini çözümlemek
- Kontrol algoritmalarını anlamak
- Otonom görev mantığını analiz etmek
- Gerçek sistem geliştirme altyapısı oluşturmak

Bu repository bir deney ortamıdır.

---

# 🛠 KULLANILAN TEKNOLOJİLER

- ArduPilot SITL
- Gazebo Classic
- MAVProxy
- MAVLink
- Ubuntu 20.04

---

# 📌 GELECEK ÇALIŞMALAR

- EKF sensör füzyon analizi
- PID tuning derin inceleme
- Görüntü işleme entegrasyonu
- ROS2 entegrasyon katmanı
- Gerçek donanım adaptasyonu

---

# 👤 YAZAR

G]lheda KIZILHAN
İHA Simülasyon ve Uçuş Kontrol Sistemleri Çalışmaları  

---

# 🏁 SONUÇ

Bu proje bir simülasyon değil,  
bir uçuş kontrol sisteminin mühendislik seviyesinde incelenmesidir.

VTOL sistemini anlamak,  
iki ayrı uçağın fiziğini aynı gövdede çözmektir.
