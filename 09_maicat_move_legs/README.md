# Maicat Tutorial
## [Only for Ubuntu] Control the legs using the keyboard:

Each of Maicat's legs is equipped with three actuators.<br/>
Hence, it uses 12 actuators to stand up, sit down, rotate, and move.<br/>
<br/>
The Education Version (EV), which is the target of this tutorial, uses Python to control the actuators by default,<br/>
but for an even more precise control of the movement, it is recommended to control it with CPP.<br/>
Following the process below you can use CCP control instead of Python.

(Maicat Terminal)
```python
sudo systemctl stop maibot_bringup.service
ros2 launch maibot_bringup maibot.launch.py namespace:=serialnumber(UUID)
```

(PC Terminal)
```python
# Install xterm if needed
sudo apt install xterm

ros2 launch maibot_teleop teleop.launch.py namespace:=serialnumber(UUID)
```

&nbsp;

Nine sets of keys can be used to direct Maicat's movements, each corresponding to a different direction and behavior,<br/>
If you hold down the Shift key, you can also do other types of movement:

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

&nbsp;

[Next - Macat gazebo](../10_maicat_gazebo/README.md)
