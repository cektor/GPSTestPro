# GPS Test Pro - Profesyonel GNSS Test Uygulaması

<div align="center">
  <img src="app/src/main/res/drawable/gpslogo.png" alt="GPS Test Pro Logo" width="150" height="150"/>
  <br/><br/>
  
[![Android](https://img.shields.io/badge/Platform-Android-green.svg)](https://www.android.com/)
[![API](https://img.shields.io/badge/API-24%2B-brightgreen.svg)](https://android-arsenal.com/api?level=24)
[![Kotlin](https://img.shields.io/badge/Kotlin-1.9.22-blue.svg)](https://kotlinlang.org)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-2024.02.00-blue)](https://developer.android.com/jetpack/compose)
[![License](https://img.shields.io/badge/License-Educational-orange.svg)](LICENSE)

**🇹🇷 Türkçe** | **[🇬🇧 English](README.md)**

</div>

---

## 📱 Hakkında

**GPS Test Pro**, GPS/GNSS uydu sinyallerini test etmek ve analiz etmek için geliştirilmiş profesyonel bir Android uygulamasıdır. Modern Android teknolojileri ile geliştirilmiş olup, gerçek zamanlı uydu takibi, sinyal analizi ve konum bilgisi sağlar.

**Kotlin** ve **Jetpack Compose** kullanılarak sıfırdan modern MVVM mimarisi ile geliştirilmiştir.

---

## ✨ Özellikler

### 🛰️ **Sinyal Ekranı**
- Bar grafiklerle gerçek zamanlı sinyal gücü görselleştirmesi
- Çoklu takımyıldız desteği: GPS (ABD 🇺🇸), GLONASS (Rusya 🇷🇺), GALILEO (AB 🇪🇺), BEIDOU (Çin 🇨🇳), QZSS (Japonya 🇯🇵), IRNSS (Hindistan 🇮🇳), SBAS
- Renkli sinyal kalitesi göstergeleri:
  - 🟢 **Yeşil**: Mükemmel sinyal (≥30 dB)
  - 🟡 **Sarı**: İyi sinyal (20-30 dB)
  - 🔴 **Kırmızı**: Zayıf sinyal (<20 dB)
  - ⚪ **Gri**: Sinyal yok
- Konum hesaplamasında kullanılan uyduların görsel gösterimi (✓)
- Ülke bayraklarıyla takımyıldızlara göre gruplandırma

### 🌌 **Gökyüzü Görünümü Ekranı**
- Pusula görünümünde gerçek zamanlı uydu konumları
- Azimut ve yükselme açısı görselleştirmesi
- Sinyal gücüne göre renklendirilmiş uydular
- Ana yönler (K, G, D, B) üst katmanı
- Vurgulama ile interaktif uydu seçimi

### 🧭 **Pusula Ekranı**
- Yumuşak animasyonlarla sensör tabanlı dijital pusula
- Derece cinsinden gerçek zamanlı yön gösterimi
- Ana ve ara yönler (K, KD, D, GD, G, GB, B, KB)
- Renkli göstergelerle pusula kalibrasyon durumu:
  - 🟢 **İyi**: Yüksek doğruluk
  - 🟡 **Orta**: Kabul edilebilir doğruluk
  - 🟠 **Düşük**: Kalibrasyon gerekli
  - 🔴 **Zayıf**: Kalibrasyon şart
- Yerleşik kalibrasyon rehberi
- Konum bilgisi gösterimi

### 🗺️ **Harita Ekranı**
- OpenStreetMap üzerinde gerçek zamanlı konum takibi
- **API anahtarı gerektirmez** (OSMDroid kullanır)
- Son 100 konumu gösteren iz kaydı
- İz kaydı için 5 metre eşik değeri
- Otomatik harita merkezleme ve yakınlaştırma
- Önbelleğe alınmış karolarla çevrimdışı çalışma

### 📊 **Veri Ekranı**
- Kapsamlı konum bilgileri:
  - Enlem ve Boylam (6 ondalık hassasiyet)
  - İrtifa (metre)
  - Hız (km/s)
  - Doğruluk (±metre)
  - Yön (derece)
  - UTC zaman damgası
- Uydu istatistikleri:
  - Toplam görünen uydu sayısı
  - Konum hesaplamasında kullanılan uydu sayısı
  - Takımyıldızlara göre dağılım
- Güzel Material 3 kartlarında düzenlenmiş

### 🔍 **Uydu Detayları Ekranı**
- Her uydu için detaylı bilgi:
  - Uydu ID (SVID)
  - Takımyıldız tipi ve ülke
  - Sinyal gücü (C/N0 dB cinsinden)
  - Sinyal kalitesi değerlendirmesi
  - Yükselme ve azimut açıları
  - Ephemeris ve Almanac durumu
  - Konum hesaplamasında kullanım
  - Bağlantı süresi takibi
- İnteraktif uydu seçimi
- Takımyıldız ve ID'ye göre sıralanabilir
- Tam ekran detay diyalogu

### 📐 **3D İzometrik Görünüm**
- Uydu konumlarının izometrik 3D görselleştirmesi
- Yükseklik tabanlı uydu gösterimi
- Sinyal kalitesine göre renklendirilmiş
- Yükselme çemberleri (0°, 30°, 60°, 90°)

### 🔥 **Sinyal Isı Haritası**
- Sinyal gücü dağılım grafiği
- Sinyal gücüne göre sıralanmış (en güçlüden en zayıfa)
- Görsel bar gösterimi
- Bireysel uydu sinyal çubukları

### 📈 **Uydu Yoğunluk Haritası**
- Takımyıldız dağılım istatistikleri
- Kullanım, kalite ve zayıf sinyal metrikleri
- Görsel yoğunluk çubukları
- Takımyıldız başına dağılım

### ℹ️ **Hakkında Ekranı**
- Uygulama bilgileri ve sürüm
- Özellik listesi
- Geliştirici bilgileri
- Teknik özellikler
- Gizlilik politikası bağlantısı

---

## 🎨 Tasarım & Kullanıcı Arayüzü

- **Modern Material 3 Tasarım** ile koyu tema
- Farklı ekran boyutlarına uyum sağlayan **Duyarlı düzenler**:
  - Kompakt (&lt;600dp): Telefonlar
  - Orta (600-840dp): Büyük telefonlar, küçük tabletler
  - Genişletilmiş (&gt;840dp): Tabletler
- **Yumuşak animasyonlar** ve geçişler
- **Animasyonlu açılır menü** navigasyonu
- Solma animasyonlu **Profesyonel açılış ekranı**
- Uygulama genelinde **Türkçe yerelleştirme**

---

## 🛠️ Teknik Özellikler

### Teknolojiler
- **Dil**: Kotlin 1.9.22
- **UI Framework**: Jetpack Compose (BOM 2024.02.00)
- **Mimari**: MVVM (ViewModel + StateFlow)
- **Minimum SDK**: 24 (Android 7.0 Nougat)
- **Hedef SDK**: 35 (Android 15)
- **Derleme SDK**: 35

### Ana Kütüphaneler
- **Jetpack Compose**: Modern bildirimsel UI
- **Material 3**: En son Material Design bileşenleri
- **Lifecycle & ViewModel**: Durum yönetimi
- **Kotlin Coroutines & Flow**: Asenkron işlemler
- **OSMDroid 6.1.18**: OpenStreetMap entegrasyonu (API anahtarı yok)
- **Google Play Services Location 21.1.0**: GPS/GNSS erişimi
- **Accompanist Permissions**: Çalışma zamanı izin yönetimi

### Temel Bileşenler
- **GnssStatus.Callback**: Gerçek zamanlı uydu verisi
- **LocationManager**: GPS konum güncellemeleri
- **SensorManager**: Pusula ve yönelim sensörleri
- **StateFlow**: Reaktif durum yönetimi

---

## 📋 İzinler

```xml
<!-- GPS & Konum -->
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />

<!-- Sensörler (Pusula) -->
<uses-permission android:name="android.permission.ACCESS_SENSOR_DATA" />

<!-- İnternet & Ağ (Harita karoları) -->
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<!-- Harici Depolama (OSM önbellek, Android <=12) -->
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
```

---

## 🚀 Kurulum & Yapılandırma

### Gereksinimler
- Android Studio Hedgehog (2023.1.1) veya üzeri
- JDK 17
- Android SDK 35
- Gradle 8.7

### Adımlar
1. **Depoyu klonlayın**
   ```bash
   git clone https://github.com/kullaniciadi/gps-test-pro.git
   cd gps-test-pro
   ```

2. **Android Studio'da açın**
   - File → Open → Proje klasörünü seçin
   - Gradle senkronizasyonunu bekleyin

3. **Projeyi derleyin**
   ```bash
   ./gradlew build
   ```

4. **Cihaz/emülatörde çalıştırın**
   - Android cihazı bağlayın veya emülatörü başlatın
   - Run (▶️) tıklayın veya Shift+F10 tuşlarına basın

5. **İzinleri verin**
   - İstendiğinde konum erişimine izin verin
   - GPS/Konum servislerini etkinleştirin

---

## 📱 Kullanım

1. **Uygulamayı başlatın** - Açılış ekranı 2.5 saniye görünür
2. **Konum iznini verin** - GPS erişimi için gereklidir
3. **Ekranlar arasında gezinin** - Sağ üstteki hamburger menüsünü (☰) kullanın
4. **Uydu sinyallerini görüntüleyin** - Sinyal ekranı gerçek zamanlı veri gösterir
5. **Konumu takip edin** - Harita ekranı iz kaydıyla konumunuzu gösterir
6. **Uyduları analiz edin** - Detaylar ekranı derinlemesine bilgi sağlar
7. **Pusulayı kontrol edin** - Pusula ekranı yön ve kalibrasyonu gösterir
8. **En iyi sonuçlar** - Açık gökyüzü görüşü olan dış mekanlarda kullanın

---

## 🏗️ Proje Yapısı

```
gps_test/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/alg/gpstestpro/
│   │   │   │   ├── MainActivity.kt
│   │   │   │   ├── model/
│   │   │   │   │   └── SatelliteInfo.kt
│   │   │   │   ├── viewmodel/
│   │   │   │   │   └── GpsViewModel.kt
│   │   │   │   ├── ui/
│   │   │   │   │   ├── GpsTestApp.kt
│   │   │   │   │   ├── screens/
│   │   │   │   │   │   ├── SplashScreen.kt
│   │   │   │   │   │   ├── SignalScreen.kt
│   │   │   │   │   │   ├── SkyScreen.kt
│   │   │   │   │   │   ├── CompassScreen.kt
│   │   │   │   │   │   ├── MapScreen.kt
│   │   │   │   │   │   ├── DataScreen.kt
│   │   │   │   │   │   ├── SatelliteDetailsScreen.kt
│   │   │   │   │   │   ├── Satellite3DScreen.kt
│   │   │   │   │   │   ├── SignalHeatmapScreen.kt
│   │   │   │   │   │   ├── SatelliteDensityScreen.kt
│   │   │   │   │   │   └── AboutScreen.kt
│   │   │   │   │   ├── theme/
│   │   │   │   │   │   └── Theme.kt
│   │   │   │   │   └── utils/
│   │   │   │   │       └── ResponsiveUtils.kt
│   │   │   ├── res/
│   │   │   │   ├── drawable/
│   │   │   │   │   └── gpslogo.png
│   │   │   │   └── values/
│   │   │   └── AndroidManifest.xml
│   │   └── build.gradle.kts
│   └── proguard-rules.pro
├── gradle/
├── README.md
├── README-TR.md
└── privacy_policy.md
```

---

## 🔒 Gizlilik & Güvenlik

**GPS Test Pro gizliliğinize saygı duyar:**

- ❌ **KİŞİSEL veri toplama YOK**
- ❌ **Bulut senkronizasyonu YOK**
- ❌ **Üçüncü taraf analitik YOK**
- ❌ **Reklam YOK**
- ✅ **Tüm işlemler yerel**
- ✅ **Konum verisi cihazda kalır**
- ✅ **Açık kaynak ve şeffaf**

Detaylar için [Gizlilik Politikası](privacy_policy.md)'na bakın.

---

## 🎯 Kullanım Alanları

- **GPS Testi**: Yeni cihazlarda GPS işlevselliğini doğrulama
- **Sinyal Analizi**: Farklı konumlarda uydu sinyal kalitesini analiz etme
- **Navigasyon Geliştirme**: Navigasyon uygulamaları için konum doğruluğunu test etme
- **Açık Hava Aktiviteleri**: Yürüyüş/kamp öncesi GPS sinyalini kontrol etme
- **Araştırma & Eğitim**: GNSS takımyıldızları hakkında öğrenme
- **Sorun Giderme**: Android cihazlarda GPS sorunlarını teşhis etme

---

## 🌍 Desteklenen GNSS Takımyıldızları

| Takımyıldız | Ülke/Bölge | Uydu Sayısı | Bayrak |
|-------------|------------|-------------|--------|
| GPS | ABD | 31+ | 🇺🇸 |
| GLONASS | Rusya | 24+ | 🇷🇺 |
| GALILEO | Avrupa Birliği | 30+ | 🇪🇺 |
| BEIDOU | Çin | 35+ | 🇨🇳 |
| QZSS | Japonya | 4+ | 🇯🇵 |
| IRNSS (NavIC) | Hindistan | 7+ | 🇮🇳 |
| SBAS | Çeşitli | Bölgesel | 🌍 |

---

## 📸 Ekran Görüntüleri

<div align="center">
  <img src="screenshots/signal.png" width="200" alt="Sinyal Ekranı">
  <img src="screenshots/sky.png" width="200" alt="Gökyüzü Görünümü">
  <img src="screenshots/compass.png" width="200" alt="Pusula">
  <img src="screenshots/map.png" width="200" alt="Harita">
</div>

---

## 🤝 Katkıda Bulunma

Katkılar memnuniyetle karşılanır! Lütfen Pull Request göndermekten çekinmeyin.

1. Projeyi fork edin
2. Özellik dalınızı oluşturun (`git checkout -b feature/HarikaBirOzellik`)
3. Değişikliklerinizi commit edin (`git commit -m 'Harika bir özellik ekle'`)
4. Dalınıza push yapın (`git push origin feature/HarikaBirOzellik`)
5. Pull Request açın

---

## 📄 Lisans

Bu proje **eğitim amaçlı** geliştirilmiştir.

---

## 👨💻 Geliştirici

**ALG Yazılım & Elektronik Inc.**  
**Fatih ÖNDER**

---

## 🙏 Teşekkürler

- Harita entegrasyonu için [OSMDroid](https://github.com/osmdroid/osmdroid)
- Harika UI framework için Android Jetpack Compose ekibi
- Tasarım kılavuzları için Material Design ekibi

---

## 📞 Destek

Sorunlar, sorular veya öneriler için:
- [Issue](https://github.com/kullaniciadi/gps-test-pro/issues) açın
- İletişim: [email@ornek.com]

---

## 🔄 Sürüm Geçmişi

### v1.0.0 (Güncel)
- ✅ İlk sürüm
- ✅ 10 fonksiyonel ekran
- ✅ Çoklu takımyıldız desteği
- ✅ Gerçek zamanlı uydu takibi
- ✅ OpenStreetMap entegrasyonu
- ✅ Kalibrasyonlu pusula
- ✅ Material 3 tasarım
- ✅ Duyarlı düzenler
- ✅ Türkçe yerelleştirme

---

<div align="center">
  
  **Kotlin & Jetpack Compose ile ❤️ ile yapıldı**
  
  ⭐ **Faydalı bulduysanız bu depoyu yıldızlayın!** ⭐
  
</div>
