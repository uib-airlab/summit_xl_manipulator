cmake_minimum_required(VERSION 2.8.3)
project(summit_xl_description)

find_package(catkin REQUIRED COMPONENTS roslaunch urdf xacro)

catkin_package(
  CATKIN_DEPENDS urdf xacro
)

include_directories(${catkin_INCLUDE_DIRS})

install(
  DIRECTORY launch meshes urdf robots vrep
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
