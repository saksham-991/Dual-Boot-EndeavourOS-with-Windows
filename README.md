# Dual-Boot-EndeavourOS-with-Windows
This repository provides a step-by-step guide to installing EndeavourOS alongside an existing Windows installation. It covers:

Disk partitioning and preparation

Creating a bootable USB using Ventoy

Running the EndeavourOS installer

Initial system configuration (username, passwords, hostname)

Post-install system update


The guide is designed to be comprehensive yet beginner-friendly, including screenshots and detailed instructions for each step. Following this tutorial will provide a solid foundation for further customization, theming, and performance optimization on EndeavourOS.


---

# 📌 Key Features

Dual-boot setup with Windows

GPT partitioning for UEFI systems

USB preparation using Ventoy

Clean, easy-to-follow step instructions

Structured documentation with screenshots

Ready for follow-up tutorials (Hyprland theming, performance tweaks)


---

# ⚡ Benefits

Ensures safe installation without data loss on Windows

Provides a professional, reproducible workflow

Demonstrates knowledge of system installation and Linux basics

Acts as a foundation for advanced tutorials (Hyprland setup, theming, performance tuning)




## STEPS

#1️⃣ Prepare Disk Space for EndeavourOS
  
1. Open Disk Management in Windows:

Press Win + S → type Disk Management → open Create and format hard disk partitions.

![Image Alt](https://github.com/saksham-991/Dual-Boot-EndeavourOS-with-Windows/blob/d0db5457c2efe8102cac1697ef10e44797487412/images/IMG_20250906_164821_287.jpg)

2. Identify the partition to shrink (usually your main Windows partition).

3. Right-click the partition → select Shrink Volume.
Enter 80000 MB (≈80 GB) as the size to shrink.

4. After shrinking, a new unallocated space appears on the disk.

5. Create a new partition in the unallocated space:

Follow the wizard → leave defaults for filesystem type (will be handled during Linux installation).

![ImageAlt](https://github.com/saksham-991/Dual-Boot-EndeavourOS-with-Windows/blob/d0db5457c2efe8102cac1697ef10e44797487412/images/IMG_20250906_164823_602.png)





---

## 2️⃣ Prepare Bootable USB with Ventoy

1. Download Ventoy for Windows:

[https://sourceforge.net/projects/ventoy/files/v1.1.07]



2. Extract the downloaded zip file and open the Ventoy application.


3. Configure Ventoy:

Go to Options → Partition Scheme → select GPT.

![Image Alt](https://github.com/saksham-991/Dual-Boot-EndeavourOS-with-Windows/blob/d0db5457c2efe8102cac1697ef10e44797487412/images/IMG_20250906_164826_358.jpg)

4. Click Install to create a bootable USB.

⚠️ This will erase all data on the USB drive; ensure no important files are on it.



5. Copy the EndeavourOS ISO to the USB drive:

[https://mirror.hyd.albony.in/endeavouros/iso/EndeavourOS_Mercury-Neo-2025.03.19.iso]

No special tools are needed; copying the ISO directly makes it bootable.



---

## 3️⃣ Boot into EndeavourOS Installer

1. Reboot your computer and boot from the USB drive.


2. In the Ventoy menu, select the EndeavourOS ISO → After booting, choose Offline Installer in the popped up menu.

![Image Alt](https://github.com/saksham-991/Dual-Boot-EndeavourOS-with-Windows/blob/d0db5457c2efe8102cac1697ef10e44797487412/images/IMG_20250906_165958_028.jpg)

3. Proceed through the installation wizard:

Language selection → Keyboard layout → Region settings.



4. Partition selection:

Select Manual Partitioning (or “Replace a Partition”).

Choose the 80 GB partition you created earlier.

Format it as ext4 (already selected).


5. Configure user information:

Computer name

Username

Password

Root password (if requested)



6. Begin the installation process.





---

## 4️⃣ Reboot and Update System

1. After installation completes, reboot the laptop.


2. Log into your new EndeavourOS system.


3. Open the terminal (Ctrl + Alt + T) and update all packages:



   ''' sudo pacman -Syu '''

4. This ensures your system is fully up-to-date.



---

# ✅ Notes

Always back up important data before modifying partitions.

GPT partition scheme is recommended for UEFI Systems.

Screenshots are encouraged to make tutorials easier to follow.

Credit is given to official EndeavourOS documentation and Ventoy for installation tools.
