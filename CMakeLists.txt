cmake_minimum_required(VERSION 3.0.2)
project(astro_nav_sim)

## Compile as C++11
add_definitions(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
        roscpp
        rospy
        std_msgs
        gazebo_ros
        tf
        nav_msgs
        map_server
        amcl
        move_base
        )

catkin_package(
        INCLUDE_DIRS include
        LIBRARIES ${PROJECT_NAME}
        CATKIN_DEPENDS roscpp rospy std_msgs gazebo_ros tf nav_msgs map_server amcl move_base
)

include_directories(
        include
        ${catkin_INCLUDE_DIRS}
)

## Install directories
install(DIRECTORY worlds
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
        )
install(DIRECTORY models
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
        )
install(DIRECTORY launch
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
        )