cmake_minimum_required(VERSION 3.5.1)
project(lanelet2)
if($ENV{ROS_VERSION} EQUAL 1)
  find_package(catkin REQUIRED)
  install(FILES package.xml DESTINATION share/lanelet2)
elseif($ENV{ROS_VERSION} EQUAL 2)
  if(POLICY CMP0057)
    cmake_policy(SET CMP0057 NEW)
  endif()
  find_package(ament_cmake_core REQUIRED)
  ament_package()
endif()
