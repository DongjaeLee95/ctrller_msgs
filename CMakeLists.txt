cmake_minimum_required(VERSION 3.0.2)
project(ctrller_msgs)

add_compile_options(-std=c++17)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  geometry_msgs
  message_generation
)

set(CMAKE_BUILD_TYPE "Release")

add_message_files(
  FILES
  PoseTarget.msg
  ThrustTorque.msg
  Pwm.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)
