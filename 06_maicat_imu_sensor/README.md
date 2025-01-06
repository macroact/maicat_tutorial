# Maicat Tutorial
## [Only for Ubuntu] Inertial Measurement Unit (IMU) Sensor:

Maicat's body is equipped with an IMU sensor, an inertial measurement unit.<br/>
It is a 9-axis sensor consisting of an acceleration sensor, an angular velocity sensor (gyroscope), and a magnetometer.<br/>
With this sensor, Maicat can calculate Roll, Pitch, and Yaw to maintain balance, and can draw a 2D map by combining it with the measurement values ​​of the ToF sensor.

&nbsp;

After executing the command below on the ROS installed PC, you can explore it on the PC screen by holding the Maicat robot in your hand and changing the direction and tilt.

```python
ros2 launch maibot_navigation2 slam.launch.py
```

&nbsp;

![maicat_ros2_imu](https://github.com/user-attachments/assets/a4ab2090-8313-4192-bf75-c81e0429492b)


[Next - Maicat touch sensor](../07_maicat_touch_sensor/README.md)
