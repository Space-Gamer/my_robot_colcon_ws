cmake_minimum_required(VERSION 3.8)
project(castor_wheel_robot_description)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)

ament_package()

install (DIRECTORY
  urdf rviz worlds
  DESTINATION share/${PROJECT_NAME}/
)