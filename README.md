# Industrial Data Architectures in Practice — Companion Repository

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

This repository contains the companion software for **_Industrial Data Architectures in Practice: A Hands-On Guide to Building Scalable Systems from PLC to Cloud, Unified Namespace, and AI_**.

It provides the practical implementations built progressively throughout the book, following a single continuous use case — a bottling production line — from the PLC layer through communication, the Unified Namespace, and beyond.

---

## 📂 Repository Structure

```
.
├── plc/        # PLC program and configuration (TIA Portal project)
├── nodered/    # Node-RED flows for edge data processing and MQTT publishing
├── emqx/       # EMQX MQTT broker configuration (docker-compose + backup)
├── ignition/   # Ignition SCADA/UNS project export (BottlingLine_UNS)
└── LICENSE
```

Each folder contains its own `README.md` with setup instructions, dependencies, and import steps specific to that component.

---

## 🚀 How to Use This Repository

The components are designed to be set up in the order they appear in the book:

| Step | Component | What it does |
|------|-----------|---------------|
| 1 | **PLC** | Deploy the base process logic and expose data via OPC UA |
| 2 | **Node-RED** | Connect to the PLC and publish data via MQTT |
| 3 | **EMQX** | Run the MQTT broker that receives the published data |
| 4 | **Ignition** | Build the Unified Namespace and persist data for analytics |

Refer to the corresponding chapter in the book for the full explanation and context behind each step. Each component's README explains prerequisites, required credentials (not included for security reasons), and how to import/restore it in your own environment.

---

## 🛠 Requirements

- [Docker](https://www.docker.com/) (for EMQX)
- [Node-RED](https://nodered.org/)
- [Siemens TIA Portal](https://www.siemens.com/) (for the PLC project)
- [Ignition](https://inductiveautomation.com/) (Inductive Automation)

---

## 🔒 A Note on Credentials

For security reasons, none of the files in this repository include real credentials (passwords, API keys, connection secrets). Where applicable, each component's README explains what needs to be configured manually (database connections, broker authentication, OPC UA endpoints) before the system will run end to end.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## ✍️ About

Written by **Adrian Daniel Martin** — University Lecturer at Politehnica University of Timișoara and MES/MOM Senior Automation Analyst at Accenture, with 10+ years of industrial experience in automation, machine integration, and IIoT architectures.
