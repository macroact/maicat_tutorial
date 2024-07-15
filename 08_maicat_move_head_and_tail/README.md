# Maicat Tutorial
# Maicat_move_head_and_tail
At this point we are going to learn how to move Maicat head and tail at the same time. We’ll use a Ros topic to send position commands to the joints.

To move the robot's head and tail simultaneously, we need to publish a message with specific position values for each joint. The command format uses a ROS topic with the following message structure: But first run this command…

Run the server node
```python
# No need of running this command
ros2 run maibot_bringup servo_node
``` 
Then on your local computer run the following movement of the maicat head and tail



```python
ros2 topic pub joint_group_position_controller/command std_msgs/Float64MultiArray "data: [-0.57, -0.3, -0.3, 0, -0.7]"

# kill the above command by Ctrl + C
```

# Explanation of the data
```python
‘-0.57’ :- Chest
‘-0.3’  :- Head Tilting(Up/Down)
‘-0.3’  :- Head Vertical(Rotation)
‘0’     :- Tail
‘-0.7’  :- Head Horizontal (Left/Right)
```
You can change the values in the array to set the robot's joints to different positions.

# Video


https://github.com/macroact/maicat_tutorial/assets/106013071/044cb235-4306-4485-8428-a8b5256daf87


[Next - Maicat moving of legs](../09_maicat_move_legs/README.md)
