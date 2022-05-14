# QuickStart Images for Linux Deploy

## [debian.tgz](https://github.com/DesktopECHO/linuxdeploy-images/raw/main/debian.tgz)
- Debian 11 (Bullseye) minimal image
- uname shim to hide reporting aarch64 when running 32-bit distros  
- Includes systemd-shim as many installers expect a working systemctl
- Dropbear SSHd listening on port 22022

## [ncd12.tgz](https://github.com/DesktopECHO/linuxdeploy-images/raw/main/ncd12.tgz)
- Lightly-forked edition of [NextCloudPi](https://github.com/nextcloud/nextcloudpi/compare/master...DesktopECHO:master) 
- When the Linux container is created NextCloudPi provisions automatically via install.sh
- Idential otherwise to debian.tgz above
