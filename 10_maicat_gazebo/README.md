# Maicat Tutorial
# Maicat Gazebo
After making sure you have install ROS2 (sudo apt install ros-humble-desktop), also run this command:
```python
    sudo apt install ros-humble-gazebo* (don't forget the *)
```
This will install Gazebo and ROS2 Gazebo packages. 

NEW UPDATE: You may also need to source this file:
What you can do is just add this line at the end of your .bashrc (after the line to source ros2):
```python
    source /usr/share/gazebo/setup.bash
```

# Run the Gazebo environment: 
```python
    ros2 launch maibot_gazebo maibot_gazebo.launch.py
```

# Run nav2:
```python
    ros2 launch maibot_navigation2 navigation.launch.py
```
To navigate:
- Click '2D Nav Goal'.
- Click and drag at the position you want the robot to go.
  
![maicat_nav2](https://github.com/macroact/maicat_tutorial/assets/106013071/90751657-4bc9-4f9e-9bb7-d88695391434)


[Next - Maicat slam](../11_maicat_slam/README.md)
