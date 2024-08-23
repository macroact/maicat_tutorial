# Maicat Tutorial

# Maicat Slam
First of all you need to stop maicat services for high speed executing the Joint position group of maicat.
Then you need to run the launch file on maicat terminal


```python
(maicat via ssh)
sudo systemctl stop maibot_bringup.service
ros2 launch maibot_bringup maibot_slam.launch.py

(PC-terminal)
# Install xterm
sudo apt install xterm

ros2 service call /enable_servo std_srvs/srv/SetBool "{data: True}"
ros2 launch maibot_teleop teleop.launch.py
```

![maicat_slam-ezgif com-optimize](https://github.com/macroact/maicat_tutorial/assets/106013071/b0f72f1d-6f1e-4fde-9cc5-4e08a17ec69e)
