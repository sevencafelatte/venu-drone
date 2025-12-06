# venu-drone
![Status](https://img.shields.io/badge/Project-Rebooting-blue)
![Stage](https://img.shields.io/badge/Phase-Reviewing%20Old%20Files-yellow)
![Build](https://img.shields.io/badge/Firmware-Build%20Pending-lightgrey)
![License](https://img.shields.io/badge/License-MIT-green)
# 🛸 Mini Drone Project — System Reboot & Architecture Reconstruction

This repository contains the restructured and modernized version of my earlier autonomous mini-drone project.  
I am currently reviewing my previous firmware, hardware notes, log files, and prototype designs to rebuild a coherent architecture before moving forward with development.

The goal of this reboot is to establish a clean, modular, and testable drone stack that includes:

- A flight controller firmware (IMU → Sensor Fusion → PID → Motor Mixing)
- A radio control system (RX/TX protocol, packet integrity, channel mapping)
- Simulation support (Gazebo / MATLAB models)
- Supporting tools (log parsing, telemetry visualization, firmware flashing utilities)

---

## 🔄 Current Phase: Legacy File Review

Before writing new firmware, I am focusing on:

### **1. Legacy Code Analysis**
- Extracting reusable modules (`PID`, `motor_control`, `imu_driver`)
- Identifying outdated or deprecated HAL APIs
- Cleaning or rewriting modules for maintainability

### **2. Architecture Reconstruction**
- Re-establishing subsystem boundaries  
- Updating directory structure to follow embedded best practices  
- Migrating toward a unified coding standard (C99 or C11)

### **3. Hardware Validation**
- Reviewing ESC, IMU, and power stage notes  
- Checking sensor interfaces (I²C/SPI timing, sampling constraints)  
- Re-documenting frame geometry for mixer calculations

---

## 🚀 Upcoming Work

### **Firmware Roadmap**
- [ ] Rewrite the IMU driver layer  
- [ ] Implement a configurable complementary filter (→ Madgwick → EKF pipeline)  
- [ ] Rebuild motor mixing for quad-X configuration  
- [ ] Implement loop timing and scheduler  
- [ ] Add link-loss failsafe + arming logic  

### **Tooling Roadmap**
- [ ] Flight log format (binary + CSV export)  
- [ ] Real-time plotting tool (Python / Matplotlib)  
- [ ] Firmware uploader script for dev workflow  

### **Hardware Roadmap**
- [ ] Validate IMU orientation & axis alignment  
- [ ] Recheck ESC throttle calibration curves  
- [ ] Select battery + regulator combination  
- [ ] Build V1 prototype frame  

---

## 📂 Repository Layout (Technical)
firmware/
flight_controller/
remote_control/
common/
simulation/
tools/
hardware/
tests/

---

## 📒 Dev Log Entries (per update)

Each commit or weekly update will follow a structured template:

### **Dev Log Template**
```md
## 📝 Dev Log — <Date>

### ✅ What I Reviewed Today
- 

### 🔍 Insights From Old Files
- 

### 🔧 What I Refactored / Cleaned
- 

### 🚀 Next Small Steps
- 

### 🧠 Notes to Future Me
- 
