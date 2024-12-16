# 마이캣(Maicat) 튜토리얼
## 머리와 꼬리 움직이기:

머리와 꼬리를 움직이는 액추에이터는 마이캣의 가슴 부위와 머리에 4개, 꼬리에 1개가 있어요.<br/>
아래와 같은 순서로 정의되며 각도는 라디안값을 이용합니다.<br/>
각각의 한계 각도도 함께 확인을 해주세요.

머리와 꼬리 부위의 명칭과 제한 각도(라디안)
- Chest (Up/Down) : 머리 전체를 상하로 움직임 [-1.9, 0.0]
- Head Vertical (Up/Down) : 고개만 상하로 움직임 [-0.4, 0.0]
- Head Tilting (Left/Right) : 고개를 좌우로 기울임 [-0.5, 0.5]
- Tail (Up/Down) : 꼬리를 상하로 움직임 [0.0, 1.8]
- Head Horizontal (Left/Right) : 머리를 좌우 회전으로 움직임 [-0.78, 0.78]

&nbsp;

### [블록 코딩의 경우]

&nbsp;

### [우분투의 경우]
ROS가 설치된 PC에서 아래와 같은 명령어로 머리와 꼬리를 동시에 움직일 수 있어요.<br/>
5개의 라디안값은 위와 같은 순서로 지정하며 그 제한 각도에 유의를 해주세요.<br/>

```python
ros2 topic pub 시리얼넘버(UUID)/joint_group_position_controller/command std_msgs/Float64MultiArray "data: [-0.57, -0.1, -0.3, 0.6, 0.3]"
```

&nbsp;

https://github.com/macroact/maicat_tutorial/assets/106013071/044cb235-4306-4485-8428-a8b5256daf87


[Next - 다리](../09_maicat_move_legs/README.md)
