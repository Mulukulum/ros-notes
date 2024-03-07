- ## Services are another method of communication for nodes in the ROS graph.
- ## Services are based on a call-and-response model
- ## Services only provide data when they are specifically called by a client.

![Services](Images/Services.gif)
# Services

```sh
ros2 services list # Shows list of services
```

- Services have types that describe how the request and response data of a service is structured.
- Service types have two parts: 
	- 1.)  Message for the *request*
	- 2.) Message for the *response*

```sh
ros2 service type <service_name> # Shows the type of the service
ros2 service list -t # Shows types
ros2 service find std_srvs/srv/Empty # Shows all services of this type
```

## Get information about the message type using
```sh
ros2 interface show std_srvs/srv/Empty
```

## Call a service using : 
```sh
ros2 service call <service_name> <service_type> <arguments>
```
