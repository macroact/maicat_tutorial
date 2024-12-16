# 마이캣(Maicat) 튜토리얼
## [우분투에만 해당] 키보드를 이용한 다리 제어:

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

9개의 키 세트를 사용하여 각각 다른 방향과 동작에 해당하는 마이캣의 움직임을 지시할 수 있고,<br/>
Shift키와 함께 누르면 다른 형태의 움직임도 가능해요:

```python
Reading from the keyboard  and Publishing to Twist!
---------------------------
Moving around:
u    i    o
j    k    l
m    ,    .
For Holonomic mode (strafing), hold down the shift key:
---------------------------
U    I    O
J    K    L
M    <    >
t : up (+z)
b : down (-z)
anything else : stop
q/z : increase/decrease max speed by 10%
w/x : increase/decrease only linear speed by 10%
e/c : increase/decrease only angular speed by 10%
CTRL-C to quit
```

&nbsp;

![control_maicat](https://github.com/user-attachments/assets/29e33904-531a-4251-b68f-c6791a70238c)


[Next - Macat gazebo](../10_maicat_gazebo/README.md)
