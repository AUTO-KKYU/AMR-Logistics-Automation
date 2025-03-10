# AMR Logistics Automation System
<div align="center">
    <img src="https://github.com/addinedu-ros-4th/ros-repo-2/assets/118419026/dd1da530-6c66-4815-94ef-1b23f385e5c4" width="700" height="300">
</div>

<div align="center">

| [![Video 4](https://img.youtube.com/vi/72EWf1t_NVw/sddefault.jpg)](https://youtu.be/72EWf1t_NVw) |
|:---:|
| [최종 시연 영상](https://youtu.be/72EWf1t_NVw) |

</div>

<div align="center">

</div>

## Table of Contents
  * [1. 🤖프로젝트 소개](#1-프로젝트-소개)
    + [1.1. 프로젝트 개요](#11-프로젝트-개요)
    + [1.2. 프로젝트 역할](#12-프로젝트-역할)
    + [1.3. 기술 스택](#13-기술-스택)
  * [2. 📋프로젝트 역할 기여](#2-프로젝트-역할-기여)
    + [2.1. 시스템 아키텍처 설계](#21-시스템-아키텍처-설계)
    + [2.2. 하드웨어 아키텍처 설계](#22-하드웨어-아키텍처-설계)
    + [2.3. 소프트웨어 아키텍처 설계](#23-소프트웨어-아키텍처-설계)
    + [2.4. ROS MAP Localization](#24-ros-map-localization)
      - [2.4.1. Nav2 Parameter 조정](#241-nav2-parameter-조정)
    + [2.5. 3D Pose Estimation](#25-3d-pose-estimation)
      - [2.5.1. Camera Calibration](#251-camera-calibration)
      - [2.5.2. ArUCo Navigation](#252-aruco-navigation)
    + [2.6. Human Following](#26-human-following)
  * [3. ✅필수 조건](#3-필수-조건)
  * [4. ⏩실행 방법](#4-실행-방법)

## 1. 🤖프로젝트 소개
**Duration: 2024.04.17 - 2024.06.13**

AI 자율주행 로봇 4기 수강생 중 **최우수상** <br>
팀 이름 : **물류왕 김탁규** <br>
프로젝트 기간 : **2024.04.17 - 2024.06.13** <br>
발표자료 : https://docs.google.com/presentation/d/1zWYl33Bm2CBIjSyX9Pe78l9VBHL1Ysp2sf91z0QALls/edit?usp=drive_link

| Phase                                    | Dates                        |
|------------------------------------------|------------------------------|
| **Project Plan**                         | 2024.04.15 - 2024.04.30      |
| **Project Design**                       | 2024.05.01 - 2024.05.15      |
| **프로젝트 계획(UR/SR)**                         | 2024.04.15 - 2024.04.30      |
| **프로젝트 설계**                       | 2024.05.01 - 2024.05.15      |
| **High-Level Design (DB, Interface)**    | 2024.05.15 - 2024.05.21      |
| **Low-Level Design (Module, Data Structure, Algorithm)** | 2024.05.20 - 2024.05.25      |
| **H/W Production and Testing**           | 2024.05.15 - 2024.05.23      |
| **Implementation**                       | 2024.05.06 - 2024.06.11      |
| **Verification & Validation**                         | 2024.05.27 - 2024.06.11      |
| **Presentation Preparation and Finalization** | 2024.06.08 - 2024.06.13      |
| **하드웨어 제작 및 테스트**           | 2024.05.15 - 2024.05.23      |
| **소프트웨어 구현**                       | 2024.05.06 - 2024.06.11      |
| **구현 검증(Validation of program/debugging)**    | 2024.05.27 - 2024.06.11      |
| **발표 자료 제작 및 Clean Code** | 2024.06.08 - 2024.06.13      |

### 1.1. 프로젝트 개요
- 입고, 출고, 수집 등 물류 프로세스에서 Fork Lift 프레임 기반 자율주행 로봇을 활용.
- 물류 운영 효율성을 높이기 위해 다중 로봇 제어 시스템 구현.
- 인간-로봇 상호작용(HRI)을 통한 물류 센터 운영 최적화.
- 입고 제품 등록, 선반 재고 관리, 소비자 주문 처리 시스템 등 구현.

<img src="https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/25960a9e-af9d-46dc-9f70-1cfc5d5e6168">

### 1.2. 프로젝트 역할
<table>
  <thead>
    <tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center;">송용탁</td>
      <td style="text-align:center;">Team Leader</td>
      <td>- 로봇 시스템 통합 및 제어 <br> - 로봇 메커니즘 설계 <br> - SLAM & NAV <br> - 로봇 주행 환경 구축 </td>
    </tr>
    <tr>
      <td style="text-align:center;">김동규</td>
      <td style="text-align:center;">Team Member</td>
      <td>- ArUco 기반 정밀 Navigation <br> - 딥러닝 기반 Human Following Robot  <br> - 로봇 주행 환경 구축 <br> - 프로젝트 Confluence 관리 </td>
    </tr>
    <tr>
      <td style="text-align:center;">유겸희</td>
      <td style="text-align:center;">Team Member</td>
      <td>- SLAM <br> - 관리자 GUI 설계 <br> - 데이터베이스 구축 <br> - 로봇 주행 환경 구축  </td>
    </tr>
    <tr>
      <td style="text-align:center;">이재혁</td>
      <td style="text-align:center;">Team Member</td>
      <td>- SLAM & NAV <br> - 경로 주행 알고리즘 설계 <br> - 다중 로봇 제어시스템 구현 <br> - 로봇 주행 환경 구축  </td>
    </tr>
    <tr>
      <td style="text-align:center;">장하린</td>
      <td style="text-align:center;">Team Member</td>
      <td>- SLAM <br> - 관리자 GUI 설계 <br> - 사용자(소비자) GUI 설계 <br> - 데이터베이스 구축 </td>
    </tr>
    <tr>
      <td style="text-align:center;">최가은</td>
      <td style="text-align:center;">Team Member</td>
      <td>- 다중 로봇 업무 관리 스케줄링 <br> - 로봇 통신 서버 구축 <br> - 프로젝트 GITHUB 및 JIRA 관리 </td>
    </tr>
  </tbody>
</table>

### 1.3. 기술 스택
||||
|:---:|:---|:---|
|**Develop EnV**|<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=Ubuntu&logoColor=white"> <img src="https://img.shields.io/badge/VISUAL STUDIO CODE-007ACC?style=for-the-badge&logo=VisualStudioCode&logoColor=white">|
|**TECH**|<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54"> <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white"> <img src="https://img.shields.io/badge/ros2-%2322314E?style=for-the-badge&logo=ros&logoColor=white"> <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white"> <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white"> <img src="https://img.shields.io/badge/PyQt5-%23217346.svg?style=for-the-badge&logo=Qt&logoColor=white"> <img src="https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white"> |
|**H/W**|<img src="https://img.shields.io/badge/-RaspberryPi 4-C51A4A?style=for-the-badge&logo=Raspberry-Pi"> <img src="https://img.shields.io/badge/-Arduino Mega-00979D?style=for-the-badge&logo=Arduino&logoColor=white">|
|**COMMUNICATION**|<img src="https://img.shields.io/badge/confluence-%23172BF4.svg?style=for-the-badge&logo=confluence&logoColor=white"> <img src="https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white"> <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=Slack&logoColor=white">  <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">|

## 2. 📋프로젝트 역할 기여

### 2.1. 시스템 아키텍처 설계

<img src="https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/9a9e5e40-1a1d-45e5-b85e-094c319c2f4b">

### 2.2. 하드웨어 아키텍처 설계
<img src= "https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/5f911581-c86e-44b8-a48b-21adc2f979da">

### 2.3. 소프트웨어 아키텍처 설계
<img src="https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/e0b8a28a-6034-4173-8754-e2a6924e7939">

### 2.4. ROS MAP Localization
@@ -116,7 +128,7 @@
<img src="https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/e1b13aa6-233f-44a0-8731-5b5d0a101e0a">

#### 2.4.1. Nav2 Parameter 조정
*- nav2_params.yaml*
     - Purpose : To apply an appropriate environmental representation for the robot.
 
 | Parameter           | Costmap Type | Before                                | After                                 |
 |---------------------|--------------|---------------------------------------|---------------------------------------|
 | **inflation_layer** | Local        | `plugin: "nav2_costmap_2d::InflationLayer"`<br>`cost_scaling_factor: 3.0`<br>`inflation_radius: 0.25` | `plugin: "nav2_costmap_2d::InflationLayer"`<br>`cost_scaling_factor: 1.0`<br>`inflation_radius: 0.15` |
 | **inflation_layer** | Global       | `plugin: "nav2_costmap_2d::InflationLayer"`<br>`cost_scaling_factor: 3.0`<br>`inflation_radius: 0.35` | `plugin: "nav2_costmap_2d::InflationLayer"`<br>`cost_scaling_factor: 3.0`<br>`inflation_radius: 0.15` |

### 2.5. 3D Pose Estimation

#### 2.5.1. Camera Calibration
<img src= "https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/ed869dcf-58b9-48e1-8ad6-d9a389a769ce">

#### 2.5.2. ArUCo Navigation
<img src= "https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/acb06277-3130-40a1-b1d1-ec2a3675a078">

### 2.6. Human Following
<img src="https://github.com/AUTO-KKYU/AMR-Logistics-Automation/assets/118419026/eeb94530-05e6-4cb7-ba7e-3fccffb6b9e1">

## 3. ✅필수 조건

**How to install ROS2 Humble on PC [Ubuntu 22.04]**
- Follow the guidelines within the site
  -  https://github.com/AUTO-KKYU/ROS2-Study

## 4. ⏩실행 방법

**General Setup**

```sh
git clone https://github.com/AUTO-KKYU/AMR-Logistics-Automation.git

cd ros-repo-2/robot
colcon build
source ./install/local_setup.bash

cd ../server
colcon build
source ./install/local_setup.bash
```

*- Recommend: Use the SSH method for remote access*
- ex) ssh -X your_rasp_name@your_rasp_ip

**Robot 1/2/3 PC (Raspberry Pi PC)**
- Domain ID : 91 / 92 / 93

```sh
# bringup robot : arduino (encoder motor) + Raspberry (YD LIDAR)
ros2 launch minibot_bringup bringup_robot.launch.py

# Aruco & Step motor (fork lift) Node
ros2 launch robot_aruco aruco_detect.launch.py

# human following mode
ros2 launch human_following following.launch.py
```

**Robot 1/2/3 PC (LOCAL PC)**
```sh
export ROS_DOMAIN_ID = 91 / 92 / 93

# check ROS_DOMAIN_ID SETTINGS
printenv grep -i ROS_DOMAIN_ID

source /opt/ros/humble/setup.bash
source ~/.bashrc

# Robot Controller
ros2 run robot_controller robot_controller

# slam toolbox + nav2 package
ros2 launch minibot_navigation2 bringup_launch.py map:=`ros2 pkg prefix minibot_navigation2`/share/minibot_navigation2/maps/re_map.yaml

# rviz visualization
rviz2 -d `ros2 pkg prefix minibot_navigation2`/share/minibot_navigation2/rviz/nav2_view.rviz
```

**Server**
```sh
export ROS_DOMAIN_ID = 90
source /opt/ros/humble/setup.bash
source ~/.bashrc

# websocket bridge
ros2 launch rosbridge_server rosbridge_websocket_launch.xml

# ros2 domain bridge
ros2 run domain_bridge domain_bridge ~/your_path/server/config/bridge_config.yaml

# task allocator server
ros2 launch task_manager task_manager_launch.py
```

**Consumer GUI**
```sh
(venv) (root folder) python3 gui/consumer/src/ui_main.py
```

**Manager GUI**
```sh
(inside gui folder) ros2 run manager.pkg manager_main.py
```

**Robot test Service**
```sh
# aruco control service call
# location : I1,I2,I1 / O1,O2,O3 / P1,P2,P3 / R1,R2 / A1,A2 / B1,B2 / C1,C2
# direction : forward, backward
ros2 service call /aruco_control task_msgs/srv/ArucoCommand "{location: O1, direction: forward}"

# step control service call
# floor : 1,2
# direction : up, down
ros2 service call /step_control task_msgs/srv/StepControl "{floor: 2, direction: up}"

# camera control service call
# data : True / False
ros2 service call /camera_control std_srvs/srv/SetBool "{data: True}"
```

**Server test Service**
```sh
# waypoint move service call
# location : I1,I2,I1 / O1,O2,O3 / P1,P2,P3 / R1,R2 / A1,A2 / B1,B2 / C1,C2
# lift : Up, Down
ros2 service call /allocate_task_92 task_msgs/srv/AllocateTask "{location: "I2", lift: 'Up'}"
```

| [![Video 1](https://img.youtube.com/vi/8Qt1J9MkPb4/sddefault.jpg)](https://youtu.be/8Qt1J9MkPb4) | [![Video 2](https://img.youtube.com/vi/RSHB1A6I8J8/sddefault.jpg)](https://youtu.be/RSHB1A6I8J8) |
|:---:|:---:|
| <div align="center">[ArUCo 3D Pose Estimation](https://youtu.be/8Qt1J9MkPb4)</div> | <div align="center">[Human Following Robot](https://youtu.be/RSHB1A6I8J8)</div> |
