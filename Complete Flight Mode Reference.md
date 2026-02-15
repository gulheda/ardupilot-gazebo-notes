# ✈️ ArduPlane VTOL – Complete Flight Mode Reference

Bu doküman ArduPlane VTOL firmware içindeki tüm uçuş modlarını:

- Fizik modeli
- Kontrol mantığı
- Gaz davranışı
- GPS kullanımı
- Otonomi seviyesi
- Operasyonel kullanım

açısından detaylı şekilde açıklar.

---

# 🧠 VTOL Nedir?

VTOL (Vertical Take-Off and Landing) iki farklı uçuş sistemini birleştirir:

1. 🔵 Multicopter (Rotor tabanlı dikey uçuş)
2. 🔴 Fixed Wing (Kanat tabanlı aerodinamik uçuş)

Mod değiştirildiğinde sadece kontrol değil, **fizik modeli değişir.**

---

# 🔵 BÖLÜM 1 – VTOL (Q) MODLARI

Bu modlarda araç dikey rotorlarla uçar.

---

## QSTABILIZE

**Fizik:** Multicopter  
**Gaz:** Yükseklik kontrol eder  
**GPS:** Kullanılmaz  
**Otonomi:** Manuel stabilize  

Roll ve pitch stabilize edilir.  
Pozisyon tutulmaz.

> Kontrollü manuel hover.

---

## QHOVER

**Fizik:** Multicopter  
**Gaz:** Yükseklik  
**GPS:** Zayıf/opsiyonel  
**Otonomi:** Manuel  

Pilot gaz verir, araç dikey hareket eder.  
Drift olabilir.

> Manuel dikey uçuş.

---

## QLOITER

**Fizik:** Multicopter  
**Gaz:** Yükseklik  
**GPS:** Aktif  
**Otonomi:** Yarı otonom  

Pozisyon sabit tutulur.  
Stick bırakıldığında konum korunur.

> Sabit hover.

---

## QLAND

**Fizik:** Multicopter  
**Gaz:** Autopilot yönetir  
**GPS:** Opsiyonel  
**Otonomi:** Tam  

Bulunduğu yerde dikey iner.

> Otonom dikey iniş.

---

## QRTL

**Fizik:** Multicopter  
**Gaz:** Autopilot  
**GPS:** Aktif  
**Otonomi:** Tam  

Home’a gider → Hover → İner.

> VTOL eve dönüş.

---

## QACRO

**Fizik:** Multicopter  
**Gaz:** Manuel  
**GPS:** Yok  
**Otonomi:** Yok  

Açısal hız kontrolü. Stabil değil.

> Dikey akro modu.

---

## QAUTOTUNE

**Fizik:** Multicopter  
**Gaz:** Otomatik  
**GPS:** Gerekmez  
**Otonomi:** PID tuning  

Q mod PID parametrelerini ayarlar.

---

## LOITERALTQLAND

**Fizik:** Multicopter  
**Gaz:** Otomatik  
**GPS:** Aktif  
**Otonomi:** Hibrit  

LOITER yapar → Sonra QLAND.

---

# 🔴 BÖLÜM 2 – SABİT KANAT (PLANE) MODLARI

Bu modlarda uçuş kanat kaldırma kuvvetiyle gerçekleşir.

---

## MANUAL

**Fizik:** Sabit kanat  
**Gaz:** İleri hız  
**GPS:** Yok  
**Otonomi:** Yok  

Servo girişleri direkt uygulanır.

> Ham uçuş.

---

## STABILIZE

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Yok  
**Otonomi:** Yarı  

Attitude stabilize edilir.

---

## TRAINING

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Yok  
**Otonomi:** Limitli  

Yatış açısı sınırlandırılır.

---

## ACRO

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Yok  
**Otonomi:** Yok  

Açısal hız kontrolü.

---

## FBWA (Fly By Wire A)

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Opsiyonel  
**Otonomi:** Güvenlik destekli  

Pilot açı verir.  
Autopilot aşırı yatışı ve stall’ı engeller.

---

## FBWB

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Aktif  
**Otonomi:** Yarı  

Pitch = Yükseklik  
Throttle = Hız  

---

## CRUISE

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Aktif  
**Otonomi:** Yarı  

Yükseklik ve yön tutulur.

---

## CIRCLE

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Gerekmez  
**Otonomi:** Yarı  

Sabit yarıçapta daire.

---

## LOITER

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Aktif  
**Otonomi:** Tam  

GPS noktasında daire çizer.

---

## RTL

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Aktif  
**Otonomi:** Tam  

Home’a sabit kanat uçuşla döner.

---

## AUTO

**Fizik:** Hibrit  
**Gaz:** Otomatik  
**GPS:** Aktif  
**Otonomi:** Tam  

Mission waypoint’lerini yürütür.  
Gerekirse Q ↔ Plane transition yapar.

---

## GUIDED

**Fizik:** Sabit kanat  
**Gaz:** Otomatik  
**GPS:** Aktif  
**Otonomi:** Tam  

Anlık verilen koordinata gider.

---

## AUTOTUNE

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Opsiyonel  
**Otonomi:** PID tuning  

---

## TAKEOFF

**Fizik:** Sabit kanat  
**Gaz:** Otomatik  
**GPS:** Opsiyonel  
**Otonomi:** AUTO içinde  

Pist kalkışı yapar.

---

## THERMAL

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Aktif  
**Otonomi:** Tam  

Termal hava akımı arar.

---

## AUTOLAND

**Fizik:** Sabit kanat  
**Gaz:** Otomatik  
**GPS:** Aktif  
**Otonomi:** Tam  

Glide slope ile pist inişi yapar.

---

## AVOID_ADSB

**Fizik:** Sabit kanat  
**Gaz:** Hız  
**GPS:** Aktif  
**Otonomi:** Tam  

Hava trafik çarpışma önleme.

---

## INITIALISING

Sistem açılış durumu.  
Uçuş yapılamaz.

---

# 🎯 Kritik Kavrayış

| Özellik | Q Modlar | Plane Modlar |
|----------|-----------|--------------|
| Lift Kaynağı | Rotor itki | Kanat aerodinamiği |
| Throttle | Yükseklik | Hız |
| Dikey Kalkış | ✅ | ❌ |
| Uzun Menzil Verimlilik | ❌ | ✅ |
| Hover | ✅ | ❌ |

---

# 🏁 Sonuç

VTOL sistemi iki ayrı uçuş mimarisini tek firmware içinde birleştirir.

Mod değişimi:

- Fizik modeli
- Motor dağılımı
- Stabilizasyon algoritması
- Enerji tüketimi
- Kontrol yaklaşımı

değiştirir.

Mod seçimi, uçuş fiziği seçimidir.

