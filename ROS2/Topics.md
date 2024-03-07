# What is it?
### ROS 2 breaks complex systems down into many modular nodes. Topics are a vital element of the ROS graph that allows nodes to exchange messages.
# What can it do?
### A node may publish data to any number of topics and simultaneously have subscriptions to any number of topics.

![TopicMultiplePublisherandMultipleSubscriber](Images/TopicMultiplePublisherandMultipleSubscriber.gif)

Use 
```sh
rqt_graph
```
to view the ROS Graph.

# Topics
```sh
ros2 topic info <topic_name> # Shows information about topic

# Type: geometry_msgs/msg/Twist
# Publisher count: 1
# Subscription count: 2
```

## `ros2 topic list -t` shows the topics with their respective types

## `ros2 topic echo <topic_name>` prints the data on that topic to the terminal.

## `ros2 interface show <datatype>` shows the individual components of said data type.
```
ros2 interface show geometry_msgs/msg/Twist

Vector3  linear
            float64 x
            float64 y
            float64 z
    Vector3  angular
            float64 x
            float64 y
            float64 z
```

# Publishing to a Topic
## Now that you have the message structure, you can publish data to a topic directly from the command line using:

```sh
ros2 topic pub <topic_name> <msg_type> '<args>' 
```
- [i] The `-r rate` argument can be used to publish the value at a particular rate. 

### The `'<args>'` argument is the actual data you’ll pass to the topic,
### This argument must be in YAML format.
```sh
ros2 topic pub --once /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0, y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 1.8}}" 
```

# Publishing Rate of a Topic
```sh
ros2 topic hz <topic_name>
```

