# Maicat Tutorial
# Maicat Gazebo

```python
ros2 launch maibot_gazebo maibot_gazebo.launch.py 
```
# Run gmapping package and move_base: (Still need to fix sth, will make it work in next PR)
```python
ros2 launch maibot_navigation2 slam.launch.py
```
To start mapping:

- Click '2D Nav Goal'.
- Click and drag at the position you want the robot to go.


- Save the map by running:

      cd <your_ws>/maicat_pc/src/maibot_navigation2/map
      ros2 run nav2_map_server map_saver_cli -f new_map

# Autonomous Navigation:

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

   <img src="src/docs/images/maicat_nav2.gif" width="640"/>

# Physical robot maicat:
- Use the maicat app to allow the robot to connect to Wi-Fi. 

# Run the maicat: 
	(PC-terminal) ros2 topic pub joint_group_position_controller/command std_msgs/Float64MultiArray "data: [0.0]"
		      # Publish about 10 times and then cancel. (ctrl + c)
		      ros2 launch maibot_teleop teleop.launch.py

[Next - Maicat slam](../11_maicat_slam/README.md)
