cmake_minimum_required(VERSION 2.4.6)
include($ENV{ROS_ROOT}/core/rosbuild/rosbuild.cmake)

#project(beginner_tutorial)
#find_package(catkin REQUIRED COMPONENTS roscpp tf std_msgs geometry_msgs nav_msgs sensor_msgs cmake_modules)
# Set the build type.  Options are:
#  Coverage       : w/ debug symbols, w/o optimization, w/ code-coverage
#  Debug          : w/ debug symbols, w/o optimization
#  Release        : w/o debug symbols, w/ optimization
#  RelWithDebInfo : w/ debug symbols, w/ optimization
#  MinSizeRel     : w/o debug symbols, w/ optimization, stripped binaries
#set(ROS_BUILD_TYPE RelWithDebInfo)


rosbuild_init()

#set the default path for built executables to the "bin" directory
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#set the default path for built libraries to the "lib" directory
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

#uncomment if you have defined messages
#rosbuild_genmsg()
#uncomment if you have defined services
#rosbuild_gensrv()

#common commands for building c++ executables and libraries

rosbuild_add_executable(Hello_world_executable src/ros_hello_world.cpp )
rosbuild_add_executable(Hello_world_executable_test src/ros_hello_world.cpp)
rosbuild_add_executable(publisher_talker src/publisher_talker.cpp)
rosbuild_add_executable(subscriber_node src/subscriber_node.cpp)

#rosbuild_add_library(${PROJECT_NAME} src/example.cpp)
#target_link_libraries(${PROJECT_NAME} another_library)
#rosbuild_add_boost_directories()
#rosbuild_link_boost(${PROJECT_NAME} thread)
#rosbuild_add_executable(example examples/example.cpp)
#target_link_libraries(example ${PROJECT_NAME})





####Link about CMakeLists.txt
#http://wiki.ros.org/rosbuild/CMakeLists
#http://wiki.ros.org/ROS/Tutorials/Creating%20a%20Package%20by%20Hand       //creating a package by hand
#
