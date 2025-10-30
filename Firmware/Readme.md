> [!Important]
> This is a **_Unofficial_** mirror the official firmware releases for the AD5X

# Official Links

- [AD5X Download Center](https://www.flashforge.com/blogs/download-document/ad5x)
- [AD5X Wiki](https://wiki.flashforge.com/en/ad5x)

# How to Update Firmware

- [OTA (Over the Air) _or internet update_](https://wiki.flashforge.com/en/ad5x/manual/firmware_upgrade)
- [USB update: Youtube vdeo](https://www.youtube.com/watch?v=7ZL3QakQhYw)



# Firmware releases

- [Firmware_1.1.7-1.1.0](AD5X-1.1.7-1.1.0-3.0.6-20250912-Factory.tgz)
- [Firmware_1.1.6-1.1.0](AD5X-1.1.6-1.1.0-3.0.6-20250729.tgz)
- [Firmware_1.1.5-1.0.9](AD5X-1.1.5-1.0.9-3.0.6-20250718-Factory)
- [Firmware_1.1.3-1.0.8](AD5X-1.1.3-1.0.8-3.0.6-20250705-Factory)
- [Firmware_1.1.1-1.0.7](AD5X-1.1.1-1.0.7-3.0.6-20250612.tgz)
- [Firmware_1.1.0-1.0.7](AD5X-1.1.0-1.0.7-20250517.tgz) _(Note the wrong version on link on official download page filename is correct)_
- [Firmware_1.0.9-1.0.6](AD5X-1.0.9-1.0.6-20250424.tgz)
- [Firmware_1.0.8-1.0.5](AD5X-1.0.8-1.0.5-20250418.tgz)
- [Firmware_1.0.7-1.0.3](AD5X-1.0.7-1.0.3-20250408.tgz)
- [Firmware_1.0.5-1.0.3](AD5X-1.0.5-1.0.3-20250402.tgz)
- [Firmware_1.0.4-1.0.3](AD5X-1.0.4-1.0.3-20250318.tgz)
- [Firmware_1.0.2-1.0.2](AD5X-1.0.2-1.0.2-20250120.tgz)

# Firmware Release Note

[Official AD5X Firmware Release History](https://wiki.flashforge.com/en/ad5x/manual/firmware_release_history)

### AD5X-1.1.6-1.1.0-3.0.6-20250729

#### New Features:

1. Added automatic NIM log cleanup on startup.

#### Bug Fixes and Performance Enhancements:

1. Refined error codes.

2. Updated extruder board MCU program.

### AD5X-1.1.5-1.0.9-3.0.6-20250718

#### New Features:

1. Added Turkish translation.

2. Added configuration file backup feature.

3. Updated library files.

4. Added extruder control to the manual control page.

#### Bug Fixes and Performance Enhancements:

1. Fixed the translation of the prompt displayed when material info is incorrect on the print preview page.

2. Added a waiting prompt when switching from Wi-Fi to Ethernet.

3. Fixed an issue where remote slicing remained offline after network changes.

4. Removed hardware timer

5. Fixed other known bugs.

### AD5X-1.1.3-1.0.7-3.0.6-20250702

#### Bug Fixes and Performance Enhancements:

1. Fixed interface freezing issue.

2. Fixed abnormal filament extrusion when enabling leveling before printing.

3. Optimized the leveling function.

4. Adjusted Z-axis motor current to 0.9.

5. Fixed the issue where the pause button displayed incorrectly after auto filament loading/unloading timeout.

### AD5X-1.1.1-1.0.7-3.0.6-20250612

#### New Features:

1. Added Exclude objects feature.

#### Bug Fixes and Performance Enhancements:

1. Updated translations on the status page.

2. Optimized the power loss recovery feature.

3. Added Z offset display on the status page.

4. Fixed several bugs.

### AD5X-1.1.0-1.0.7-20250517

#### New Features:

1. Automatically release the E motor during printing pauses.

2. Automatically release the X, Y, Z, and E motors upon print cancellation or completion.

3. Upon printing pause initiation, the extruder fan activates, wait for 4 seconds, and the fan automatically deactivates when the pause action is completed.

#### Bug Fixes and Performance Enhancements:

1. Optimize power loss recovery.

2. Fix several bugs.

### AD5X-1.0.9-1.0.6-20250424

#### New Features:

1. Add the function to retry MCU upgrade via USB after a failure.

#### Bug Fixes and Performance Enhancements:

1. Change the movement mode when cutting filament.

2. Increase the line thickness for filament status display in the material station.

3. Fix the issue caused by selecting the wrong channel.

4. Adjust Z-offset value during printing: change the unit from 0.025 to 0.01.

5. Add a control switch for the odometer roller.

6. Change the prompt for factory reset.

7. Disable motion and filament-change functions during printing.

### AD5X-1.0.7-1.0.3-20250408

#### Bug Fixes and Performance Enhancements:

1. Fix the odometer roller false error reporting issue

### AD5X-1.0.5-1.0.3-20250402

#### Bug Fixes and Performance Enhancements:

1. Remove the automatic clearing of the Z-offset value when leveling.

2. Optimize the leveling logic during the startup guide.

3. Fix the issue where the filament unloading timeout warning occasionally appears after power loss recovery during filament change.

4. Update the print model used in the startup guide.

5. Improve the accuracy of odometer roller error reporting.

6. Modify the filament retraction length to 100mm for all four channels after power loss recovery during filament change.

### AD5X-1.0.4-1.0.3-20250317

#### New Features:

1. Add compatibility for slicing T0-T15 channels.

2. Add channel display for auto loading.  

3. Add channel display for auto loading. 

Bug Fixes and Performance Enhancements:

1. Optimize pre-leveling preparation actions. 

2. Fix several bugs.

### AD5X-1.0.2-1.0.2-20250120

#### New Features:

 1. First release
