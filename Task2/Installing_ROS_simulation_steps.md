# These will be the steps to install the tools needed for simulating, mapping, and controlling a turtlebot robot.

the links should direct you to the required commands immediatly.

1. Make sure you already have a running VM with ubuntu 18.04 OS, and already installed ROS Melodic inside it.
2. Enter this [Turtlebot3 Install](https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/#pc-setup) website and follow the instructions to install Install Dependent ROS 1 Packages , and Install TurtleBot3 Packages.
3. Enter this website [Simulation Install](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/#install-simulation-package) and follow the instructions to install a Simulation Package **You ONLY should  do the first step in this page which is (6. 1. 1. Install Simulation Package)**.
4. Make sure to Type "*$ cd*" or make a new terminal after the 3rd step
5. After you are done type in this command in the terminal "*$ source catkin_ws/devel/setup.bash*"

6. open this website and follow the instructions at [6. 2. 1. Launch Simulation World](https://emanual.robotis.com/docs/en/platform/turtlebot3/slam_simulation/#launch-simulation-world-1) which says "TurtleBot3 World" to launch Turtlebot and also launch the gazebo world.
7. In the same website as step 6 scroll down in the page to here [6. 2. 2. "Run SLAM Node"](https://emanual.robotis.com/docs/en/platform/turtlebot3/slam_simulation/#run-slam-node-1) to run the SLAM Node and see the generated map by the Robot.

6. open this website [6. 2. 3. Run Teleoperation Node](https://emanual.robotis.com/docs/en/platform/turtlebot3/slam_simulation/#run-teleoperation-node-1) After you run the 2 codes Now you should be able to control the robot using the keys WASDX to roam around the gazebo simulated map.
7. After you are done exploring the map with your robot you should save the map using (Ctrl + Alt + T).
