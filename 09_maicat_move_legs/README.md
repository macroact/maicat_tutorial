# Maicat Tutorial
# Maicat Move Leg and Controlling Maicat using your PC keyboard

Activate the motors
```python
ros2 service call /enable_servo std_srvs/srv/SetBool "{data: True}"
```

```python
ros2 launch maibot_teleop teleop.launch.py
```

Controlling Maicat using a PC is straightforward, much like driving a car. We utilize a set of 9 keys to direct Maicat's movements, each corresponding to different directions and actions:
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


![Screenshot from 2024-07-01 16-37-29](https://github.com/macroact/maicat_tutorial/assets/106013071/12048b6b-728a-411d-a6e2-937510daf6e4)


[Next - Macat gazebo](../10_maicat_gazebo/README.md)
