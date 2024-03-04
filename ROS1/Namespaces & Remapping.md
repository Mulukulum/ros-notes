# Namespaces
## Messages Streams are called [[../ROS2/Topics]] in ROS

- ### Following the convention of Unix paths and Internet URIs, ROS uses the forward slash (/) to delimit namespaces. 
- ### ROS can launch identical nodes into separate namespaces to avoid name collisions.
- ### A robot with two cameras could launch two camera drivers in separate namespaces, such as left and right, which would result in image streams named left/image and right/image.

# A problem with this approach is if another node was expecting to get data from a topic called `images` it won't be able to get this information now

# Remapping

- ### In ROS, any string in a program that defines a name can be remapped at runtime. As one example, there is a commonly used program in ROS called image_view that renders a live video window of images being sent on the image topic
- ### Using remapping, we can instead cause the image_view program to render the right/image topic, or the left/image topic, without having to modify the source code.
## Syntax :  `./image_view image:=right/image` 
<br>

![](<Images/Remapping Diagram.png>)

## Pushing a node into a namespace can be accomplished with a special `__ns` namespace-remapping syntax. 

## Example `./camera __ns:=right`






