# Where-Am-I
Project 3 of Robotics Software Engineering Nanodegree Program 

## Overview of the Project 
In this project I utilized ROS AMCL package to accurately localize a mobile robot inside a map in the Gazebo simulation environments. The primary aspects of this project include:
* Creating a ROS package that launches a custom robot model in a custom Gazebo world.
* Utilize the ROS AMCL package and the Tele-Operation / Navigation Stack to localize the robot.
* Explore, add, and tune specific parameters corresponding to each package to achieve the best possible localization results.

## What you will need to run 
* Gazebo >= 7.0
* ROS Kinetic
* ROS navigation package \
`sudo apt-get install ros-kinetic-navigation`
* ROS map_server package \
`sudo apt-get install ros-kinetic-map-server`
* ROS move_base package \
`sudo apt-get install ros-kinetic-move-base`
* ROS amcl package \
`sudo apt-get install ros-kinetic-amcl`

## How to run 
* Open Ubuntu bash and execute the command `sudo apt-get update && sudo apt-get upgrade -y`
* Install the necessary packages 
* Clone this repository 
* Open the repository and make \
`cd /home/workspace/P3-Where-Am-I/catkin_ws/` \
`catkin_make`
* Launch my_robot in Gazebo to load both the world and the plugins \
`roslaunch my_robot world.launch`
* Launch amcl node \
`roslaunch my_robot amcl.launch`
* Testing: \
  You have two options to control your robot while it localize itself here:
  1) Send navigation goal via RViz
  2) Send move command via teleop package.

Navigate your robot, observe its performance and tune your parameters for AMCL. \
\
**Option 1: Send 2D Navigation Goal** \
* Your first option would be sending a 2D Nav Goal from RViz. The move_base will try to navigate your robot based on the localization. Based on the new observation and the odometry, the robot to further perform the localization. \
* Click the `2D Nav Goal button` in the toolbar, then click and drag on the map to send the goal to the robot. It will start moving and localize itself in the process. If you would like to give amcl node a nudge, you could give the robot an initial position estimate on the map using `2D Pose Estimate`. \

**Option 2: Use teleop Node** \
* You could also use teleop node to control your robot and observe it localize itself in the environment. \
* Open another terminal and launch the teleop script: 

`rosrun teleop_twist_keyboard teleop_twist_keyboard.py`



