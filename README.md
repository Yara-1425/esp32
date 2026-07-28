
# ESP32 Web Server Servo & LED Control

An IoT project built using an **ESP32** microcontroller acting as a Wi-Fi Access Point (AP) to control a servo motor and status LEDs through a simple web interface.

---

##  Project Overview

This system allows a user to connect directly to the ESP32's Wi-Fi network (`ESP32_YARA`) and open a web control panel to:

* **Open Position:** Moves the servo motor to $180^\circ$, turns **ON** the Green LED, and turns **OFF** the Red LED.
* **Close Position:** Returns the servo motor to $0^\circ$, turns **OFF** the Green LED, and turns **ON** the Red LED.

---

## Components Used

* ESP32 Development Board
* Servo Motor
* Green LED & Red LED
* Resistors 
* Breadboard and Jumper Wires

---

##  Wiring Connections 

All components share a **common Ground (GND)** connected via the breadboard.

| Component | Pin Type | ESP32 GPIO / Rail Pin |
| --- | --- | --- |
| **Servo Motor** | Signal (Yellow) | **GPIO 15** |
|  | VCC (Red) | **5V** |
|  | GND (Brown) | **GND** (via Breadboard common rail) |
| **Green LED** | Anode (+) | **GPIO 16** (via resistor) |
|  | Cathode (-) | **GND** (via Breadboard common rail) |
| **Red LED** | Anode (+) | **GPIO 17** (via $220\Omega$ resistor) |
|  | Cathode (-) | **GND** (via Breadboard common rail) |

> **Note on Breadboard Ground:** All negative terminals (GND) of the servo motor and both LEDs are plugged into the same vertical common ground rail on the breadboard, which is linked directly to a single **GND** pin on the ESP32.

---

## Circuit Wiring Diagram

<img width="480" height="640" alt="WhatsApp Image 2026-07-29 at 12 24 07 AM" src="https://github.com/user-attachments/assets/60dfd0b6-b81f-42e5-b20a-e0e66325bc38" />


---

##  How to Run the Project

1. Open the code in **Arduino IDE** (ensure the ESP32 board package and `ESP32Servo` library are installed).
2. Upload the code to your ESP32 board.
3. Open the **Serial Monitor** (Baud rate: `115200`) to view the Access Point IP address.
4. Connect your phone or laptop to the Wi-Fi network:
* **SSID:** `ESP32_YARA`
* **Password:** `12345678`


5. Open your web browser and navigate to: `[http://192.168.4.1](http://192.168.4.1)`
6. Click **Open** or **Close** to control the hardware!

---

##  Demo
!(Demo.gif)
