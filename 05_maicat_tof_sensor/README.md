# 마이캣(Maicat) 튜토리얼
## [우분투에만 해당] Time of Flight 센서:

마이캣은 이마에 탑재된 2개의 ToF 센서를 이용하여 장애물을 파악하고 2차원 지도를 그리는 SLAM을 구현합니다.<br/>
우선은 ROS가 설치된 PC에 마이캣 PC용 패키지를 설치하세요.

```python
# run the following command
git clone https://github.com/macroact/maicat_pc.git
cd maicat_pc
source install/setup.bash
```

&nbsp;

이후에 아래 명령으로 다음 장의 IMU센서를 함께 확인할 수 있어요.

```python
ros2 topic pub 시리얼넘버(UUID)/control_teensy std_msgs/Int64 "data: 51"
ros2 launch maibot_navigation2 slam.launch.py 
```

&nbsp;

![maicat_ros2_tof](https://github.com/user-attachments/assets/be6020f4-3b16-4b80-ba11-fe5dc4d2cc0c)


[Next - IMU 센서](../06_maicat_imu_sensor/README.md)
