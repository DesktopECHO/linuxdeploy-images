# QuickStart Images for Linux Deploy

## [f40kde-arm64.tgz](https://github.com/DesktopECHO/linuxdeploy-images/releases/download/v1.0/f40kde-arm64.tgz) · Refreshed September 2024
- Fedora 40 for ARM64-based Andrid devices
- KDE Plasma 6.1
- xRDP with h.264 codec
<img src="https://github.com/user-attachments/assets/7177cd35-30b4-4fdc-b3a9-443c76530a23" width="384">
<img src="https://github.com/user-attachments/assets/94482c26-2609-4272-8af0-5139e329dbb2" width="384">
<img src="https://github.com/user-attachments/assets/8cad1bb9-8158-4e16-8016-2c7db75513a0" width="768">


## [bookworm-aarch64.tgz](https://github.com/DesktopECHO/linuxdeploy-images/raw/main/bookworm-aarch64.tgz)
- Debian 12 (Bookworm) minimal image, ARM64

## [debian.tgz](https://github.com/DesktopECHO/linuxdeploy-images/raw/main/debian.tgz)
- Debian 11 (Bullseye) minimal image 32-bit ARMv7
- uname shim to hide reporting aarch64 when running 32-bit distros  
- Includes systemd-shim as many installers expect a working systemctl
- Dropbear SSHd listening on port 22022

## [ncd12.tgz](https://github.com/DesktopECHO/linuxdeploy-images/raw/main/ncd12.tgz)
- Lightly-forked edition of [NextCloudPi](https://github.com/nextcloud/nextcloudpi/compare/master...DesktopECHO:master) 
- [Video](https://www.youtube.com/watch?v=RuHJ_S9DcG4) of the deployment at work
- When the Linux container is created NextCloudPi provisions automatically via install.sh
- Idential otherwise to debian.tgz above

# Instructions:

- Open web browser on device and download+install the Linux Deploy APK.  You can also download this from the Play Store if preferred:

  - Get the latest version at: **https://github.com/meefik/linuxdeploy/releases**
  - Android 4.x requires an older release: **https://github.com/meefik/linuxdeploy/releases/tag/2.5.1**

- Open **Linux Deploy** and change ONLY these settings:
     -  Open the 'Hamburger menu' (Symbol with three dashes at top left of screen) then touch **Settings**.  Place a checkmark on these options:
        -  **Lock Screen** (If you want to keep display always on)
        -  **Lock Wi-Fi** (If your device has Wi-Fi)
        -  **Wake Lock** 
        -  **Autostart**
     -  Open **Properties Menu** (To the right of the 'Stop' button)
        -  Distribution: **rootfs.tar**
        -  Source Path: **https://github.com/DesktopECHO/linuxdeploy-images/raw/main/debian.tgz** (Or **ncd12.tgz** for NextCloudPi)
        -  Image size: **2047** (Or **4095** if installing NextCloud)
        -  Set password for user **android**
        -  Init -> **Enable**
        -  Init System -> **sysv**
     -  Open **Options** Menu (Three dots at top right of screen)
        -  Select **Install** and "OK" to confirm. 
        -  Wait a few minutes for the image to install.
          
     -  When install is complete, the Linux Deploy console window will show the following at the end of the console output: 
              
        `````[HH:mm:ss] >>> :: Configuring core/unchroot ...`````
        
        `````[HH:mm:ss] >>> deploy`````
        
    -  **Before you continue, make sure the Linux Deploy Console is free of error messages.**  If you have trouble installing the image in Linux Deploy it may be because of SELinux.  See this [post on XDA](https://forum.xda-developers.com/t/app-tool-2-0-official-the-selinux-switch.3656502/) for an APK to disable SELinux.  
  
Touch the **[ ▸ START ]** button, and "OK" to confirm - The instance takes a few seconds to "boot" 
