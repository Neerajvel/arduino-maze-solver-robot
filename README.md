# Arduino Maze Solver Robot

Autonomous maze solving robot built using **Arduino Uno**, **IR sensors**, and a **Motor Driver (H-Bridge)** that navigates a maze using a **Left-Hand Rule Algorithm**.

This project demonstrates concepts from:

- Embedded Systems
- Robotics
- Sensor-based navigation
- Autonomous decision making

---

# Project Overview

The robot detects and follows a path using **Infrared (IR) sensors** and autonomously solves a maze by prioritizing **left turns at junctions**.

The algorithm ensures the robot explores the maze systematically until the exit is reached.

This project was developed as part of **Embedded Systems Workshop 2024**.

---

# Hardware Components

| Component | Quantity |
|--------|--------|
| Arduino Uno | 1 |
| IR Sensor Modules | 3 |
| Motor Driver (H-Bridge) | 1 |
| DC Motors | 2 |
| Robot Chassis | 1 |
| Wheels | 2 |
| Battery Pack | 1 |
| Breadboard | 1 |
| Jumper Wires | Multiple |

---

# System Architecture

Robot consists of three main subsystems:

### Sensor System
IR sensors detect the **black line on the maze track**.

### Control System
Arduino processes sensor input and decides the next movement.

### Actuation System
Motor driver controls the **two DC motors** to move the robot.

---

# Navigation Algorithm

The robot follows a **Left Priority Algorithm**.

This ensures the robot explores the maze using the **Left Hand Rule**.

Algorithm logic: :contentReference[oaicite:0]{index=0}

### Cases

**Case 1**
Middle sensor detects line  
➡ Move Forward

**Case 2**
Left sensor detects line  
➡ Turn Left

**Case 3**
Right sensor detects line  
➡ Turn Right

**Case 4**
Left + Middle detect line  
➡ Turn Left

**Case 5**
Left + Right detect line  
➡ Turn Left

**Case 6**
All sensors detect line  
➡ T-junction → Turn Left

**Case 7**
No sensor detects line  
➡ Rotate Left until line detected

**Case 8**
Right + Middle detect line  
➡ Move Forward

---

# Hardware Setup

The robot uses an **H-Bridge motor driver** to control motor direction and speed.

Motor control is achieved using **PWM pins from the Arduino Uno**.

Hardware connection details: :contentReference[oaicite:1]{index=1}

### Key Points

- Arduino provides control signals
- Motor driver amplifies current for motors
- 12V powers motors
- 5V logic powers the driver

---

# IR Sensor Calibration

Proper calibration is essential for accurate line detection.

Steps:

1. Place sensor about **3 cm above the track**
2. Adjust the **sensitivity potentiometer**
3. Rotate until **LED indicator turns ON when over black tape**

Calibration instructions: :contentReference[oaicite:2]{index=2}

---

# Code

The Arduino program reads sensor values and performs motor control accordingly.

Main file:

```
code/maze_solver.ino
```

Key functions include:

- Sensor reading
- Direction decision
- Motor control logic
- Maze navigation algorithm

---

# Applications

This project demonstrates concepts used in:

- Autonomous robots
- Warehouse robots
- Path planning systems
- Embedded robotics systems

---

# Future Improvements

Possible upgrades:

• Implement **shortest path optimization**  
• Add **PID control for smoother motion**  
• Store maze path using **stack or graph traversal**  
• Integrate **machine vision using camera module**  
• Convert to **SLAM-based navigation**

---

# Demonstration

Add your robot images or videos in the `/images` folder.

Example:

```
images/robot.jpg
images/maze_test.jpg
```

---

# Learning Outcomes

Through this project:

- Implemented autonomous navigation logic
- Worked with sensor calibration
- Designed motor control systems
- Applied embedded C programming

---

# Author

Neerajvel D

Electronics & Communication Engineering  
Embedded Systems | Robotics | C++ | Machine Learning
