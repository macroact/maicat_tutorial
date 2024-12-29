# 마이캣(Maicat) 튜토리얼
&nbsp;
## '블록 코딩' 또는 '우분투 & ROS2 Humble' 설치
### [블록 코딩]
마이캣의 기본 기능을 이용할 수 있는 초급 과정의 교육을 위해서는 블록 코딩을 추천합니다.
- 블록 코딩 파일은 다음 링크에서 다운로드 할 수 있습니다.
[maicat_block_coding_1.0.1.zip](https://github.com/user-attachments/files/18271225/maicat_block_coding_1.0.1.zip)
- 다운로드 후 압축을 풀고 maicat_block_coding.html 파일을 더블클릭으로 실행하시면 아래와 같은 화면이 브라우저에 나타납니다.
![main-screen](https://github.com/user-attachments/assets/c21183c9-7d20-431b-9aa2-0ff54d490e7f) 

&nbsp;

### [우분투 & ROS2 Humble]
마이캣의 모든 기능을 이용하는 중·고급 과정의 교육을 위해서는 ROS2 Humble 설치를 추천합니다.
ROS2 Humble은 우분투 22.04 LTS(Long-Term Support)에 최적화된 버전입니다.
- 우분투 22.04 LTS (jammy) : 다음 링크에서 다운로드 할 수 있습니다.
https://ubuntu.com/download/desktop
- ROS2 Humble : 다음 링크를 참고하여 설치하세요.
https://docs.ros.org/en/humble/Installation/Alternatives/Ubuntu-Development-Setup.html

&nbsp;
## 마이캣 구성품
### 레디백
택배 박스 안에는 레디백이 들어 있으며, 그 내부에는 마이캣과 충전기, 어댑터, 러그가 각각 하나씩 있습니다.
![in_maicat_bag](https://github.com/user-attachments/assets/ecccaf49-2994-416b-9394-810ca51fa20b)

### 충전 스테이션 조립
충전기와 러그에 있는 방향을 표시하는 작은 홈과 충전기 바닥의 돌출부에 유의하며 결합하고 홈이 있는 방향으로 밀어주세요.<br/>
어댑터의 잭은 러그의 가장자리에 있는 커넥터와 연결한 후 어댑터를 콘센트에 꽂아주세요.
![charging_station](https://github.com/user-attachments/assets/b20f14d6-837d-4c93-80bb-4ab96bbdf800)


&nbsp;
## 마이캣 전원 켜기
로봇을 사용하기 위해서는 아래 그림과 같이 먼저 배 부분에 있는 배터리 씰을 제거해야 합니다.
그리고, 꼬리 부분에 있는 전원 버튼을 눌러 전원을 켜세요.<br/>
마이캣은 충전스테이션 위에 그림과 같이 올려주세요. 전원이 켜지면 눈을 감고 있는 모양이 나타납니다. 
![maicat_power_charging](https://github.com/user-attachments/assets/f432e77c-0b34-4336-a05b-30fc5b49e9fc)

&nbsp;
## 순서
0. [음성 명령](00_maicat_voice_commands/README.md)
1. [네트워크 설정 및 IP주소 확인](01_maicat_network/README.md)
2. [눈 디스플레이](02_maicat_eyes/README.md)
3. [입](03_maicat_mouth/README.md)
4. [카메라](04_maicat_camera/README.md)
5. [ToF 센서](05_maicat_tof_sensor/README.md)
6. [IMU 센서](06_maicat_imu_sensor/README.md)
7. [터치 센서](07_maicat_touch_sensor/README.md)
8. [머리와 꼬리](08_maicat_move_head_and_tail/README.md)
9. [다리](09_maicat_move_legs/README.md)
10. [가제보](10_maicat_gazebo/README.md)
11. [SLAM](11_maicat_slam/README.md)
