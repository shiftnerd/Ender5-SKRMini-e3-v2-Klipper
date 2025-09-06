# Ender 5 (Late 2020) – SKR Mini E3 V2 Klipper Config & Firmware

This repository contains a working `.cfg` and `.bin` for running **Klipper** on a late-2020 **Creality Ender 5** equipped with a **BIGTREETECH SKR Mini E3 V2** mainboard.  
The printer is otherwise stock (no aftermarket extruder, hotend, or frame modifications).

## Contents
- `printer.cfg` – tuned Klipper configuration for Ender 5 + SKR Mini E3 V2  
- `firmware.bin` – compiled Klipper firmware for SKR Mini E3 V2

## Hardware Setup
- **Printer**: Creality Ender 5 (late 2020 production)  
- **Mainboard**: BIGTREETECH SKR Mini E3 V2  
- **Stepper Drivers**: TMC2209 (onboard)  
- **Stock Components**: Hotend, extruder, bed, Z assembly, wiring harness

## Features
- Correct **rotation_distance** for stock X/Y/Z axes and extruder  
- Basic **pressure advance** and **input shaper** values that worked well on this machine  
- Safe homing and bed mesh probing enabled  
- Pre-mapped pins for the SKR Mini E3 V2 board

## Usage

1. **Flash the firmware**  
   - Copy `firmware.bin` onto a microSD card.  
   - Insert into the SKR Mini E3 V2 and reboot the printer.  
   - The board should automatically flash the firmware.  

2. **Install the config**  
   - Copy `printer.cfg` to your Klipper config directory (typically `/home/pi/printer.cfg` on a Raspberry Pi).  
   - Restart Klipper (`sudo service klipper restart` or via Mainsail/Fluidd).  

3. **Fine-tune**  
   - Verify endstop positions and adjust if your machine differs.  
   - Re-calibrate pressure advance and input shaper for your filament and speeds.  
   - Double-check thermistor and probe settings if you’ve swapped parts.  

⚠️ **Note:** This configuration is specific to **my late-2020 Ender 5**. Even with the same hardware, tolerances vary. Always verify limits before running high-speed moves.

## Disclaimer
These files are provided **as-is**, with no guarantee they will work for every Ender 5 / SKR Mini E3 V2 setup. Flashing firmware and using custom configs always carries some risk—make backups and proceed carefully.

## License
MIT License – feel free to fork, adapt, and share.
