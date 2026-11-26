# Engineering Plan — Autonomous Quadruped Monitoring Robot

> **Stage:** 2 — Build · **Platform:** D-Robotics RDK X5 + TROS  
> **Related:** [Proposal](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/PROPOSAL.md) · [Architecture](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/ARCHITECTURE.md) · [Roadmap](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/ROADMAP.md)  
> **Scope:** A quadruped robot with an ability to navigate anywhere accross the room and monitor eldery.

## 1. Bill of Materials (BOM)

Hardware required for the current prototype and final demonstration. Costs are estimates; include only relevant components.

| # | Component | Qty | Supplier / Model / SKU | Voltage & Interface | Status | Est. Cost |
|---|-----------|-----|------------------------|---------------------|--------|-----------|
| 1 | RDK X5 | 1 | D-Robotics | 5V / 5A USB-C; Ethernet | In use | $100 |
| 2 | ESP32 DevKit | 1 | ESP32 DevKit | 5V; 3.3V GPIO; Communication | In use | – |
| 3 | Camera | 1 | - | 5V | Integrating | – |
| 4 | Servo Motors | 12, TBD | miniServo | - | Installed | $35 |
| 5 | Light sensors | 1 | - | 5V | Planned | – |
| 6 | Power system | 1 | Battery / regulator | 5V | Planned | – |
| 7 | 3D parts | 3 | PETG | – | Built | $0 (Self-Print) |
| 8 | Storage | 1 | microSD | SD interface | In use | $15 |

## 3. Top Five Risks

Project-specific risks, their observable triggers, preventive measures and practical fallbacks.

| # | Risk | Trigger | Mitigation |
|---|------|---------|------------|
| 1 | Lidar measurements unsuitable for mapping | Unstable or invalid range data / scan | Recalibration before SLAM integration |
| 2 | ESP32–RDK communication failure | Dropped messages, timeout or stale commands | Implement communication monitoring and command timeouts |
| 3 | Servos overheat | Unexpected power surges/ Inconsistency in commands | Replace Servo |

## 4. Planned Repository Structure

```text
rdk-x5-stage1/
├── README.md
├── ROADMAP.md
├── PROPOSAL.md
├── ARCHITECTURE.md
├── LICENSE
├── requirements.txt
├── src/
├── evidence/
    ├── Flash_ssh.log
    ├── Sensor.png
    ├── Yolo11_demo.png
    ├── Yolo11_original.png
    ├── hardware.png
└── docs/
    └── ENGINEERING_PLAN.md
```

> **Planning principle:** Detailed task tracking belongs in `ROADMAP.md`. This document summarizes the hardware, milestones, engineering risks and intended code organization. Mark work complete only when its acceptance criteria have been verified.
