cmake_minimum_required(VERSION 3.0.2)
project(enshu_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

# Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  sensor_msgs
  std_msgs
  message_generation
)

# Generate messages in the 'msg' folder
add_message_files(
  FILES
  HandResult.msg
  Bbox.msg
  BboxArray.msg
)

# Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  sensor_msgs geometry_msgs
)
###################################
## catkin specific configuration ##
###################################
catkin_package(
CATKIN_DEPENDS message_runtime
)
