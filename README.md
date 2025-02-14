# Intelligent Weather Station on ESP32

## Project Description

The "Intelligent Weather Station on ESP32" project is a comprehensive system for monitoring atmospheric conditions. It consists of an IoT device based on the ESP32 microcontroller and a web application that visualizes collected data. The system uses sensors to measure temperature, humidity, atmospheric pressure, and air quality. Data is transmitted to the backend via the MQTT protocol and displayed in the web application. 

## Features

### ESP32 (Device Software)
- Measurement of environmental parameters using the BME280 sensor.
- Communication with the backend via MQTT.
- WiFi support for data transmission.
- Ability to configure measurement frequency.
- LED indicator signaling data transmission.

### Backend (Server Application - Django)
- Subscription to environmental data from ESP32.
- Storing data in a database (Django ORM).
- Handling MQTT events.
- Ability to configure sensor parameters.

### Frontend (Web Application - Angular)
- Display of measurement data in the form of charts.
- Management of weather stations.
- Configuration of measurement parameters.
- Notifications for exceeding predefined thresholds.

## Requirements

### ESP32
- ESP32 with WiFi support.
- BME280 sensor.
- USB power supply.
- PlatformIO ecosystem

### Backend
- Python 3.9+
- Django 4+
- Mosquitto MQTT Broker
- SQLite / PostgreSQL database

### Frontend
- Angular 15+
- Node.js 16+
- Angular CLI


## System Architecture

```
[ESP32] --(WiFi)--> [MQTT Broker] --(Django ORM)--> [Database]
                                 |
                                 v
                           [Web Application]
```

## API

- **Data subscription:** `/users/{user_id}/devices/{device_id}/data`
- **Change measurement frequency:** `/request/frequency`
- **MQTT message format:**
```json
{
  "temperature": 23.5,
  "humidity": 45.6,
  "pressure": 1013.2,
  "mac": "A1:B2:C3:D4:E5:F6"
}
```

## Authors
- **Kamila Baizakova**
- **Lidia Moryc**
- **Adam Stajek**

## License
This project is available under the MIT license.
](https://github.com/IOT-ISI24/IoT-server)
