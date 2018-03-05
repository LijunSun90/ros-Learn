
# Learn ROS and SLAM through turtlebot 3 burger: Useful commands:

**Reference: **[http://emanual.robotis.com/docs/en/platform/turtlebot3/slam/#slam](http://emanual.robotis.com/docs/en/platform/turtlebot3/slam/#slam)

**Warning** : Make sure to run the [Bringup](https://github.com/LijunSun90/swarm-robots-SLAM-Learn/blob/master/ros_burger_learn.md) instruction before performing Example.


## 1. Create a Map with Teleoperation

**[Remote PC]** Open a new terminal and launch the SLAM file. If you have TurtleBot3 Burger,

   >$ export TURTLEBOT3_MODEL=burger
   
   >$ roslaunch turtlebot3_slam turtlebot3_slam.launch


**[Remote PC]** Visualize the model in 3D with RViz.

   >$ rosrun rviz rviz -d `rospack find turtlebot3_slam`/rviz/turtlebot3_slam.rviz

**[Remote PC]** Teleoperation with Keyboard

   >$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

## 2. Save the Map

**[Remote PC]** Open a new terminal and run the map saver node.

   >$ rosrun map_server map_saver -f ~/map

map.pgm and map.yaml files will be created in the ~/ ($HOME directory : /home/<username>) directory.
