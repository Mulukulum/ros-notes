# What are they?
- ## Configuration Values for nodes are the Parameters
- ## Node settings basically
- ### Can store parameters datatypes like numerics and strings


## Get a parameter
```sh
ros2 param get <node_name> <parameter_name>
```
## Set a parameter
```sh
ros2 param set <node_name> <parameter_name> 
```
## Get current parameters
```sh
ros2 param dump <node_name>
```
## Load parameters
```sh
ros2 param load <node_name> <parameter_file>
# To load parameters on startup
ros2 run <package_name> <executable_name> --ros-args --params-file file.yaml
```
- [i] ROS2 Nodes take their inputs in YAML format


