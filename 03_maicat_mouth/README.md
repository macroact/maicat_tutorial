# 마이캣(Maicat) 튜토리얼
## 입과 소리:

### 블록 코딩의 경우
마이캣의 입을 움직이면서 울음소리를 낼 수 있어요.

![meow](https://github.com/user-attachments/assets/53d953cd-acc9-469e-8f26-fbe28b647950)

&nbsp;
### 우분투의 경우
마이캣의 입을 제어하는 명령은 아래와 같아요.

    21~29: 끝자리 숫자 x 10ms 속도로 입을 열었다 닫기
    30: 빠르게 입을 열기
    31: 천천히 입을 열기
    32: 천천히 입을 닫기
    33: 빠르게 입을 닫기

```python
ros2 topic pub 시리얼넘버(UUID)/control_teensy std_msgs/Int64 "data: 원하는 입 제어 번호"
```

&nbsp;

소리를 내며 입을 제어하는 명령은 아래와 같아요.

```python
ros2 topic pub 시리얼넘버(UUID)/sound/meow std_msgs/Int64 "data: 원하는 소리 번호"
```

&nbsp;

글자를 사람의 목소리로 변환하는 TTS는 아래의 명령어로 확인할 수 있어요.

```python
ros2 topic pub 시리얼넘버(UUID)/sound/speech std_msgs/String "data: 원하는 문장"
```


&nbsp;

https://github.com/macroact/maicat_tutorial/assets/106013071/7d608775-537f-4ec0-b6a8-b917261cce64



[Next - 카메라](../04_maicat_camera/README.md)
