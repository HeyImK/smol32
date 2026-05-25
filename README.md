# smol32
# CH32V006 Minimalist Dev Board

A sleek, ultra-minimal, and breadboard-compatible development board built around the **WCH CH32V006F8P6** (TSSOP-20) RISC-V microcontroller. Designed to be routed, reviewed, and ready for production in a single evening.

---

## 📸 Hardware Preview

| Top View (3D Render) | Bottom View (3D Render) |
| :---: | :---: |
| ![Board Front](Documentation/3D_Board_Front.png) | ![Board Back](Documentation/3D_Board_Back.png) |

---

## ✨ Features

* **Core MCU:** CH32V006F8P6 RISC-V processor running up to 24MHz (utilizing the factory-trimmed internal RC oscillator for zero external component overhead).
* **Breadboard Friendly:** Slim "DIP-20" footprint spanning exactly **0.6 inches** across the center breadboard trench, leaving two rows free on either side for fast jumper wiring.
* **Power Interface:** Native USB-C connector wired for **Power Only** (includes $5.1\text{ k}\Omega$ CC pulldowns for compatibility with modern Type-C chargers).
* **Onboard NeoPixel:** A single integrated **WS2812B RGB Smart LED** powered directly by the 5V USB rail, protected with an inline $330\text{ }\Omega$ data resistor.
* **Tactile Controls:** Dedicated onboard **Reset (RST)** and **Bootloader (BOOT)** hardware buttons for quick prototyping control loops.
* **1-Wire Debugging:** Breaks out WCH's proprietary 1-wire Serial Debug Interface (SDI) alongside hardware reset to interface flawlessly with low-cost programmers or external microcontrollers running `Ardulink`.

---

## 🎛️ Pinout Configuration

The board breaks out all 20 physical MCU pins directly into standard 2.54mm (0.1") male headers. The functional internal allocations are mapped below:

### Dedicated Infrastructure Pins
* **Pin 1 (PD4):** Dedicated Bootloader Mode Button (Pulls to GND)
* **Pin 4 (PD7):** Dedicated Hardware Reset Button (Pulls to GND) & Debug Header Link
* **Pin 7 (VSS):** Ground Plane
* **Pin 9 (VDD):** 3.3V Regulated System Voltage (via XC6206 LDO)
* **Pin 10 (PC0):** WS2812B NeoPixel Data In (`RGBLD` via $330\text{ }\Omega$ resistor)
* **Pin 18 (PD1):** Single-Wire Debug Interface (`SWIO` Data Stream)

### Available General Purpose IO Pool (14 Pins Free)
The remaining **14 pins** are broken out completely unassigned for breadboard prototyping, supporting standard digital IO, ADC analog inputs, UART serial communications, or SPI peripherals.
