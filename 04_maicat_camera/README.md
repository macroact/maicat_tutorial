# Maicat Tutorial
## Camera Features

### [For Block-Coding]
You can check out the robot's nose camera and explore the camera feature using the "Take photo"-block.

<img src="https://github.com/user-attachments/assets/de96fd5a-f3fe-4a75-910b-7f038e90719c" alt="camera" width="250"/>


You can see the photos.

![photos_Button](https://github.com/user-attachments/assets/050ac058-243c-4f5b-88a8-ce751a9b6147)
![photos](https://github.com/user-attachments/assets/c6c8c357-5f62-4554-8cb5-9f31f07719b8)

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
