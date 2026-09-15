# NRSuite (App Edition)

> This is still on developement, for the meantime you can check the termux version here: https://github.com/7wp81x/NRsuite

Turn a $3 ESP32 into a wireless security research toolkit for your Android phone. No root required.

![Platform](https://img.shields.io/badge/platform-Android-green.svg)
![ESP32](https://img.shields.io/badge/chip-ESP32--C3%20%7C%20S3%20%7C%20S2-orange.svg)
![No Root](https://img.shields.io/badge/root-not%20required-brightgreen.svg)

NRSuite pairs an ESP32 microcontroller (connected over USB-OTG) with an Android app, offloading the radio layer to the ESP32 so a stock, unrooted phone can be used as a wireless research toolkit. This repository hosts release builds only — the app's source is closed.

> **Authorized use only.** Only use this on networks and devices you own or have explicit written permission to test. Unauthorized interception of network traffic or disruption of network communications is illegal in most jurisdictions.

## What it does

- **Wi-Fi scanning** — SSID, BSSID, channel, RSSI, security type
- **Packet sniffing** — fixed-channel or channel-hopping promiscuous capture, `.pcap` export, live streaming
- **EAPOL / handshake capture** — passive capture with optional BSSID/client filtering
- **Deauthentication testing** — standalone, or combined with sniffing to trigger and capture a handshake
- **Captive portal / AP mode** — custom SSID, channel, and HTML page
- **BLE & USB HID emulation (BadBLE / BadUSB)** — scripted keystroke injection against a paired host
- **USB mass storage bridge** — read/write/delete files on the ESP32's onboard flash
- **Beacon broadcasting** — custom/hidden SSIDs, fixed channel, stable or random BSSIDs
- **Multi-device support** — switch between several connected boards

## Requirements

- Android phone with USB-OTG support (no root needed)
- Supported ESP32 board: C3, S3, S2, or classic WROOM-32 devkit
- USB-OTG cable
- NRSuite firmware flashed to the board (see [Releases](../../releases))

## Installation

1. Download the latest APK from the [Releases](../../releases) page.
2. Flash the matching firmware build to your ESP32 (instructions included in the release notes).
3. Install the APK and grant USB permission when prompted on first connect.
4. Plug in your ESP32 via OTG cable and open the app.

## Supported hardware

| Board | Wi-Fi | BLE HID | USB Mass Storage / BadUSB |
|---|:---:|:---:|:---:|
| ESP32-C3 | ✅ | ✅ | ❌ (no USB-OTG) |
| ESP32-S3 | ✅ | ✅ | ✅ |
| ESP32-S2 | ✅ | ❌ (no BT radio) | ✅ |
| Classic ESP32 devkit | ✅ | ✅ | ❌ (no USB-OTG) |

## Legal

This app is intended for authorized security research, penetration testing on infrastructure you own or are explicitly contracted to test, and educational use only. Deauthentication, packet injection, rogue AP, and HID-injection features can disrupt networks or compromise devices if misused — doing so without authorization is a criminal offense in many jurisdictions. The authors are not responsible for misuse.

## Support

Issues and feature requests can be filed in this repo's [Issues](../../issues) tab. Source code is not published; this repository distributes compiled releases only.
