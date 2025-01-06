# Maicat Tutorial
## [Only for Ubuntu] SLAM:

Because SLAM features require a lot of resources, stop existing services and run only the required nodes.<br/>

&nbsp;

(Maicat Terminal)
```python
sudo systemctl stop maibot_interaction.service
sudo systemctl stop maibot_gpt.service
sudo systemctl stop maibot_bringup.service
sudo systemctl stop maibot.service
sudo systemctl stop maibot_boot.service

ros2 launch maibot_bringup maibot_slam.launch.py
```

(PC Terminal)
```python
# Install xterm
sudo apt install xterm

ros2 launch maibot_teleop teleop.launch.py
```

![maicat_slam-ezgif com-optimize](https://github.com/macroact/maicat_tutorial/assets/106013071/b0f72f1d-6f1e-4fde-9cc5-4e08a17ec69e)
