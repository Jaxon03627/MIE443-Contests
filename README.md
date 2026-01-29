# MIE443-Contests


// real test commend

//Status Check
ros2 topic echo /battery_state 


ros2 action send_goal /dock irobot_create_msgs/action/Dock "{}"


ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -p stamped:=True
