#  Wi-Fi and Bluetooth Signal Tracker

A portable, custom-built RF signal scanner and power detector designed for knowing wireless signals, measuring signal strength and can be used to be safe. Built around the ESP32-C3 microcontroller and the AD8318 logarithmic RF power detector, this device provides real-time visual readings alongside multi-sensory (visual, audible, and tactile) feedback.

---

## Key Features

* **Core Processor:** ESP32-C3-WROOM-02 handling Wi-Fi/Bluetooth scanning, logic, and native USB programming.
* **RF Detection Engine:** AD8318 RF Power Detector module paired with an SMA antenna connector for precise wideband signal measurement.
* **Display:** 2.4-inch SPI TFT LCD (ILI9341) for live graphical signal readouts.
* **UI Controls:** EC11 Rotary Encoder with an integrated push button, expanded over I2C using a PCA9536 GPIO expander to free up MCU pins.
* **Multi-Sensory Alerts:**
  * **RGB LED:** Addressable WS2812B LED (Red = Strong, Yellow = Medium, Green = Weak).
  * **Audio:** Active piezo buzzer providing frequency-pitched sound feedback.
  * **Haptics:** Coin vibration motor driven by a low-side MOSFET.
  * **Flashlight:** Integrated 1W white LED powered directly from the battery line.
* **Power & Charging:**
  * Powered by a standard 3.7V Li-Po/Li-ion single cell.
  * Onboard USB-C port backed by an MCP73831 charger IC (set to 500mA).
  * AP2112K-3.3 (600mA) ultra-low-dropout regulator for stable logic power.
  * Dedicated slide switch for physical battery cut-off.
  * Resistor voltage divider network for monitoring battery percentage in real time.

---
## Bill of Materials (BOM) Summary

| Category | Component | Description / Footprint |
| :--- | :--- | :--- |
| **Microcontroller** | ESP32-C3-WROOM-02 | Main Wi-Fi/BLE MCU (`RF_Module:ESP32-C3-WROOM-02`) |
| **RF Detector** | AD8318 / U.FL Jack | RF Power Detector (`CSP-16` / `U.FL-R-SMT-1`) |
| **Power Management** | MCP73831 & AP2112K-3.3 | Li-Po Charger & 600mA LDO Regulator (`DFN-8` / `SOT-23-5`) |
| **Display** | 2.4" ILI9341 TFT | 320x240 SPI Screen Module Header (`1x14 2.54mm`) |
| **I2C Expander** | PCA9536D | 4-bit GPIO Expander for Encoder (`SOIC-8`) |
| **Input** | EC11 Encoder | Rotary Encoder with Switch (`RotaryEncoder_EC11E`) |
| **Lighting** | WS2812B & 1W White LED | RGB Status LED & Flashlight (`5050 SMD` / `3535 SMD`) |
| **Drivers** | AO3400A / 2N7002 | N-Channel MOSFETs (`SOT-23`) |
| **Passives** | Resistors / Capacitors | Standard 0805 SMD footprints |

## Tools Used

* **Design Software:** KiCad)
## schematics:
<img width="1097" height="765" alt="image" src="https://github.com/user-attachments/assets/6b4f247e-17f9-4d2f-95c8-479e1ef87bc0" />
## pcb:
<img width="261" height="508" alt="image" src="https://github.com/user-attachments/assets/905fd175-f3c0-477f-8f56-f08501816b44" />
