# Kali Linux Installation Guide 🐧

![Kali Linux Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2b/Kali-dragon-icon.svg/2048px-Kali-dragon-icon.svg.png)

This repository provides a step-by-step guide to installing **Kali Linux as a normal software** inside your existing operating system (Windows/Linux/Mac). We will use free virtualization tools like **VirtualBox** or **VMware**. This method is safe and won't affect your main operating system.

---

## Prerequisites 📋

Before you begin, ensure you have the following:

-   A computer with at least **4GB RAM** (8GB is highly recommended for smooth performance).
-   At least **25GB of free disk space**.
-   **Virtualization Technology** (VT-x/AMD-v) enabled in your computer's BIOS/UEFI.
-   Virtualization Software:
    -   [VirtualBox](https://www.virtualbox.org/) (Free, open-source)
    -   OR [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html) (Free for personal use)

---

## Steps

### 1. Download Kali Linux ISO 📥

First, you need the official installer image.

-   Go to the [Official Kali Linux Downloads page](https://www.kali.org/get-kali/#kali-installer-images).
-   Download the **"Installer"** ISO file for your system (e.g., 64-bit).

![Screenshot of the Kali Linux downloads page](./images/1-kali-download-page.png)

### 2. Install VirtualBox

-   Download and install **VirtualBox** for your host operating system.
-   Download and install the **VirtualBox Extension Pack** from the same page for better USB support and other features.

### 3. Create a New Virtual Machine 🖥️

-   Open VirtualBox and click the **"New"** button.
-   **Name:** `Kali Linux`
-   **Type:** `Linux`
-   **Version:** `Debian (64-bit)`

![Screenshot of creating a new VM in VirtualBox](./images/2-create-new-vm.png)

### 4. Assign Resources ⚙️

Allocate your computer's resources to the new virtual machine.

-   **RAM:** Minimum **2GB** (2048 MB), but **4GB** (4096 MB) or more is recommended.
-   **Processors:** Assign at least **2 CPU cores**.
-   **Hard Disk:** Choose "Create a virtual hard disk now" and set the size to **25GB or more**.

![Screenshot of assigning RAM and CPU in VirtualBox](./images/3-assign-resources.png)

### 5. Mount the ISO 💿

Tell the VM to boot from the Kali Linux installer you downloaded.

-   Select your Kali Linux VM and go to **Settings → Storage**.
-   Click on the empty optical drive under "Controller: IDE".
-   Click the disc icon on the right and select the **Kali Linux ISO file**.

![Screenshot of mounting the ISO in VM Storage Settings](./images/4-mount-iso.png)

### 6. Start the VM and Install Kali 🚀

-   Select the VM and click **"Start"**.
-   In the boot menu, use the arrow keys to select **"Graphical Install"** and press Enter.
-   Follow the on-screen installation steps:
    -   Choose your language, region, and keyboard layout.
    -   Create a user account and a strong password.
    -   For partitioning, choose **"Guided - use entire disk"**. This is safe as it only affects the virtual disk.
    -   Confirm the changes and let the system install. Install the GRUB bootloader when prompted.

![Screenshot of the Kali Linux Graphical Install screen](./images/5-graphical-install.png)

### 7. First Login ✨

-   After the installation is complete, the VM will restart.
-   You will be greeted by the login screen. Log in with the username and password you created.

![Screenshot of the Kali Linux login screen](./images/6-kali-login-screen.png)

---

## Alternative Method: Prebuilt Virtual Machine (Easier) ✅

For a much faster setup, you can download a ready-to-use virtual machine.

-   Download the **Kali Linux VirtualBox image** from the [Kali Downloads page](https://www.kali.org/get-kali/#kali-virtual-machines).
-   In VirtualBox, go to **File → Import Appliance...** and select the `.ova` file you downloaded.
-   Start the imported machine. The default login credentials are:
    -   **User:** `kali`
    -   **Password:** `kali`
-   **Important:** Change the default password immediately after your first login!

---

## Post-Installation Notes 📝

Always update your new Kali system after installation. Open a terminal and run the following command:

```bash
sudo apt update && sudo apt full-upgrade -y

```
