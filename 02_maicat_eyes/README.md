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

ROS2가 설치된 PC에서 다음과 같이 명령어를 입력하여 원하는 색상과 모양으로 바꿔보세요.

```python
ros2 topic pub --once teensy/command std_msgs/Int32 "data: number of the shape of eye you need"
# You will see the change of eyes color and eye style
```

영상

![Maicat_eyes_expressions_emotion-ezgif com-optimize](https://github.com/macroact/maicat_tutorial/assets/106013071/98a80e0c-b105-490c-bc51-b6e511328f80)


[Next - 입](../03_maicat_mouth/README.md)
