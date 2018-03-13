
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
