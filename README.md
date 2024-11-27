# LongDriver
## Self-balancing Two-Wheel Vehicle Operation Guide

## Table of Contents
- [1. Hardware Preparation](#1-hardware-preparation)
- [2. Software Installation](#2-software-installation)
- [3. Operation Procedure](#3-operation-procedure)
- [4. Testing Functions](#4-testing-functions)
- [5. Troubleshooting](#5-troubleshooting)

## 1. Hardware Preparation
### Required Components
- Arduino Uno/Mega
- MPU6050 (Tilt angle sensor)
- 2 DC motors + L298N Driver
- Remote control module (RF24L01)
- Battery and power circuit
- Two-wheel vehicle frame

### Hardware Connection
#### MPU6050
| MPU6050 Pin | Arduino Pin |
|-------------|-------------|
| VCC         | 5V         |
| GND         | GND        |
| SDA         | A4         |
| SCL         | A5         |

#### L298N & Motors
| L298N Pin | Arduino Pin |
|-----------|-------------|
| ENA       | Pin 5      |
| IN1       | Pin 6      |
| IN2       | Pin 7      |
| IN3       | Pin 8      |
| IN4       | Pin 9      |
| ENB       | Pin 10     |

## 2. Software Installation
1. Install Arduino IDE
2. Install Required Libraries:
   - Wire.h
   - MPU6050.h
   - RF24.h
3. Download code from repository and upload to Arduino

## 3. Operation Procedure
1. Check hardware connection
2. Power up the system
3. Place the car in vertical position
4. Wait 3-5 seconds for the sensor to stabilize
5. The car will automatically start balancing

## 4. Testing Functions
### 4.1 Tilt Sensor Check
1. Open Serial Monitor (9600 baud)
2. Place the car upright -> angle ≈ 0°
3. Slightly tilt the car -> check the display angle

### 4.2 Automatic Balance Check
1. Place the car upright
2. The car will automatically adjust:
   - Lean left -> left motor accelerates
   - Lean right -> right motor accelerates

### 4.3 Remote Control Check
1. Turn on the remote control
2. Test the commands:
   - Move forward/backward
   - Turn left/right
   - Stop

## 5. Troubleshooting
### The vehicle does not balance itself
- Check the MPU6050 connection
- Check the battery voltage
- Recalibrate the PID parameters

### The vehicle shakes a lot
- Decrease the Kp value in the PID
- Increase the Kd value
- Check the stability of the vehicle frame

### The remote control does not work
- Check the connection
- Check the transmission channel address
- Check the remote battery

## Important Notes
- Always place the vehicle upright when starting
- Maintain stable battery voltage
- Check the tightness of the connections
- Calibrate the PID based on the actual weight
