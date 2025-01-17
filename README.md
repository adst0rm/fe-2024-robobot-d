<div align=center>
 ROBOBOT_D team's repository for WRO Future Engineers 2024 - Republican Stage
 
 Members: Temirgaleev Alan, Ergen Adil

 ![Green and White Creative Robot Logo](https://github.com/user-attachments/assets/85363e8c-e6a4-487a-b768-3a5f3a600cf6)

</div>

***



Engineering materials
====
## Introduction

This repository contains all important files and information about our autonomous driving car "Robobot-D". As a base/microcontroller we chose the Lego Mindstorms EV3, which we equipped with the PixyCam CMUcam5 V1 (Lego Mindstorms version) for object recognition. The reasons for choosing the EV3 were the high reliability as well as the already existing knowledge and experience with the system from Lego incl. programming. The software ran on an EV3 brick with the original Lego Mindstorms EV3 firmware. We went a step further for the National finals and tried to program the EV3 brick based on the EV3G using some additional blocks. Hope was increased flexibility and versatility, but reliability was lacking.

## Main content

* `Photo of Team` contains 2 photos of the team (an official one and one funny photo).
* `Robot-Photo` contains 6 photos of the vehicle (from every side, top and bottom).
* `Video` contains the video.md file with the link to a video with a driving demonstration.
* `Technical drawing` contains schematic diagrams of the electromechanical components, illustrating all the elements (electronic components and motors) used in the vehicle and how they connect to each other.
* `Program_Code` contains the code of control software for all components which were programmed to participate in the competition.
* `models` contains all the 3D-printed parts of the vehicle. 
* `other` contains the PCBs of the vehicle and the datasheets of all the components.


 ## Detailed content

* [**Mobility management**](#mobility-management)
  * [Chassis design and differential](#chassis-design-and-differential)
  * [Weight distribution](#weight-distribution)
  * [Camera position](#camera-position)
  * [Motor selection](#motor-selection)
* [**Power and Sense Management**](#power-and-sense-management)
  * [Sense Management](#sense-management)
  * [Power Management](#power-management)
* [**Obstacle management**](#obstacle-management)
* [**Pictures**](#pictures)
  * [Robot Photos](#robot-photos)
  * [Team Photos](#team-photos)
* [**Performance videos**](#performance-videos)
* [**Engineering factor**](#engineering-factor)

# Mobility Management
<p>   Our robot is constructed using LEGO components, specifically the LEGO MINDSTORMS Education Core Set (Serial number 45544) along with various other LEGO EV3 sets, including the EV3 Expansion Set, the EV3 Homeschool Combo Pack, and more. The robot's wheels are sourced from the LEGO Technic set and its expansion set. </p> </br>
  

### Chassis design and differential
Our chassis design is based on the Ackerman driving geometry, which allows for maximum steering angles and improves the robot's ability to turn smoothly. The rear axle has a differential installed in order to improve turning even more. The turning radius is lowered when one tire rotates more slowly than the other during a turn because of this difference. Thus, the steering system and the differential are the two main parts that control our robot's turning.
<table>
<tr>
<th width=250>

![image](https://github.com/user-attachments/assets/282ffcd7-f450-4515-aed0-8ff8df879a8c)



### Weight distribution
  Since our robot is an autonomous vehicle with a steering system and a differential in the back axle, we must make it somewhat heavier and disperse the weight behind the center of the vehicle to keep the wheels from slipping. Our odometry and the program are affected by the wheels sliding on the back axle.

  
### Camera position
  For the best vision and obstacle management, our camera is positioned as far back and higher than is practical. In order to improve obstacle management, it was also slightly slanted downward to show blocks that were near the robot and to restrict the view.

</div>

### Motor selection
  We have a choice between 2 types of LEGO motors: large motor and medium motor, the large motor is powerful but the speed is lower, the medium motor is not that powerful but have a great speed. In the end, The Robobot-D robot was driven by a Lego EV3 medium motor via the rear axle with differential (better cornering). For steering, we also used a Lego EV3 Medium motor connected to a steering device. To make the bot drive as straight as possible, we initially installed a Lego gyro sensor, which was reset after the start and then measured the turning position.
  
* Large servo motor (actuator) -The Large Motor block controls a Large Motor. You can turn a motor on or off, control its power level, or turn the motor on for a specified amount of time or rotation.
![image](https://github.com/user-attachments/assets/2422e364-e3d2-4ca9-9e32-c1ca85810b42)
![image](https://github.com/user-attachments/assets/957359f1-9d8b-483c-a02f-d8a71c482054)


* Medium-size servo motor - maximum speed of 250 rpm, running torque 0.08 Nm and stopping torque of 0.12 Nm, also with integrated encoder, identical to that of a large engine.
* ![image](https://github.com/user-attachments/assets/089aceea-fc7a-44a3-97cb-29c6a3e55f1e)

</br>![image](https://github.com/user-attachments/assets/39789d3a-ae00-4139-8728-5525c9ea616f)


   
# <hr/>
# Power and sense management </br>
## Power management </br>
  The core of our robot is <a href="#">EV3 Programmable Brick</a>, the power comes from a rechargable 10V Lithium Battery. EV3 P-Brick have 4 ports for motors and 4 ports for sensors. 
  <table>
<tr>
<th width=400>
  
 ![image](https://github.com/user-attachments/assets/6d3bff78-76cd-4908-bde2-d5a062081cfc)

</th>
</tr>
</table>
[Electroschemes/wiring diagrams]()
  
## Sense management </br>
  The Robobot-D robot was driven by a Lego EV3 medium motor via the rear axle with differential (better cornering). For steering, we also used a Lego EV3 Medium motor connected to a steering device. To make the bot drive as straight as possible, we initially installed a Lego gyro sensor, which was reset after the start and then measured the turning position. Furthermore, a Lego color sensor detects if a colored line is crossed. This is useful for counting sections and stopping after three laps on the one hand, and initiating a turn on the other. Before an obstacle race, we mount the aforementioned PixyCam to drive around the red and green obstacles. We were not able to distinguish the thick and colored lines from the obstacles with the camera and to evaluate them in a meaningful way to do without a color sensor. During a race without obstacles, the robot also orientates itself with the help of two Lego ultrasonic sensors, which measure the distances to the walls. One of them measure to the left side and the other to the front side. For a higher speed, we installed a Lego EV3 Large motor with transmission after the regional final. But in the curves we have to slow down the speed to recognize the colored lines because we had troubles with it.

# <hr/>
<!-- 

























-->
# Obstacle management
  For the obstacle detection we used Pixy2 camera and PixyMon v2 application to configure it. To use it in LEGO MINDSTORMS application you need to install special library. All of the downloads are able in official site of Pixy2 <a href="https://pixycam.com/downloads-pixy2/">https://pixycam.com/downloads-pixy2/</a>. </br> </br>

![image](https://github.com/user-attachments/assets/2ed68598-b1ac-4fc1-b993-aec5c4b1a24c)


To calculate linear function we use this site: <a href="desmos.com">https://planetcalc.ru/8110/?ysclid=m0a3s77i4p794636345</a>.
</br>
<div align = center style="display: flex; flex-direction: column; align-items: center; justify-content: center; color: gray">

<table>
<tr>
<th width=250>
  
<p> 
PixyMon v2 application
</p>
</th>
</tr>
</table>

<table>
<tr>
<th width=400>


<p>
Pixy block for LEGO MINDSTORMS
</p>
</th>
</tr>
</table>
</div>

# <hr/>

# Pictures


## Team Photos
![photo_5417878494471375894_y](https://github.com/user-attachments/assets/6530e9bb-c027-4262-bb48-ff9ffa3827b4)

# <hr/>

<!-- 










-->
# Performance videos
### Open Challenge: [https://www.youtube.com/watch?v=abwXTLdPtoA ](https://youtu.be/AMCNVDYtPBo?si=Wjnw0hX1lhmFwcLa) </br>
### Obstacle Challenge: [https://www.youtube.com/watch?v=in7TNcsKKQ0](https://youtu.be/GPkDe-8WeTw?si=uFDIkXFSMs9KY6m9) </br>
### Robot parts discussion: [https://www.youtube.com/watch?v=4ONiXjtQosE](https://youtu.be/I4duiq9KFX4?si=GOTIThVYBHVnM5RF) </br>
# <hr/>
<!-- 







-->
# Engineering Factor
### Construction making
  For our construction we used LEGO MINDSTORMS Education Set and wheels from LEGO SPIKE Prime Set as it conducts simple platform LEGO MINDSTORMS application for code, logic and powerful UART sensors as Gyro, Ultrasonic and Colorsensor for sense management and EV3 programmable brick as a main controller. </br>

  Pixy2 camera is a powerful tool with I2C communication protocol. It is used to distinguish colors of red, green blocks and parking in obstacle challenge, their position by relative coordinates and their relative sizes. It also has its own programm <u>PixyMon v2</u> for configuration of Pixy2 camera, with interactive interface including various settings. </br>
### Programming
  For the programming we used <a href="">LEGO MINDSTORMS</a> application. 
# <hr/>


# Our previous robot's construction

## Electronics

The robot consists of three ATMEGA32U4 microcontrollers, so it can be seen as three modules. One microcontroller as the Master, another as the I2C Slave and the last as the Sensors Slave. We chose to use three microcontrollers because we feared that they would be saturated and we could not upload the main code, and in the end we were right, the programs for each use around the 70 - 80% of the maximum program memory.

### Sensors slave

This microcontroller reads the data from three HC-SR04 ultrasonic sensors (in the front, right side and left side) and of three encoders (two on the rear wheels and one directly connected to the motor). It also controls the motor via one IFX9201SG H-bridge motor controller.
The microcontroller connects to the master via SPI communication to send the data from the sensors and receive commands to drive the motor.

### I2C slave
 
This microcontroller connects to all the sensors who use I2C communication: one MPU6050 gyroscope sensor, two VL53L1X TOF sensors (left and right) and the HuskyLens camera. It also controls 10 WS2810B LEDs that act as the vehicle’s headlights, turn signals and brake lights, and a servo that rotates a small mirror that allows the camera to see from left to right.
This microcontroller also sends its sensor data via SPI communication to the master and receives the commands to turn the LEDs on or off.
 
### Master

This microcontroller is in charge of the main program which uses all the information received from the slaves to control the entire robot (mainly the direction servo and the motor) to complete the challenge.
## Programming modules

Having in mind that there are three programs (for each microcontroller), we can also group parts of all the code in groups regarding its purpose.

### Movement

The movement of the vehicle is done by a series of instructions: The Master 32U4 sends the Sensors 32U4 the command to start the motor at a specific speed, with or without a PID controller that adjusts the speed of the motor based on its encoder so its exactly the one required. The master also changes the speed of the motor doing a exponential acceleration or deceleration when needed. Then reads the data of the MPU6050 from the I2C 32U4 to adjust the direction servo with another PID controller to drive straight. Or it moves the servo to turn the car if needed.

### Detecting walls

We mainly use the ultrasonic and TOF sensors to detect distance to walls, to know if we passed a corner and to know the turn direction.
When we pass a corner one of the lateral sensors detects a higher distance, that means there is no wall in that side, that way we know we have to turn to that side.
They can also be used to detect a signal without knowing the color.
The problems with these sensors are that the ultrasonic are very slow for our possible speeds and because the walls are black, little light is reflected to the TOF sensors (the walls we used in Ibiza reflected almost nothing) and the readings may be erratic or imprecise, but we do not know of other types of distance sensors to read walls.

### Detecting the color signals

We use a HuskyLens AI camera with the capability to recognize faces and objects, but most importantly for us, it can recognize colors. Its mounted on a 3D-printed case with an integrated servo that turns a little mirror that reflects the image received by the camera, this way it can view from left to right, around 180º. This allows us to mount the camera facing downwards and make it more compact. The only problem is that this method transposes the image and it needs to be corrected in code.
When the robot detects that it passed a corner, it turns the mirror to view what is in the next sector and the camera reads the color and position of the signals. We simplified the number of possible positions of the signals to 11, ignoring if they are in the left or right lane (only taking into account if they are in the rear, middle or front), because our vehicle is small enough that it can pass between any position of the signals.
The I2C 32U4, the one with the camera, then sends the number we assigned of the specific position in which the signals are to the Master, which saves this position for the other two laps (this way we can go faster because we do not need to read the positions again) and turns the car to position itself on the correct side.

## Debugging with graphs and telemetry

For debugging purposes we included a HC-05 bluetooth module in the vehicle, only used during testing and debuggin, during the competition it will be disconnected. With this we can see values like the speed or the distance counted from the encoders and view it in the style of Formula 1 telemetry which is more practical for comparing it to earlier tests.

## Code building, compiling and uploading process

We programmed all using the Arduino IDE like any Arduino board, but because we use the 32U4 microcontrollers directly we have to flash the bootloader to each 32U4. We flashed the Arduino Leonardo bootloader because it uses this microcontroller and we are very familiar with it. The process for flashing it requires you to connect the 32U4 to another Arduino using the ICSP communication, then the normal Arduino acts as an ISP programmer (using the example code ArduinoISP) and flashes your 32U4 with the selected bootloader.
Because this was our first time doing this we used this 
