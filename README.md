# astro_nav_sim

A ROS package for simulating and navigating planetary surfaces (Moon, Mars) in Gazebo.

---

## Features

* Custom Gazebo world files for lunar and Martian terrains
* URDF models for various rover platforms (e.g., 6-DOF arm rover, Boston Dynamics Spot)
* Launch files to start simulation environments and spawn robots
* Example navigation configurations using the ROS Navigation stack (move\_base, AMCL, costmaps)

---

## Prerequisites

* ROS Noetic (or Melodic)
* Gazebo 11 (or compatible version)
* ROS Navigation Stack
* Common ROS packages: `tf`, `map_server`, `amcl`, `move_base`

---

## Installation

```bash
# Clone into your catkin workspace
cd ~/catkin_ws/src
git clone https://github.com/yourusername/astro_nav_sim.git

# (Optional) Clone any model sources you plan to use:
# git clone https://github.com/theunknowninfinite/Modeling-and-Simulation-of-Martian-Rover.git models/martian_rover
# git clone https://github.com/aunefyren/mars_gazebo.git models/mars_gazebo
# ...

# Build and source
cd ~/catkin_ws
catkin_make
source devel/setup.bash

# add into ~/.bashrc
export GAZEBO_MODEL_PATH=~/catkin_ws/src/astro_nav_sim/models:${GAZEBO_MODEL_PATH}
export GAZEBO_RESOURCE_PATH=~/catkin_ws/src/astro_nav_sim/models:${GAZEBO_RESOURCE_PATH}

```

---


## Usage

### Lunar Simulation

```bash
roslaunch astro_nav_sim lunar.launch
```

### Martian Simulation

```bash
roslaunch astro_nav_sim martian.launch
```

## Directory Structure

```
astro_nav_sim/
├── CMakeLists.txt
├── package.xml
├── worlds/
│   ├── moon.world
│   └── mars.world
├── models/
│   ├── rover_6dof/
│   ├── spot/
│   └── ...
├── launch/
│   ├── lunar.launch
│   └── martian.launch
└── README.md
```

---

## Model Sources

The following open‑source projects provided models and environments.

* ezrassor_sim_gazebo: [https://github.com/FlaSpaceInst/ezrassor_sim_gazebo](https://github.com/FlaSpaceInst/ezrassor_sim_gazebo)
* space_ros_demos: [https://github.com/space-ros/demos](https://github.com/space-ros/demos)
* MarsSim: [https://github.com/MorpheusPD/MarsSim](https://github.com/MorpheusPD/MarsSim)
* space_robotics_gz_envs: [https://github.com/AndrejOrsula/space_robotics_gz_envs](https://github.com/AndrejOrsula/space_robotics_gz_envs)
* gazebo_models: [https://github.com/osrf/gazebo_models](https://github.com/osrf/gazebo_models)

---

## Contributing

Contributions welcome! Please fork the repo and submit pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.