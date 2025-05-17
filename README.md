# astro_nav_sim

A ROS package for simulating and navigating planetary surfaces (Moon, Mars) in Gazebo.

---

## Features

* Custom Gazebo world files for lunar and Martian terrains
* Launch files to start simulation environments and spawn robots

---

## Prerequisites

* ROS Noetic (or Melodic)
* Gazebo 11 (or compatible version)


---

## Installation

```bash
# Clone into your catkin workspace
cd ~/catkin_ws/src
git clone https://github.com/YeatsWang/astro_nav_sim.git

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

Modify the world name in the launch file
```bash
roslaunch astro_nav_sim load_world.launch
````

---

## Directory Structure
```
astro_nav_sim/
├── CMakeLists.txt
├── package.xml
├── worlds/
│   ├── moon.world            # ezrassor_sim_gazebo
│   └── mars.world
│   └── tile_test.world
│   └── mars_curiosity.world  # space_ros_demos
│   └── low_moon.world        # Space_Exploration_Rover
│   └── flat_mars.world
│   └── flat_mars.world
│   └── forest.world
├── models/
│   ├── dem_moon/
│   ├── dem_mars/
│   └── ...
├── launch/
│   └── load_world.launch
└── README.md
```


---

## Model Sources

The following open‑source projects provided models, environments and ideas.

* ezrassor_sim_gazebo: [https://github.com/FlaSpaceInst/ezrassor_sim_gazebo](https://github.com/FlaSpaceInst/ezrassor_sim_gazebo)
* space_ros_demos: [https://github.com/space-ros/demos](https://github.com/space-ros/demos)
* Space_Exploration_Rover: [https://github.com/maverickayush7/Space_Exploration_Rover](https://github.com/maverickayush7/Space_Exploration_Rover)
* MarsSim: [https://github.com/MorpheusPD/MarsSim](https://github.com/MorpheusPD/MarsSim)
* space_robotics_gz_envs: [https://github.com/AndrejOrsula/space_robotics_gz_envs](https://github.com/AndrejOrsula/space_robotics_gz_envs)
* gazebo_models: [https://github.com/osrf/gazebo_models](https://github.com/osrf/gazebo_models)

---

## Contributing

Contributions welcome! Please fork the repo and submit pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.