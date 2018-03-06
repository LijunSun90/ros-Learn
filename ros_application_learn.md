# Learn ROS applications via turtlebot 3 burger

Reference: [http://emanual.robotis.com/docs/en/platform/turtlebot3/applications/#applications] 

In order to implement these demos, you have to install the turtlebot3_applications package.

**[Remote PC]** Go to ROS source directory (/home/(user_name)/catkin_ws/src) and clone the turtlebot3_applications repository.

$ cd ~/catkin_ws/src
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_applications.git

**[Remote PC]** catkin_make to install the new package.

$ cd ~/catkin_ws && catkin_make



## 1. TurtleBot Follower Demo

Note : The follower demo was implemented only using a 360 Laser Distance Sensor LDS-01. a classification algorithm is used based on previous fitting with samples of person and obstacles positions to take actions. It follows someone in front of the robot within a 50 centimeter range and 140 degrees.

Note : Running the follower demo in an area with obstacles may not work well. Therefore, it is recommended to run the demo in an open area without obstacles.

**[TurtleBot]** In order to run the demo, parameter in LIDAR launch file has to be modified. In the param tag with frame_id as a name, replace base_scan to odom and save the file.

   >$ vi ~/catkin_ws/src/turtlebot3/turtlebot3_bringup/launch/turtlebot3_lidar.launch
   
   Note : Turtlebot Follower Demo requires scikit-learn, NumPy and ScyPy packages.
   
**[Remote PC]** Install scikit-learn, NumPy and ScyPy packages with below commands.

   >$ sudo apt-get install python-pip
   
   >$ sudo pip install -U scikit-learn numpy scipy
   
   >$ sudo pip install --upgrade pip
   
**[Remote PC]** When installation is completed, run roscore on the remote pc with below command.

   >$ roscore  
   
 **[TurtleBot]** Launch the Turtlebot3_bringup

   >$ roslaunch turtlebot3_bringup turtlebot3_robot.launch 
   
**[Remote PC]** Move to turtlebot3_follower source directory

   >$ cd ~/catkin_ws/src/turtlebot3_applications/turtlebot3_follower/src

**[Remote PC]** Launch turtlebot3_follow_filter with below command.

   >$ roslaunch turtlebot3_follow_filter turtlebot3_follow_filter.launch
   
**[Remote PC]** Launch turtlebot3_follower with below command.

   >$ rosrun turtlebot3_follower follower.py
   
   
