# my_robot
ROS Project to practice Adaptive Monte Carlo Localization (AMCL) package in a custom world

### Built on:
ROS Kinetic & Ubuntu 16.04

## Intro: 
My first try at executing AMC Localization using the AMCL and the move_base package. The world is a single floor area and it's 2D map was generated using the pgm_map_creator package. This map was then provided as the ground truth map for localization.

## Steps to Implement:
1. Create a Catkin Workspace and clone the my_robot repo in the 'src' folder.
2. Change back to the catkin workspace folder and execute catkin_make.
3. ```source devel/setup.bash```
4. ```roslaunch my_robot world.launch```
5. For Rviz open the configuration provided in the repo.
6. ```roslaunch my_robot amcl.launch```
7. In the Rviz map, using the '2D Nav Goal' option, give the robot a target position and orientation.

#### Before Localization:
![Starting](https://github.com/dhruvtya/my_robot/blob/main/Starting.JPG)

#### After Localization:
![Localization](https://github.com/dhruvtya/my_robot/blob/main/Localization.JPG)

As visible in the pictures, the red particles (depicting the estimated pose of the robot) are a little spread out in the beginning but they converge to the correct pose after a few cycles when the robot starts moving.

