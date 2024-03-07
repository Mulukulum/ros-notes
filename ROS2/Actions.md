# What are they?
- Communication type intended for long running tasks.
- ## Consists of 3 Parts : 
	- *Goal*
	- *Feedback*
	- *Result*
- Build on top of Services and Topics
- Similar to services but they can be cancelled
- Provides continuous feedback instead of a single response like 'Actions'.

### An “action client” node sends a goal to an “action server” node that acknowledges the goal and returns a stream of feedback and a result.

![Action-SingleActionClient](Images/Action-SingleActionClient.gif)

# Get all available actions
```sh
ros2 action list
```
# Get info about an action
```sh
ros2 action info <action_name>
```
# Send an Action Goal
```sh
ros2 action send_goal <action_name> <action_type> <values>
```
- [i] *`<values>`* needs to be in YAML format
- [i] Add *`--feedback`* to view the feedback from the action server

### A robot system would likely use actions for navigation. An action goal could tell a robot to travel to a position. While the robot navigates to the position, it can send updates along the way (i.e. feedback), and then a final result message once it’s reached its destination.

### Turtlesim actions involve rotation to a particular orientation. The result is "Delta" which is how much the final position is different from the initial position. The feedback is the remaining angle.
