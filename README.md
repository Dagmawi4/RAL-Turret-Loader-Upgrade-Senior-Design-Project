# RAL Turret Loader Upgrade (Senior Design Project)

## Overview
This project modernizes and automates the core loading system on the RAL production line at **Taylor Corporation – Label Works Division**.  
The original system was an outdated, relay-based control process requiring significant manual operation and prone to inefficiencies.  
Our team designed and implemented a **PLC-based automated solution** centered on an **Allen-Bradley Micro820 controller**, programmed in **Connected Components Workbench (CCW)**.  

The new system:
- **Fully automates core feeding and loading** from a vibratory bowl feeder to a turret rewinder.
- **Improves reliability, efficiency, and scalability** of the RAL line.
- **Enhances safety** through integrated interlocks and emergency stop handling.
- Provides a **clean, maintainable electrical system** designed to industrial standards.

This project served as a bridge between academic theory and professional engineering practice, giving our team hands-on experience with industrial automation, electrical panel design, and system integration.

---

## Features
- **Automated Core Handling**
  - Transfers cardboard cores from a **vibratory bowl feeder**.
  - Moves cores along a **belt conveyor** with integrated sensor feedback.
  - Rotates and loads cores into the **CTC turret rewinder** via pneumatic actuators.
- **PLC-Controlled Sequences**
  - Step-by-step MOV-based logic for each process stage.
  - TON/RTO timers for synchronization.
  - Power-up reset logic and fault recovery routines.
- **Industrial Electrical Panel**
  - Designed in **AutoCAD Electrical** with labeled wiring, power distribution, and I/O mapping.
  - Integrates IFM safety controller (G1501S), terminal blocks, relays, fuses, and VFD for the conveyor.
- **Safety-First Design**
  - Dedicated E-stop loop with dual-channel verification.
  - Sensor interlocks to prevent unsafe operation.
  - Compliant with **NFPA 79**, **UL 508A**, **IEC 61131-3**, **OSHA**, and **NEC** standards.

---

## Hardware and Tools
- **Allen-Bradley Micro820 PLC (2080-LC20-20QWB)** – primary logic controller.
- **IFM G1501S Safety Controller** – emergency stop and safety loop management.
- **IFM DN4013 24VDC Power Supply** – powers sensors, solenoids, and PLC.
- **Oriental Motor BLE2D60-A Drive** – controls the conveyor motor.
- Pneumatic solenoids for:
  - Bowl feeder
  - Core stop gate
  - Vacuum pickup
  - Rotation and actuator extension
- **AutoCAD Electrical** for wiring schematics and panel layout.
- **Connected Components Workbench (CCW)** for ladder logic development and testing.

---

## How the System Works
1. **Bowl Feeder** orients and unloads cardboard cores onto a belt.  
2. **Core Transport** subsystem moves the core via conveyor and gate, guided by sensors.  
3. **Core Rotate & Load** subsystem uses vacuum pickup and rotation to place the core into the turret rewinder.  
4. **PLC Sequencer** manages each phase using modular steps and timers, advancing only when sensors verify conditions.  
5. **Safety Controller** monitors the system continuously, halting all motion on E-stop or fault.

---

## Repository Contents

- [Images](./Images) – Photos of the control panel, schematics, CAD models, and system hardware  
- [Videos](./Videos) – Demo videos of the system in operation  
- [Documentation](./Documentation) – Final project report, presentation slides, wiring diagrams, and schematics  
- [PLC_Code](./PLC_Code) – Connected Components Workbench (.ccwarc) project file and ladder logic PDFs  
- [README.md](./README.md) – Project overview (this file)


---

## Opening the PLC Program
1. Download the `.ccwarc` archive from the `/PLC_Code` folder.  
2. Open in **Connected Components Workbench (CCW)**.  
3. Ladder logic PDFs are also included for quick review without CCW.

---

## Team & Collaboration
This project was completed by:
- **Dagmawi Abera**
- **Omar Elkenawy**
- **Hamede Abdulgafur**

With special thanks to:
- **Lance Noska** (Controls Engineer, Taylor Corporation) – Project mentor and technical advisor.  
- **Jeff** – Assistance with panel wiring and assembly.  
- The **Taylor Corporation engineering team** for sponsorship and real-world integration support.

---

## Future Recommendations
- **HMI Interface** for operator control and live system feedback.  
- **Diagnostic indicators (LEDs/status lights)** on the control panel for fast troubleshooting.  
- **Modular I/O expansion** to accommodate future features.  
- **Cycle timing optimization** to maximize throughput.  
- Enhanced documentation (e.g., QR-coded wiring references for quick maintenance).

---

## License
This repository is intended for **academic and portfolio use**.  
For commercial deployment or adaptation, please contact the project authors.

