
# Some useful ros commands:

## Navigating the ROS Filesystem

> rospack = ros + pack(age)
---

rospack allows you to get information about packages. In this tutorial, we are only going to cover the find option, which returns the path to package.

Usage:

$ rospack find [package_name]
Example:

$ rospack find roscpp

> roscd = ros + cd
---

roscd is part of the rosbash suite. It allows you to change directory (cd) directly to a package or a stack.

Usage:

$ roscd [locationname[/subdir]]

To verify that we have changed to the roscpp package directory, run this example:

$ roscd roscpp


> rosls = ros + ls
---

rosls is part of the rosbash suite. It allows you to ls directly in a package by name rather than by absolute path.

Usage:

$ rosls [locationname[/subdir]]

Example:

$ rosls roscpp_tutorials


## CreatingPackage

First change to the source space directory of the catkin workspace:

$ cd ~/catkin_ws/src

Now use the catkin_create_pkg script to create a new package called 'beginner_tutorials' which depends on std_msgs, roscpp, and rospy:

$ catkin_create_pkg beginner_tutorials std_msgs rospy roscpp      

Now you need to build the packages in the catkin workspace:

$ cd ~/catkin_ws

$ catkin_make

After the workspace has been built it has created a similar structure in the devel subfolder as you usually find under /opt/ros/$ROSDISTRO_NAME.

To add the workspace to your ROS environment you need to source the generated setup file:


$ . ~/catkin_ws/devel/setup.bash
