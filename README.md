# RTL-to-GDSII Implementation of a Multiply-Accumulate (MAC) Unit

> Complete ASIC implementation of a synthesizable Multiply-Accumulate (MAC) Unit using **Verilog HDL**, **Cadence** for functional verification, and **OpenLane (Sky130 PDK)** for RTL-to-GDSII physical design.

![Verilog](https://img.shields.io/badge/Language-Verilog-blue)
![OpenLane](https://img.shields.io/badge/OpenLane-RTL--to--GDS-success)
![Sky130](https://img.shields.io/badge/PDK-Sky130-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

# Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Design Specifications](#design-specifications)
- [Repository Structure](#repository-structure)
- [MAC Architecture](#mac-architecture)
- [RTL Design](#rtl-design)
- [Functional Verification](#functional-verification)
- [Physical Design Flow](#physical-design-flow)
- [Results](#results)
- [Tools Used](#tools-used)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

# Project Overview

The **Multiply-Accumulate (MAC) Unit** is one of the most fundamental arithmetic blocks used in Digital Signal Processing (DSP), Artificial Intelligence (AI) accelerators, processors, image processing systems, and embedded applications.

This project presents the complete implementation of a synthesizable MAC Unit following a modern ASIC design methodology. The design was developed in **Verilog HDL**, functionally verified using **Cadence simulation tools**, and physically implemented using the **OpenLane RTL-to-GDSII flow** with the **Sky130 Process Design Kit (PDK)**.

The objective of this project is to demonstrate an end-to-end digital ASIC design flow, beginning with RTL design and verification, followed by synthesis, floorplanning, placement, clock tree synthesis (CTS), routing, timing verification, DRC analysis, and final GDSII generation.

---

# Features

- RTL implementation using Verilog HDL
- Modular MAC architecture
- Functional verification using Cadence
- Self-contained Verilog testbench
- RTL-to-GDSII implementation using OpenLane
- Logic synthesis
- Floorplanning
- Standard cell placement
- Clock Tree Synthesis (CTS)
- Global and Detailed Routing
- Static Timing Analysis (STA)
- Design Rule Checking (DRC)
- GDSII Layout Generation

---

# Design Specifications

| Parameter | Description |
|-----------|-------------|
| Design | Multiply-Accumulate (MAC) Unit |
| HDL | Verilog HDL |
| Verification | Cadence |
| Physical Design | OpenLane |
| PDK | Sky130 |
| Flow | RTL → GDSII |
| Output | GDSII Layout |

---

# Repository Structure

```
MAC-Unit-OpenLane
│
├── rtl/
├── testbench/
├── simulation/
│   ├── waveforms/
│   ├── reports/
│   └── screenshots/
│
├── openlane/
│   ├── gds/
│   ├── reports/
│   └── screenshots/
│
└── README.md
```

---

# MAC Architecture

The MAC unit performs the following operation:

```
Output = (A × B) + Accumulator
```

The design consists of the following major components:

- Multiplier
- Adder
- Accumulator Register
- Control Logic
- Output Register

> **Architecture diagram will be added here.**

---

# RTL Design

The RTL design was developed using **Verilog HDL** with a modular architecture to improve readability, scalability, and verification.

The design includes:

- MAC module
- Multiplier
- Adder
- Accumulator
- Control logic

The source files are available in the `rtl/` directory.

---

# Functional Verification

The functionality of the MAC Unit was verified using **Cadence** simulation tools.

The verification process included:

- Reset operation
- Clock synchronization
- Multiplication functionality
- Accumulation over multiple cycles
- Functional correctness verification

Waveform screenshots are available in the `simulation/waveforms/` directory.

> **Cadence waveform images will be added here.**

---

# Physical Design Flow

After functional verification, the RTL design was implemented using the **OpenLane RTL-to-GDSII flow**.

The physical implementation consists of the following stages:

- RTL Synthesis
- Floorplanning
- Power Planning
- Standard Cell Placement
- Clock Tree Synthesis (CTS)
- Global Routing
- Detailed Routing
- Static Timing Analysis (STA)
- Design Rule Checking (DRC)
- GDSII Generation

Screenshots from each stage are available in the `openlane/screenshots/` directory.

---

# Results
The final implementation successfully completed the RTL-to-GDSII flow using the Sky130 PDK. Functional verification was performed in Cadence, followed by physical implementation in OpenLane.

| Metric | Value |
|--------|------:|
| Standard Cells | **268** |
| Number of Wires | **257** |
| Chip Area | **2882.7648 µm²** |
| Worst Setup Slack | **+6.67 ns** |
| Worst Hold Slack | **+0.29 ns** |
| Total Negative Slack (TNS) | **0.00 ns** |
| Worst Negative Slack (WNS) | **0.00 ns** |


| Stage | Status |
|--------|--------|
| RTL Design | ✅ Completed |
| Functional Verification | ✅ Passed |
| Logic Synthesis | ✅ Completed |
| Floorplanning | ✅ Completed |
| Placement | ✅ Completed |
| CTS | ✅ Completed |
| Routing | ✅ Completed |
| Timing Analysis | ✅ Passed |
| DRC Verification | ✅ Completed |
| GDSII Generation | ✅ Successful |

---

# Tools Used

| Tool | Purpose |
|------|----------|
| Verilog HDL | RTL Design |
| Cadence | Functional Verification |
| OpenLane | RTL-to-GDSII Flow |
| OpenROAD | Physical Design |
| Magic | Layout Visualization |
| Netgen | LVS Verification |
| Sky130 PDK | Standard Cell Library |

---

# Future Improvements

- Parameterizable MAC architecture
- Signed arithmetic support
- Booth Multiplier implementation
- Wallace Tree Multiplier
- Pipelined MAC architecture
- Power analysis and optimization
- Formal verification

---
