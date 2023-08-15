# RoboticsAI.task2

## The second task of Robotics and AI is about Learning ROS through simulation with TurtleBot3 and Gazebo involves.

 1.Install ROS: First, you'll need to install ROS on your computer. You can follow the instructions on the ROS wiki to install the version that is appropriate for your operating system.
 2.Install TurtleBot3 and Gazebo: Once you have ROS installed, you can install the TurtleBot3 and Gazebo packages.
 3.Launch a simulation: Once you have TurtleBot3 and Gazebo installed, you can launch a simulation to test your code. You can do this by running a launch file that sets up the simulation environment and starts the necessary nodes.
 4.Develop and test your code: With the simulation environment up and running, you can start developing and testing your ROS code. You can use tools like RViz to visualize your robot and its surroundings, and you can use Gazebo to simulate sensors like cameras and lidars.
5.Iterate and refine: As you develop your code, you can iterate and refine it based on the results of your simulations. This allows you to experiment with different algorithms and approaches without risking damage to physical robots.

### install ROS packages:
```
sudo apt install ros-noetic-joy ros-noetic-teleop-twist-joy \
  ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
  ros-noetic-rgbd-launch ros-noetic-depthimage-to-laserscan \
  ros-noetic-rosserial-arduino ros-noetic-rosserial-python \
  ros-noetic-rosserial-server ros-noetic-rosserial-client \
  ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
  ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
  ros-noetic-compressed-image-transport ros-noetic-rqt* \
  ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers \
  ros-noetic-gazebo-ros-pkgs
```
Also install  TurtleBot's servo actuators and main communication:
```
sudo apt install ros-noetic-dynamixel-sdk
sudo apt install ros-noetic-turtlebot3-msgs
```

Install TurtleBot3 Simulations:

```
sudo apt install ros-noetic-turtlebot3
```

```
cd ~/catkin_ws/src/
git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
cd ~/catkin_ws && catkin_make
```

Finally set up environment variables:
```
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
source ~/.bashrc
```

### Simulation:
1. Launch Gazebo world.
2. Run the SLAM:
```
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
3. Launch the teleoperation node:
```
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

![258571015-34573417-c34c-4754-a209-c962c67db0ac](https://github.com/NouraNF/RoboticsAI.task2/assets/96024712/4607f9dd-1a36-49e2-b8aa-25ab91f74516)
