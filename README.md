# Task-1

install VirtualBox

install Ubuntu 18.04

Install ROS melodic by those commands in WIKI ROS
http://wiki.ros.org/melodic/Installation/Ubuntu

Then I started Installing the package arduino robot arm by those commands :
  $ cd ~/catkin_ws/src
	$ sudo apt install git
	$ git clone https://github.com/smart-methods/arduino_robot_arm
  $ cd ~/catkin_ws
	$ rosdep install --from-paths src --ignore-src -r -y
	$ sudo apt-get install ros-melodic-moveit
	$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
	$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
	$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
  $ catkin_make

after that the and RViz was working and I can control the arm 
Now I want to use Gezabo and control the arm by using the same plug of RViz so I used those Commands :
 First I need to change the permission so I enter this command
 	$ cd catkin/src/arduino_robot_arm/robot_arm_pkg/scripts
then 
	$ sudo chmod +x joint_states_to_gazebo.py
now I am done with changing
then I opened each command in single terminal :
$ roslaunch robot_arm_pkg check_motors.launch
$ roslaunch robot_arm_pkg check_motors_gazebo.launch
$ rosrun robot_arm_pkg joint_states_to_gazebo.py --- this one you have to enter it on the last. after you opened RViz and Gezabo.
