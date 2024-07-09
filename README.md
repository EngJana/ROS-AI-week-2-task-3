# ROS-AI-week-2-task-3
ROS and AI week 2 samrt methods internship
task 3: ROS1-ROS2 Bridge

# ROS1-ROS2 Bridge Installation and Talker-Chatter Example
setting up the ROS1-ROS2 bridge and run the talker-output example

1.	source ROS noetic in one: 
$ source /opt/ros/noetic/setup.bash
2. another for ROS2 foxy in the other: 
$ source /opt/ros/foxy/setup.bash
3.	Install rospy_tutorials package in ROS1 environment: 
$ sudo apt install ros-noetic-rospy-tutorials
4.	Run the talker node: 
$ rosrun rospy_tutorials talker
<img width="854" alt="ros1b" src="https://github.com/EngJana/ROS-AI-week-2-task-3/assets/173661625/401dc514-981e-4172-b5ab-d8932d13e882">

6.	In a separate terminal check the list of available topics in ROS1: 
$ source /opt/ros/noetic/setup.bash
7. Verify if the /chatter topic is listed among the topics: 
$ rostopic list
8.	Install the ROS1-ROS2 bridge in a new terminal:
$ source /opt/ros/noetic/setup.bash
$ source /opt/ros/foxy/setup.bash
$ ros2 run ros1_bridge dynamic_bridge  
9.	In another terminal check the topic listed in ros2: 
$ ros2 topic list
10.	creating a subscriber for the /rosout topic using the ros2 topic echo command: 
$ ros2 topic echo /rosout

#### ROS2 receives the messages published by the ROS1 talker node and display it.
<img width="863" alt="ros2b" src="https://github.com/EngJana/ROS-AI-week-2-task-3/assets/173661625/94612a0f-232e-4301-92f3-13ba2004580e">



