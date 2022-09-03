## How to compile and install

### 1. Build/Compile
- Ubuntu
```bash
apt install meson ninja-build libgee-0.8-dev libgnome-menu-3-dev cdbs valac libvala-*-dev libglib2.0-dev libwnck-3-dev libgtk-3-dev xterm python3 python3-wheel python3-setuptools gnome-menus
```
- Clone repository
```bash
git clone https://github.com/libredeb/lightpad.git
cd lightpad/
```
- Build
```shell
meson build --prefix=/usr
cd build
ninja
```
- Output file: build/com.github.libredeb.lightpad

### 2. Install
- Copy executable file to /opt/lightpad
```shell
sudo mkdir /opt/lightpad
sudo cp build/com.github.libredeb.lightpad /opt/lightpad
```
- Create shortcut file in /usr/share/applications/com.github.libredeb.lightpad.desktop
```ini
[Desktop Entry]
Name=Applications
GenericName=Application Launcher
Comment=Lightweight, look nice and powerful application launcher
Categories=GNOME;GTK;Utility;
Exec=/opt/lightpad/com.github.libredeb.lightpad
Icon=start-here-symbolic
Terminal=false
Type=Application
; NoDisplay=true
StartupNotify=false
```
- Start it by keyboard and use mouse to add it to Plank quickly
- Edit the shortcut, remove "; " character before NoDisplay=true to hide it from application menu
- Create shortcut key for quick open
    - System -> Preferences -> Hardware -> Keyboard Shortcuts > click Add
    - Name: LightPad
    - Command: com.github.libredeb.lightpad

### 3. References
<https://github.com/libredeb/lightpad>
<https://github.com/ubuntubudgie/budgie-lightpad-applet>
