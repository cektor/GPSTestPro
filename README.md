# GPS Test Pro - Professional GNSS Testing Application

<div align="center">
  <img src="gpslogo.png" alt="GPS Test Pro Logo" width="150" height="150"/>
  <br/><br/>
  
[![Android](https://img.shields.io/badge/Platform-Android-green.svg)](https://www.android.com/)
[![API](https://img.shields.io/badge/API-24%2B-brightgreen.svg)](https://android-arsenal.com/api?level=24)
[![Kotlin](https://img.shields.io/badge/Kotlin-1.9.22-blue.svg)](https://kotlinlang.org)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-2024.02.00-blue)](https://developer.android.com/jetpack/compose)
[![License](https://img.shields.io/badge/License-Educational-orange.svg)](LICENSE)

**[🇹🇷 Türkçe](README-TR.md)** | **🇬🇧 English**

</div>

---

## 📱 About

**GPS Test Pro** is a professional Android application for testing and analyzing GPS/GNSS satellite signals. Developed with modern Android technologies, it provides real-time satellite tracking, signal analysis, and location information.

Built from scratch using **Kotlin** and **Jetpack Compose** with a modern MVVM architecture.

---

## ✨ Features

### 🛰️ **Signal Screen**
- Real-time signal strength visualization with bar charts
- Support for multiple constellations: GPS (USA 🇺🇸), GLONASS (Russia 🇷🇺), GALILEO (EU 🇪🇺), BEIDOU (China 🇨🇳), QZSS (Japan 🇯🇵), IRNSS (India 🇮🇳), SBAS
- Color-coded signal quality indicators:
  - 🟢 **Green**: Excellent signal (≥30 dB)
  - 🟡 **Yellow**: Good signal (20-30 dB)
  - 🔴 **Red**: Weak signal (<20 dB)
  - ⚪ **Gray**: No signal
- Visual indication of satellites used in position fix (✓)
- Grouped by constellation with country flags

### 🌌 **Sky View Screen**
- Real-time satellite positions on compass view
- Azimuth and elevation angle visualization
- Color-coded satellites by signal strength
- Cardinal directions (N, S, E, W) overlay
- Interactive satellite selection with highlighting

### 🧭 **Compass Screen**
- Sensor-based digital compass with smooth animations
- Real-time heading display in degrees
- Cardinal and intercardinal directions (N, NE, E, SE, S, SW, W, NW)
- Compass calibration status with color indicators:
  - 🟢 **Good**: High accuracy
  - 🟡 **Medium**: Acceptable accuracy
  - 🟠 **Low**: Needs calibration
  - 🔴 **Poor**: Calibration required
- Built-in calibration guide
- Location information display

### 🗺️ **Map Screen**
- Real-time location tracking on OpenStreetMap
- **No API key required** (uses OSMDroid)
- Breadcrumb trail showing last 100 locations
- 5-meter threshold for trail recording
- Automatic map centering and zoom
- Works offline with cached tiles

### 📊 **Data Screen**
- Comprehensive location information:
  - Latitude and Longitude (6 decimal precision)
  - Altitude (meters)
  - Speed (km/h)
  - Accuracy (±meters)
  - Bearing (degrees)
  - UTC timestamp
- Satellite statistics:
  - Total visible satellites
  - Satellites used in fix
  - Breakdown by constellation
- Organized in beautiful Material 3 cards

### 🔍 **Satellite Details Screen**
- Detailed information for each satellite:
  - Satellite ID (SVID)
  - Constellation type and country
  - Signal strength (C/N0 in dB)
  - Signal quality rating
  - Elevation and azimuth angles
  - Ephemeris and Almanac status
  - Usage in position fix
  - Connection duration tracking
- Interactive satellite selection
- Sortable by constellation and ID
- Full-screen detail dialog

### 📐 **3D Isometric View**
- Isometric 3D visualization of satellite positions
- Height-based satellite rendering
- Color-coded by signal quality
- Elevation circles (0°, 30°, 60°, 90°)

### 🔥 **Signal Heatmap**
- Signal strength distribution chart
- Sorted by signal power (strongest to weakest)
- Visual bar representation
- Individual satellite signal bars

### 📈 **Satellite Density Map**
- Constellation distribution statistics
- Usage, quality, and weak signal metrics
- Visual density bars
- Per-constellation breakdown

### ℹ️ **About Screen**
- Application information and version
- Feature list
- Developer information
- Technical specifications
- Privacy policy link

---

## 🎨 Design & UI

- **Modern Material 3 Design** with dark theme
- **Responsive layouts** adapting to different screen sizes:
  - Compact (&lt;600dp): Phones
  - Medium (600-840dp): Large phones, small tablets
  - Expanded (&gt;840dp): Tablets
- **Smooth animations** and transitions
- **Animated dropdown menu** navigation
- **Professional splash screen** with fade-in animation
- **Turkish localization** throughout the app

---

## 🛠️ Technical Specifications

### Technologies
- **Language**: Kotlin 1.9.22
- **UI Framework**: Jetpack Compose (BOM 2024.02.00)
- **Architecture**: MVVM (ViewModel + StateFlow)
- **Minimum SDK**: 24 (Android 7.0 Nougat)
- **Target SDK**: 35 (Android 15)
- **Compile SDK**: 35

### Key Libraries
- **Jetpack Compose**: Modern declarative UI
- **Material 3**: Latest Material Design components
- **Lifecycle & ViewModel**: State management
- **Kotlin Coroutines & Flow**: Asynchronous operations
- **OSMDroid 6.1.18**: OpenStreetMap integration (no API key)
- **Google Play Services Location 21.1.0**: GPS/GNSS access
- **Accompanist Permissions**: Runtime permission handling

### Core Components
- **GnssStatus.Callback**: Real-time satellite data
- **LocationManager**: GPS location updates
- **SensorManager**: Compass and orientation sensors
- **StateFlow**: Reactive state management

---

## 📋 Permissions

```xml
<!-- GPS & Location -->
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />

<!-- Sensors (Compass) -->
<uses-permission android:name="android.permission.ACCESS_SENSOR_DATA" />

<!-- Internet & Network (Map tiles) -->
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<!-- External Storage (OSM cache, Android <=12) -->
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
```

---

## 🚀 Installation & Setup

### Prerequisites
- Android Studio Hedgehog (2023.1.1) or later
- JDK 17
- Android SDK 35
- Gradle 8.7

### Steps
1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/gps-test-pro.git
   cd gps-test-pro
   ```

2. **Open in Android Studio**
   - File → Open → Select project folder
   - Wait for Gradle sync

3. **Build the project**
   ```bash
   ./gradlew build
   ```

4. **Run on device/emulator**
   - Connect Android device or start emulator
   - Click Run (▶️) or press Shift+F10

5. **Grant permissions**
   - Allow location access when prompted
   - Enable GPS/Location services

---

## 📱 Usage

1. **Launch the app** - Splash screen appears for 2.5 seconds
2. **Grant location permission** - Required for GPS access
3. **Navigate between screens** - Use the hamburger menu (☰) in top-right
4. **View satellite signals** - Signal screen shows real-time data
5. **Track location** - Map screen displays your position with trail
6. **Analyze satellites** - Details screen provides in-depth information
7. **Check compass** - Compass screen shows heading and calibration
8. **Best results** - Use outdoors with clear sky view

---

## 🏗️ Project Structure

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

## 🔒 Privacy & Security

**GPS Test Pro respects your privacy:**

- ❌ **NO personal data collection**
- ❌ **NO cloud synchronization**
- ❌ **NO third-party analytics**
- ❌ **NO advertising**
- ✅ **All processing is local**
- ✅ **Location data stays on device**
- ✅ **Open source and transparent**

See [Privacy Policy](privacy_policy.md) for details. **Location data stays on device**
- ✅ **Open source and transparent**

See [Privacy Policy](privacy_policy.md) for details.

---

## 🎯 Use Cases

- **GPS Testing**: Verify GPS functionality on new devices
- **Signal Analysis**: Analyze satellite signal quality in different locations
- **Navigation Development**: Test location accuracy for navigation apps
- **Outdoor Activities**: Check GPS signal before hiking/camping
- **Research & Education**: Learn about GNSS constellations
- **Troubleshooting**: Diagnose GPS issues on Android devices

---

## 🌍 Supported GNSS Constellations

| Constellation | Country/Region | Satellites | Flag |
|--------------|----------------|------------|------|
| GPS | USA | 31+ | 🇺🇸 |
| GLONASS | Russia | 24+ | 🇷🇺 |
| GALILEO | European Union | 30+ | 🇪🇺 |
| BEIDOU | China | 35+ | 🇨🇳 |
| QZSS | Japan | 4+ | 🇯🇵 |
| IRNSS (NavIC) | India | 7+ | 🇮🇳 |
| SBAS | Various | Regional | 🌍 |

---

## 📸 Screenshots

<div align="center">
  <img src="screenshots/signal.png" width="200" alt="Signal Screen">
  <img src="screenshots/sky.png" width="200" alt="Sky View">
  <img src="screenshots/compass.png" width="200" alt="Compass">
  <img src="screenshots/map.png" width="200" alt="Map">
</div>

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is developed for **educational purposes**.

---

## 👨‍💻 Developer

**ALG Yazılım & Elektronik Inc.**  
**Fatih ÖNDER**

---

## 🙏 Acknowledgments

- [OSMDroid](https://github.com/osmdroid/osmdroid) for map integration
- Android Jetpack Compose team for the amazing UI framework
- Material Design team for design guidelines

---

## 📞 Support

For issues, questions, or suggestions:
- Open an [Issue](https://github.com/yourusername/gps-test-pro/issues)
- Contact: [your-email@example.com]

---

## 🔄 Version History

### v1.0.0 (Current)
- ✅ Initial release
- ✅ 10 functional screens
- ✅ Multi-constellation support
- ✅ Real-time satellite tracking
- ✅ OpenStreetMap integration
- ✅ Compass with calibration
- ✅ Material 3 design
- ✅ Responsive layouts
- ✅ Turkish localization

---

<div align="center">
  
  **Made with ❤️ using Kotlin & Jetpack Compose**
  
  ⭐ **Star this repo if you find it useful!** ⭐
  
</div>
