cmake_minimum_required(VERSION 2.8.3)
project(project11_nav_msgs)

find_package(catkin REQUIRED 
  actionlib_msgs
  geometry_msgs
  message_generation
  nav_msgs
  project11_msgs
  roscpp
  std_msgs
)

add_action_files(DIRECTORY action FILES
 multibeam_coverage.action
)

add_message_files(
  FILES
  BoundingBox.msg
  Curve.msg
  CurvedTrajectory.msg
  GeoOccupancyPolygon.msg
  GeoOccupancyVectorMap.msg
  GeoPolygon.msg
  OccupancyPolygon.msg
  OccupancyVectorMap.msg
  RobotState.msg
  TaskFeedback.msg
  TaskInformation.msg
  TaskInformationList.msg
  Trajectory.msg
)

generate_messages(
  DEPENDENCIES
  actionlib_msgs
  geometry_msgs
  nav_msgs
  project11_msgs
  std_msgs
)

catkin_package(CATKIN_DEPENDS message_runtime geometry_msgs project11_msgs)
