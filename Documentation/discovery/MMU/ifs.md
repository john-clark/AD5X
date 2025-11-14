## **Flashforge AD5X Intelligent Filament Switcher (IFS) Board – FPP0302 Main Board v1.0.4**

**Board Marking:** `FPP0302 Main Board v1.0.4`

**Date code:** `2021-08-05`

**Form factor:** 85 × 45 mm 2-layer PCB

**Function:** Manages multi-filament routing and detection for the AD5X printer.


## **Key Components & Markings**

###  Main Controller – Nuvoton N32G455REL7 (U5, back side)

* 32-bit **ARM Cortex-M4** microcontroller, comparable to STM32F4-series parts.
* 128 KB Flash, 32 KB SRAM, up to 96 MHz core clock.
* Handles:
  * Filament sensor monitoring and switching logic.
  * Communication with the printer’s mainboard via RS-485.
  * Motor or actuator control for channel switching.

###  RS-485 Communication Interface – “RS485-IN” port (front, top-right)

* 4-pin JST-XH-style connector for the cable to the **main printer board** .
* The **4-wire harness** going to the main board carries:
  * **VCC** (5 V or 24 V power input)
  * **GND**
  * **D+ / D–** (differential data pair, RS-485 standard)
* Provides robust half-duplex serial communications between the IFS and the printer mainboard.

- Suggests that the printer’s mainboard communicates with the IFS via a **robust, differential serial protocol**, not standard USB.

#### RS-485 Transceiver – GateMod GM05GE 4254I (U2, lower-left)

* Converts UART logic from the MCU to differential RS-485.
* Enables long cable runs and noise immunity between boards.
* Works in tandem with the Nuvoton MCU’s UART interface.

#### 🔌 Peripheral Connectors (front, upper half)

* **SILK1 – SILK5** : Local sensor and filament channel interfaces.

  Each likely corresponds to an optical or mechanical filament sensor or motor driver channel.
* **TMS / Zero-CHK / 2Wire** : Internal diagnostics or expansion test headers.

  * "TMS"
  * “Zero-CHK” likely references a **zero-position sensor** or home switch input.
  * “2Wire” may refer to an I²C or simple digital sensor line.
* **A / B headers (right edge)** : stepper driver for selecting filament channels.

###  Local Power Regulation (front, bottom-center)

* Switching regulator with coil labeled **L8 = 100** and diodes/caps cluster (C12–C17).
* Provides 5 V → 3.3 V regulation for the MCU and transceivers.
* Bulk electrolytic and ceramic caps ensure stable logic supply.

#### **Driver Section (R60–R66 area)**

- Cluster of resistors and decoupling capacitors forming part of the **power and driver stage**.
- Suggests some level of current control or protection for switching elements or motors

#### Driver or Multiplexer ICs – MS355776 JCGDE9E (U3, U4, back side)

* Two identical chips positioned symmetrically on the back side (likely **motor drivers**, **analog switches**, or **MOSFET arrays**).
  * Functions could include:
    * Stepper or DC motor control for filament feed paths.
    * Switching multiple filament sensor lines.
    * Possibly multiplexing signals to support multiple filament channels.

---

### **Board Communication Path**


| Link                         | Connector                 | Signaling                       | Function                                    |
| ------------------------------ | --------------------------- | --------------------------------- | --------------------------------------------- |
| To Main Printer Board        | 4-pin “RS485-IN”        | RS-485 (Differential UART)      | Command/control interface to AD5X mainboard |
| To Local Sensors / Actuators | SILK1–SILK5, A/B headers | GPIO / PWM / I²C (3.3 V logic) | Filament sensor inputs & driver outputs     |
| Debug / Test                 | TMS, Zero-CHK, 2Wire      | Internal                        | Factory programming & calibration           |


## Possible Alternatives

- **Seleadlab MMX Multi Material Extruder Full Kit Multi Material MMU 3D Printer for Voron2.4 Trident** Original to the Low Rider

  - [AliExpress](https://www.aliexpress.us/item/3256808621305078.html) 
  - [Printables](https://www.printables.com/model/1181017-mmx-multi-material-extruder-exclusive-final-releas)
  - [gist](https://gist.github.com/StefanKruk/24bad4b4887b5f01f8370a23bd7d6597)

- **Multi-Material Upgrade Unit for Klipper & Voron 3D Printers – Blurolls Low Rider MMU Easy Install Compact Design Open Source**

  - [AliExpress](https://www.aliexpress.us/item/3256809802160419.html)
  - [Printables](https://www.printables.com/model/1314513-low-rider-mmu-for-any-klipper-printer)

- **BLV AMS BMCU 370X BMCU 370C Open source AMS MMU solutions AMS lite 370 130 BMCU370 support Auto Refill Farm**

  - [AliExpress](https://www.aliexpress.us/item/3256808814657000.html)
  - [Github](https://github.com/nozzlenaut/BMCU/tree/main)
  - [Makerworld](https://makerworld.com/en/models/1088880-bmcu-v2-5-for-personal-use#profileId-1081967)

- Pico MMU

  - [Makerworld](https://makerworld.com/en/models/1636170-mmu-multi-material-upgrade-diy#profileId-1728491)
  - [Github](https://github.com/lhndo/LH-Stinger/wiki/Pico-MMU)