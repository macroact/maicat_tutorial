# Maicat Tutorial
## Mouth and Sound

### [For Block-Coding]
While moving Maicat's mouth you can let the robot make catlike sounds.

<img  src="https://github.com/user-attachments/assets/3a3ee120-0c68-4d54-b1f5-b5a0dedcbad2"  alt="meow" width="250" />

While Maicat's mouth is moving the robot can speak like a human. 

<img src="https://github.com/user-attachments/assets/cf0369c3-11df-4c48-aff9-f26cee65b67c" alt="bc-talk" width="250">

You can command the desired speech by writing words in the blank space.

<img src="https://github.com/user-attachments/assets/4a739ffc-0fce-4ee0-bbf8-ae09eab25e9b" alt="bc-custom-talk" width="250">

&nbsp;
### [For Ubuntu]
The commands to control Maicat's mouth are as follows

    21~29: Open and close your mouth at the speed of the last digit x 10ms
    30: Open the mouth quickly
    31: Open the mouth slowly
    32: Close the mouth slowly
    33: Close the mouth quickly

```python
ros2 topic pub serial number(UUID)/control_teensy std_msgs/Int64 "data: desired mouth control number"
```

&nbsp;

The commands to control the mouth while making sounds are shown below.

```python
ros2 topic pub serial number(UUID)/sound/meow std_msgs/Int64 "data: desired sound number"
```

&nbsp;

The TTS, that converts text into a human voice, can be found using the command below.

```python
ros2 topic pub serial number(UUID)/sound/speech std_msgs/String "data: sentence you want"
```


&nbsp;

https://github.com/macroact/maicat_tutorial/assets/106013071/7d608775-537f-4ec0-b6a8-b917261cce64



[Next - Maicat camera](../04_maicat_camera/README.md)
