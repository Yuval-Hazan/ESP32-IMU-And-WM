# ESP32 Wireless Monitoring System with IMU

This project implements a wireless monitoring system on an ESP32, featuring an Inertial Measurement Unit (IMU) for motion tracking and an integrated wireless connection module. The goal is to gather, process, and transmit sensor data wirelessly for remote monitoring, suitable for applications in robotics, IoT, and more.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The **ESP32 Wireless Monitoring System** combines real-time data processing and wireless communication capabilities using the ESP32 microcontroller. The system collects motion data from an IMU sensor, processes it, and sends it over Wi-Fi, allowing for real-time remote monitoring of the device's movement and orientation.

## Features

- **Real-Time IMU Data Acquisition**: Collects and processes orientation and motion data.
- **Wireless Transmission**: Transmits data over Wi-Fi for remote monitoring.
- **Modular Design**: Structured code with reusable modules, such as `WirelessMonitor` and `IMU`.
- **Scalable Configuration**: Easily adaptable to various use cases by modifying the configuration files.

## Requirements

- **Hardware**:
  - ESP32 Development Board
  - IMU Sensor (e.g., MPU6050)
  - Wi-Fi Connection

- **Software**:
  - PlatformIO (recommended) or Arduino IDE
  - ESP-IDF or ESP32 Core for Arduino
  - Libraries:
    - `AsyncTCP`
    - `ESPAsyncWebServer`

## Installation

1. **Clone the repository**:

2. **Install PlatformIO** (recommended for ESP32 projects):
   - Follow the [PlatformIO installation guide](https://platformio.org/install/cli).

3. **Install Required Libraries**:
   - PlatformIO automatically installs libraries specified in the `platformio.ini` file.

4. **Build and Upload**:
   ```bash
   pio run --target upload
   ```

## Usage

1. Power on the ESP32 device.
2. Connect to the Wi-Fi network specified in the configuration.
3. The device will start streaming IMU data over the Wi-Fi.
4. Access the data through the specified IP address and port.

## Configuration

- **WirelessMonitor Settings**:
  - Configure the Wi-Fi SSID, password, and IP address in `WirelessMonitor.h`.
  
- **IMU Settings**:
  - Adjust sensor settings in `IMU.h` to match the specific IMU model and desired data output.

## File Structure

```plaintext
├── lib
│   ├── EmbeddedFiles
│   │   ├── EmbeddedFiles.cpp
│   │   └── EmbeddedFiles.h
│   ├── IMU
│   │   ├── IMU.cpp
│   │   └── IMU.h
│   └── WirelessMonitor
│       ├── WirelessMonitor.cpp
│       └── WirelessMonitor.h
└── src
    └── main.cpp
```

## Contributing

Contributions are welcome! Please fork the repository, create a new branch, and submit a pull request for review.

## License

This project is licensed under the MIT License.
