# MIE443-Contests

//Reboot Everything
sudo reboot
//Kill Everything
killall -9 gzserver gzclient gazebo

// Simulation
//Start Everything at the Same time
ros2 launch turtlebot4_gz_bringup turtlebot4_gz.launch.py model:=lite rviz:=true SLAM:= true

// real test commend

//Status Check
ros2 topic list //if unsure about the topic

ros2 topic echo /battery_state 
ros2 run teleop_twist_keyboard teleop_twist_keyboard
ros2 topic echo /tf

//Launch Turtle Commend
ros2 launch turtle

// ROS2 Real World Execution Commend
ros2 action send_goal /dock irobot_create_msgs/action/Dock "{}"

ros2 action send_goal /undock irobot_create_msgs/action/Dock "{}"

ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -p stamped:=True
