# 마이캣(Maicat) 튜토리얼
## [우분투에만 해당] 가제보를 이용한 시뮬레이션:

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

(PC 터미널 1)
```python
ros2 launch maibot_gazebo maibot_gazebo.launch.py
```

(PC 터미널 2)
```python
ros2 launch maibot_navigation2 navigation.launch.py
```

&nbsp;

내비게이션 실행:
- 메뉴에서 '2D Nav Goal' 선택.
- 마이캣을 이동시킬 곳을 클릭하고 드래그로 방향까지 결정하면 마이캣이 움직이기 시작해요.
  
![maicat_nav2](https://github.com/macroact/maicat_tutorial/assets/106013071/90751657-4bc9-4f9e-9bb7-d88695391434)


[Next - SLAM](../11_maicat_slam/README.md)
