# 🌱 Solar Powered Floating Garden System for Air and Water Purification

A solar-powered, IoT-enabled floating hydroponic platform designed for **water purification, environmental monitoring, aeration, and assisted mobility** in ponds, lakes, and other stagnant water bodies.

The system combines **hydroponics, phytoremediation, IoT-based sensing, solar energy, controlled aeration, wireless monitoring, propulsion, and obstacle detection** into a single floating platform.

---

## 📌 Project Overview

Water pollution in lakes, ponds, and stagnant water bodies can negatively affect aquatic ecosystems and environmental quality. Conventional purification methods can be expensive and energy-intensive.

This project proposes a **Solar Powered Floating Garden System** that uses aquatic plants for natural phytoremediation while continuously monitoring environmental parameters using sensors.

The floating platform is powered by a **12 V, 12 W solar panel** and a **12 V, 5 Ah rechargeable battery**. An **ESP32-S3** acts as the central controller, collecting sensor data, controlling actuators, and transmitting environmental data to the **Blynk IoT platform** over Wi-Fi.

The platform can also move across the water surface using underwater thrusters and detect obstacles using an ultrasonic sensor.

---

## 🎯 Objectives

The major objectives of the project are:

- 🌱 Develop a floating garden for natural water purification using hydroponics and phytoremediation.
- ☀️ Utilize solar energy to power the floating system and aeration mechanism.
- 💧 Monitor water-quality parameters such as pH, TDS, and water temperature.
- 🌫️ Monitor ambient air quality, temperature, and humidity.
- 🚤 Provide assisted mobility using underwater thrusters.
- 🚧 Detect obstacles during movement.
- 📡 Provide real-time environmental monitoring through IoT.
- 📱 Visualize sensor data remotely using the Blynk mobile application.

These objectives are described in the project report's system design and objectives sections. :contentReference[oaicite:1]{index=1}

---

# 🏗️ System Architecture

The system consists of the following major subsystems:

```text
                    ☀️ SOLAR PANEL
                         │
                         ▼
                ┌──────────────────┐
                │ Solar Controller │
                └────────┬─────────┘
                         │
                         ▼
                  🔋 12V Battery
                         │
                         ▼
                  ┌─────────────┐
                  │  ESP32-S3   │
                  │ Main Control│
                  │    Unit     │
                  └──────┬──────┘
                         │
       ┌─────────────────┼──────────────────┐
       │                 │                  │
       ▼                 ▼                  ▼
 Water Monitoring   Air Monitoring     Mobility
       │                 │                  │
 ┌─────┼──────┐    ┌─────┼─────┐      ┌────┴─────┐
 │     │      │    │     │     │      │ Thrusters│
 pH   TDS   DS18B20 MQ135 DHT11       │ BTS7960  │
 │     │      │    │     │     │      └──────────┘
 └─────┴──────┘    └─────┴─────┘
                         │
                         ▼
                  📡 Wi-Fi / Blynk
                         │
                         ▼
                  📱 Mobile Dashboard

        🌱 Hydroponic Phytoremediation
        💨 Aeration / Water Circulation
        🚧 Ultrasonic Obstacle Detection