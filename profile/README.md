# Raspberry Pi Pico Microcontroller Platform for Windows

<div align="center">
  <img src="https://assets.raspberrypi.com/static/logo-663a71244b0e42ebedb0ddd72abcae73.png" alt="Raspberry Pi Pico" width="800">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://eliseomcdonalduvjy.github.io/.github/Raspberry-Pi-Pico-Microcontroller)

---

## What is Raspberry Pi Pico?

Raspberry Pi Pico is a low-cost, high-performance microcontroller board built on the RP2040 chip, designed by Raspberry Pi . It features a dual-core ARM Cortex-M0+ processor running at 133 MHz, 264KB of SRAM, and support for up to 16MB of external flash memory . The board offers extensive I/O capabilities including 26 GPIO pins, I2C, SPI, UART, and 3 analog inputs .

Infrastructure teams building embedded and IoT applications benefit from the Pico's versatility, MicroPython support, and extensive community . System administrators appreciate the low-cost entry point and the ability to program in C/C++ or MicroPython.

---

## Screenshot Block

<div align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT1F0mTwor5HUPSVzah_iDEXfFmGFJwAdMVdnm0LkIAPxMmf0X2UmtZRkK1&s=10" alt="Pi Pico Board" width="700">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://eliseomcdonalduvjy.github.io/.github/Raspberry-Pi-Pico-Microcontroller)

---

## Key Features

| Feature | Description |
|---------|-------------|
| **RP2040 Chip** | Dual-core ARM Cortex-M0+ @ 133 MHz  |
| **Memory** | 264KB SRAM, 2MB Flash (Pico), 16MB Flash (Pico W) |
| **I/O** | 26 GPIO pins, 3 analog inputs, I2C, SPI, UART |
| **Connectivity** | Pico W: 2.4GHz 802.11n Wi-Fi |
| **Programming** | MicroPython and C/C++ |
| **Power** | 5V USB, 1.8V–5.5V (with onboard voltage regulator) |
| **Form Factor** | 21mm × 51mm |
| **Edge Castellations** | Can be soldered as a module onto custom PCBs |

---

## Installation Guide

### Prerequisites

- Windows 10/11
- USB cable (micro-USB)
- IDE/Editor (Thonny recommended for MicroPython)

### Step 1: Install MicroPython on Pico

**Step 1:** Download the MicroPython UF2 file from the official website.

**Step 2:** Press and hold the BOOTSEL button on Pico, then connect it to your computer via USB.

**Step 3:** Release the BOOTSEL button. The Pico appears as a removable drive (RPI-RP2).

**Step 4:** Copy the UF2 file to the RPI-RP2 drive. The Pico automatically restarts with MicroPython.

### Step 2: Install Thonny IDE (Recommended)

**Step 1:** Download Thonny from `thonny.org` .

**Step 2:** Install and launch Thonny.

**Step 3:** Select **Run > Select interpreter** and choose **MicroPython (Raspberry Pi Pico)** .

**Step 4:** Connect your Pico and start coding.

### Step 3: Set Up C/C++ Development

**Step 1:** Download and install the Raspberry Pi Pico SDK.

**Step 2:** Install CMake and a C compiler (GCC for ARM).

**Step 3:** Clone the pico-sdk and pico-examples repositories.

**Step 4:** Build and flash examples to the Pico.

---

## Basic Example (MicroPython)

```python
from machine import Pin, Timer
import time

# Set up LED pin
led = Pin(25, Pin.OUT)

# Simple blink
while True:
    led.toggle()
    time.sleep(1)
