# Smart Irrigation System 🌱

## Circuit Connection
![Circuit Connection](https://circuitdigest.com/sites/default/files/projectimage_mic/IoT-based-Smart-Irrigation-System-using-Soil-Moisture-Sensor-and-ESP8266-NodeMCU.jpg)

## Components Required

### 1. Soil Moisture Sensor
![Soil Moisture Sensor](https://cdn.shopify.com/s/files/1/0559/1970/6265/files/Blog_Images_9_1ae88b10-e693-4466-9e01-f5203ddb80a3_2048x2048.png?v=1715681817)

Specifications:
- Operating Voltage: 3.3V - 5V
- Output: Both Analog and Digital
- Dual LED indicators
- Adjustable sensitivity via potentiometer

### 2. PIR Motion Sensor (HC-SR501)
![PIR Motion Sensor](https://www.componentsinfo.com/wp-content/uploads/2020/04/hc-sr501-pir-sensor-module-pinout.jpg)

Specifications:
- Operating Voltage: 5V - 12V
- Detection Range: 3-7 meters
- Detection Angle: 120 degrees
- Adjustable delay time

### 3. Additional Components
- Node MCU ESP8266
- Relay module
- Bread board
- Jumper cables
- 12v Battery
- Water pump

## Connection Guide

### NodeMCU Connections:
```
- D0 (GPIO16) -> Soil Moisture Sensor (Digital Out)
- A0         -> Soil Moisture Sensor (Analog Out)
- D1 (GPIO5)  -> PIR Sensor Output
- D2 (GPIO4)  -> Relay Signal
- 3V3        -> Sensors VCC
- GND        -> Common Ground
```

### Soil Moisture Sensor:
```
- VCC  -> NodeMCU 3.3V
- GND  -> NodeMCU GND
- DO   -> NodeMCU D0
- AO   -> NodeMCU A0
```

### PIR Motion Sensor:
```
- VCC  -> NodeMCU 3.3V
- GND  -> NodeMCU GND
- OUT  -> NodeMCU D1
```

### Relay Module:
```
- VCC  -> NodeMCU 3.3V
- GND  -> NodeMCU GND
- IN   -> NodeMCU D2
- NO   -> Pump Positive
- COM  -> Battery Positive
```

## Software Requirements
- Arduino IDE
- Required Libraries:
  - ESP8266WiFi
  - ESP8266WebServer
  - DHT sensor library

## Installation Steps

1. Hardware Setup:
   - Connect components according to the circuit diagram
   - Ensure proper power supply connections
   - Verify sensor placements

2. Software Setup:
   - Install Arduino IDE
   - Add ESP8266 board support
   - Install required libraries
   - Upload the code

## Code Repository

```bash
git clone https://github.com/Pradeepkumar0246/SMART-IRRIGATION-SYSTEM.git
```

## Features
- Automated irrigation based on soil moisture
- Motion detection for security
- Real-time monitoring
- WiFi connectivity
- Mobile app control
- Water usage optimization

## Calibration Process
1. Soil Moisture Sensor:
   - Dry soil reading: ~800-1024
   - Wet soil reading: ~300-500
   - Set threshold: ~650 (adjustable)

2. PIR Sensor:
   - Adjust sensitivity using left potentiometer
   - Set delay time using right potentiometer
   - Test detection range

## Troubleshooting

### Common Issues:
1. Moisture Sensor Issues:
   - Clean sensor prongs
   - Check power connections
   - Verify analog readings

2. PIR Sensor Problems:
   - Allow 1-minute warmup
   - Adjust sensitivity
   - Check placement angle

3. Pump Not Working:
   - Verify relay connections
   - Check power supply
   - Test pump separately

## Contributing
1. Fork the repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Create Pull Request

## License
This project is licensed under the MIT License.

## Contact

For questions and support:
- Email: pradeepkumarmece21@gmail.com
- GitHub Issues
- Pull Requests

## Acknowledgments
- Thanks to all contributors
- Circuit design references
- Open-source community support

---
**Note**: This project is designed for educational and agricultural purposes. Always ensure proper safety measures when working with electrical components and water systems.