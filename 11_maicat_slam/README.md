# Maicat Tutorial

# Maicat Slam

```python
(maicat via ssh) sudo systemctl stop maibot_boot.service
	                 sudo systemctl stop maibot.service
	                 sudo systemctl stop maibot_bringup.service
	                 ros2 launch maibot_bringup maibot_slam.launch.py

	(PC-terminal) ros2 topic pub joint_group_position_controller/command std_msgs/Float64MultiArray "data: [0.0]"
		      # Publish about 10 times and then cancel. (ctrl + c)
		      ros2 launch maibot_teleop teleop.launch.py
   <img src="src/docs/images/maicat_slam.gif" width="640"/>
```

![maicat_slam-ezgif com-optimize](https://github.com/macroact/maicat_tutorial/assets/106013071/b0f72f1d-6f1e-4fde-9cc5-4e08a17ec69e)
