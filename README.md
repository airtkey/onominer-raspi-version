# 📦 UM980 GNSS Module – 3D Printable Case

This repository contains a 3D-printable case specifically designed for the **UM980 GNSS module**. It’s part of a DIY GNSS miner setup and is ideal for projects such as Onocoy or dual-use with Geodnet.

## 🧩 Features

- Custom fit for the **UM980 GNSS module**
- Space for a **3010 cooling fan** (soldered directly to the module)  
  – or use a passive **aluminum heatsink** instead
- Two case versions:
  1. **Standard case** – compact, minimal design  
  2. **Splitter version** – extra room for a splitter to share GNSS antenna with another miner (e.g. Geodnet)

## 📄 Part List

A full hardware list is available in the included PDF:  
📎 **[partlist.pdf](./partlist.pdf)**

It contains all required components for:
- the UM980 GNSS module
- cooling options (fan or heatsink)
- cabling and power
- optional splitter setup

## 🚀 Installation Guide

This case is part of a DIY GNSS miner setup. Here's how to set up the software on your Raspberry Pi (or similar device):

### 1. Flash the OS
Download and flash **Raspberry Pi OS (Lite)** to your microSD card using [Raspberry Pi Imager](https://www.raspberrypi.com/software/).  
Enable SSH and Wi-Fi before booting (you can create an empty `ssh` file and a `wpa_supplicant.conf` in the boot partition).

### 2. Connect via SSH
Insert the SD card into your Raspberry Pi and power it up.  
Then connect using an SSH client like **PuTTY**:

Default credentials (recommended to change later):
Username: admin
Password: admin

### 3. Update and Reboot

Run the following commands:

sudo apt update
sudo apt upgrade
sudo reboot

### 4. Connect Your GNSS Receiver

Once the Pi has rebooted, connect your Unicore, Bynav, or Septentrio GNSS receiver via USB.

### 5. Install the ELT_RTKBase Software

Open a terminal (ssh with putty) on the Pi and run two times:

"wget https://github.com/GNSSOEM/ELT_RTKBase/raw/main/install.sh
chmod +x install.sh
./install.sh"


The script will install the required software and drivers, and start the dashboard (usually accessible at http://raspberrypi.local:3000).

💡 After installation, you can configure your receiver and connect it to a network like Onocoy directly from the web dashboard.

## 🖨️ Print Instructions

- File format: `.stl`
- Recommended material: **PETG** or **PLA+**
- Orientation: print flat (bottom side down)
- Supports: **not required**
- Infill: 15–30%

## 🧰 Assembly

1. Place the UM980 module inside the case.
2. Mount the **3010 fan** above the chip – connect power directly to the module pins *(or skip if using a passive heatsink)*.
3. Route the USB-C and antenna cables through the side cutouts.
4. Close the lid – some variants support screw or snap-fit.

## 🔀 Splitter Variant

The "Splitter" case version has space to install a **GNSS splitter**, allowing you to run the UM980 module **in parallel with another GNSS miner** (e.g. for multimining with Geodnet + Onocoy).

> 🛠️ Important: Be sure to use an **active splitter** with power passthrough if your antenna needs voltage.

## 📷 Preview
  
(https://github.com/airtkey/onominer-raspi-version/blob/main/IMG_20250618_121334.jpg)

## 🔗 Related Links

- [Onocoy Network](https://onocoy.com)
- [UM980 Base Setup (ELT_RTKBase)](https://github.com/GNSSOEM/ELT_RTKBase)


## 📬 Contact

Questions? Ideas?  
Feel free to:
  
- Reach out via [YouTube](http://www.youtube.com/@airtkey)  
- Message me on **Discord** – you’ll find me in the **Onocoy server**   as alex_multimining.
- Or on **X (Twitter)**: [@alex_multimining](https://x.com/AlexMultiMining)

---

