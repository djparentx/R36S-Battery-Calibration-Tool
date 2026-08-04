[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/O8Z424G15Y)

# R36S Battery Calibration Tool
v1.3 by djparent

---

## Overview

The **R36S Battery Calibration Tool** is a complete battery profiling and correction utility for the R36S handheld.  
It records real battery discharge data, builds a custom battery curve, and improves percentage accuracy across the full charge range.

This tool helps replace unreliable stock battery readings with a calibrated profile based on your actual device.

---

## Features

- Self updates to latest GitHub release
- Full battery discharge logging
- Automatic curve generation from recorded data
- Multi-session averaging for improved accuracy
- Custom curve import/export support
- Live corrected battery percentage service
- Session quality checks and outlier detection
- Supports multiple system languages
- Safe uninstall with stock behavior restore

---

## How It Works

The tool monitors battery voltage during a full discharge cycle, then uses that data to create a corrected battery percentage curve.

Once applied, the included background service updates battery readings in real time using your calibrated profile.

---

## Basic Instructions Summary

1. Fully charge the device while powered off.
2. Start a new calibration session from the tool.
3. Use the device normally until it shuts off.
4. Recharge to full.
5. Apply the recorded session data.
6. Enable the calibration service.

For better accuracy, repeat the process multiple times and use the averaging feature.
### OPEN THE SCRIPT IN A TEXT READER TO VIEW FULL INSTRUCTIONS

---

## Recommended Setup

- Turn **WiFi** and **Bluetooth** off
- Avoid charging during calibration
- Do not power off or use sleep mode
- Keep device at normal temperature
- Use screensaver/video playback for steady drain

---

## Files & Locations

### System Files

- `/etc/systemd/system/battery-cal.service`
- `/usr/local/bin/battery-cal-daemon.sh`
- `/usr/local/etc/battery-cal/curve.conf`
- `/usr/local/etc/battery-cal/session.csv`

### Exported User Data

- `/roms/battery_data/session#.csv`
- `/roms/battery_data/average.csv`
- `/roms/battery_data/average.log`
- `/roms/battery_data/custom.csv`

---

## Menu Functions

### Calibrate Battery

- Start new calibration
- Apply current session
- Apply exported session
- Apply calculated average
- Apply custom curve
- Export session data

### View Battery Curve

- Compare stock vs corrected curve
- Export active curve for editing

### Service Control

- Enable / Disable live battery correction service

---

## Multiple Sessions

Running more than one session improves accuracy.

- **3 sessions** = better results  
- **5 sessions** = best results  

Use **Create Session Average** to combine valid samples into a stronger battery profile.

---

## Custom Curve Editing

You can export the active curve to `custom.csv`, edit it manually in a spreadsheet or text editor, then re-import it through the tool.

This allows fine-tuning or correcting specific battery percentages.

---

## Uninstall

The uninstall option removes:

- calibration service
- daemon script
- curve data
- session logs
- temporary files

Stock battery behavior is restored automatically.

---

## Notes

This tool is designed specifically for handheld battery correction and long-term accuracy improvements.

Calibration takes several hours, but once complete, it provides far more reliable battery reporting than stock settings.

---

## License

MIT License

---

Created by **djparent**  
Based on live battery calibration principles for handheld Linux devices.
