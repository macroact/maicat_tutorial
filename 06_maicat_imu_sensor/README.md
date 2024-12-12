# 마이캣(Maicat) 튜토리얼
## [우분투에만 해당] Inertial Measurement Unit 센서:

마이캣의 몸통 중앙에는 관성 측정 장치인 IMU 센서가 탑재되어 있어요.<br/>
가속도 센서(Acceleration Sensor), 각속도 센서(Gyroscope, 자이로스코프), 지자기 센서(Magnetometer)로 구성된 9축 센서입니다.<br/>
이 센서로 마이캣은 Roll, Pitch, Yaw를 계산하여 균형을 잡기도 하고 ToF센서의 측정값과 결합하여 2차원 지도를 그릴 수 있어요.

&nbsp;

ROS가 설치된 PC에서 아래 명령을 실행한 후 마이캣을 손에 들고 방향과 기울기에 변화를 주면 PC 화면에서 확인할 수 있어요.

```python
ros2 launch maibot_navigation2 slam.launch.py
```

&nbsp;

![maicat_ros2_imu](https://github.com/user-attachments/assets/a4ab2090-8313-4192-bf75-c81e0429492b)


[Next - 터치 센서](../07_maicat_touch_sensor/README.md)
