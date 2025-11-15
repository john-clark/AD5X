# IFS Protocol Excel Document

_Found on telegram_

| COMMAND | RESULT | Input 1 | Output  1 | Output 2 |
| --- | --- | --- | --- | --- |
| F24 C2 | selecting the ifs channel, in this case 2 (clamping the filament) | F24 C2 \r\n | F24 ok. Chan 2. \r\n | F24 ok. FFS not ready. |
| F10 C4 L90 S300 | feed through channel 4 with a LENGTH of 90MM AND A SPEED of 300 (confirmed) | F10 C4 L90 S300 \r\n | F10 ok. FFS channel 4 feeding. \r\n |  |
| F11 C4 L70 S600 | pull the rod out of the 4 channel 70mm speed 600 (confirmed) | F11 C4 L70 S600 \r\n | F11 ok. FFS channel 4 exiting. \r\n |  |
| F39 C4 | loosening the pressure of the selected channel edge to make it easier for the head to pull | F39 C4 \r\n | F39 ok. FFS channel 4 release. \r\n |  |
| F23 C2 | UNKNOWN | F23 C2 \r\n | F23 ok. chan 1. \r\n | F23 ok. no chan. ( EVEN IF THE COMMAND WAS SENT WITHOUT AN ARGUMENT ) |
| F13 | survey of the current state of the ISF, not yet deciphered | F13 \r\n | F13 ok. FFS_state: 5 stateside: 9 chan: 4 ffs_channels_insert: 0 stall_state: 0 jinsi_GCONF: 000001dc qiehuan_GCONF: 000001dc vibr: 0 |  |
| F112 | UNKNOWN | F112 \r\n | F112 ok. \r\n |  |
| F19 | checking the IFS firmware | F19 \r\n | F19 ok. four color. version: 3.0.5 \r\n |  |
| F37 | It will outweigh the firmware update mode. |  |  |  |
|  |  |  |  |  |
| F45 | Something's wrong with the ifs drivers. |  | F45 ok.GSTAT: 00000000 \r\n | F45 ok.GSTAT: 00000001 \r\n |
| F44 | the status of the IFS steppers ? |  | F44 ok.DRV_STATUS: 00000000 \r\n (inserted 1 and 4) | F44 ok.DRV_STATUS: 80000000 \r\n (inserted rod 2) |
|  |  |  |  |  |
| F12 | ROD DETECTION | F12 \r\n | F12 ok. 1 0 0 0 пруток 1 обнаружен |  |
|  |  |  |  |  |
| F14 | UNKNOWN | F14 \r\n | F14 ok. stall: 0 0 0 0 |  |
| F15 | UNKNOWN | F15 \r\n | F15 ok. |  |
| F18 | general loosening of the clamp | F18 \r\n | F18 ok. |  |
| F20 | UNKNOWN | F20 \r\n | F20 ok. |  |
| F21 | Outputs data from the odometer | F21 \r\n| F21 ok. <br>silk: 405 1696 1634 1682 <br>stall: 2846 3294 3355 3317|  |
|  |  |  |  |  |
| F22 | checking for the presence of a bar but in human form | F22 \r\n | F22 ok. ffs_channels_insert: 1 |  |
| F23 C1 | UNKNOWN | F23 ok. chan 1. | F23 ok. no chan. (IF SENT WITHOUT AN ARGUMENT ) |  |
| F30 | UNKNOWN | F30 \r\n | F30 ok. |  |
| F40 | UNKNOWN | F40 \r\n | F40 ok.stall count: C1: 3 C2: 4 C3: 1 C4: 1 |  |
| F41 | UNKNOWN | F41 \r\n | F41 ok.GCONF: 000001dc |  |
| F42 | NOT implemented | F42 \r\n | F42 ok.stepper_motor: 0 stepper_motor_irun: 0 |  |
| F43 | UNKNOWN | F43 \r\n | F43 ok. |  |
| F50 | UNKNOWN | F50 \r\n | F50 ok.GCONF: 000001dc |  |
| F51 | UNKNOWN | F51 \r\n | F51 ok.GSTAT: 00000000 |  |
| F52 | UNKNOWN | F52 \r\n | F52 ok.CHOPCONF: 00000000 |  |
| F53 | UNKNOWN | F53 \r\n | F53 ok.DRV_STATUS: 80000000 |  |
| F60 | UNKNOWN | F60 \r\n | F60 ok.GCONF: 000001dc |  |
| F61 | UNKNOWN | F61 \r\n | F61 ok.GSTAT: 00000000 |  |
| F62 | UNKNOWN | F62 \r\n | F62 ok.CHOPCONF: 00000000 |  |
| F63 | UNKNOWN | F63 \r\n | F63 ok.DRV_STATUS: 00000000 |  |

### Notes:
- Protocol parameters
- Transmission Rate 115200
- transmissions 1 stop bit
- LSB Transmission Direction
- communication in 8-bit parcels
- Line communication
- Transmissions without no parity bit
- ttyS4 hardware
- In all transmissions there is a byte resolution of 0xFF that is sent from the host after 200ms...
