# MobileRobot-Openloopcontrol
## Aim:

To develop a Python control code to move the mobile robot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

## STEP 1:
robomaster is a built-in module in Python from which robots are imported and import time
## STEP 2:
initialize the robot by giving an initialize function for the robot to get commands from the user and
move
## STEP 3:
give a value to the x-axis so that the robot moves in the forward direction and for the robot to
move towards left or right give a certain value to y
## STEP 4:
the value assigned to the z variable indicates the speed of the robot
## STEP 5:
set_led would determine the colors of the LED lights on each side of the robot with certain values of
red, green, and blue to be given to get the color
## STEP 6:
give a distance, speed, and color change for the specified path, and at the end give close to finish the
program
## STEP 7:
End of program.

## Program
```
python program to move the mobile robot along the predicted path
Developed by: SREEKUMAR S
Register number:23008070

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0.4, y=0, z=75, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=192,b=192,effect="on")

    ep_chassis.move(x=0, y=0, z=90, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=235,g=153,b=153,effect="on")

    ep_chassis.move(x=1.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=-30, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=128,b=128,effect="on")

    ep_chassis.move(x=1.2, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=45, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")
    
    ep_chassis.move(x=1.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=153,b=204,effect="on")
    
    ep_chassis.move(x=0, y=0, z=95 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")

    ep_chassis.move(x=2.1, y=0, z=0,xy_speed=1.3 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=85 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0.4, y=0, z=0, xy_speed=1.3 ).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")


    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)



## MobileRobot Movement Video:

[[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)]([https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE](https://youtube.com/shorts/DN7oSsqC-tU))](https://youtube.com/shorts/DN7oSsqC-tU)

## Result:
Thus the Python program code is developed to move the mobile robot in the predefined path.


```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
