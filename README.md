# Rocket Telemetry & Flight Data System 🚀

An embedded systems and telemetry software architecture designed for flight data acquisition, real-time control, and telemetry visualization. Developed as a Senior Capstone Project at Fayetteville State University.

## 🛠️ System Architecture & Technology Stack

The project utilizes a multi-node wireless network over Bluetooth Low Energy (BLE) to orchestrate data collection and mechanical actuation:

*   **Hardware Ecosystem:**
    *   `1x Arduino Nano 33 BLE Sense`: Positioned on the water rocket payload to aggregate sensor data.
    *   `1x Arduino Nano 33 BLE`: Configured as the central controller to actuate physical servos.
    *   `1x Arduino Nano 33 BLE`: Dedicated to managing real-time data streaming between the central controller and the peripheral flight node.
*   **Software & Data Engineering:**
    *   **Firmware:** C++ / Arduino embedded programming (`.ino`) implementing BLE communication protocols.
    *   **Data Acquisition:** Real-time logging of IMU and environmental telemetry, including **Acceleration, Gyroscope, Magnetometer, and Altitude**.
    *   **Dashboard & Visualization:** Python application featuring a custom graphical user interface built with **PyQt5** and dynamic telemetry data graphing leveraging **Matplotlib**.

---

## 🚀 Installation & Execution Guide

Follow these steps to set up the local environment and run the telemetry dashboard.

### 1. Prerequisites & Environment Setup
Ensure you have Python 3.8+ installed on your system. Clone the repository and navigate to the project directory:

```bash
git clone https://github.com
cd rocket-telemetry-system
```

### 2. Install Dependencies
Install all required packages instantly using the project's dependency manifest:

```bash
pip install -r requirements.txt
```

### 3. Running the Telemetry Dashboard
Launch the main Python interface to begin monitoring the flight data visualizations:

```bash
python uiDesign.py
```

### 🔌 Firmware Deployment (Embedded Hardware)
* Open `RocketFlight_central.ino` and `RocketFlight_peripheral.ino` using the Arduino IDE.
* Install the `ArduinoBLE` library via the Library Manager.
* Compile and flash the respective files to your **Arduino Nano 33 BLE** boards to initiate node-to-node wireless communications.

---

## 👥 Engineering Team & Academic Supervision

*   **Developers:** Jean Paul Fermaint, Christian Torres
*   **Class Professor:** Dr. Jin
*   **Project Advisor:** Professor Joe Kabbes
*   **Timeline:** Fall 2021
