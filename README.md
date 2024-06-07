# TWO-WHEELED-SELF-BALANCING-ROBOT
 Design and control of a two-wheel self-balancing robot
 In this project is to design and implementation of PID based two wheeled self-balancing robot to solve the inclination angle problem to balance the movement of robot and to implement in real time. We are designing the code and implement an efficient selfbalancing PID algorithm using the embedded controller and to implement in real time. Accelerometer is fitted on the robot to measure the angle of tilt during load imbalance. It gives a summary of the work done in the fields of mechanical design, electronics, software design, system characterization and control theory. This wide array of fields necessary for the realization of the project holds the project up as a leading example in the field of 
mechatronics. Here special focus will be on the modelling of the robotic system and the simulation results of various control methods required for the stabilization of the system. 

![01](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/2f7dee22-4e6f-48e9-8bc0-a1bcf8dc6ae3)


 The design and components of a self-balancing robot are detailed, emphasizing the use of sensors, actuators, and control algorithms to maintain an upright position. Essential components include a structural frame, an Arduino UNO microcontroller for data processing, an MPU 6050 sensor for orientation and acceleration measurement, an L298N motor driver for controlling DC geared motors, a battery for power, a switch for power management, an HC-05 Bluetooth module for wireless communication, and wiring and wheels for electrical connections and mobility. The design process incorporates SolidWorks for mechanical design and a PID control algorithm, with block diagrams illustrating the system architecture and demonstrating improved balancing performance post-PID implementation. Applications of this technology include self-balancing unicycles, bikes, Segway robots, hoverboards, and wheelchairs.
![02](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/a8b32c2f-4d74-452a-9bf8-1c92bc2e7d86)
# Components 
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/99ea7b38-4c93-4b5c-9685-185b74166750)

# Flowchart 
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/f2fc71c6-f074-4efc-a3c6-156d4a7cc38d)

# Modeling
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/4036ab1e-8545-4f83-a68d-1134e2a442a8)

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/bb72425e-7952-4658-ab0a-a5558f6ac4d0)

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/8da4d086-f76b-4332-87f6-2906070fca99)

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/dc1d188e-0a1f-42fc-b9a8-cb5a0e2dcd45)

# Response before applying PID Control   
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/316fbfd2-fd20-4204-8321-e5d41d71f294)

The plot shows that Response is unstable, as response increases to infinity with time.

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/91445d88-041d-4386-9002-38532cf5a1e8)

The system has 3 poles (two at left, one at right) (P1(-12.4), P2(-0.25),P3(12.3)), 1 zeros(marginal zero)  

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/427bd863-0cef-47fb-b44d-4e0fa58e669e)

Take-off point (-2.72), while there is a pole on the right, the system is unstable.

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/fc36ec3d-4ba5-4adb-9c61-128895c7de30)

No rotation about -1, but there is a pole on right, so the system is unstable. (Z=N+P = 1)

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/b395aef7-829e-4b07-ada8-c5b1373c990e)

From our study, (if system have any negative in phase margin or gain margin or both are negative, system is unstable). In the previous plot the gain margin equals a negative number so the system is unstable. 


# PID control

Transfer Function after the PID 
Kp  33 
Kd 1.4 
Ki 50
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/02f242c2-2ada-415c-b1b5-f4b07abbc4c8)
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/f4c5f205-ccfc-4f3b-86f4-ddb2916d9f18)
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/28fded57-8ae5-4757-9819-aa8912adfe27)

# Response after applying PID Control 
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/f2276d54-7092-49c3-8424-dcf135bd8f00)
![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/02aab6a8-6443-48c5-b2ca-0578e2b45fdd)

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/907999a4-a659-43b6-9268-7bc4dc23a45d)

The system has 4 poles (all at left) (P1(-26.4-18.3j), P2(-26.4+18.3j), P3(-1.85),P4(0)), 3 zeros(Z1(-21.9),Z2(-1.63),Z3(0))   

![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/c934fa47-fdc9-45c9-a09f-6d544ca9580a)

 Take-off point (-40.7), there is not pole on the right, the system is stable forever.

 ![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/14168427-0162-419c-9041-e22ab283e2e4)
 
 No rotation about -1, there is no poles on right, so the system is stable. (Z=N+P = 0) 

 ![image](https://github.com/mohamed-alaa-saber/TWO-WHEELED-SELF-BALANCING-ROBOT/assets/77857955/b16701e5-f263-45f4-a42a-e759881a4ce3)
 
From our study, (if both are positive system is stable), In the previous plot the gain margin and the phase margin equal a positive number so the system is stable. 



