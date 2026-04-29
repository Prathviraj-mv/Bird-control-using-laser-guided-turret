# Smart AI-Based Bird Deterrence System

A real-time vision-based bird deterrence system designed to detect, track, and safely repel birds using computer vision and a laser-based actuation mechanism.

---

## 1. Overview

Bird infestation in monuments and public infrastructure leads to structural degradation due to corrosive droppings and nesting. Traditional deterrence methods such as spikes, nets, and chemical repellents are intrusive, visually disruptive, and require continuous maintenance.

This project implements an automated, non-invasive system using computer vision and control systems to detect birds and deter them in real time.

---

## Project Images

### System Setup
| <img src= "Images/WhatsApp Image 2026-04-29 at 12.04.01.jpeg" >| <img src= "Images/WhatsApp Image 2026-04-29 at 12.07.15.jpeg">|
| --------------------------- | --------------------------- |

## 2. System Architecture


The system operates as a closed-loop pipeline:

Camera → Processing Unit → Bird Detection → Localization → Control → Actuation

---

## 3. Working Principle

1. The camera captures continuous video frames  
2. Frames are processed using a YOLO-based detection model  
3. Birds are detected and bounding box coordinates are extracted  
4. The center of the bounding box is compared with the frame center  
5. Position error is computed  
6. A control signal is generated using a proportional controller  
7. Motors adjust orientation to track the target  
8. Laser is activated to deter the bird  

---

## 4. Control System

The system uses a proportional control strategy:

Control = Kp × Error

- Horizontal error controls the stepper motor (pan axis)  
- Vertical error controls the servo motor (tilt axis)  

---

## 5. Hardware Components

| Component | Description |
|----------|------------|
| Raspberry Pi 5 (8GB) | Main processing unit |
| IMX335 5MP Camera | Image acquisition |
| NEMA 17 Stepper Motor | Pan control |
| MG996R Servo Motor | Tilt control |
| A4988 / DRV8825 | Stepper motor driver |
| PCA9685 | Servo PWM driver |
| Green Laser Module (532 nm, ≤5 mW) | Deterrence mechanism |
| Power Supply Unit | System power |
| Mechanical Mount | Structural support |
---

## 6. Software Stack

- Python  
- OpenCV  
- YOLOv5 / YOLOv8  
- Custom CNN models (for comparison)  
- Raspberry Pi OS  
- GPIO and motor control libraries  

---


## Outcome

- Functional prototype of a real-time bird detection and deterrence system  
- Integration of AI, embedded systems, and control engineering  
- Scalable and adaptable solution for real-world deployment  

---


## License

This project is released under the MIT License.
