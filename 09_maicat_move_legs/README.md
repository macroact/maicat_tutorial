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


![control_maicat](https://github.com/user-attachments/assets/29e33904-531a-4251-b68f-c6791a70238c)


[Next - Macat gazebo](../10_maicat_gazebo/README.md)
