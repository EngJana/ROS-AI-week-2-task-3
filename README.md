# ROS-AI-week1-task-3
ROS and AI week 1 
task 3: ROS1-ROS2 Bridge

# ROS1-ROS2 Bridge Installation and Talker-Chatter Example
setting up the ROS1-ROS2 bridge and run the talker-chatter example
## Open two terminals for ROS1
1.	source ROS noetic in one: 
$ source /opt/ros/noetic/setup.bash
2. another for ROS2 foxy in the other: 
$ source /opt/ros/foxy/setup.bash
3.	Install rospy_tutorials package in ROS1 environment: 
$ sudo apt install ros-noetic-rospy-tutorials
4.	Run the talker node: 
$ rosrun rospy_tutorials talker
5.	In a separate terminal check the list of available topics in ROS1: 
$ source /opt/ros/noetic/setup.bash
6.Verify if the /chatter topic is listed among the topics: 
$ rostopic list

## Open two terminals for ROS2
7.	Install the ROS1-ROS2 bridge in a new terminal: 
$ ros2 run ros1_bridge dynamic_bridge --bridge-all-topics --bridge-topic /ros1/chatter std_msgs/String  
8.	In another terminal check if the /chatter topic is now listed using the ros2 topic list command: 
$ ros2 topic list
9.	creating a subscriber for the /chatter topic using the ros2 topic echo command: 
$ ros2 topic echo /chatter

#### ROS2 receives the messages published by the ROS1 talker node and display it.
