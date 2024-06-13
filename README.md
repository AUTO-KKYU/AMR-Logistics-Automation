# AMR Logistics Automation System
<div align="center">
    <img src="https://github.com/addinedu-ros-4th/ros-repo-2/assets/118419026/dd1da530-6c66-4815-94ef-1b23f385e5c4" width="700" height="300">
</div>

## Table of Contents
  * [1. 🤖Project Introduction](#1-project-introduction)
    + [1.1. Project Overview](#11-project-overview)
    + [1.2. Project Position](#12-project-position)
    + [1.3. Tech Stack](#13-tech-stack)
  * [2. 📋Role Contributions](#2-role-contributions)
    + [2.1. System Architecture](#21-system-architecture)
    + [2.2. Hardware Architecture](#22-hardware-architecture)
    + [2.3. 3D Pose Estimation](#23-3d-pose-estimation)
      - [2.3.1. Camera Calibration](#231-camera-calibration)
      - [2.3.2. ArUCo Navigation](#232-aruco-navigation)
    + [2.4. Human Following](#24-human-following)
  * [3. ✅Prerequisite](#3-prerequisite)


## 1. 🤖Project Introduction
**Duration: 2024.04.17 - 2024.06.13**

### 1.1. Project Overview
- Utilizing forklift frame-based autonomous driving robots in logistics processes such as inbound, outbound, and collection.
- Implementing a multi-robot control system to enhance the efficiency of logistics operations.
- Optimizing logistics center operations through Human-Robot Interaction (HRI).
- Implementing systems for inbound product registration, shelf inventory management, and consumer order processing.

<img src="https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/25960a9e-af9d-46dc-9f70-1cfc5d5e6168">

### 1.2. Project Position
<table>
  <thead>
    <tr>
      <th style="text-align:center;">Name</th>
      <th style="text-align:center;">Classification</th>
      <th style="text-align:center;">Role</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center;">DONG GYU KIM</td>
      <td style="text-align:center;">Team Member</td>
      <td>- ArUco Navigation <br> - DL based Human Following Robot <br> - Analysis User/System Requirement <br> - Architecture and Algorithm Design <br> - Setting up Driving Environment <br> - Confluence Management </td>
    </tr>
  </tbody>
</table>




### 1.3. Tech Stack
||||
|:---:|:---|:---|
|**Develop EnV**|<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=Ubuntu&logoColor=white"> <img src="https://img.shields.io/badge/VISUAL STUDIO CODE-007ACC?style=for-the-badge&logo=VisualStudioCode&logoColor=white">|
|**TECH**|<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54"> <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white"> <img src="https://img.shields.io/badge/ros2-%2322314E?style=for-the-badge&logo=ros&logoColor=white"> <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white"> <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white"> <img src="https://img.shields.io/badge/PyQt5-%23217346.svg?style=for-the-badge&logo=Qt&logoColor=white"> <img src="https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white"> |
|**H/W**|<img src="https://img.shields.io/badge/-RaspberryPi 4-C51A4A?style=for-the-badge&logo=Raspberry-Pi"> <img src="https://img.shields.io/badge/-Arduino Mega-00979D?style=for-the-badge&logo=Arduino&logoColor=white">|
|**COMMUNICATION**|<img src="https://img.shields.io/badge/confluence-%23172BF4.svg?style=for-the-badge&logo=confluence&logoColor=white"> <img src="https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white"> <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=Slack&logoColor=white">  <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">|

## 2. 📋Role Contributions

### 2.1. System Architecture

<img src="https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/9a9e5e40-1a1d-45e5-b85e-094c319c2f4b">

### 2.2. Hardware Architecture
<img src= "https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/5f911581-c86e-44b8-a48b-21adc2f979da">

### 2.3. 3D Pose Estimation

#### 2.3.1. Camera Calibration
<img src= "https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/ed869dcf-58b9-48e1-8ad6-d9a389a769ce">

#### 2.3.2. ArUCo Navigation
<img src= "https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/acb06277-3130-40a1-b1d1-ec2a3675a078">

### 2.4. Human Following
<img src="https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/eeb94530-05e6-4cb7-ba7e-3fccffb6b9e1">

## 3. ✅Prerequisite

**How to install ROS2 Humble on PC [Ubuntu 22.04]**
- Follow the guidelines within the site
    - environment : https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html
    - dev tools : https://docs.ros.org/en/humble/Installation/Alternatives/Ubuntu-Development-Setup.html#install-development-tools-and-ros-tools
    - colcon : https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Colcon-Tutorial.html#install-colcon

**ArUCo version on OpenCV**
```sh
pip install opencv-contrib-python==4.7.0.68 opencv-python==4.7.0.68
```

**Raspberry pi 4 GPIO settings**
```sh
# GPIO 그룹 설정
sudo groupadd gpio
# 사용자를 gpio 그룹에 추가
sudo usermod -aG gpio kkyu_rasp
# udev 규칙 파일 설정
sudo nano /etc/udev/rules.d/99-gpio.rules
# udev 규칙 내용 작성
SUBSYSTEM=="gpio*", PROGRAM="/bin/sh -c '\\
chown -R root:gpio /sys/class/gpio && chmod -R 770 /sys/class/gpio;\\
chown -R root:gpio /sys/devices/virtual/gpio && chmod -R 770 /sys/devices/virtual/gpio;\\
chown -R root:gpio /sys$devpath && chmod -R 770 /sys$devpath\\
'"
# udev 규칙 적용
sudo udevadm control --reload-rules
sudo udevadm trigger
sudo reboot now
```

**Raspberry pi 4 permission settings**
```sh
sudo chown root:gpio /dev/gpiomem
sudo chmod g+rw /dev/gpiomem
sudo chmod a+rw /dev/i2c-* 
```

**Raspberry pi 4 camera settings**
```sh
sudo chmod 777 /dev/video0
```

**Websocket Dependency**
```sh
pip install websocket-client
pip install PyQt5 websocket-client
```

**Others**
```sh
sudo apt install ros-humble-test-msgs
```

**.bashrc settings**
```sh
echo "Humble is activated.!"
source /opt/ros/humble/setup.bash
echo "Minibot is activated.!"
source ~/ros-repo-2/robot/install/local_setup.bash
echo "Server is activated.!"
source ~/ros-repo-2/server/install/local_setup.bash
echo "ROS_DOMAIN_ID is set 213"  # 각 로봇에 대한 ID : 213, 214, 215
export ROS_DOMAIN_ID=213

sudo chmod 777 /dev/video0
sudo chown root:gpio /dev/gpiomem
sudo chmod g+rw /dev/gpiomem
sudo chmod a+rw /dev/i2c-*
```
