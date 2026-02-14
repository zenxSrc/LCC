# Lenovo Battery Conservation Mode Controller (LCC)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  
[![Stars](https://img.shields.io/github/stars/zenxSrc/LCC?style=social)](https://github.com/zenxSrc/LCC)  
[![Forks](https://img.shields.io/github/forks/zenxSrc/LCC?style=social)](https://github.com/zenxSrc/LCC)  
[![Language](https://img.shields.io/badge/Java%20%2B%20Shell-007396?logo=java&logoColor=white)](https://github.com/zenxSrc/LCC)

**Easily toggle Lenovo's Battery Conservation Mode on Linux – keep your battery healthy at 55-60% charge!**

A lightweight utility (GUI + TUI) strictly for Lenovo laptops on Linux to enable/disable Conservation Mode, which caps charging to extend battery lifespan when mostly plugged in.

## Features
- **Simple toggle** between enabled/disabled states  
- **Real-time status** display with color indicators  
- **Dual interfaces**: Modern Java Swing GUI + classic terminal TUI (using dialog)  
- Root privilege check & error handling  
- Minimal dependencies  

## Prerequisites
- Lenovo laptop with Conservation Mode support (most IdeaPad/Legion series)  
- Linux kernel with ideapad_acpi driver  
- Java 8+ (for GUI)  
- `dialog` package (for TUI – install via apt/yum/pacman)  
- sudo/root access  

Check if your model supports it:  
```bash
ls /sys/bus/platform/drivers/ideapad_acpi/*/conservation_mode
```

## Installation
- Clone the repo
```
git clone https://github.com/zenxSrc/LCC.git
cd LCC
```
## For GUI (recommended):
Compile and run the Java app
```
javac BatteryConservationController.java
sudo java BatteryConservationController
```

## For Terminal TUI:
```
sudo bash toggle_conservation.sh
```

## Usage
- Launch GUI → Click toggle button → Enjoy longer battery life
- In TUI → Arrow keys to select Enable/Disable → Enter to apply
- Changes apply instantly; check battery icon or run cat /sys/.../conservation_mode (1 = enabled).

## Supported Models
Tested on various IdeaPad & Legion models – should work on any Lenovo using ideapad_acpi VPC2004 conservation_mode file. Report issues for unsupported ones!

## Troubleshooting

- Path not found? → Not supported on your model or wrong driver
- Java issues? → Install default-jdk / openjdk-17-jdk
- Permission denied? → Always use sudo

## Contributing
Pull requests welcome! Feel free to add auto-compilation, packaging (AUR/Flatpak), more models testing, or a tray icon version.

## License
MIT License – free to use, modify, distribute.

Made with ❤️ for Linux Lenovo users.
# Star ⭐ if it saves your battery!
