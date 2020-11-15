cmake_minimum_required(VERSION 3.0.2)
project(gazebo_panda)

find_package(catkin
  REQUIRED COMPONENTS
    gazebo_ros
    gazebo_ros_control
    realtime_tools
    roscpp
    roslint
    std_msgs
    tf_conversions
)

# Depend on system install of Gazebo
find_package(GAZEBO REQUIRED)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${GAZEBO_CXX_FLAGS}")
find_package(Eigen3 REQUIRED)

catkin_package(
 CATKIN_DEPENDS
  gazebo_ros_control
  realtime_tools
  roscpp
  tf_conversions
)

roslint_cpp()
link_directories(
  ${GAZEBO_LIBRARY_DIRS}
  ${catkin_LIBRARY_DIRS}
)

include_directories(include
  ${catkin_INCLUDE_DIRS}
  ${GAZEBO_INCLUDE_DIRS}
)


install(
  DIRECTORY config launch worlds share
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
