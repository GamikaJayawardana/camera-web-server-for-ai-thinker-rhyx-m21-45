# 📸 ESP32-CAM Web Server for RHYX-M21-45 Camera (AI-Thinker) | Camera Init Fix

<p align="center">
  <img src="https://img.shields.io/badge/ESP32-CAM-blue?style=for-the-badge&logo=espressif" />
  <img src="https://img.shields.io/badge/Arduino-IDE-00979D?style=for-the-badge&logo=arduino" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/PSRAM-Required-success?style=for-the-badge" />
</p>

<p align="center">
  <b>🚀 A complete ESP32-CAM Web Server specifically optimized for AI-Thinker boards using the RHYX-M21-45 camera sensor.</b><br>
  Fixes the infamous <code>Camera init failed (0x20004)</code> error and provides stable video streaming.
</p>

---

# ⭐ Why This Repository?

Many newly manufactured **AI-Thinker ESP32-CAM** boards no longer come with the traditional **OV2640** camera.

Instead, they include the **RHYX-M21-45** module.

Unfortunately, the official Arduino examples were designed primarily for the OV2640, causing thousands of users to encounter errors such as:

```text
Camera init failed with error 0x20004
Camera probe failed
Camera init failed
```

If your ESP32-CAM works electrically but refuses to initialize the camera, this repository is exactly what you need.

---

# ✨ Features

✅ Supports AI-Thinker ESP32-CAM

✅ Optimized for RHYX-M21-45 camera

✅ Stable WiFi Web Server

✅ Live Camera Streaming

✅ Correct AI Thinker Pin Mapping

✅ RGB565 Pixel Format

✅ Dual Frame Buffers

✅ PSRAM Optimized

✅ Stable 20MHz Camera Clock

✅ Ready for Computer Vision

✅ Face Detection Compatible

✅ Beginner Friendly

---

# 🚀 What Makes This Different?

Unlike the default Arduino examples, this project includes important compatibility changes.

| Feature | Official Example | This Repository |
|----------|-----------------|----------------|
| RHYX-M21-45 Support | ❌ | ✅ |
| RGB565 Configuration | ❌ | ✅ |
| PSRAM Optimization | Partial | ✅ |
| Stable 20MHz Clock | ❌ | ✅ |
| Dual Frame Buffers | ❌ | ✅ |
| AI Ready | ❌ | ✅ |

---

# 🔧 Optimized Camera Configuration

The project is configured with:

```cpp
camera_config_t config;

config.pixel_format = PIXFORMAT_RGB565;
config.xclk_freq_hz = 20000000;
config.fb_location = CAMERA_FB_IN_PSRAM;
config.fb_count = 2;
```

These settings dramatically improve compatibility with the RHYX-M21-45 module while also making the project suitable for:

- Face Detection
- Face Recognition
- OpenCV
- TensorFlow Lite
- Edge AI
- Object Detection

---

# 📦 Hardware Requirements

- ESP32-CAM AI Thinker
- RHYX-M21-45 Camera Module
- FTDI Programmer (if required)
- USB Cable
- Stable 5V Power Supply

---

# 💻 Software Requirements

- Arduino IDE
- ESP32 Board Package
- ESP32 Camera Library

---

# ⚙ Arduino IDE Settings

These settings are **very important**.

| Setting | Value |
|----------|-------|
| Board | AI Thinker ESP32-CAM |
| Flash Frequency | 80MHz |
| Flash Mode | QIO |
| PSRAM | Enabled ✅ |
| Upload Speed | 115200 |
| Partition Scheme | Huge APP (3MB No OTA/1MB SPIFFS) |

---

# 📶 Configure WiFi

Open the sketch and replace your WiFi credentials.

```cpp
const char* ssid = "YOUR_WIFI_SSID";
const char* password = "YOUR_WIFI_PASSWORD";
```

Example:

```cpp
const char* ssid = "GamikaKJ";
const char* password = "00001111";
```

---

# 🚀 Upload Instructions

### Step 1

Connect GPIO0 to GND.

### Step 2

Press the RESET button.

### Step 3

Click Upload.

### Step 4

Wait until uploading finishes.

### Step 5

Disconnect GPIO0 from GND.

### Step 6

Press RESET again.

---

# 🌐 Open the Camera Stream

Open the Serial Monitor.

Baud Rate:

```
115200
```

After connecting to WiFi you'll see something like:

```
WiFi connected

Camera Ready!

http://192.168.1.100
```

Open the IP address in your browser.

You'll get:

- Live Video Stream
- Camera Controls
- Image Capture
- Camera Settings

---

# 📸 Applications

Perfect for:

- Smart Home Projects
- Security Cameras
- AI Vision
- Face Detection
- Face Recognition
- Robot Vision
- IoT Projects
- Home Automation
- Object Detection
- Machine Learning
- OpenCV Projects

---

# 🛠 Troubleshooting

## Camera init failed (0x20004)

✔ Verify the ribbon cable is inserted correctly.

✔ Lock the black connector.

✔ Enable PSRAM.

✔ Select AI Thinker ESP32-CAM.

✔ Restart the board.

---

## Brownout Detector Triggered

The ESP32-CAM needs a stable power supply.

Use:

- 5V / 2A USB Adapter
- Quality USB Cable

Avoid powering directly from weak FTDI modules.

---

## No Serial Output

Check:

- Baud Rate = 115200
- Correct COM Port
- Press RESET

---

## Camera Image is Black

- Reinsert the ribbon cable.
- Clean the camera connector.
- Confirm RHYX-M21-45 is firmly attached.

---

# 📂 Project Structure

```
ESP32-CAM-RHYX-M21-45/
│
├── ESP32_CAM_WebServer.ino
├── README.md
├── LICENSE
└── images/
```

---

# 🤝 Contributing

Contributions are welcome!

If you discover improvements, fixes, or better configurations for RHYX-M21-45, feel free to:

- Fork the repository
- Create a feature branch
- Commit your changes
- Open a Pull Request

---

# ⭐ Support the Project

If this repository helped you solve your camera initialization problem:

⭐ Star this repository

🍴 Fork it

📢 Share it with others

Your support helps improve the project and assists other ESP32-CAM users.

---

# 📈 SEO Keywords

ESP32-CAM RHYX-M21-45, ESP32 Camera Init Failed, ESP32 Camera Error 0x20004, AI Thinker ESP32-CAM Fix, RHYX-M21-45 Camera Module, ESP32 Web Server, ESP32 Camera Web Server, ESP32 AI Camera, ESP32 Face Detection, ESP32 Face Recognition, ESP32 Camera RGB565, ESP32 PSRAM, ESP32 Camera Initialization Fix, ESP32 Camera Streaming, ESP32 Arduino Camera, ESP32 Camera Example, ESP32-CAM Tutorial, ESP32 Computer Vision, ESP32 OpenCV, ESP32 Object Detection, ESP32 Machine Learning, ESP32 Edge AI, OV2640 Alternative, RHYX-M21-45 Solution.

---

# 📜 License

This project is licensed under the **MIT License**.

Feel free to use, modify, and distribute it.

---

<p align="center">
Made with ❤️ for the ESP32 Community

<b>If this project saved you hours of debugging, don't forget to ⭐ Star the repository!</b>
</p>
