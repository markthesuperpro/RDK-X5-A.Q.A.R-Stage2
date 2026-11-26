## Installation and Setup

### 1. Prepare the RDK X5

- Download system image via [RDK OS v3.5.0 Image](https://archive.d-robotics.cc/downloads/os_images/rdk_x5/rdk_os_3.5.0-2026-4-9/rdk-x5-ubuntu22-preinstalled-desktop-3.5.0-arm64.img.xz)
- Download [Rufus](https://rufus.ie/en/)
______________________________________________________________________________________________________________________________________________________________
- 1.Boot up rufus and flash the system image downloaded into the MicroSD card attached via the USB MicroSD card reader.
- 2.Disconnect the card reader and put the MicroSD card into the RDK x5 board's microSD card slot.
- 3.Boot up RDK board via USB charging port using a USB adapter (+cable).

## 2. Connect to the RDK X5

### 1.Booting up RDK os

- After booting up the board with RDK os successfully, proceed with [RDK Studio](https://developer.d-robotics.cc/en/rdkstudio?ref=drobotics.ghost.io) software
- Next, connect the pc with the board via a USB cable connected by the USB quicklink port.
- Inside RDK Studio, signin with your account and click into <Device & Development> tab and select <Remote Desktop>

### 2.Setting up SSH

- In OS desktop, select Applications>RDK Configuration, there a terminal window will popup.
- In the terminal window, use the arrow keys to select <I1 SSH>, press enter and enable the SSH service
- Finally, exit the terminal window and use the cmd or powershell from your laptop to ssh to the board using this command:
  
```bash
ssh root@<<Your board IP>>
```

**Evidence:**

[SSH Connection](evidence/Flash_ssh.log)

## Running the Demo

### 1. Navigation

Navigate to the /app/pydev_demo/ and select the demo as of your uses. For this exampke I'll be using pose detection:

```bash
cd /app/pydev_demo/04_pose_sample/01_ultralytics_yolo11_pose/
```

### 2. Run the Demo

Run the demo by using python:

```bash
python ultralytics_yolo11_pose.py
```

### 3. Model Output

## Original.png
![AI model output](evidence/Yolo11_original.png)

## Result
![AI model output](evidence/Yolo11_demo.png)

**Observed result:**

The model successfully identifies the people walking on the crosswalk.
