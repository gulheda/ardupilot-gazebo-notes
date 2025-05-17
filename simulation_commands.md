# simülasyonu başlatırken 

sim_vehicle.py -v ArduCopter -f gazebo-iris --model JSON --map --console

# gazeboyu başlatırken 

gz sim -v4 -r iris_runway.sdf

#
arm throttle ->	Motorları çalıştırır (uçuşa hazır).

disarm ->	Motorları durdurur (güvenli moda geçer).

mode GUIDED ->	GPS destekli, komut kontrollü uçuş sağlar.

mode STABILIZE	-> Manuel uçuş modu (denge sağlar).

mode RTL ->	Kalkış yapılan noktaya otomatik geri dönüş.

mode LOITER	-> Olduğu yerde sabit kalır (hover).

mode AUTO	-> Görevleri (waypoint) otomatik takip eder.

mode LAND -> Bulunduğu yere yumuşak iniş yapar.

# MANUEL RC KONTROL KOMUTLARI

rc 1 1500 -> # Roll: sola-sağa yatış

rc 2 1500 -> # Pitch: ileri-geri

rc 3 1500 -> # Throttle: irtifa/yükseklik

rc 4 1500 -> # Yaw: yön değiştirme

# Değer aralığı genelde 1000–2000 arasındadır. 1500 nötr/denge konumudur.

# POZİSYON/KONUM KONTROLÜ (GPS)

tion <lat> <lon> <alt> ->	Drone’u belirli bir GPS noktasına yönlendirir.

guided> goto <lat> <lon> <alt> ->	(Bazı MAVProxy sürümlerinde çalışır)

rtl	-> Dönüş ve iniş (Return to Launch).

wp list ->	Kayıtlı görev noktalarını listeler.

wp load -> <dosya>	Görev noktası dosyası yükler.

wp set -> <index> <lat> <lon> <alt>	Görev noktasını el ile ayarlar.

wp save	-> Mevcut görev noktalarını dosyaya yazar.

wp clear-> Tüm görev noktalarını temizler.

# GÖREV VE YÖNLENDİRME KOMUTLARI

# Komut   	Açıklama

mission list ->	Yüklenmiş görevleri listeler.

mission reset	-> Görevi başa sarar.

mission start	-> Görevleri başlatır.

mission pause	-> Görevi geçici olarak duraklatır.

mission resume	-> Görevi kaldığı yerden sürdürür.

# SİMÜLASYON VE ARAÇ TESTİ

status	-> Drone’un durum bilgilerini listeler.

param show <parametre> ->	Parametre değeri gösterir.

param set <parametre> <değer> ->	Yeni parametre değeri atar.

watchdog reboot    ->    	Drone yazılımını yeniden başlatır (SITL için).

battery 100	-> Simülasyonda batarya doluluğunu ayarlar.

speed <m/s> ->	Drone hızını sınırlar.

# MAVProxy Yardımcıları

help	               ->  Kullanılabilir komutları listeler.

module list	         -> Yüklü modülleri listeler.

module load <isim>	 -> Modül yükler. Örnek: module load geofence

module unload <isim> -> Modül kaldırır.

# Drone haritada gözükmüyorsa:

map penceresinde sağ tıklayıp “Follow” ya da “Track Vehicle” varsa seç.

vehicle 1 komutu ile aktif aracı değiştirmeyi dene.


 # Drone’un maksimum yatay (ileri/geri/sağ/sol) hızını belirlemek için:

param set WPNAV_SPEED 500

WPNAV_SPEED	Waypoint  -> navigasyon hızı (cm/s cinsindedir).

500 → 5 m/s	Hızı 5 m/s olarak ayarlamış oluruz.

# Parametre	Açıklama

RTL_ALT	RTL ->  sırasında ne kadar yükseklikten dönsün (cm)

RTL_SPEED	-> Dönüş sırasında hızı (cm/s)

LAND_SPEED ->	İniş hızı (cm/s)

param set RTL_ALT 1000      -> 10 metre irtifadan geri dön

param set RTL_SPEED 400     -> 4 m/s dönüş hızı

param set LAND_SPEED 50     ->  0.5 m/s iniş hızı


param set WPNAV_SPEED 500	-> Navigasyon hızı (5 m/s).

param set WPNAV_ACCEL 250 -> 	İvme ayarı.

param set RTL_SPEED 300 -> 	Geri dönüş hızı.

# simülasyon durdumak için

CTRL + C

pkill gzserver

pkill gzclient

status                # Uçuş durumu


arm status            # Arming durumu
