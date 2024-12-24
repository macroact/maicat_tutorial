# 마이캣(Maicat) 튜토리얼
## 디스플레이에 표시되는 마이캣의 눈을 바꿔보세요

마이캣의 눈 색상 또는 모양을 바꿀 수 있어요.
디스플레이 변경 번호는 0~9입니다.
색상 번호는 아래와 같아요.

    0: 노랑
    1: 파랑
    2: 분홍

그리고, 모양 번호는 아래와 같아요.

    3: 일반적인
    4: 행복한
    5: 놀란
    6: 화난
    7: 슬픈
    8: 졸린
    9: 잠든

&nbsp;
### [블록 코딩의 경우]
- '시작'
블록 코딩에서 실행할 명령들은 '시작' 블록 안에 넣어야 합니다.
마우스로 '시작' 블록을 실행 화면 안으로 끌어 놓아 주세요.

<img src="https://github.com/user-attachments/assets/581c8a8c-5931-48cb-8aab-a00b9e5ccc08" alt="bc-start" width="250">

- '눈 스타일'
이제 원하시는 눈 타입을 끌어다 '시작' 블록 안으로 옮겨 주세요.

<img src="https://github.com/user-attachments/assets/58eebacb-d5cf-4e49-9476-4f2ec5be5fa7" alt="bc_eye" width="250"/>

- 휴지통

더 이상 사용하지 않는 블록은 마우스로 끌어 휴지통 아이콘 위에 놓아 주세요.

![trash](https://github.com/user-attachments/assets/796d9e0e-b132-4d5f-b425-740ae434a23a)    

- 중심, 확대, 축소

화면 중심 위치 또는 확대와 축소를 위해 사용됩니다.

![zoom](https://github.com/user-attachments/assets/0fffbb61-505e-47f5-8591-8a29ce5e59d5)

&nbsp;
### [우분투의 경우]
ROS2가 설치된 PC에서 다음과 같이 명령어를 입력하여 원하는 색상과 모양으로 바꿔보세요.

```python
ros2 topic pub 시리얼넘버(UUID)/control_teensy std_msgs/Int64 "data: 변경하고 싶은 눈 번호"
```


&nbsp;
<br/>
![Maicat_eyes_expressions_emotion-ezgif com-optimize](https://github.com/macroact/maicat_tutorial/assets/106013071/98a80e0c-b105-490c-bc51-b6e511328f80)

&nbsp;
[Next - 입](../03_maicat_mouth/README.md)
