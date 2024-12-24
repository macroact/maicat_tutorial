# 마이캣(Maicat) 튜토리얼
## 카메라 기능:

### [블록 코딩의 경우]
사진 찍기 블록을 이용하여 마이캣의 코에 장착된 카메라 기능을 확인할 수 있어요.

- '시작'
블록 코딩에서 실행할 명령들은 '시작' 블록 안에 넣어야 합니다.
마우스로 '시작' 블록을 실행 화면 안으로 끌어 놓아 주세요.

<img src="https://github.com/user-attachments/assets/581c8a8c-5931-48cb-8aab-a00b9e5ccc08" alt="bc-start" width="250">

- '카메라 촬영'
카메라 촬영을 끝어다 '시작' 블록 안으로 옮겨 주세요.

<img src="https://github.com/user-attachments/assets/baf7216c-7d62-43f1-b98a-05dc95e83783" alt="camera" width="250" />

- 휴지통

더 이상 사용하지 않는 블록은 마우스로 끌어 휴지통 아이콘 위에 놓아 주세요.

![trash](https://github.com/user-attachments/assets/796d9e0e-b132-4d5f-b425-740ae434a23a)    

- 중심, 확대, 축소

화면 중심 위치 또는 확대와 축소를 위해 사용됩니다.

![zoom](https://github.com/user-attachments/assets/0fffbb61-505e-47f5-8591-8a29ce5e59d5)

&nbsp;
### [우분투의 경우]
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
