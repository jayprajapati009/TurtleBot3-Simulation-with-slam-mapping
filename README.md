# TurtleBot3-Simulation-with-slam-mapping
This is a small documentation to use TurtleBot3 Simulation in ROS (Melodic) and Gazebo (9) along with slam mapping.

Install [ROS Melodic from here](http://wiki.ros.org/melodic/Installation/Ubuntu) and [Gazebo 9 from here](http://gazebosim.org/tutorials?cat=install&tut=install_ubuntu&ver=9.0).

### Install the TurtleBot3 Files 

To install the TurtleBot3 files follow the commands given below one by one,

```sh
cd ~/catkin_ws/src/
```

```sh
git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
```

```sh
git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
```

```sh
cd ~/catkin_ws && catkin_make
```

Now open the bashrc file by the command given below,

```
gedit ~/.bashrc
```

and add the below given line to the bottom of the bashrc file,

```
export TURTLEBOT3_MODEL=burger
```

Save the file and close it and then source the file using the following command, 

```
source ~/.bashrc
```

### Install the TurtleBot3 Simulation Files 

To download the files follow the commands,

```
cd ~/catkin_ws/src/
```

```
git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
```

```sh
cd ~/catkin_ws && catkin_make
```

### Install the SLAM Module

Open a new Terminal Window,

```
sudo apt install ros-melodic-slam-gmapping
``` 

### Simulating TurtleBot3 in Gazebo

Open Gazebo a new Terminal Window,

```
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

Open SLAM in a new Terminal Window in the rviz.

```
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```

Starting the Autonomous Navigation of the robot in a new Terminal Window:

```
roslaunch turtlebot3_gazebo turtlebot3_simulation.launch
```

#### And Kudos we made it, the first simulation using ROS and Gazebo. Thanks to Open Source!!

----------------------------------------------------------------------------------------------------------------------------

Tutorial Credits : https://automaticaddison.com/how-to-launch-the-turtlebot3-simulation-with-ros/
