# Basic commands : 

```sh
ros2 node list # Lists nodes
ros2 topic list # Lists Topics
ros2 service list # Lists services
ros2 action list # Lists actions
```
# ros2 run
```sh
ros2 run <package_name> <executable_name>
```

## Remapping

[Remapping](https://design.ros2.org/articles/ros_command_line_arguments.html#name-remapping-rules) allows you to reassign default node properties, like node name, topic names, service names, etc., to custom values.

```sh
ros2 run turtlesim turtlesim_node --ros-args --remap __node:=my_turtle
```

The `__node` attribute is special in that it decides the name of the node. 

# ros2 node
```sh
ros2 node info <node_name>
```

Gets more information about that particular node.

Example:
```sh
ros2 node info /my_node
```
