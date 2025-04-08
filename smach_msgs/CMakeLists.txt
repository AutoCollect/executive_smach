cmake_minimum_required(VERSION 3.10)

# Suppress developer warnings (equivalent to using -Wno-dev on the command line)
set(CMAKE_SUPPRESS_DEVELOPER_WARNINGS 1 CACHE INTERNAL "Suppress developer warnings")

project(smach_msgs)

find_package(catkin REQUIRED COMPONENTS 
  message_generation std_msgs)

add_message_files(FILES
  SmachContainerInitialStatusCmd.msg
  SmachContainerStructure.msg
  SmachContainerStatus.msg)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime)
