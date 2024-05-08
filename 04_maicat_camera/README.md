# Maicat Tutorial

Maicat robotic system features an advanced functionality with its Maicat camera, designed for streaming video, conducting facial recognition, and monitoring the home. This versatile camera can be used not only for home security but also to confirm when your children return from school. Below, I will provide a detailed explanation of how to operate the ROS topics to manage both streaming and image capture using the Maicat camera.

```python
ros2 run maibot_cam cam
```
First run this on your PC
```python
ros2 topic pub /encode_cam std_msgs/Bool "data: 1"
# kill the above command by Ctrl + Z
```
Then on the same PC terminal run the following command:
```python
rqt
```
# Images 
**Here

In your rqt graph, you will find "Plugins" located in the top left corner. Under "Plugins," navigate to "Visualization" and select "Image View." This will allow you to see live images streamed from the Maicat cam.

Plugins -> Visualization -> Image View


[Next - Maicat TOF sensor](../05_maicat_tof_sensor/README.md)
