# CAN-Based Network Traffic Management System

### A C2000-Based Real-Time CAN Traffic Monitoring and Adaptive Message Scheduling System

---

## 📌 Project Overview

The CAN-Based Network Traffic Management System is an embedded application designed to monitor Controller Area Network (CAN) communication in real time, identify network congestion, and intelligently manage message transmission based on priority and timing constraints.

In automotive and other real-time embedded applications, multiple electronic control units (ECUs) communicate over a shared CAN bus. During periods of high network traffic, important messages may experience increased waiting times and deadline violations.

This project proposes an adaptive traffic management mechanism that monitors communication parameters and prioritizes time-critical messages while allowing non-critical, delay-tolerant traffic to be temporarily deferred.

## 🎯 Objectives

- Monitor CAN bus communication in real time.
- Measure bus utilization and message arrival frequency.
- Analyse message waiting time and queue length.
- Detect network congestion and deadline violations.
- Develop an adaptive, deadline-aware message scheduling mechanism.
- Preserve time-critical communication during high traffic conditions.
- Independently verify transmitted and received CAN messages.

## ⚙️ Proposed System Architecture

The system is designed around a TI C2000 microcontroller and CAN communication interfaces.

### Major Hardware Components

| Component | Purpose |
|---|---|
| TI C2000 Microcontroller | Main processing and scheduling unit |
| MCP2515 CAN Controller | CAN message handling |
| MCP2562FD CAN Transceiver | CAN physical-layer interface |
| CAN Bus Interface | Communication between CAN nodes |
| Crystal Circuit | Clock generation for CAN controller |
| Termination Circuit | CAN bus signal termination |
| Status Indicators | Visual indication of system status |

The C2000 LaunchPad is used as an external development platform and interfaces with the custom-designed PCB through header connections.

## 🧠 Working Principle

The proposed system operates through the following stages:

**1. CAN Traffic Reception**

Incoming CAN messages are received and processed through the CAN communication interface.

**2. Traffic Monitoring**

The system analyses important communication parameters, including:
- Message ID
- Message arrival time
- Message frequency
- Bus utilization
- Waiting time
- Queue length
- Message deadline

**3. Congestion Detection**

The monitored parameters are evaluated to identify high bus-load conditions and potential communication delays.

**4. Adaptive Message Scheduling**

A scheduling mechanism evaluates message criticality and timing constraints to determine transmission order.

Time-critical messages are prioritised, while non-critical and delay-tolerant messages may be temporarily deferred during congestion.

**5. Communication Verification**

An independent CAN monitoring node checks the transmitted message ID and data against the received message.

A PASS/FAIL result is determined based on the comparison.

## 🔬 Key Features

- Real-time CAN traffic monitoring.
- Bus utilization analysis.
- Congestion detection.
- Deadline-aware message scheduling.
- Adaptive traffic management.
- Independent CAN transmission and reception verification.
- Communication status validation.

## 🛠️ Technologies Used

| Category | Technology |
|---|---|
| Microcontroller | TI C2000 |
| CAN Controller | MCP2515 |
| CAN Transceiver | MCP2562FD |
| Programming Language | Embedded C |
| Communication Protocol | CAN |
| Peripheral Interface | SPI |
| PCB Design | KiCad |
| Development Environment | Code Composer Studio |

## 📂 Repository Structure

```text
CAN-BASED-NETWORK-TRAFFIC-MANAGEMENT/
│
├── README.md
│
├── Documentation/
│   └── README.md
│
├── Hardware/
│   └── README.md
│
├── Firmware/
│   └── README.md
│
├── Testing/
│   └── README.md
│
└── Images/
    └── README.md
```

## 📊 Project Development Status

| Development Stage | Status |
|---|---|
| Project Concept and Architecture | Completed |
| Circuit Schematic Design | Completed |
| Electrical Rule Check (ERC) | Passed |
| Footprint Assignment | Completed |
| PCB Layout and Routing | In Progress |
| PCB Fabrication | Pending |
| Hardware Assembly | Pending |
| Firmware Development | Pending |
| CAN Communication Testing | Pending |
| Adaptive Scheduling Validation | Pending |

## 🎯 Expected Outcomes

- Reliable monitoring of CAN communication.
- Identification of network congestion conditions.
- Improved handling of time-critical messages.
- Reduced unnecessary delays for critical communication.
- Verified CAN message transmission and reception.
- Demonstration of adaptive traffic management in real-time embedded applications.

## 👩‍💻 Project Information

**Project Title:** CAN-Based Network Traffic Management System

**Domain:** Embedded Systems and Automotive Electronics

**Platform:** TI C2000

**PCB Design Tool:** KiCad

**Project Type:** Individual Academic Project

**Project Duration:** August 2026 – November 2026

**Mentor:** Sivasundar

---

*This project is currently under development. Hardware implementation, firmware integration and experimental validation are being carried out progressively.*
