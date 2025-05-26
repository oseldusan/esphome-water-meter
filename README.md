# ESPHome Watermeter



## Table of Contents

* [About](#about)
* [Features](#features)
* [Hardware Requirements](#hardware-requirements)
* [Software Requirements](#software-requirements)
* [Getting Started](#getting-started)
    * [Prerequisites](#prerequisites)
    * [Installation](#installation)
    * [Configuration](#configuration)
* [Usage](#usage)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)
* [Acknowledgments](#acknowledgments)

---

## About

The **ESPHome Watermeter** project aims to provide an open-source solution for monitoring water consumption using mechanical water meter with open contact .
Whether you want to track your household's water usage, detect leaks, or simply gain insights into your water habits, this project offers a flexible and extensible platform to do so. 
It leverages **ESP32 board, mechanical watermeter ENBRA ER-AM and ENBRA AT-MBUS-NE-02** to provide real-time data and historical data for HomeAssistant. It shows real rate and Total consumption , which is stored it ESP32 itself.  

---

## Features

* **Real-time Water Usage Monitoring:** Get instant readings of water flow.
* **Historical Data Logging:** Store  water consumption in ESP32 flash memory.
* **Leak Detection Alerts:** (Optional, if implemented) Receive notifications for unusual water usage patterns, using Automations in HomeAssistant.
* **Data Visualization:** (Optional, if integrated with a dashboard) View consumption trends through graphs and charts in HomeAssistant.
* **Remote Accessibility:** (Optional, if using an HomeAssistant and remote access) Monitor your water usage from anywhere.
* **Low Power Consumption:**  Designed for efficient operation. 
* **Modular Design:** Easy to adapt and extend with different sensors or platforms.

---

## Hardware Requirements

To get started with the Watermeter project, you'll need the following hardware components:

* **Microcontroller:** e.g., ESP32 board
* **Water Meter:** ENBRA ER-AM
* **Impulse Module:** ENBRA AT-MBUS-NE-02 
* **Power Supply:**  5V power adapter
* **Box**
* **Wiring**
* **Pipes and Fittings:** For integrating the flow meter into your water line.

---

## Software Requirements

* **ESPHome**  
* **HomeAssistant** (Optional) 
* **Data Visualization Platform:** (Optional) e.g., Grafana, Home Assistant

---

## Getting Started

Follow these instructions to set up and run the Watermeter project.

### Prerequisites

* Basic understanding of electronics and microcontrollers.
* Basic understanding of ESPHome.

### Hardware
* Thats easy part. Just connect your pulse module directly to ESP32 board . Green wire to GND on ESP32 , brown wire e.g. to G13  

### Installation

1.  Install HomeAsistant
2.  Install Add-On ESPHome Device Builder
3.  Open New Device
4.  Copy watermeter-main.yaml
5.  Configure
6.  Connect ESP32 board & Install 

### Configuration

1.  Modify water-meter.yaml
2.  pin: GPIO13     - modify where did you connect your water meter pulse module
3.  Modify IP address ifto your needs  
    #manual_ip:
    static_ip: 192.168.3.208 # XXX
    gateway: 192.168.3.254 # XXX
    subnet: 255.255.255.0 # XXX

## Usage

Once the Watermeter is set up and running, it will start collecting water usage data. 

* **Real-time Monitoring:** Data will be sent to your HomeAssistant 
* **Data Analysis:** Add at Homeassistant/Energy/.../Energy Configuration/Water consumption/Add Entity Watermeter main Total water consumption  
* **Leak Detection:** (If implemented) Set up alerts on your HASS to notify you of continuous unexpected water flow using Automations.

---

## Contributing

We welcome contributions to the Watermeter project! If you have ideas for improvements, bug fixes, or new features, please follow these steps:

1.  **Fork** the repository.
2.  **Create a new branch** (`git checkout -b feature/your-feature-name`).
3.  **Make your changes** and commit them (`git commit -m 'Add new feature'`).
4.  **Push** to your branch (`git push origin feature/your-feature-name`).
5.  **Create a Pull Request** to the `main` branch of this repository.

Please ensure your code adheres to the existing style and includes relevant documentation.

---

## License

This project is licensed under the ** GPLv3 License**. See the `LICENSE` file for details.

---

## Contact

If you have any questions, suggestions, or just want to get in touch, feel free to:

* Open an issue on GitHub.

---

## Acknowledgments

* Thanks to [**Milo**].
