# Maicat Tutorial

# Maicat_TOF_Sensor (Time of Flight)

Maicat uses ToF sensor data to detect obstacles and integrates this information into the robot's navigation algorithms. It also monitors specific distances to prevent collisions and measures distances for positioning. We combine the ToF sensor data with the IMU sensor to enhance the accuracy of mapping and navigation.

```python
# run the following command
git clone https://github.com/macroact/maicat_pc.git
cd maicat_pc
source install/setup.bash
```

```python
ros2 topic pub /control_teensy std_msgs/Int64 "data: 51"
ros2 launch maibot_navigation2 slam.launch.py 
```

![maicat_ros2_tof](https://github.com/user-attachments/assets/be6020f4-3b16-4b80-ba11-fe5dc4d2cc0c)


[Next - Maicat IMU sensor](../06_maicat_imu_sensor/README.md)
