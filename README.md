# H00518884_B31OT_Individual_Assignment
# ESP32 Environmental Monitoring System

## Overview
Complete IoT system integrating ESP32-C3, DHT11 sensor, MQTT, Node-RED, and MongoDB.
Achieves 30ms end-to-end latency with real-time dashboard and historical analytics.

## System Architecture
![circuit_diagram](https://github.com/user-attachments/assets/547981d4-615b-4cdb-843f-eb09055c2807)

## Performance Metrics
- Latency: 30ms average (sensor to dashboard)
- Uptime: 99%+ over 24-hour test
- Storage: 1.5MB/day

## Hardware Requirements
- ESP32-C3 microcontroller
- DHT11 temperature/humidity sensor
- WS2812B NeoPixel LED

## Software Requirements
- Arduino IDE 2.3.6
- Mosquitto MQTT broker 2.0.15+
- Node-RED 24.11.0
- MongoDB 7.0.25

### Power Analysis
- Active (WiFi TX): 180mA peak
- Idle (WiFi connected): 75mA
- Average: 80mA
- Battery projection: 25h (current) or 156 days (with deep sleep at 5min intervals)

### Known Issues
- DHCP renewal causes brief disconnection (watchdog auto-recovers)
- DHT11 occasional NaN readings (filtered in code)
- No local buffering during WiFi outages
