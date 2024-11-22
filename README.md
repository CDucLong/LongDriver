"# LDriver"  
LDriver - Self-balancing Two-Wheel Vehicle Operation Guide  
#1. Prepare hardware  
Arduino Uno/Mega  
MPU6050 (Tilt angle sensor)  
#2 DC motor + L298N Driver  
Remote control module (RF24L01)  
Battery and power circuit  
Two-wheel vehicle frame  
#Hardware connection:   
#MPU6050:  
VCC -> 5V  
GND -> GND  
SDA -> A4  
SCL -> A5  
#L298N & motor:  
ENA -> Pin 5  
IN1 -> Pin 6  
IN2 -> Pin 7  
IN3 -> Pin 8  
IN4 -> Pin 9  
ENB -> Pin 10  
#2. Software Installation  
Install Arduino IDE  
Install libraries:  
Wire.h  
MPU6050.h  
RF24.h  
Download code from repository and upload to Arduino  
#3. Operation procedure  
Check hardware connection  
Power up the system  
Place the car in vertical position  
Wait 3-5 seconds for the sensor to stabilize  
The car will automatically start balancing  
#4. Test each function  
#4.1 Check the tilt sensor  
Open Serial Monitor (9600 baud)  
Place the car upright -> angle ≈ 0°  
Slightly tilt the car -> check the display angle  
#4.2 Check the automatic balance  
Place the car upright  
The car will automatically adjust:  
Lean left -> left motor accelerates  
Lean right -> right motor accelerates  
#4.3 Check the remote control  
Turn on the remote control  
Test the commands:  
Move forward/backward  
Turn left/right  
Stop  
#5. Troubleshooting  
The vehicle does not balance itself  
Check the MPU6050 connection  
Check the battery voltage  
Recalibrate the PID parameters  
The vehicle shakes a lot  
Decrease the Kp value in the PID  
Increase the Kd value  
Check the stability of the vehicle frame  
The remote control does not work  
Check the connection  
Check the transmission channel address  
Check the remote battery  
#Important note  
Always place the vehicle upright when starting  
Maintain stable battery voltage  
Check the tightness of the connections  
Calibrate the PID based on the actual weight  
