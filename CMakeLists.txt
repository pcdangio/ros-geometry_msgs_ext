cmake_minimum_required(VERSION 3.0.2)
project(geometry_msgs_ext)

# Find catkin and package dependenies.
find_package(catkin REQUIRED COMPONENTS
  message_generation)

# Add messages.
add_message_files(
  FILES
  angle.msg
  point.msg
  pose.msg
  quaternion.msg
  transform.msg
  vector.msg)

# Add services.
add_service_files(
  FILES
  get_transform.srv)

# Generate messages.
generate_messages()

# Create catkin package.
catkin_package(CATKIN_DEPENDS message_runtime)