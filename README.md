# Task 5 - Robot Description (ROS 2 Jazzy)

## Overview

This repository contains the solution for **Task 5 – Robot Description** from the **ETGAH ROS 2 Training Program**.

The project demonstrates how to build a complete mobile robot description using **Xacro**, visualize it in **RViz2**, and spawn it inside **Gazebo Sim** using ROS 2 Jazzy.

The robot model includes:

* Differential drive mobile robot
* Base footprint and base link
* Left and right driving wheels
* Rear caster wheel
* LiDAR sensor
* ZED stereo camera
* Proper visual, collision, and inertial properties
* Gazebo plugins and ROS-Gazebo bridge configuration

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
* Custom mesh integration
* Realistic inertial properties
* Collision geometry
* RViz visualization
* Gazebo simulation
* ROS-Gazebo bridge configuration
* Complete TF tree

---

## Robot Components

The robot consists of:

* **Base Footprint**
* **Base Link**
* **Left Wheel**
* **Right Wheel**
* **Caster Wheel**
* **LiDAR Sensor**
* **ZED Stereo Camera**

The wheels are generated using reusable **Xacro macros**, making the robot description cleaner and easier to maintain.

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
* Physical inertia
* Mass properties
* Fixed joints
* Continuous wheel joints
* Sensor meshes
* Gazebo-specific configuration

---

## TF Tree

The generated TF tree is included in:

```text
TF_Tree.pdf
```

It illustrates the relationship between the robot links and coordinate frames.

---

## Demonstration

Two demonstration videos are included inside the repository.

### RViz Visualization

```text
Demo_videos/display_launch_file.mp4
```

Shows the robot model loaded in RViz2 with the TF tree.

### Gazebo Simulation

```text
Demo_videos/gazebo_launch_file.mp4
```

Shows the robot successfully spawned inside Gazebo Sim.

---

## Requirements

* ROS 2 Jazzy
* Gazebo Sim
* RViz2
* xacro
* robot_state_publisher
* joint_state_publisher_gui
* ros_gz_sim
* ros_gz_bridge
* TurtleBot3 Gazebo package

---

## Learning Objectives

This project demonstrates the following ROS 2 concepts:

* Building robot models using Xacro
* Creating reusable robot components
* Defining visual and collision geometries
* Adding inertial properties
* Using meshes inside URDF/Xacro
* Launching robots in RViz2
* Spawning robots into Gazebo Sim
* Configuring ROS-Gazebo communication
* Understanding the TF tree

---

## Author

**Ahmed Shalash**

