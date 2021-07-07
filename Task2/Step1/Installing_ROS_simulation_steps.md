# These will be the steps to install the tools needed for simulating, mapping, and controlling a turtlebot robot.


**1.Make sure you already have a running VM with ubuntu 18.04 OS, and already installed ROS Melodic inside it.**

**2.type in the commands down below in the terminal**

||_Install ROS 1 on Remote PC 3. 1. 2._
 ```
$ sudo apt update
$ sudo apt upgrade
$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_melodic.sh
$ chmod 755 ./install_ros_melodic.sh 
$ bash ./install_ros_melodic.sh
 ```
||_Install Dependent ROS 1 Packages 3. 1. 3._
```
$ sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy \
  ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc \
  ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan \
  ros-melodic-rosserial-arduino ros-melodic-rosserial-python \
  ros-melodic-rosserial-server ros-melodic-rosserial-client \
  ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server \
  ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro \
  ros-melodic-compressed-image-transport ros-melodic-rqt* \
  ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers
```
||_Install TurtleBot3 Packages 3. 1. 4._
```
$ sudo apt-get install ros-melodic-dynamixel-sdk
$ sudo apt-get install ros-melodic-turtlebot3-msgs
$ sudo apt-get install ros-melodic-turtlebot3

```
**3. Enter these codes in the terminal to install Simulation packages**

||_Simulation Install 6. 1. 1._
```
$ cd ~/catkin_ws/src/
$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make

```
 
**4. Make sure to Type "*$ cd*" or make a new terminal after the 3rd step**

**5. After you are done type in this command in the terminal**
```
$ source ~/catkin_ws/devel/setup.bash
```
**6.In a new terminal Run these commands in the terminal to launch the simulation world.**

||_6. 2. 1. Launch Simulation World_
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

```


**7.In a new terminal Run these commands in the terminal to launch the SLAM Node.**

||_6. 2. 2. "Run SLAM Node"_
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
**to run the SLAM Node and see the generated map by the Robot.**

**8.In a new terminal Run this command to be able to interact and control the robot**

||_6. 2. 3. Run Teleoperation Node_
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
**After you run the 2 codes Now you should be able to control the robot using the keys WASDX to roam around the gazebo simulated map.**

**9. After you are done exploring the map with your robot you should save the map using (Ctrl + Alt + T).**

**You are done.**

For more information make sure to visit this website from which i took these steps [Robotis](https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/).
