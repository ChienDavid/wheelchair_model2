cmake_minimum_required(VERSION 2.8.3)
project(wheelchair_description)
# add_compile_options(-std=c++11)
find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  roscpp
  rospy
  rviz
  tf
  urdf
  xacro
)

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
#  INCLUDE_DIRS include
#  LIBRARIES wheelchair_description
#  CATKIN_DEPENDS geometry_msgs roscpp rospy rviz tf urdf xacro
#  DEPENDS system_lib
)

###########
## Build ##
###########

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

#############
## Install ##
#############

install(DIRECTORY meshes rviz urdf
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
 )
#############
## Testing ##
#############

