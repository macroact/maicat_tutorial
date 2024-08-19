# Maicat Tutorial
# Maicat Touch Sensor

Maicat is equipped with three touch sensors and located at:
Head: Top of the head
Back Head: Rear part of the head
Back: Middle section of the back

When any of these sensors are touched, the robot responds with various expressions and a "meow" sound to engage with the user in a friendly way.

# Head Sensor
When you gently touch the sensor at the top of the head, the robot will respond with a joyful expression and a playful "meow" sound, creating a delightful interaction.
# Back Head Sensor
Touching the sensor at the back of the head triggers a different expression and a happy "meow" to acknowledge your touch.
# Back Sensor
When you touch the sensor located in the middle of the back, the robot will react with yet another unique expression and sound, designed to bring you closer to it emotionally.

# SSH Command
To gain access to Maicat and work with the nodes, you need to send your GitHub account details along with the Maicat UUID to support@macroact.com. The support team will verify your credentials and ensure that your request is processed promptly. Once your information is validated, you will receive an email confirming that full access has been granted. After receiving this confirmation, you'll be able to access all features of Maicat and work with the nodes as needed.

To acces Maicat on your Computer you can use the SSH command. SSH will allow you to securely connect to another machine over a network. Open your terminal and type the bellow ssh command.
After you run the command, you'll be prompted to enter the password associated with maicat user. 
```python
#input the SSH command then enter the password
ssh maicat@maibot.local
```
```python
cd /maicat_automatic
source install/setup.bash
ros2 run maibot_interaction touch_node
```
You can significantly enhance your interactive maicat project by integrating a touch node, a Teensy node, and a sound node. 
This setup allows for a dynamic interaction where the cat's eye color changes and sounds are produced based on touch input.

```python
ros2 run maibot_interaction touch_node
```

```python
# Run this on your local computer.
ros2 topic pub teensy/command std_msgs/Int32 "data: 30/33"
```
```python
# Maicat eye features and eye color depend on the type of touch input.

3: Normal
4: Happy
5: Surprise
6: Angry
7: Sad
8: Sleepy
9: Sleep

```

[Next - Maicat moving head and tail](../08_maicat_move_head_and_tail/README.md)
