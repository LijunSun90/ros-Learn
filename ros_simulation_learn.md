# Learn ROS and burger simulation 

**Warning** : The contents in this chapter corresponds to the Remote PC (your desktop or laptop PC) which will control TurtleBot3. Do NOT apply this instruction to your TurtleBot3.


## 1. TurtleBot3 Fake Node Implementation

Install dependent packages for TurtleBot3 Simulation.
---

Note : turtlebot3_simulation package requires TurtleBot3 package as a prerequisite.

   >$ cd ~/catkin_ws/src/
   
   >$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
   
   >$ cd ~/catkin_ws && catkin_make
   
   
TurtleBot3 fake node is a very simple simulation node that can be run without having an actual robot. You can even control the virtual TurtleBot3 in RViz with a teleop node.
---

   >$ export TURTLEBOT3_MODEL=burger
   
   >$ roslaunch turtlebot3_fake turtlebot3_fake.launch
   
   >$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch   
   
   
   
## 2. Gazebo

You should set Turtlebot3 model parameter. Select either burger or waffle for the model parameter in the below command.

   >$ export TURTLEBOT3_MODEL=burger
   
Below command will load TurtleBot3 on the default Gazebo environment TurtleBot3 empty world.

   >$ roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch
   

If you wish to load more interesting map, please use below command instead of above command.
TurtleBot3 world is a map consists of simple objects that makes up the shape of TurtleBot3 symbol.
 
   >$ export TURTLEBOT3_MODEL=burger
   
   >$ roslaunch turtlebot3_gazebo turtlebot3_world.launch   
   
In order to control TurtleBot3 with a keyboard, please launch teleoperation feature with below command in a new terminal window.

   >$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
   
In order to run TurtleBot3 simulation that autonomously navigates around the map, open a new terminal window and enter below command.

   >$ export TURTLEBOT3_MODEL=burger
   
   >$ roslaunch turtlebot3_gazebo turtlebot3_simulation.launch
   
RViz visualizes published topics while simulation is running. You can launch RViz in a new terminal window by entering below command.

   >$ export TURTLEBOT3_MODEL=burger
   
   >$ roslaunch turtlebot3_gazebo turtlebot3_gazebo_rviz.launch   
   
   
