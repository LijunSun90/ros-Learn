# Learn ROS and SLAM through turtlebot 3 burger: Useful commands:

## Example: Bringup

Reference: file:///home/lijunsun/Downloads/TurtleBot3.html

**[Remote PC]** Run roscore.

>$ roscore

**[TurtleBot]** Bring up basic packages to start TurtleBot3 applications.

   >$ roslaunch turtlebot3_bringup turtlebot3_robot.launch

   Tip : If you want to launch Lidar sensor and core separately, please use below commands.

   >$ roslaunch turtlebot3_bringup turtlebot3_lidar.launch
 
   >$ roslaunch turtlebot3_bringup turtlebot3_core.launch

**[Remote PC]** Run RViz

   >$ export TURTLEBOT3_MODEL=burger
   
   >$ roslaunch turtlebot3_bringup turtlebot3_remote.launch
   
   >$ rosrun rviz rviz -d `rospack find turtlebot3_description`/rviz/model.rviz
   
   
