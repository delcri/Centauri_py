## 🤖 Centauri_py – Robotic Manipulator Control Interface

Centauri_py is a robotics project focused on **controlling a real robotic manipulator** through a **graphical user interface developed in Python using Pygame**, enabling direct **joint-space control** and communication with physical hardware via **serial communication (Arduino)**.

This project was developed as part of hands-on robotics work, emphasizing **software–hardware integration**, actuator control, and human-machine interface (HMI) design.

## 🧠 Key Features

* 🎮 Python GUI built with Pygame
* 🎛️ Joint control via sliders
* 🔄 Real-time joint angle transmission
* 🔌 **Serial communication with Arduino**
* ✋ Basic gripper control
* 🔁 Reset button to return to home position
* 🧩 Architecture prepared for inverse kinematics (IK) integration

---

## ⚙️ Technical Overview

* Current control is implemented in **joint-space**.
* Each slider corresponds to one manipulator joint.
* Slider values are scaled to real joint angles.
* Commands are sent to the microcontroller via structured serial messages.
* X, Y, Z input fields are included in the interface but **are not yet connected to an active inverse kinematics algorithm**.

---

## 🛠️ Technologies Used

* Python 3
* Pygame (GUI)
* PySerial
* Arduino
* Physical servo/motor control

---

## 📂 Project Structure

```
Centauri_py/
│
├── interfaces/        # Pygame-based GUIs
├── serial_control/    # Arduino communication
├── images/            # UI resources
├── scripts/           # Control scripts
└── README.md
```

---

## 🚀 How to Run

1. Connect the robotic manipulator via USB
2. Configure the serial port:

   ```python
   arduino_port = '/dev/ttyACM0'
   ```
3. Run the interface:

   ```bash
   python3 main.py
   ```

---

## 📈 Future Work

* Full **inverse kinematics (IK)** integration using Cartesian coordinates
* 2D/3D manipulator visualization
* ROS 2 migration
* Hybrid joint-space / task-space control
* Mathematical documentation of kinematics

