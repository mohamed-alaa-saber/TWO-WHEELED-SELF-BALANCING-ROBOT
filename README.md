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

∑𝐹𝑥=0 
�
�−𝒃𝒙−𝑴𝒙−𝒎𝒙−𝒎𝒍𝜽𝒄𝒐𝒔𝜽+𝒎𝒍𝜽𝟐𝒔𝒊𝒏𝜽=𝟎                    (1)  
∑𝐹𝑦=0 
�
�𝒈+𝒎𝒈−𝒎𝒍𝜽𝒔𝒊𝒏𝜽+𝒎𝒍𝜽𝟐𝒄𝒐𝒔𝜽=𝟎                                    (2) 
∑𝑀𝐴=0 
�
�𝒈𝒍𝒔𝒊𝒏𝜽+𝑰𝜽+𝒎𝒍𝟐𝜽+𝒎𝒍𝒙𝒄𝒐𝒔𝜽=𝟎                                    (3) 
Equations (1), (2), and (3) are combined, hence the force equation is obtained alone the 
horizontal and vertical directions, 
(𝑰+𝒎𝒍𝟐)𝜽+𝒎𝒈𝒍𝒔𝒊𝒏𝜽=−𝒎𝒍𝒙𝒄𝒐𝒔𝜽                                      (4) 
(𝑴+𝒎)𝒙+𝒃𝒙+𝒎𝒍𝜽𝒄𝒐𝒔𝜽−𝒎𝒍𝜽𝟐𝒔𝒊𝒏𝜽=𝑭                        (5) 
Equations (4) and (5) are two linear equations of the transfer function, 
 where 𝑞=𝜋. With assumption 𝜃=𝜋+∅, 
�
�𝒐𝒔𝜽=−𝟏                                                                                  (6) 
�
�𝒊𝒏𝜽=−∅                                                                                  (7) 
�
�𝟐
 𝒅𝒕𝟐
 =𝟎                                                                                         (8) 
After Processing the equations (6), (7) and (8) approach to non-linear, then we obtained two 
variations of motion equations. The U value represents the input, 
(𝑰+𝒎𝒍)𝟐∅−𝒎𝒈𝒍∅=𝒎𝒍𝒙                                                       (9) 
(𝑴+𝒎)𝒙+𝒃𝒙+𝒎𝒍∅=𝑼                                                       (10) 
14 
 
By applying Laplace transform on equations (9) and (10), 
(𝑰+𝒎𝒍𝟐)∅(𝒔)𝒔𝟐−𝒎𝒈𝒍∅(𝒔)=𝒎𝒍𝑿(𝒔)𝒔𝟐                                 (11) 
(𝑴+𝒎)𝑿(𝒔)𝒔𝟐+𝒃𝑿(𝒔)𝒔+𝒎𝒍∅(𝒔)𝒔𝟐=𝑼(𝒔)                          (12) 
We yielded the transfer function for TWBMR from the equations (11) and (12). 
∅(𝒔)
 𝑼(𝒔)
 =
 𝒎𝒍
 𝒒 𝑺
 𝑺𝟑+𝒃(𝑰+𝒎𝒍𝟐)
 𝒒 𝑺𝟐−(𝑴+𝒎)𝒎𝒈𝒍
 𝒒 𝑺−𝒃𝒎𝒈𝒍
 𝒒
                             (13) 
Where 𝒒=[(𝑴+𝒎)(𝑰+𝒎𝒍𝟐)−(𝒎𝒍)𝟐]

# PID control
