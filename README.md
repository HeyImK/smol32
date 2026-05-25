# smol32
# CH32V006 Minimalist Dev Board

A small and powerful mini dev-board powered by a WCH CH32V006F8P6, and also integrates a WS2812B Neopixel.

---

## Pictures

| Top View | Bottom View |
| :---: | :---: |
| ![Board Front](Images/smol32.png) | ![Board Back](Images/smol32.png) |

---

## Features

* **Core MCU:** CH32V006F8P6 RISC-V processor running up to 24MHz and with 8KB Ram
* **Power Interface:** Native USB-C connector wired for **Power Only** 
* **Onboard NeoPixel:** A single integrated **WS2812B RGB Smart LED** 
* **Tactile Controls:** Dedicated onboard **Reset (RST)** and **Bootloader (BOOT)** hardware buttons.
* **1-Wire Debugging:** Breaks out WCH's proprietary 1-wire Serial Debug Interface (SDI) and NRST for programming via other micrcontrollers running ardulink.

---

## Pinout Configuration

The board breaks out all 20 physical MCU pins directly into standard 2.54mm (0.1") male headers. The functional internal allocations are mapped below:

### Dedicated Infrastructure Pins
* **Pin 1 (PD4):** Dedicated Bootloader Mode Button (Pulls to GND)
* **Pin 4 (PD7):** Dedicated Hardware Reset Button (Pulls to GND) & Debug Header Link
* **Pin 7 (VSS):** Ground Plane
* **Pin 9 (VDD):** 3.3V Regulated System Voltage (via XC6206 LDO)
* **Pin 10 (PC0):** WS2812B NeoPixel Data In 
* **Pin 18 (PD1):** Single-Wire Debug Interface (`SWIO` Data Stream)

### Available General Purpose IO Pool (14 Pins Free)
The remaining **14 pins** are broken out completely unassigned for breadboard prototyping, supporting standard digital IO, ADC analog inputs, UART serial communications, or SPI peripherals.
