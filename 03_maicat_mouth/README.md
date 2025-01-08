# Maicat Tutorial
## Mouth and Sound

### [For Block-Coding]
While moving Maicat's mouth you can let the robot make catlike sounds.

<img  src="https://github.com/user-attachments/assets/da9e06ec-7727-4ab3-bcc1-616437921401"  alt="meow" width="250" />

While Maicat's mouth is moving the robot can speak like a human. 

<img src="https://github.com/user-attachments/assets/fce6eb5d-373a-4a6a-84b2-a7046c16fc58" alt="bc-talk" width="250">

You can command the desired speech by writing words in the blank space.

<img src="https://github.com/user-attachments/assets/3e92ea58-3786-48ef-ab69-e4ded9fcda05" alt="bc-custom-talk" width="250">

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
