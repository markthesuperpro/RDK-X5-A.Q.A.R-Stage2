# Autonomous-Quadruped-Assisting-Robot-A.Q.A.R

**Robotics Dream Keeper Challenge — Winter 2026**

- **Participant:** Mark
- **Project:** RDK X5-Autonomous-Quadruped-Monitoring-Robot
- **Current stage:** Stage 2 — Build
- **Hardware:** D-Robotics RDK X5 + ESP32
- **Repository status:** Development

---

## Project Overview

**Target data flow:**

`Sensors → RDK X5 (TROS / ROS 2) → SLAM → Nav Firmware → ESP32 → Servos`

**Target Perception Pipeline:**

`Camera → AI Perception → Monitoring Events`

The RDK X5 performs navigation and sensory calculations. The ESP32 handles motor control and converts movement commands into quadruped locomotion.

See [ARCHITECTURE.md](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/ARCHITECTURE.md) for the complete system design, ROS 2 interfaces, compute allocation and failure handling.

## Hardware

| Component | Model / Specification | Purpose |
|---|---|---|
| Development board | D-Robotics RDK X5 | Main computing platform |
| Storage | microSD card | System storage and Boot Firmware |
| ESP32 | ESP32 DEVKIT | Motor Controller |
| Camera | - | Video Stream |
| LiDar | - | Sensory |
| 3D Parts (for robot) | Made with PETG | Robot foundations |
| Servo Motors | microServo | Robot movement |
| Development PC | Laptop | Development and remote access |

### Hardware Setup

![Hardware setup](evidence/hardware.png)
*stage 1*

**Connection details:**
| Component | Connection | Purpose |
|---|---|---|
| Development board | USB Port+Cable | Remote desktop |
| MicroSD card | MicroSD card port | System storage and Boot Firmware |
| Camera | UDP | Video Stream |
| ESP32 | UDP | Motor Controller |
| LiDar Sensor | Serial | Environment detection |
| USB power supply cable | USB cable + Adapter | Charging RDK |
| Development laptop | - | Programming and Screen |


## Tested Software Environment

| Component | Version / Configuration |
|---|---|
| RDK OS | [RDK OS v3.5.0 Image](https://archive.d-robotics.cc/downloads/os_images/rdk_x5/rdk_os_3.5.0-2026-4-9/rdk-x5-ubuntu22-preinstalled-desktop-3.5.0-arm64.img.xz) |
| Ubuntu | Ubuntu 22.04.5 LTS (GNU/Linux 6.1.83 aarch64) |
| Linux kernel | v6.1.83 |
| CPU architecture | aarch64 |
| Python | 3.15.2 |
| ROS 2 | Humble |
| SLAM | TBD |
| Nav Firmware | Humble |
| Other dependencies | ffmpeg* |

# Stage 1 - Ignite

### Architecture Explanation

1. **Input:** Image captured from either the USB Camera or the web
2. **Inference / Logic:** Data is processed through the demo programs
3. **Output:** Displayed Via FFmpeg in the terminal

## Prerequisites and Dependencies

### Hardware Requirements

- RDK X5 hardware
- USB webcam
- microSD card and USB MicroSD card reader
- 2x USB cables + Adapters

### Software Requirements

- [RDK OS v3.5.0 Image](https://archive.d-robotics.cc/downloads/os_images/rdk_x5/rdk_os_3.5.0-2026-4-9/rdk-x5-ubuntu22-preinstalled-desktop-3.5.0-arm64.img.xz)
- Python 3.15.2

## Installation and Setup

See the Stage1_setup guide here: 
[Stage1_guide](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/STAGE1_SETUP.md)

# Stage 2 — Build

The next step is to start connecting each of the components and wrapping things up.

|Document|Description|
|--------|-----------|
| [PROPOSAL.md](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/PROPOSAL.md) | Concepts, Intended Use, Solutions, Progress Status, etc. |
| [ARCHITECTURE.md](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/ARCHITECTURE.md) | System Flow, Components, Node_lists, Safety |
| [ROADMAP.md](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/ROADMAP.md) | Tasks milestones |
| [ENGINEERING_PLAN.md](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/blob/main/docs/ENGINEERING_PLAN.md) | BOM, Five Risks, Repo structure |

https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2
## Results and Verification

Record actual observations from your experiments.

| Test | Configuration | Actual Result | Status |
|---|---|---|---|
| System boot | N/A | System boot successfully | ok. |
| Network / SSH | Enabled | Successful SSH | working. |
| Sensor | Webcam connected | Can transmit Photo and Video | working. |
| AI inference (#TODO) | N/A | N/A | N/A |
| Actuator | Enabled | Working, 90 degree test and calibration test yeild great result. | working. |

### Performance Measurements (#TODO)

Only include measurements you have actually taken.

| Metric | Measurement | Test Conditions |
|---|---|---|
| Inference latency | N/A | - |
| Inference throughput | N/A | - |
| CPU utilization | N/A | - |
| BPU utilization | N/A | - |
| Memory usage | N/A | - |
| Temperature | N/A | - |
| Power consumption | N/A | - |

### Additional Evidence

- [Demonstration video](YOUR_VIDEO_LINK) - (#TODO)
- [Detailed experiment report](https://github.com/markthesuperpro/RDK-X5-A.Q.A.R-Stage2/tree/main/docs)

## Next Challenge Stages

| Stage | Planned development |
|---|---|
| Stage 1 — Ignite | Initial hardware and AI demonstration |
| Stage 2 — Build | Further development and integration |
| Stage 3 — Launch | Complete project demonstration and evaluation |

## License

This project's original materials are licensed under MIT License.

See [LICENSE](LICENSE) for details.

Third-party components remain subject to their respective licenses.

## Challenge Information

**Program:** Robotics Dream Keeper Challenge 2026 Winter

**Organizer:** D-Robotics

**Current stage:** Stage 2

- [Official Challenge Repository](https://github.com/D-Robotics/Robotics-Dream-Keeper-Challenge-Winter)
- [Project Showcase](https://github.com/D-Robotics/Robotics-Dream-Keeper-Challenge-Winter/blob/main/projects/Mark-Project-rdk-x5-stage1-demo.md)
- [Community Update](https://discord.com/channels/1300358874280230994/1503706103752429618/threads/1565947368782831757)
