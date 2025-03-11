# 🚀 PlatformIO using Devcontainers  

This repository provides an example of a **devcontainer** setup for building **ESP-IDF projects** using **PlatformIO** inside a [Devcontainer](https://code.visualstudio.com/docs/devcontainers/containers) with **VSCode**.  

## ✅ Prerequisites  

Before you begin, ensure you have the following installed and set up:  

- 🖥 **Visual Studio Code**  
- 🐳 **Docker** (Linux) or **Docker Desktop** (Windows/Mac)  
- 🏁 **On Windows**  
  - ⚙️ **WSL 2 enabled**  
  - 🔌 To use real devices inside the container, you need `usbipd-win`. Follow the [setup instructions](https://docs.espressif.com/projects/vscode-esp-idf-extension/en/latest/additionalfeatures/docker-container.html).  
- 🔌 **A compatible ESP32 development board** (Optional)  
  - 🛠 Ensure you have the necessary **USB-to-serial drivers** installed (if applicable).  

---

## ⚙️ Building  

Run the following commands to build and upload firmware:  

```sh
# 🏗 Build the project
pio run

# 🚀 Upload firmware to the board
pio run --target upload

# 🎯 Build for a specific environment (e.g., ESP32 Dev Module)
pio run -e esp32dev

# 📡 Upload firmware for a specific environment
pio run -e esp32dev --target upload

# 🧹 Clean build files
pio run --target clean
```

## 🔩 Supported Hardware

🔗 Official hardware documentation:  

- **ESP32-S3-DevKitM-1**  
  📖 [Hardware Reference](https://docs.espressif.com/projects/esp-dev-kits/en/latest/esp32s3/esp32-s3-devkitm-1/user_guide.html#hardware-reference)  
- **ESP32-C6-DevKitC-1**  
  📖 [Hardware Reference](https://docs.espressif.com/projects/esp-dev-kits/en/latest/esp32c6/esp32-c6-devkitc-1/index.html)  

## 💡 Demo Code
🔗 Get started with a simple **Blink** demo from Espressif’s official repository:  
[ESP-IDF Blink Example](https://github.com/espressif/esp-idf/tree/master/examples/get-started/blink/main)  
