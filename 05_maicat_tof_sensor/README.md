# Maicat Tutorial
## [Ubuntu only] Time of Flight (ToF) Sensor:

Maicat implements SLAM using the two ToF sensors on its forehead to identify obstacles and draw a two-dimensional map.
First, on a PC were ROS is installed, install the Maicat Package for PC.

```python
# run the following command
git clone https://github.com/macroact/maicat_pc.git
cd maicat_pc
source install/setup.bash
```

&nbsp;

Afterwards, you can check the IMU sensor in the next chapter together with the command below.

```python
ros2 topic pub serial number(UUID)/control_teensy std_msgs/Int64 "data: 51"
ros2 launch maibot_navigation2 slam.launch.py 
```

&nbsp;

![maicat_ros2_tof](https://github.com/user-attachments/assets/be6020f4-3b16-4b80-ba11-fe5dc4d2cc0c)


[Next - Maicat IMU sensor](../06_maicat_imu_sensor/README.md)
