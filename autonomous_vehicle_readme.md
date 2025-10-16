# Autonomous Vehicle Enhancement Project
**Platform: NXP RDDRONE-FMUK66 Based Autonomous Vehicle**

## Project Overview
This project extends the capabilities of an existing line-following autonomous vehicle by implementing advanced sensor integration, wireless debugging capabilities, and manual control features. The core focus lies in optimizing vehicle performance through real-time telemetry and enhancing development workflow through robust communication protocols.

## Key Objectives

### 1. **Optical RPM Sensor Integration**
Implementation of wheel speed monitoring through optical encoders to enable closed-loop motor control. This sensor data will interface with the FMUK66 board via GPIO interrupts, providing real-time rotational feedback for precise speed regulation and slip detection.

### 2. **Adaptive Power Management System**
Development of an intelligent motor throughput compensation algorithm that correlates RPM data with power consumption metrics. This system will dynamically adjust PWM signals to maintain consistent vehicle performance despite battery voltage drop, ensuring stable operation throughout the discharge cycle.

### 3. **Wireless Debug Interface**
Establishment of a wireless communication link (via UART-to-WiFi or Bluetooth module) for remote debugging and real-time telemetry monitoring. This interface will enable live parameter tuning of the PID controller, FSM state visualization, and sensor data streaming without physical connection constraints.

### 4. **Joystick Control Interface**
Integration of a wireless gamepad/joystick controller for manual override and testing capabilities. The control signals will be transmitted through a dedicated wireless protocol (2.4GHz RF or Bluetooth), allowing seamless switching between autonomous and manual operation modes.

### 5. **Enhanced Multi-Protocol Communication Architecture**
Optimization of the existing communication framework that manages:
- **I2C** protocol for Pixy2 camera vision data at 400kHz
- **GPIO** interrupts for ultrasonic sensor distance measurements and RPM sensor pulse counting
- **PWM** signal generation for servo steering control and motor speed regulation
- **UART/SPI** for wireless module integration

### 6. **Real-Time Telemetry Dashboard**
Development of a monitoring system that aggregates sensor data from all communication channels (camera tracking deviation, ultrasonic distance, wheel RPM, battery voltage) and transmits it via the wireless interface for comprehensive vehicle state analysis.

### 7. **Robust Protocol Error Handling**
Implementation of communication fault tolerance mechanisms including timeout detection, data validation checksums, and automatic reconnection procedures for wireless links, ensuring reliable operation in electromagnetically noisy environments.