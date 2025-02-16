# Advanced Drone Control System

This project is a GUI-driven, fully autonomous long-range drone control system with dead-reckoning for environmental monitoring using LoRa technology. The main functionalities of this project include:

- **IMU Integration:**  
  Uses the MPU6050 for accelerometer and gyroscope data via I2C (using the `smbus` library).

- **PID Control:**  
  Implements a PID controller for managing drone altitude.

- **Extended Kalman Filter (EKF):**  
  An EKF is implemented for sensor fusion, which estimates the drone’s state (position and velocity) by combining sensor data with a predictive model. This helps to smooth out sensor noise and improve control accuracy.

- **Motor Control:**  
  Controls ESCs (Electronic Speed Controllers) via the `pigpio` library to set motor speeds.

- **GUI Interface:**  
  A Tkinter-based GUI allows manual control of motor speeds via sliders and directional buttons (Hover, Forward, Backward, Left, Right, and Emergency Stop).

## Prerequisites

- Python 3.x
- [pigpio](http://abyz.me.uk/rpi/pigpio/) (ensure the pigpio daemon is running)
- `smbus` Python library (for I2C communication)
- `tkinter` (usually comes with Python)
- `numpy`

## Setup

1. **Install Required Libraries:**  
   You can install the required Python libraries via pip (if not already installed):

   ```bash
   pip install numpy
   pip install pigpio
   pip install smbus
