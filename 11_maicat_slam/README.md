# 마이캣(Maicat) 튜토리얼
## [우분투에만 해당] SLAM:

우선, 현재 사용하는 우분투의 버전에 맞는 가제보를 설치해야 합니다.<br/>
https://gazebosim.org/docs/harmonic/install_ubuntu/ (우분투 Jammy(22.04)의 경우)

[TOF 센서](../05_maicat_tof_sensor/README.md) 장에서 설명한 바와 같이 PC용 패키지도 설치해야 합니다.<br/>

&nbsp;

이후에 동일한 PC에서 마이캣 가제보를 실행시키고 동작을 확인할 수 있어요.<br/>
다만, 2개의 launch 파일을 실행시키지 위해 2개의 터미널 창을 열어야 하며<br/>
각각의 창에서 PC용 패키지의 환경이 구성되어 있어야만 합니다.

```python
cd maicat_pc (pc용 패키지 설치 폴더)
source install/setup.bash
```

&nbsp;


# Maicat Tutorial

# Maicat Slam
First of all you need to stop maicat services for high speed executing the Joint position group of maicat.
Then you need to run the launch file on maicat terminal


```python
(maicat via ssh)
sudo systemctl stop maibot_bringup.service
ros2 launch maibot_bringup maibot_slam.launch.py

(PC-terminal)
# Install xterm
sudo apt install xterm

ros2 service call /enable_servo std_srvs/srv/SetBool "{data: True}"
ros2 launch maibot_teleop teleop.launch.py
```

![maicat_slam-ezgif com-optimize](https://github.com/macroact/maicat_tutorial/assets/106013071/b0f72f1d-6f1e-4fde-9cc5-4e08a17ec69e)
