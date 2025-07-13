# 🔥 Smart Heater Control System using ESP32 🌡️💨
*Project for upliance.ai (https://upliance.ai/?srsltid=AfmBOoqaXwpgha1sDLENXtZ07TLbJTEJi1c0p-KKkMcSN8Pf2yfajjCP)*  

> ⚙️ **Intelligent, safety-first heater controller** built using the ESP32 platform, integrating **real-time sensor feedback** and **finite state machine (FSM)** logic for smart temperature management.  
> Simulate easily on **Wokwi** or deploy with real hardware. 🧠🔧

---

## 🚀 Features At a Glance

✅ **Real-time** temperature & humidity monitoring via **DHT22**  
🔥 **Heater & Fan Control** based on dynamic thresholds  
🧠 **State Machine Logic** with 5 operational modes  
📺 **LCD Display (I2C 16x4)** for live feedback  
🔊 **Auditory Alerts** using active buzzer in OVERHEAT state  
💻 Output to **Serial Monitor** for debugging  
🧪 **Simulation-ready** via [Wokwi](https://wokwi.com/)

---

## 🎯 System States

| 💡 State Name     | 🔍 Description                                          |
|------------------|---------------------------------------------------------|
| 💤 **IDLE**        | System waiting, no heater/fan activity                 |
| 🔥 **HEATING**     | Temperature below threshold — heater is ON             |
| 🟡 **STABILIZING** | Near target temp — heater cycles to stabilize          |
| ✅ **TARGET_REACHED** | Desired temp reached — heater/fan OFF                |
| 🚨 **OVERHEAT**    | Temp > 35°C — activates fan & buzzer for safety       |

> FSM transitions ensure smooth and intelligent state changes based on environment conditions.

---

## 🧰 Required Components

| 🧩 Component                 | 🔎 Purpose                                  |
|-----------------------------|---------------------------------------------|
| 🧠 **ESP32 Dev Board**        | Central microcontroller                     |
| 🌡️ **DHT22 Sensor**           | Measures temp & humidity                    |
| 📺 **16x4 I2C LCD**           | Displays current readings & system state    |
| 🔊 **Active Buzzer**          | Beeps on overheat                           |
| ⚙️ **Relay Modules x2**       | Simulates heater and fan control            |

---

## 🔄 How It Works

1. 📥 **Sensor Reading**  
   Reads temp & humidity every 1 second.

2. 🧠 **State Evaluation (FSM)**  
   Determines which state the system should be in:
   - `IDLE` → `HEATING` → `STABILIZING` → `TARGET_REACHED` → `OVERHEAT`

3. 🔁 **Actuation**  
   - 🔥 **Heater ON** if temp < lower limit  
   - 💨 **Fan ON + Buzzer** if temp > 35°C  
   - ✅ All OFF when in target range

4. 📺 **LCD & Serial Output**  
   - Live temperature, humidity, state, and actuator status

---

## 📊 LCD Display Layout

| Temp: 28.4°C Hum: 55% |
| State: HEATING |
| Heater: ON Fan: OFF |
| Buzzer: OFF |


---

## 🔬 Simulation Ready
 
🧪 Perfect for testing, debugging, or demo presentations for real system development.

---

## 🧠 Applications

- 🏠 Smart home heater automation  
- 🧪 Lab incubator monitoring  
- 🌡️ Climate-controlled storage rooms  
- 🎓 Educational FSM projects using ESP32

---
