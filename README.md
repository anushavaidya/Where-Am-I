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
* Testing 
⋅⋅



