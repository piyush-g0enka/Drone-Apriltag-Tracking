# Drone ApriltagTracking

Drone - MODAL AI VOXL2

First install the voxl-mpa updated .deb package in the drone. This package is modified to output apriltag id in header.frame_id field of tagpose topics.

Place apriltag_localize and px4_ros_com in a ros2 workspace in the drone and build the packages. Installation of px4_msgs ROS2 package is also required.
 
## YouTube Video
[![Drone Apriltag Tracking Video](https://github.com/piyush-g0enka/Drone-Apriltag-Waypoint-Navigation/blob/main/images/yt.png)](https://www.youtube.com/watch?v=SFHdX0v_6u8)


## Usage

``` bash
$ ros2 run voxl_mpa_to_ros2 voxl_mpa_to_ros2_node 

$ ros2 run apriltag_localize apriltag_localize_node 

$ python3 ~/[path_to_package]/px4_ros_com/src/examples/offboard_py/offboard_apriltag_tracking.py

```

You could also run offboard_apriltag_tracking.py as ROS2 nodes using ros2 run command. For that they need to be configured in the CMakeLists.txt file 
