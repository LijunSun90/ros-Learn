
# Learn ROS and navigation through turtlebot 3 burger: Useful commands:

**Reference:** [http://emanual.robotis.com/docs/en/platform/turtlebot3/navigation/#navigation](http://emanual.robotis.com/docs/en/platform/turtlebot3/navigation/#navigation)

**Warning** : Make sure to run the [Bringup](https://github.com/LijunSun90/swarm-robots-SLAM-Learn/blob/master/ros_burger_learn.md) instruction before performing Example.

The Navigation locates TurtleBot3 to the calculated position in the map by combining actual sensor data and anticipated position data.


## 1. Perform Navigation

**[Remote PC]** Launch the navigation file. If you have TurtleBot3 Burger,

   >$ export TURTLEBOT3_MODEL=burger

   >$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
   
   
**[Remote PC]** Launch the Rviz.

   >$ rosrun rviz rviz -d `rospack find turtlebot3_navigation`/rviz/turtlebot3_nav.rviz

**[Remote PC]** Before starting the navigation, RViz should be updated with initial location and pose of TurtleBot3. To upate the initial data, follow the instruction below.

* Click the 2D Pose Estimate button.

* Click on the approxtimate point in the map where the TurtleBot3 is located and drag the cursor to indicate the direction where TurtleBot3 faces.

Every green arrow stands for an expected position of TurtleBot3. The laser scanner will draw approximate figures of wall on the map. If the drawing doesn’t show the figures incorrectly, repeat localizing the TurtleBot3 from clicking 2D Pose Estimate button above.

**[Remote PC]** If TurtleBot3 is localized, it will automatically create the path to the target position. In order to set a goal position, follow the instruction below.

* Click the 2D Nav Goal button.

* Click on a specific point in the map to set a goal position and drag the cursor to the direction where TurtleBot should be facing at the end.

Setting a goal position might fail if the path to the goal position cannot be created. If you wish to stop the robot before it reaches to the goal position, set the current position of TurtleBot3 as a goal position.
