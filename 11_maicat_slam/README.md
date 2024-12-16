# 마이캣(Maicat) 튜토리얼
## [우분투에만 해당] SLAM:

SLAM 기능에는 많은 리소스를 사용해야 하기 때문에 기존 서비스를 중단하고 필요한 노드만 실행시킵니다.<br/>

&nbsp;

(마이캣 터미널)
```python
sudo systemctl stop maibot_interaction.service
sudo systemctl stop maibot_gpt.service
sudo systemctl stop maibot_bringup.service
sudo systemctl stop maibot.service
sudo systemctl stop maibot_boot.service

ros2 launch maibot_bringup maibot_slam.launch.py
```

(PC 터미널)
```python
# Install xterm
sudo apt install xterm

ros2 launch maibot_teleop teleop.launch.py
```

![maicat_slam-ezgif com-optimize](https://github.com/macroact/maicat_tutorial/assets/106013071/b0f72f1d-6f1e-4fde-9cc5-4e08a17ec69e)
