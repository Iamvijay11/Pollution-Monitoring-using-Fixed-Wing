# Drone-Based Air Pollution Monitoring System

## Introduction

Air pollution is a growing concern worldwide due to its adverse impact on human health, the environment, and climate. Traditional pollution monitoring systems rely on stationary sensors that are limited in coverage and spatial flexibility. In many regions, especially rural or inaccessible areas, fixed air quality monitoring infrastructure is either unavailable or insufficient to capture real-time variations in pollutant concentrations.

Unmanned aerial vehicles (UAVs) have emerged as promising platforms for environmental monitoring. Their mobility, flexibility, and ability to reach difficult terrains make them highly suitable for dynamic data collection. Among various UAV types, fixed-wing drones offer extended flight durations and higher coverage, making them ideal for monitoring large geographical areas.

This project aims to design and implement a fixed-wing drone-based air pollution monitoring system equipped with air quality sensors and IoT connectivity for real-time data transmission and visualization.

---

## Problem Statement

Existing air pollution monitoring systems are stationary, expensive, and limited in spatial coverage, making it difficult to detect real-time variations in air quality, especially in remote or underserved areas. These limitations hinder effective environmental analysis, health assessments, and policy formulation.

To overcome this, the project proposes a mobile, low-cost air quality monitoring system using a fixed-wing drone equipped with environmental sensors. This system will measure key pollutants such as PM2.5, NOx, CO, CO₂, and O₃ in real time, enabling wide-area data collection and transmission. The solution aims to generate high-resolution air quality data to support environmental research, public health monitoring, and evidence-based policymaking.

---

## Motivation

### 1. Severe Health Impact of Air Pollution
- Air pollution causes over 7 million deaths annually (WHO).
- 91% of the global population lives in areas exceeding WHO air quality limits.
- Cities like Delhi record PM2.5 levels > 200 µg/m³ (13x WHO safe limit).

### 2. Limitations of Fixed Monitoring Stations
- Stationary, expensive, and sparse.
- Poor spatial and vertical resolution.
- Inadequate coverage in rural or uneven terrains.

### 3. Advantages of Drone-Based Mobile Monitoring
- Cost-effective and mobile.
- Can reach difficult or inaccessible locations.
- Provides dynamic spatial and vertical data.

### 4. Bridging Data Gaps and Enabling Smart Decisions
- Real-time data + drone mobility = smarter decisions.
- Supports health assessments and public policy.
- Promotes sustainable environmental management.

---

## Goals and Objectives

### Goal
Develop a drone-based pollution monitoring system capable of collecting and transmitting real-time air quality data across large and remote areas.

### Objectives
- Design and fabricate a fixed-wing drone to carry sensors and electronics.
- Integrate air quality sensors (e.g., MQ135) with Arduino Mega.
- Log data to an SD card.
- Transmit real-time data using LoRa modules.
- Ensure stable flight and reliable sensor performance.
- Conduct test flights to validate system performance.

---

## Methodology

### Selection of Fixed-Wing Drone
- Used EPP foam-based fixed-wing drone.
- Lightweight, durable, and RC-controlled.
- Adequate internal space for sensor electronics.

### Sensor and Microcontroller Integration
- **Sensors:** MQ135 (multi-gas), MQ-7 (CO), MG811 (CO₂), MiCS-4514 (NOx), MQ-131 (Ozone), PM2.5 (GP2Y1010AU0F).
- **Microcontroller:** Arduino Mega.
- Powered by the drone's Li-ion battery.
- External sensor placement in propeller downwash for ambient air exposure.

### IoT Connectivity and Data Transmission
- Data logging to SD card.
- Real-time transmission via LoRa (Tx onboard, Rx ground station).
- Arduino IDE for firmware development.

### Testing and Calibration
- Sensors calibrated using manufacturer curves.
- Ground and flight testing ensured hardware compatibility and data accuracy.
- Evaluated drone stability and sensor performance in motion.

---

## Field Deployment and Observations

- Stable drone flight and consistent data transmission.
- Spatial variations in pollutant levels detected:
  - Higher near roads/industrial zones.
  - Lower in open areas.
- Validated effectiveness of mobile air quality monitoring.

---

## Sensors Used

| Sensor | Pollutant | Notes |
|--------|-----------|-------|
| MQ-7   | CO        | Detects CO up to 10,000 ppm |
| MG811  | CO₂      | Requires pre-heating |
| MiCS 4514 | NOx     | MEMS-based, low power |
| MQ-131 | O₃       | SnO₂, variable conductivity |
| GP2Y1010AU0F | PM2.5 | Uses IR and phototransistor |

---

## Observations (Heatmaps Overview)

### 1. CO [ppb]
- Hotspots > 3000 ppb near roads.
- Lower levels inside open areas.

### 2. CO₂ [ppm]
- High levels > 4500 ppm in northern/southwestern zones.
- Lower in open field center.

### 3. PM2.5 [µg/m³]
- > 200 µg/m³ near western boundary.
- Dust and roadside activity likely sources.

### 4. NO₂ [ppm]
- Range: 0.170–0.187 ppm.
- Slight spike in southeastern corner.

### 5. NO [ppm]
- Peaks around 0.055 ppm near roads.
- Combustion-related pollutant.

### 6. O₃ [ppb]
- Some values > 1500 ppb; few negative values (sensor limitations).
- Indicates dynamic atmospheric processes.

---

## Conclusion

This drone-based air pollution monitoring system demonstrated:
- Real-time data collection and transmission.
- Monitoring of CO, NOx, O₃, PM2.5, and CO₂.
- Spatial resolution through drone mobility.
- Visualization through pollutant heatmaps.

Advantages:
- Access to hard-to-monitor zones.
- Variable altitude monitoring.
- Data supports public health and policy decisions.

---

## Future Work

### 1. Regulatory Integration and Data Sharing
- Ensure drone compliance.
- Collaborate with agencies for public dashboards.

### 2. Network Expansion
- Monitor larger areas.
- Enable long-term environmental studies.

### 3. Autonomous Flight and Alerts
- Enable autopilot.
- Add real-time alert generation.

### 4. Machine Learning Integration
- Predict pollution trends.
- Identify sources and hotspots.

### 5. Sensor Improvement
- Enhance sensitivity and accuracy.
- Calibrate regularly for reliable readings.

---

## Authors
- Vijay Kumar, IIT Kharagpur

> _For any inquiries, feel free to contact or raise issues in the repository._

---

## License

This project is released under the MIT License.

---

## Acknowledgements

- World Health Organization (WHO) statistics
- Arduino, LoRa, and sensor documentation
- TATA Steel Sports Complex (field testing location)
