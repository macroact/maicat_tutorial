# Maicat Tutorial
## Camera Features

### [For Block-Coding]
You can check out the robot's nose camera and explore the camera feature using the "Take photo"-block.

<img src="https://github.com/user-attachments/assets/baf7216c-7d62-43f1-b98a-05dc95e83783" alt="camera" width="250"/>

You can see the photos.

![photos_Button](https://github.com/user-attachments/assets/f29436cd-e772-47df-946e-a075c3f59ca2)
![photos](https://github.com/user-attachments/assets/5573fae4-1c13-44ba-b013-0504eef3b615)

&nbsp;
### [For Ubuntu]
First, on a PC were ROS is installed, use the below command to turn on robot Maicat's camera. 

```python
ros2 topic pub serial number(UUID)/enable_camera std_msgs/Bool "data: True"
```

After that run 'rqt'.
```python
rqt
```
When the rqt UI screen appears, click “Plugins” --> “Visualization” --> “Image View” from the menu on the top left. 
Then, select the corresponding UUID/camera topic from the drop-down box to see the video that Maicat is broadcasting.

[camera.webm](https://github.com/macroact/maicat_tutorial/assets/106013071/eb620e88-22f9-40d6-8518-54440af4eda2)


[Next - Maicat TOF sensor](../05_maicat_tof_sensor/README.md)
