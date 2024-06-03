# Maicat Tutorial
# Maicat Mouth
To control the movement of maicat in ROS2 (Robot Operating System 2), you'll need to set up and execute several commands in your ROS2 workspace. Below is a step-by-step guide to get you started, focusing on opening and closing the maicat's mouth using specific ROS2 commands.
Ensure that your ROS2 workspace is properly set up and sourced. This typically involves cloning the necessary repositories and building the workspace using colcon build. 

Before interacting with maicat, start the main ROS2 nodes using the ```python ros2 maibot.launch.py``` file. This launch file typically initializes all necessary hardware interfaces, drivers, and configurations.

# Run the launch file to bring up the robotic maicat
```python
ros2 launch maibot_bringup maibot.launch.py
```
To control the mouth of the robotic maicat, you will publish messages to a specific topic. In this case, the topic is teensy/command which takes std_msgs/Int32 type messages.

# Opening the Mouth 
You will send an integer value 30 to signify this action.
```python
ros2 topic pub teensy/command std_msgs/Int32 "data: 30"
```

# Closing the Mouth 
You will send an integer value 33 to signify this action.
```python
ros2 topic pub teensy/command std_msgs/Int32 "data: 33"
```
# Video 

[Next - Maicat camera](../04_maicat_camera/README.md)
