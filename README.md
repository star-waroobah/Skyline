# Skyline

[![View PCB on KiCanvas](https://hack.club/pcb-badge)](https://kicanvas.org/?repo=https://github.com/<OWNER>/<REPOSITORY>/tree/main/pcb)

<img width="873" height="882" alt="Screenshot 2026-11-08 231744" src="https://github.com/user-attachments/assets/a5ec6f88-d9d3-4cd6-86ec-57d8bf569733" />


Skyline is a custom flight controller for a quadcopter drone using the STM32F722 microcontroller. It will act as the brain of the drone.

I made this as the half life week 5 project.

## Features

- **STM32F722RET6 MCU** with 25 MHz and 32.768 kHz crystals, plus reset and boot buttons
- **USB-C port** for power and programming
- **4 motor outputs** (PA0–PA3) through one 8-pin 4-in-1 ESC header
- **Receiver header** (UART, 3.3 V) for ELRS or similar radios
- **Battery voltage monitoring**, with the divider sized for a 4S battery
- **SWD header** as a backup way to flash firmware
- **Plug-in IMU (SPI) and barometer (I2C) headers** for breakout boards
- **microSD slot** for flight logging
- **Dual power input:** two SS34 diodes let the board run from USB or the battery
- **LMR51430 3.3 V buck regulator** that accepts up to 36 V in
- **Hand-solderable:** 0603 and 0805 parts and 2.54 mm headers


## How it works

It uses an IMU sensor to detect movement and orientation and a barometer to estimate altitude. The board receive commands from a radio receiver and send signals to four ESCs to control the motors and help keep the drone stable. It also have USB-C for connectivity, a microSD card for flight data logging, and battery voltage monitoring. 

## PCB
<img width="1920" height="1080" alt="Screenshot (659)" src="https://github.com/user-attachments/assets/b6b9c9fa-3760-418e-977d-30829305ade8" />

## Schematic
<img width="1153" height="785" alt="Screenshot 2026-11-07 173534" src="https://github.com/user-attachments/assets/a7c43781-a92b-4112-8adb-5dd3271175a4" />

## 3D View
<img width="873" height="882" alt="Screenshot 2026-11-08 231744" src="https://github.com/user-attachments/assets/066e4bcd-c03f-42a9-8553-575df7809e04" />
<img width="828" height="888" alt="Screenshot 2026-11-08 231801" src="https://github.com/user-attachments/assets/8d121ca3-fd18-445c-aca2-c64af9d6b551" />

## Bill of Materials

Full BOM: [`hardware/BOM.csv`](hardware/BOM.csv)

| Part | Qty | Notes |
|------|-----|-------|
| [Microcontroller] | 1 | |
| [IMU / sensor] | 1 | |
| [Motors] | 4 | |
| [ESCs / motor drivers] | 4 | |
| [Battery] | 1 | |
| [Frame] | 1 | |

## Credits

- Symbols and footprints from EasyKiCad2 / EasyEDA converted libraries (included in `hardware/`).
- I also took guidance from the Hack Club guide (https://blueprint.hackclub.com/starter-projects/flightcontroller)
