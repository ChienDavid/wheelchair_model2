cmake_minimum_required(VERSION 2.8.3)
project(wheelchair_gazebo)
add_compile_options(-std=c++11)
find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  geometry_msgs
  nav_msgs
  roscpp
  sensor_msgs
  std_msgs
  tf
)

find_package(gazebo REQUIRED)

################################################
## Declare ROS messages, services and actions ##
################################################

################################################
## Declare ROS dynamic reconfigure parameters ##
################################################

###################################
## catkin specific configuration ##
###################################

catkin_package(
  INCLUDE_DIRS include
  CATKIN_DEPENDS gazebo_ros geometry_msgs nav_msgs roscpp sensor_msgs std_msgs tf
)

###########
## Build ##
###########

link_directories(${GAZEBO_LIBRARY_DIRS})

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
  ${GAZEBO_INCLUDE_DIRS}
)

#############
## Install ##
#############

#############
## Testing ##
#############

