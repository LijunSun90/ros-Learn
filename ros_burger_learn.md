# Learn ROS through turtlebot 3 burger: Useful commands:

## Example 1: Bringup

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
   
   >$ rosrun rviz rviz -d \`rospack find turtlebot3_description\`/rviz/model.rviz
   
   
**Warning** : Make sure to run the above Bringup instruction before performing the following examples.   
   
   
## Example 2: Teleoperation by keyboard

**[Remote PC]** Launch the file for simple teleoperation test.

   >$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch


## Example 3: rqt

Reference: [Link](http://emanual.robotis.com/docs/en/platform/turtlebot3/example/#example)

The rqt is a Qt-based framework for GUI development for ROS. The rqt is a tool that allows users to easily see the topic status by displaying all the topics in the topic list. There are topic names, types, bandwidth, Hz, value in GUI.

**[Remote PC]** Run the rqt.

   >$ rqt

Tip : If rqt is not displayed, select the plugin -> Topics -> Topic Monitors.


## Example 4: Interactive Markers

Reference: [Link](http://emanual.robotis.com/docs/en/platform/turtlebot3/example/#example)

Turtlebot3 can be moved by interactive markers on RViz. You can move the turtlebot3 to rotate or linear using interactive markers.

**[Remote PC]** Open a new terminal and launch the remote file. 

   >$ roslaunch turtlebot3_bringup turtlebot3_remote.launch

**[Remote PC]** launch the interactive markers file.

   >$ roslaunch turtlebot3_example interactive_markers.launch
   
**[Remote PC]** Visualize the model in 3D with RViz.

   >$ rosrun rviz rviz -d `rospack find turtlebot3_example`/rviz/turtlebot3_interactive.rviz


## Example 5: Obstacle Detection

Turtlebot3 can be moved or stopped by LDS data. When the turtlebot3 moves, it stops when it detects an obstacle ahead.

**[Remote PC]** Run the obstacle file.

   >$ rosrun turtlebot3_example turtlebot3_obstacle.py


## Example 6: Point operation

Turtlebot3 can be moved by 2D point(x,y) and z-angular. For example, if you insert (0.5, 0.3, 60), turtlebot3 moves to point (x = 0.5m, y = 0.3m) and then rotates 60 deg.

**[Remote PC]** launch the pointop file.

   >$ roslaunch turtlebot3_example turtlebot3_pointop_key.launch


## Example 7: Patrol

Turtlebot3 can be moved by custom routes. There are three routes(rectangle, triangle and circle). This example uses action topic. Action client translates patrol data(mode, area, count) to action server. And then action server translates cmd_vel to turtlebot3.

**[Remote PC]** Run the patrol server file.

   >$ rosrun turtlebot3_example turtlebot3_server.py
   
**[Remote PC]** Run the patrol client file.

   >$ rosrun turtlebot3_example turtlebot3_client.py
