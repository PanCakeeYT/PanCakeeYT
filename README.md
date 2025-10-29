<p align="center">
  <img src="https://komarev.com/ghpvc/?username=PanCakeeYT&label=Profile+Views&color=00ffd1&style=flat-square" alt="profile views" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&size=22&duration=4000&pause=700&color=00FFD1&center=true&vCenter=true&width=600&lines=Hi+there!+I'm+Abdelrahman;Embedded+Systems+%26+Firmware+Engineer;Real-Time+Control+Systems;ESP32+%26+ESP-NOW+Developer;C%2B%2B+%7C+Python+%7C+React" alt="typing" />
</p>

<p align="center">
  Embedded Systems & Firmware Engineer. Focusing on real-time control systems, low-latency IoT communication (ESP-NOW), and custom hardware integration.
</p>

<p align="center">
  <img src="https://i.imgur.com/2nLwIIf.gif" alt="animated divider" width="100%">
</p>

## 📊 My GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=PanCakeeYT&show_icons=true&theme=tokyonight&rank_icon=github" alt="github stats" height="170" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=PanCakeeYT&layout=compact&theme=tokyonight" alt="top languages" height="170" />
  <br><br>
  <!-- This is the "crazier" animated graph replacing the streak -->
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=PanCakeeYT&theme=tokyo-night&hide_border=true&line=00FFD1&point=00FFD1&area=true&area_color=00FFD1" alt="github activity graph" />
</p>

<p align="center">
  <img src="https://i.imgur.com/2nLwIIf.gif" alt="animated divider" width="100%">
</p>

## 🛠️ My Tech Stack

<div align="center">

**Firmware & Hardware:**<br>
<img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white&animation=spin" alt="C++">
<img src="https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white&animation=spin" alt="Arduino">
<img src="https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white" alt="ESP32">
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
<br><br>

**Software & UI:**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React">
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
<img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
<br><br>

**Tools & Platforms:**<br>
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git">
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions">
<img src="https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white" alt="VS Code">
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman">

</div>

<p align="center">
  <img src="https://i.imgur.com/2nLwIIf.gif" alt="animated divider" width="100%">
</p>

## 🚀 Core Project: ESP32 1:10 RC Platform

I am currently developing a custom 1:10 scale RC platform from the ground up. The system is built on a multi-ESP32 architecture (Transmitter, Receiver, and Engine Sound) communicating via **ESP-NOW** for low-latency control.

### System Architecture

[TX ESP32] <--ESP-NOW--> [RX ESP32] ---> L298N, Servos, Lights
    |                                 |
 (TFT, Joystick, Pots)                +--> [EES ESP32] --> TDA2030A Amp + Speaker
Key Features
Gyro Stabilization: Implementing ISR-driven, MDAPU6050-based steering correction with a target latency of <5ms.

Real-Time Engine Sound (EES): Mapping throttle/load data to pitch-shifted PCM/WAV samples, synchronized with a TDA2030A amplifier.

Modular Firmware: OTA-ready code with clear separation for TX, RX, and EES subsystems.

Telemetry & Failsafes: Real-time data streaming via WebSocket and robust connection-loss detection.

Hardware-First Control: Using hardware timers (LEDC) for stable, non-blocking PWM and control loops.

<p align="center"> <img src="https://i.imgur.com/2nLwIIf.gif" alt="animated divider" width="100%"> </p>

🐍 My Contribution Graph
<p align="center"> <!-- This path assumes your repo is PanCakeeYT/PanCakeeYT and the action saves to the 'output' branch --> <img src="https://github.com/PanCakeeYT/PanCakeeYT/blob/output/github-contribution-grid-snake.svg" alt="contribution snake" /> </p>

<p align="center"> <img src="https://i.imgur.com/2nLwIIf.gif" alt="animated divider" width="100%"> </p>
