- # Usually hosted on port 11311 
	- [i] Use `echo $ROS_MASTER_URI` to see the port
# What it is:
- ## Metadata node that allows ROS nodes to find each other
# What it isn't :
- ## A server to transfer messages
<br>
- [!]  # **IMPORTANT**:
- ### ROS is NOT a client server based architecture. 
- ### All communications happen peer-to-peer between nodes. 
- ### ROS Master is only a node that provides information to other nodes about the whereabouts of all the other nodes. 
- ### ROS nodes cannot communicate without ROS Master
<br>

![](<Images/ROSCore Graph.png>)
- [i] ### Every node connects to roscore at startup to register details of the message streams it publishes and the streams to which it wishes to subscribe.

- [i] ### When a new node appears, roscore provides it with the information that it needs to form a direct peer-to-peer connection with other nodes publishing and subscribing to the same message topics.
