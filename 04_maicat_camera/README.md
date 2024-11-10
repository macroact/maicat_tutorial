# Maicat Tutorial
# Maicat Camera
Maicat system features an advanced functionality with its Maicat camera, designed for streaming video, conducting facial recognition, and monitoring the home. This versatile camera can be used not only for home security but also to confirm when your children return from school. Below, I will provide a detailed explanation of how to operate the ROS topics to manage both streaming and image capture using the Maicat camera.


First run this on your PC

```python
ros2 topic pub /enable_camera std_msgs/Bool "data: True"
```

Then on the same PC terminal run the following command:
```python
rqt
```
In your rqt graph, you will find "Plugins" located in the top left corner. Under "Plugins," navigate to "Visualization" and select "Image View." This will allow you to see live images streamed from the Maicat cam.

Plugins -> Visualization -> Image View

[camera.webm](https://github.com/macroact/maicat_tutorial/assets/106013071/eb620e88-22f9-40d6-8518-54440af4eda2)


[Next - Maicat TOF sensor](../05_maicat_tof_sensor/README.md)
