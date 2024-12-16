# 마이캣(Maicat) 튜토리얼
## [우분투에만 해당] 가제보를 이용한 시뮬레이션:

우선, 현재 사용하는 우분투의 버전에 맞는 가제보를 설치해야 합니다.<br/>
https://gazebosim.org/docs/harmonic/install_ubuntu/ (우분투 Jammy(22.04)의 경우)

마이캣의 다리에는 각각 3개의 액추에이터가 탑재되어 있어요.<br/>
즉, 12개의 액추에이터를 이용하여 일어나거나 앉고, 회전과 이동을 하게 됩니다.<br/>
<br/>
이 튜토리얼의 대상이 되는 EV(Education Version)에는 기본적으로 파이썬으로 액추에이터를 제어하는데,<br/>
동작의 정밀한 제어를 위해서는 CPP로 제어하는 것을 추천합니다.<br/>
이를 위해서 아래와 같은 과정으로 파이썬 대신 CPP 제어를 할 수 있어요.

(마이캣 터미널)
```python
sudo systemctl stop maibot_bringup.service
ros2 launch maibot_bringup maibot.launch.py namespace:=시리얼넘버(UUID)
```

(PC 터미널)
```python
ros2 launch maibot_teleop teleop.launch.py namespace:=시리얼넘버(UUID)
```

&nbsp;


# Maicat Tutorial
# Maicat Gazebo

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
