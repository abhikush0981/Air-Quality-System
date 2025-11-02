# Air Quality Monitoring & Control System

A real-time air quality monitoring and control system with an intuitive web dashboard for tracking environmental parameters and managing air purification systems.

![Air Quality System](https://img.shields.io/badge/Status-Active-success)
![Version](https://img.shields.io/badge/Version-1.0.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 🌟 Features

- **Real-Time Monitoring**: Continuous tracking of PM2.5, PM10, CO₂, VOCs, and environmental parameters
- **Live Dashboard**: Interactive web interface with real-time data visualization
- **AQI Tracking**: Air Quality Index calculation and color-coded status indicators
- **Historical Data**: 7-day trend analysis with interactive charts
- **Smart Controls**: Toggle controls for air purifier, ventilation, and auto-adjustment mode
- **Responsive Design**: Mobile-friendly interface with dark mode support
- **Alert System**: Real-time notifications when air quality thresholds are exceeded

## 📊 Monitored Parameters

| Parameter | Description | Unit |
|-----------|-------------|------|
| **AQI** | Air Quality Index | 0-500 scale |
| **PM2.5** | Fine Particulate Matter | μg/m³ |
| **PM10** | Coarse Particulate Matter | μg/m³ |
| **CO₂** | Carbon Dioxide | ppm |
| **VOC** | Volatile Organic Compounds | ppb |
| **Temperature** | Ambient Temperature | °C |
| **Humidity** | Relative Humidity | % |
| **Pressure** | Atmospheric Pressure | hPa |

## 🚀 Quick Start

### Prerequisites

- Modern web browser (Chrome, Firefox, Safari, Edge)
- No server or backend required - runs entirely in browser

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/air-quality-monitoring-system.git
   cd air-quality-monitoring-system
   ```

2. **Open the application**
   ```bash
   # Simply open index.html in your browser
   open index.html
   # Or on Windows
   start index.html
   # Or on Linux
   xdg-open index.html
   ```

3. **That's it!** The system will start displaying simulated sensor data.

## 📁 Project Structure

```
air-quality-monitoring-system/
├── index.html              # Main application file
├── assets/
│   ├── css/
│   │   └── styles.css     # Separated stylesheet (optional)
│   └── js/
│       └── app.js         # Separated JavaScript (optional)
├── docs/
│   ├── INSTALLATION.md    # Installation guide
│   └── API.md             # API documentation (for future integration)
├── screenshots/           # Application screenshots
├── README.md              # This file
├── LICENSE                # MIT License
└── .gitignore             # Git ignore rules
```

## 💡 Usage

### Basic Usage

1. Open `index.html` in a web browser
2. View real-time air quality data on the dashboard
3. Monitor AQI trends in the 7-day chart
4. Toggle system controls (purifier, ventilation, auto-mode)
5. Check alert notifications for air quality changes

### Control Panel

- **Air Purifier**: Toggle air purification system on/off
- **Ventilation System**: Control ventilation fan operation
- **Auto-Adjustment Mode**: Enable automatic air quality management
- **Alert Notifications**: Enable/disable real-time alerts

## 🔧 Customization

### Connecting Real Sensors

To integrate with actual IoT sensors, modify the `updateSensorData()` function in the JavaScript section:

```javascript
// Replace simulated data with API calls
async function updateSensorData() {
    const response = await fetch('YOUR_SENSOR_API_ENDPOINT');
    const data = await response.json();

    document.getElementById('aqi-value').textContent = data.aqi;
    document.getElementById('pm25').textContent = data.pm25 + ' μg/m³';
    // Update other values...
}
```

### Adjusting Update Intervals

```javascript
// Change update frequency (in milliseconds)
setInterval(updateTimestamp, 1000);  // Update every 1 second
setInterval(updateSensorData, 5000); // Update every 5 seconds
```

### Customizing Thresholds

Modify AQI thresholds in the CSS or JavaScript:

```javascript
if (aqi <= 50) {
    // Good air quality
} else if (aqi <= 100) {
    // Moderate air quality
}
// Add custom thresholds...
```

## 🎨 Design System

The application uses a custom design system with:
- CSS custom properties (variables) for consistent theming
- Automatic dark mode support via `prefers-color-scheme`
- Responsive grid layout for all screen sizes
- Smooth animations and transitions

## 🌐 Browser Support

- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Opera: ✅ Full support
- IE11: ❌ Not supported

## 📱 Responsive Design

The system is fully responsive and works on:
- 📱 Mobile phones (320px+)
- 📱 Tablets (768px+)
- 💻 Laptops (1024px+)
- 🖥️ Desktops (1280px+)

## 🔐 Security Considerations

- No backend storage (runs entirely client-side)
- No personal data collection
- No external dependencies or CDN requirements
- Safe for offline use

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Design system inspired by modern UI frameworks
- AQI standards based on EPA guidelines
- Icons: Unicode emoji (no external dependencies)

## 📧 Contact

Project Link: [https://github.com/yourusername/air-quality-monitoring-system](https://github.com/yourusername/air-quality-monitoring-system)

## 🗺️ Roadmap

- [ ] Integration with real IoT sensors (ESP32, Arduino)
- [ ] Historical data export (CSV, JSON)
- [ ] Email/SMS alert notifications
- [ ] Multi-location monitoring
- [ ] Mobile app version
- [ ] Backend API for data storage
- [ ] Machine learning predictions
- [ ] Comparison with nearby stations

## 📸 Screenshots

### Desktop View
![Dashboard Desktop](docs/screenshots/desktop-view.png)

### Mobile View
![Dashboard Mobile](docs/screenshots/mobile-view.png)

### Dark Mode
![Dark Mode](docs/screenshots/dark-mode.png)

---

**Made with ❤️ for cleaner air and healthier environments**
