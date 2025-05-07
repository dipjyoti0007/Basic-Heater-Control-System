🔥 Heater Control System with State Machine using ESP32
This project simulates a smart heater control system built on the ESP32 platform, designed to manage temperature levels efficiently using real-time sensor feedback and state-based logic. It uses a DHT22 sensor to monitor temperature and humidity, and actuates a heater, fan, and buzzer accordingly, while displaying the system state on a 16x4 I2C LCD display.



🚀 Features

-- Real-time temperature and humidity monitoring using DHT22

-- Heater and fan control based on temperature thresholds

-- State-based logic system:

---- IDLE: System inactive

---- HEATING: Temperature below target

---- STABILIZING: Approaching target

---- TARGET_REACHED: Desired temperature maintained

---- OVERHEAT: Safety shutdown with fan & buzzer alert

-- Visual feedback on LCD and Serial Monitor

-- Auditory alert via active buzzer on overheat

-- Simulation-ready using Wokwi for virtual testing



🧰 Hardware Components

- ESP32 Dev Board

- DHT22 Temperature and Humidity Sensor

- I2C 16x4 LCD

- Active Buzzer

- 2× relays (to simulate fan and heater)



🔄 Operation

* Continuously reads temperature and humidity every second.

* Based on temperature, the system transitions through five states using a finite state machine (FSM).

* The LCD displays current temperature, humidity, heater/fan status, and active state.

* An overheat condition (>35°C) triggers a buzzer and fan for safety.
