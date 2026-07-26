# ThinkPad L14 Gen 1 (AMD) Hackintosh EFI

This EFI is designed for the **Lenovo ThinkPad L14 Gen 1 (AMD)** and aims to provide a stable and reliable Hackintosh experience on supported macOS versions.

## Features

### ✅ Working

* Wi-Fi
* Bluetooth
* Graphics acceleration (Metal)
* Function (Fn) keys
* Battery management (using AMD Power Gadget)
* Built-in webcam
* Fan control (using YogaSMC)
* Audio
* Sleep/Wake
* USB ports
* Keyboard and touchpad
* AirDrop (if used AirportItlwm)
* USB Tethering


### ⚠️ Not Working

* Fingerprint reader (Goodix)
* AirDrop (if used Itlwm)
* AirPlay / Screen Mirroring

---

# Tested Hardware

| Component              | Model                                     |
| ---------------------- | ----------------------------------------- |
| **Laptop**             | Lenovo ThinkPad L14 Gen 1 (AMD)           |
| **CPU**                | AMD Ryzen 5 PRO 4650U                     |
| **GPU**                | AMD Radeon™ Graphics (Vega 6)             |
| **Memory**             | 16 GB Kingston Fury DDR4                  |
| **Wi-Fi**              | Intel Wi-Fi 6 AX200                       |
| **Bluetooth**          | Intel Wireless Bluetooth                  |
| **Ethernet**           | Realtek PCIe GbE Family Controller        |
| **Audio**              | Realtek Audio / AMD High Definition Audio |
| **Storage**            | Patriot P300 NVMe SSD (DRAM-less)         |
| **Fingerprint Reader** | Goodix (Unsupported)                      |

---

# Notes

This EFI was built specifically for the hardware listed above. While it may work on similar Ryzen-based ThinkPads, compatibility with other hardware is **not guaranteed**.

If you are going to use the internet installation, use a wired internet connection on macOS Tahoe and Sequoia.

This is because Wi-Fi activation happens after the installation, **post install**.

If you intend to use this EFI on another machine, make sure to:

* Generate your own SMBIOS.
* Adjust the ACPI tables if necessary.
* Create your own USB mapping.
* Update the kexts and OpenCore to the latest stable versions whenever possible.

Use this project as a reference and customize it for your own hardware.

---

# macOS Compatibility

### macOS Tahoe

✅ **Supported (using the "EFI macOS Tahoe" folder)**

Use the dedicated EFI included in this repository and patch

Use RP Core patch: https://github.com/luchina-gabriel/RP-CORE

Current status without patch:

* Wi-Fi does not work without patch.
* Audio does not work without patch.
* Overall system stability is poor, if using **HeliPort**.

Current status with patch:

* Overall system works similarly to Sonoma.

---

### macOS Sequoia

✅ **Supported**

Use the standard EFI.

Replace AirportItlwm with the appropriate version of itlwm and use HeliPort for Wi-Fi management.

After this change, the system works similarly to Sonoma.

---

### macOS Sonoma

✅ **Fully supported**.

No modifications are required. Everything listed in the **Working** section functions as expected.

---

### macOS Catalina → Ventura

✅ **Supported**.

Simply replace **AirportItlwm** with the version that matches your target macOS release.

After replacing the kext, the system behaves the same as Sonoma.

---

### Older macOS Versions

❌ **Not supported**.

---

### IMPORTANT

**The EFI macOS Tahoe folder is intended exclusively for macOS Tahoe**

For all earlier macOS versions, use the standard EFI folder.

---

# Credits

This EFI was developed based on the following projects:

* **Collin8000** – ThinkPad T14 Gen 1 AMD Hackintosh
  https://github.com/Collin8000/Thinkpad-T14-Gen-1-Amd-Hackintosh

* **OpCore Simplify** – Base configuration and OpenCore generation

Special thanks to:

* **Acidanthera** – OpenCore and the official kexts
* **OpenIntelWireless** – AirportItlwm, itlwm and IntelBluetoothFirmware
* **Apple** – macOS
* **Dortania** – The excellent OpenCore Install Guide
* **Collin8000** – Base EFI 
* **luchina-gabriel** – RP Core

---