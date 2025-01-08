# Maicat Tutorial
## Moving Head_and Tail

The actuators that move the Maicat's head and its tail are distributed four actuators in the breast and head area, and one in the tail module.<br/>
They are defined in the below order and with the angles being in radians.<br/>
Please check each limit angle as well.

Name of head and tail area and limiting angle (radian)
- Chest (Up/Down) : Moves the entire head and neck part up and down [-1.9, 0.0]
- Head Vertical (Up/Down) : Only moves the head up and down [-0.4, 0.0]
- Head Tilting (Left/Right) : Tilts the head lef and right [-0.5, 0.5]
- Tail (Up/Down) : Moves the tail up and down [0.0, 1.8]
- Head Horizontal (Left/Right) : Rotates the head in a left and right motion [-0.78, 0.78]

&nbsp;

### [For Block-Coding]
You can move Maicat's head and tail simultaneously.

<img src="https://github.com/user-attachments/assets/dbcb1947-ab34-4d92-80c3-96839cf7fd04" alt="motion" width="250" />

&nbsp;

### [For Ubuntu]
On a PC with ROS installed, you can move the head and tail at the same time with the following command. <br/>
Specify the five radian values ​​in the order above and pay attention to the angle limit.<br/>

```python
ros2 topic pub serial number(UUID)/joint_group_position_controller/command std_msgs/Float64MultiArray "data: [-0.57, -0.1, -0.3, 0.6, 0.3]"
```

&nbsp;

https://github.com/macroact/maicat_tutorial/assets/106013071/044cb235-4306-4485-8428-a8b5256daf87


[Next - Maicat moving of legs](../09_maicat_move_legs/README.md)
