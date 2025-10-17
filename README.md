# ros_project_team-5
# ☕ Café Delivery Robot – ROS End Semester Project

## 📘 Overview
**Café Delivery Robot** is a ROS 2 (Humble)-based **TurtleBot3 simulation** project developed using **Gazebo 11**.  
It demonstrates an autonomous **service robot** operating inside a **café environment**, performing indoor navigation, obstacle detection and item delivery between tables and counters.

This project was built for the **End-Semester Practical**, under the workspace **`sem_proj`**.

---

## 🚀 Features
- 🤖 TurtleBot3 (Burger) robot simulation  
- 🏠 Realistic café world with tables, walls, and décor  
- 🗺️ SLAM & navigation-ready environment  
- 🎮 Launch files for spawning and control  
- 🎥 Optional ROS 2 bag recording  
- ⚙️ Modular and reusable ROS 2 package structure  

---

## 📁 Project Structure
```
sem_proj
├── src/
│   └── delivery_bot/
│       ├── launch/
│       │   ├── obstacle_course.launch.py
│       │   ├── hamburger_walker.launch.py
│       ├── worlds/
│       │   ├── obstacle_course.world
│       └── scripts/
│           └── hamburger_drive.py
├── build/
├── install/
└── README.md
```
---

## ⚙️ Prerequisites
- Ubuntu 22.04 LTS  
- ROS 2 Humble Hawksbill  
- Gazebo 11  
- TurtleBot3 packages  
- Colcon build system  

---

## 🧩 Installation and Setup

# Create and build workspace
```
mkdir -p ~/sem_proj/src
cd ~/sem_proj/src
```
# Clone this repository
```
```

# Build the workspace
```
cd ~/sem_proj
colcon build
```
# Source the setup file
```
source install/setup.bash
```
---

## 🎮 Running the Simulation

 1️⃣ Launch the Café World and Robot in Gazebo
```
ros2 launch delivery_bot obstacle_course.launch.py x_pose:=0 y_pose:=0
```
 2️⃣  Run Cartographer / SLAM for Mapping
```
ros2 launch delivery_bot cartographer.launch.py use_sim_time:=True
```

 3️⃣Navigate or Control the Robot
```
ros2 launch delivery_bot hamburger_walker.launch.py
```

---

## Acess the simulation video in ppt 

## Once all nodes are running:
 - The TurtleBot3 Burger will spawn inside the café world in Gazebo.
 - Open RViz2 to visualize SLAM mapping and navigation paths.
 - The robot autonomously moves between café tables and counter positions, simulating item delivery.
 - You can modify waypoints and delivery routes by editing the `hamburger_drive.py` script.

---

## 📸 Example Output
- Café environment loaded in Gazebo with tables and walls.
- Real-time SLAM map generated in RViz2.
- The robot navigating autonomously using pre-defined waypoints.

---

## 🧰 Troubleshooting

# Check environment variable
```
echo $TURTLEBOT3_MODEL
```
# Source setup file again
```
source ~/sem_proj/install/setup.bash
```

# Clean and rebuild if errors occur
```
cd ~/sem_proj
colcon build --symlink-install --packages-select delivery_bot
```
---

## 👨‍💻 Authors
```
 Team 5 — End Semester Project
 Amrita Vishwa Vidyapeetham , Chennai Campus
 Course: Robotics & Automation (ROS 2 Simulation)
 Members:
 - Anirudh V - CH.SC.U4AIE23003
 - Madhumita K - CH.SC.U4AIE23027
 - Rishitha Mopuri - CH.SC.U4AIE23030
 - Akshanth Chouhan- CH.SC.U4AIE23031
```


## 🧩 Future Enhancements
- Add voice command control for delivery requests
- Include multi-robot coordination inside café
- Real-world deployment using TurtleBot3 hardware
