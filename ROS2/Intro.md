## ROS2 doesn't have the concept of ROS Core.
## Instead it uses DDS in the backend so nodes can find each other.

# ROS Graph

The ROS graph is a network of ROS 2 elements processing data together at the same time. It encompasses all executables and the connections between them if you were to map them all out and visualize them.

![ROS2 Graph](Images/ROS2%20Graph.png)

Each node in ROS should be responsible for a single, modular purpose, e.g. controlling the wheel motors or publishing the sensor data from a laser range-finder. Each node can send and receive data from other nodes via topics, services, actions, or parameters.