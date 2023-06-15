# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:Import the required packages

<br/>

Step2:Assign the value for X axis and Y axis

<br/>

Step3:write the program to move the Robot

<br/>

Step4:Write the program to record video

<br/>

Step5:Run the program to move the robot

<br/>

## Program
```
#Developed by:SHABREENA VINCENT
#Register number: 212222230141

from robomaster import robot
import time
from robomaster import camera

if name == 'main':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera
          
    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
    ''' 
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5] 
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second)  [0.5,2]

    '''
    ep_chassis.move(x=2, y=0, z=0, xy_speed=0.95).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=204,g=255,b=255,effect="on") 
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=204,g=204,b=255,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=0,effect="on")
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=0,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on") 
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on")
    ep_chassis.move(x=0, y=0, z=-30, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on") 
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on")
    


  
 
 
    
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

## INITIAL POSITION:

![initial](https://github.com/shabreenavincent/mobilerobot-openloopcontrol/assets/119475721/deda7bd6-cd24-4323-8572-e35d5061b7f5)

## FINAL POSITIOM:

![final](https://github.com/shabreenavincent/mobilerobot-openloopcontrol/assets/119475721/ff5114ad-5ca3-453f-ba99-fdbe89e0bfc0)

<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

https://youtu.be/nZMAdS07Pls

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
