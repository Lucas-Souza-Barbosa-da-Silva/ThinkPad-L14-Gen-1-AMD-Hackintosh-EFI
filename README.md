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

### ⚠️ Not Working

* Fingerprint reader (Goodix)
* AirDrop
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

# macOS Compatibility

### macOS Tahoe

⚠️ **Not recommended**

Current status:

* Wi-Fi does not work.
* Audio does not work.
* Overall system stability is poor.

This EFI is **not recommended** for Tahoe.

---

### macOS Sequoia

Supported with one small modification.

Replace **AirportItlwm** with **itlwm** and use **HeliPort** to manage Wi-Fi connections.

After this change, the system works similarly to Sonoma.

---

### macOS Sonoma

✅ Fully supported.

No modifications are required. Everything listed in the **Working** section functions as expected.

---

### macOS Catalina → Ventura

Supported.

Simply replace **AirportItlwm** with the version that matches your target macOS release.

After replacing the kext, the system behaves the same as Sonoma.

---

### Older macOS Versions

❌ Not supported.

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

---

# Notes

This EFI was built specifically for the hardware listed above. While it may work on similar Ryzen-based ThinkPads, compatibility with other hardware is **not guaranteed**.

If you intend to use this EFI on another machine, make sure to:

* Generate your own SMBIOS.
* Adjust the ACPI tables if necessary.
* Create your own USB mapping.
* Update the kexts and OpenCore to the latest stable versions whenever possible.

Use this project as a reference and customize it for your own hardware.
