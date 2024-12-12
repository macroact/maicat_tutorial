# 마이캣(Maicat) 튜토리얼
## 카메라:

### 블록 코딩의 경우
사진 찍기 블록을 이용하여 마이캣의 코에 장착된 카메라 기능을 확인할 수 있어요.

&nbsp;
### 우분투의 경우
먼저 ROS가 설치된 PC에서 아래의 명령어로 마이캣의 카메라를 켜주세요.

```python
ros2 topic pub 시리얼넘버(UUID)/enable_camera std_msgs/Bool "data: True"
```

이후에 'rqt'를 실행시킵니다.
```python
rqt
```
rqt UI 화면이 나오면, 왼쪽 상단의 메뉴에서 "Plugins" --> "Visualization" --> "Image View"를 클릭합니다.
이후에 드롭다운 박스에서 해당하는 UUID/camera 토픽을 선택하면 마이캣이 송출하는 영상을 보실 수 있어요.

[camera.webm](https://github.com/macroact/maicat_tutorial/assets/106013071/eb620e88-22f9-40d6-8518-54440af4eda2)


[Next - TOF 센서](../05_maicat_tof_sensor/README.md)
