## Setup ROS Master Node : `roscore` 
[[ROS Master]]
## Find a Package : `rospack find [package_name]`
### Example : `rospack find roscpp`

## Change Directory to a Package : 
### `roscd <package-or-stack>[/subdir]`

### Example : `roscd roscpp/cmake`

## Run a ROS program :  `rosrun [PKG] [EXEC] [ARGS]`
## See whats in a package `rosls roscpp_tutorials`

## See current ROS Nodes Graph `rqt_graph`

## See running ROS Nodes `rosnode list`
## Get info about running Nodes : `rosnode info /<NAME>`
## Ping a ROS Node : `rosnode ping <NODE>`

#TEMP ````

roslaunch gazebo_ros empty_world.launch world_name:=$(pwd)/Tools/simulation/gazebo-classic/sitl_gazebo-classic/worlds/empty.world

