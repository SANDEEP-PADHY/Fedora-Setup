# Fedora Setup After Fresh Installation

This guide provides essential steps to configure and optimize your Fedora Linux setup. 

### 1. Update System
Make sure your system is up to date with the latest packages and security patches.

```bash
sudo dnf update -y
```

### 2. Use DNF5 (Optional, if available)
DNF5 provides faster package management and enhanced features. If available, install it.

```bash
sudo dnf install -y dnf5
```

### 3. Configure DNF
Configure DNF to limit downloads to 10 parallel downloads and use the fastest mirrors.

```bash

sudo dnf config-manager --setopt=max_parallel_downloads=10
echo -e "[main]\nfastestmirror=true" | sudo tee -a /etc/dnf/dnf.conf

```

### 4. Install Software/Firmware Updates
Install available software and firmware updates.

```bash
sudo dnf install -y dnf-plugin-system-upgrade
sudo dnf upgrade --refresh -y
```

### 5. Install NVIDIA Drivers
For NVIDIA graphics cards, install the proprietary drivers.

```bash
sudo dnf install -y akmod-nvidia
```

### 6. Include Multimedia Support
Install multimedia codecs to support various audio and video formats.

```bash
sudo dnf install -y gstreamer1-plugins-bad gstreamer1-plugins-ugly gstreamer1-plugins-free gstreamer1-plugins-good ffmpeg vlc
```

### 7. Install Flatpak
Install Flatpak for sandboxed applications and add the Flathub repository for easy app access.

```bash
sudo dnf install -y flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

### 8. Install RPM Fusion Repositories
RPM Fusion provides additional software packages not available in Fedora’s official repos.

```bash
sudo dnf install -y https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
sudo dnf install -y https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

### 9. Install Snap (Optional)
Snap is another packaging format. If you prefer Snap, install Snap support.

```bash
sudo dnf install -y snapd
sudo systemctl enable --now snapd.socket
```

### 10. Install A Browser (Optional)
**Google Chrome** is a fast, secure web browser by Google, known for its speed and simple interface.

```bash
flatpak install -y flathub com.google.Chrome
```
`OR`

**Zen BrowseR** is a privacy-focused browser you can install for enhanced security.

```bash
flatpak install -y flathub org.zenja.ZenBrowser
```

### 11. Install GNOME Shell Extension Manager
Manage GNOME extensions to customize your GNOME desktop.

```bash
sudo dnf install -y gnome-shell-extension-manager
```

### 12. Install GNOME Tweaks
GNOME Tweaks helps you customize the GNOME desktop environment.

```bash
sudo dnf install -y gnome-tweaks
```

### 13. Install GRUB Customizer (Optional)
Customize your GRUB bootloader settings (optional for advanced users).

```bash
sudo dnf install -y grub-customizer
```

### 14. Install Custom Cursor Software (Optional)
Install custom cursor themes for a better visual experience.

```bash
sudo dnf install -y xcursors
```

### 15. Install Timeshift
Timeshift is a tool to create and restore system snapshots. Essential for system backups.

```bash
sudo dnf install -y timeshift
```
## Summary of the Setup:
- **System updates** and **DNF configuration** ensure optimal performance and fast downloads.
- **Multimedia support** and **NVIDIA drivers** are included for a rich media experience.
- **Flatpak**, **Snap**, and **RPM Fusion** enable access to a wide range of applications.
- **Zen Browser**, **GNOME Shell Extensions**, **GNOME Tweaks**, and **GRUB Customizer** offer further customization for your desktop.
- **Timeshift** is included to create system snapshots for recovery.
