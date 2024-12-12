# 마이캣(Maicat) 튜토리얼
## [우분투에만 해당] 터치 센서:

마이캣의 머리와 등에는 3개의 터치 센서가 탑재되어 있어요.<br/>
이 튜토리얼의 대상이 되는 EV(Education Version)에는 기본적으로 모든 터치에 머리와 꼬리를 랜덤하게 움직이며<br/>
행복한 눈 표정을 보이도록 설정된 상태입니다.<br/>
이것을 직접 특정 부위의 터치에 "야옹" 소리를 내거나 다른 행동을 하도록 설정할 수 있어요.

- 머리 위
- 머리 뒤
- 등

&nbsp;

### SSH 접속
설정을 변경하기 위해서는 직접 소스 코드를 작성해야 합니다.<br/>
코드를 작성 및 적용하기 위해서는 마이캣의 시스템에 접속해야 하는데, 이 경우 ssh 명령을 이용합니다.<br/>
PC의 터미널에서 아래 명령을 입력하는데 호스트명은 maibot + UUID 마지막 숫자 + .local로 설정되어 있습니다.<br/>

```python
#input the SSH command then enter the password
ssh maicat@maibot.local
```

또는, 1. [네트워크 설정 및 IP주소 확인](01_maicat_network/README.md) 에서 확인한 ip 주소로 접속할 수 있어요.

```python
#input the SSH command then enter the password
ssh maicat@192.168.0.1 (마이캣 ip 주소)
```

&nbsp;

정상적으로 연결이 되면 비밀번호를 입력하라는 메시지를 볼 수 있어요.<br/>
마이캣의 기본 비밀번호는 mai2019 입니다. 알파벳은 모두 소문자로 입력해 주세요.
마이캣 시스템에 로그인 후에는 상호작용 역할을 하는 maibot_interaction.service 를 중지합니다.

```python
sudo systemctl stop maibot_interaction.service
```

&nbsp;

그리고, 터치 반응에 대해 수정할 수 있는 스크립트의 편집 화면을 불러옵니다.

```python
nano maicat_automatic/install/maibot_interaction/lib/python3.9/site-packages/boot/brain_ev_node.py
```

&nbsp;

아래 코드는 터치 반응에 대한 기본 설정입니다. 이를 원하는대로 수정한 후에 ctrl+o --> 엔터로 저장하고 ctrl+x로 편집 화면에서 빠져나옵니다.

```python
def _callback_touch(self, msg):
    if self._is_first_touch:
        subprocess.call(["sudo", "systemctl", "start", "maibot_gpt.service"])
        self._is_first_touch = False

    self._orders_teensy(4)
    self.default_head_vertical = round(random.uniform(self.servo_limit_head[0], self.servo_limit_head[1]), 2)
    self.default_head_tilt = round(random.uniform(self.servo_limit_head_side[0], self.servo_limit_head_side[1]), 2)
    self.default_tail = round(random.uniform(self.servo_limit_tail[0], self.servo_limit_tail[1]), 2)
    self._orders_servo([self.default_head_vertical, self.default_head_tilt, self.default_tail])
    time.sleep(0.4)
    self.default_head_vertical = round(random.uniform(self.servo_limit_head[0], self.servo_limit_head[1]), 2)
    self.default_head_tilt = round(random.uniform(self.servo_limit_head_side[0], self.servo_limit_head_side[1]), 2)
    self.default_tail = round(random.uniform(self.servo_limit_tail[0], self.servo_limit_tail[1]), 2)
    self._orders_servo([self.default_head_vertical, self.default_head_tilt, self.default_tail])
    self.default_head_vertical = round(random.uniform(self.servo_limit_head[0], self.servo_limit_head[1]), 2)
    self.default_head_tilt = round(random.uniform(self.servo_limit_head_side[0], self.servo_limit_head_side[1]), 2)
    self.default_tail = round(random.uniform(self.servo_limit_tail[0], self.servo_limit_tail[1]), 2)
    self._orders_servo([self.default_head_vertical, self.default_head_tilt, self.default_tail])
    self._orders_teensy(5)
```

&nbsp;

변경된 기능을 확인하기 위해 maibot_interaction.service 를 실행하고 약 1분 정도 기다린 후에 마이캣의 머리와 등을 만져보세요.

```python
sudo systemctl start maibot_interaction.service
```

&nbsp;

[Next - 머리와 꼬리](../08_maicat_move_head_and_tail/README.md)
