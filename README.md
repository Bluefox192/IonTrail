# 🛰️ IonTrail
> **Long-range telemetry for rockets and robots.**

[![License: Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-green.svg)](./LICENSE)
[![Tech: LoRa + GPS](https://img.shields.io/badge/tech-LoRa%20%7C%20GPS-blue.svg)]()
[![Status: Planning](https://img.shields.io/badge/status-planning-yellow.svg)]()

**IonTrail** is an open-source telemetry system designed to track rockets, ground robots, and other mobile systems using low-power, long-range radio (LoRa) combined with GPS. Built with modularity and reliability in mind, IonTrail aims to serve as a plug-and-play solution for aerospace and robotics hobbyists, students, and engineers.

---

## 🚀 Goals

- 📡 **Real-time location updates** via GPS.
- 🌐 **LoRa-based telemetry** with an estimated range of **1–10 km** (line-of-sight).
- 🔌 Seamless **integration with [AphelionCtrl](https://github.com/bluefox192/AphelionCtrl)** (flight or ground control system).
- 🔋 **Low power consumption** for long-duration missions.

---

## 🗂️ Project Structure

```plaintext
/iontrail
├── transmitter/     # Code and configuration for the onboard module
├── receiver/        # Ground station LoRa receiver + GPS data parser
└── dashboard/       # Data visualization interface (CLI / Web)
````

Each directory is designed to be self-contained and independently testable.

---

## 📊 Dashboard (Planned)

* **Mode 1:** Web Serial API (Chrome) for direct USB telemetry plotting.
* **Mode 2:** Python interface using `pyserial` + `matplotlib` for fast prototyping and debugging.

> Future support for saving `.csv` logs, real-time map plotting, and packet loss metrics.

---

## 🔧 Tech Stack

* **LoRa Module:** e.g., SX1278 or RFM95
* **GPS Module:** e.g., NEO-6M / u-blox M8
* **Microcontroller:** Arduino, ESP32, or STM32 (TBD)
* **Language:** C++ (MCU), Python (Ground Station), JS/HTML (Dashboard Option)

---

## 📌 To Do

* [ ] Finalize hardware selection
* [ ] Transmitter firmware: GPS read + LoRa TX
* [ ] Receiver firmware: LoRa RX + Serial out
* [ ] Dashboard plotting MVP
* [ ] Power benchmarking + sleep modes

---

## 🤝 Contributing

Contributions, feedback, and ideas are welcome! Please open an issue or pull request. For significant changes, consider discussing via an issue first.

---

## 📄 License

This project is licensed under the [Apache 2.0 License](./LICENSE) — free for both personal and commercial use with proper attribution.

---

> IonTrail is part of a broader initiative to build reliable open-source aerospace and robotics systems. Stay tuned.
