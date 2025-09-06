# Kali Linux Installation Guide

This repository provides a step-by-step guide to installing **Kali Linux as a normal software** inside your existing operating system (Windows/Linux/Mac).  
We will use virtualization tools like **VirtualBox** or **VMware**.

---

## Prerequisites
- A computer with at least **4GB RAM** (8GB recommended).
- At least **25GB free disk space**.
- Virtualization enabled in BIOS/UEFI.
- Virtualization software:
  - [VirtualBox](https://www.virtualbox.org/) (Free, open-source)  
  - OR [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html) (Free for personal use)

---

## Steps

### 1. Download Kali Linux ISO
- Go to [Kali Linux Downloads](https://www.kali.org/get-kali/#kali-virtual-machines)  
- Download the **ISO file** or prebuilt **VM image**.

### 2. Install VirtualBox
- Download and install VirtualBox for your system.  
- Install the Extension Pack (for USB and other features).

### 3. Create a New Virtual Machine
- Open VirtualBox → Click **New**.  
- Name: `Kali Linux`  
- Type: `Linux`  
- Version: `Debian (64-bit)`  

### 4. Assign Resources
- RAM: Minimum **2GB** (recommended 4GB+).  
- Processors: At least **2 cores**.  
- Hard Disk: Create a virtual disk of **25GB or more**.

### 5. Mount the ISO
- In VM Settings → Storage → Load the **Kali ISO** in the optical drive.  

### 6. Start the VM
- Boot the VM.  
- Select **Graphical Install**.  
- Follow installation steps:
  - Language, region, keyboard.
  - Create a user and password.
  - Partition disk (Use entire disk → Guided).
  - Install system + GRUB bootloader.

### 7. First Login
- After installation, restart the VM.  
- Login with your created username/password.  

---

## Alternative: Prebuilt Virtual Machine
- Download the **Kali Linux VirtualBox image** from [Kali Downloads](https://www.kali.org/get-kali/#kali-virtual-machines).
- Import into VirtualBox (File → Import Appliance).  
- Default login:  
  - User: `kali`  
  - Password: `kali`  

---

## Screenshots (to be added later)
- VM setup screenshots  
- Installation steps  

---

## Notes
- Always update after installation:
  ```bash
  sudo apt update && sudo apt upgrade -y
