# Task 5 - Robot Description

## Overview

This repository contains my solution for **Task 5 – Robot Description** from the **ETGAH ROS 2 Training Program**.

The project demonstrates how to build a complete mobile robot description using **Xacro**, visualize it in **RViz2**, and simulate it in **Gazebo Sim** using **ROS 2**.

The robot model includes:

* Differential drive mobile robot
* Base footprint and base link
* Left and right driving wheels
* Rear caster wheel
* LiDAR sensor
* ZED stereo camera
* Proper visual, collision, and inertial properties
* Gazebo plugins
* ROS-Gazebo bridge configuration

---

## Project Structure

```text
robot_description/
├── config/
│   └── gz_bridge.yaml
├── Demo_videos/
│   ├── display_launch_file.mp4
│   └── gazebo_launch_file.mp4
├── launch/
│   ├── display.launch.py
│   └── gazebo.launch.py
├── meshes/
│   ├── lidar.STL
│   └── zed.stl
├── rviz/
│   ├── gazebo_robot_view.rviz
│   └── robot_view.rviz
├── urdf/
│   ├── robot.gazebo.xacro
│   └── robot.urdf.xacro
├── TF_Tree.pdf
├── CMakeLists.txt
├── package.xml
└── README.md
```

---

## Features

* Robot description written using **Xacro**
* Modular robot design
* Differential drive mobile robot
* Custom mesh integration
* Realistic inertial properties
* Collision geometry
* RViz visualization
* Gazebo simulation
* ROS-Gazebo bridge configuration
* LiDAR sensor
* ZED camera
* Complete TF tree

---

## Robot Components

The robot consists of:

* Base Footprint
* Base Link
* Left Wheel
* Right Wheel
* Rear Caster Wheel
* LiDAR Sensor
* ZED Stereo Camera

The wheels are implemented using reusable **Xacro macros**, making the robot description modular, clean, and easy to maintain.

---

## Launch Files

### Display the Robot in RViz

```bash
ros2 launch robot_description display.launch.py
```

This launch file starts:

* Joint State Publisher GUI
* Robot State Publisher
* RViz2

It is used to inspect the robot model and verify the TF tree.

---

### Launch the Robot in Gazebo

```bash
ros2 launch robot_description gazebo.launch.py
```

This launch file:

* Starts Gazebo Sim
* Loads the TurtleBot3 House world
* Publishes the robot description
* Spawns the robot
* Starts the ROS-Gazebo bridge
* Opens RViz2

---

## Robot Description

The robot description includes:

* Visual geometry
* Collision geometry
* Inertial properties
* Mass properties
* Fixed joints
* Continuous wheel joints
* Sensor meshes
* Gazebo plugins
* ROS-Gazebo bridge configuration

---

## TF Tree

The generated TF tree for the robot is available in the repository.

📄 **View the TF Tree:** [TF_Tree.pdf](TF_Tree.pdf)

---

## Demonstration

### RViz Visualization

🎥 **Demo Video**

[▶️ display_launch_file.mp4](Demo_videos/display_launch_file.mp4)

This demonstration shows:

* Robot visualization in RViz2
* Joint State Publisher GUI
* Robot State Publisher
* Complete TF tree
* Sensor frames

---

### Gazebo Simulation

🎥 **Demo Video**

[▶️ gazebo_launch_file.mp4](Demo_videos/gazebo_launch_file.mp4)

This demonstration shows:

* Robot spawning in Gazebo Sim
* Gazebo plugins
* LiDAR sensor
* ZED camera
* ROS-Gazebo bridge
* Robot visualization in RViz2

---

## Learning Objectives

This project demonstrates the following ROS 2 concepts:

* Building robot models using Xacro
* Creating reusable robot components
* Defining visual, collision, and inertial properties
* Using custom meshes inside URDF/Xacro
* Launching robots in RViz2
* Spawning robots into Gazebo Sim
* Configuring ROS-Gazebo communication
* Understanding the TF tree
* Integrating sensors into a robot model

---

## Author

**Ahmed Shalash**
