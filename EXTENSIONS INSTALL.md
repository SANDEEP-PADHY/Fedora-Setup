Here’s a simplified version of the `README.md` with only the necessary instructions for installing the GNOME Shell extensions using the provided bash script:

```markdown
# GNOME Shell Extensions Installation Script Using Extension Manager

This repository provides a script to install and manage the following GNOME Shell extensions using **Extension Manager**:

- ArcMenu
- Blur my Shell
- Coverflow Alt-Tab
- Custom Hot Corners - Extended
- Dash to Dock
- GNOME 4x UI Improvements
- Quick Settings Audio Panel
- TopHat
- User Themes
```
## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/SANDEEP-PADHY/Fedora-Setup
cd Fedora-Setup
```

### 2. Create and Edit the Installation Script

Create the `install-extensions.sh` script:

```bash
touch install-extensions.sh
chmod +x install-extensions.sh
```

Open the script with a text editor:

```bash
nano install-extensions.sh
```

Paste the following code into the file:

```bash
#!/bin/bash

# List of extensions to install
extensions=(
  "arcmenu@arcmenu.com"
  "blur-my-shell@aunetx"
  "coverflow-alt-tab@palatis.blogspot.com"
  "custom-hot-corners-extended@G-dH.github.com"
  "dash-to-dock@micxgx.gmail.com"
  "gnome-4x-ui-improvements@leav00.new@gmail.com"
  "quick-settings-audio-panel@bennypowers"
  "tophat@inthrees.com"
  "user-theme@gnome-shell-extensions.gcampax.github.com"
)

echo "Starting GNOME Shell Extensions installation using Extension Manager..."

# Install each extension
for extension in "${extensions[@]}"; do
  echo "Installing $extension..."
  gnome-extensions install "$extension"
done

echo "Enabling extensions..."

# Enable each extension
for extension in "${extensions[@]}"; do
  gnome-extensions enable "$extension"
done

echo "All extensions installed and enabled!"
```

Save press `CTRL+O`,Exit press `CTRL+X`.

### 3. Run the Installation Script

```bash
./install-extensions.sh
```
