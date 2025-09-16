# 마이캣(Maicat) 튜토리얼
## Connection:

### Hotspot 설정
<!-- Blank -->
WiFi 계정 변경 또는 신규 등록을 위해 모바일 핫스팟 기능을 이용합니다.
- 네트워크 이름 : Macroact
- 비밀번호 : 20190507
- 밴드 : 2.4GHz
- 보안 : WPA2-Personal
<!-- Blank -->
해당 설정을 활성화시킨 후 PC를 먼저 핫스팟 네트워크에 연결합니다.</br>
이후 마이캣의 전원을 켭니다.

&nbsp;

### (PC 터미널) SSH(Secure Shell) 접속
<!-- Blank -->
- UUID : 마이캣 시리얼넘버
- 패스워드 : 기관별 설정된 비밀번호
<!-- Blank -->

```python
ssh maicat@[UUID].local
```
<!-- ```  Three backticks to start block " -->
이후에 표시되는 maicat@[UUID].local&apos;s password: 에 패스워드 입력 <code style="color : red">(한글 또는 대문자 입력 상태인지 확인)</code>
<!-- ```  Three backticks to end block -->
정상적으로 접속이 완료되면, 아래와 같이 터미널 프롬프트가 표시됩니다.
<!-- ```  Three backticks to start block " -->
```python
maicat@[UUID].local:~ $
```

&nbsp;

### 마이캣 업데이트
<!-- Blank -->
SSH 접속 상태에서 다음 명령어를 실행합니다.
<!-- Blank -->

```python
source ~/system/maibot_update.sh
```
업데이트 관련 로그가 출력된 후 마이캣은 자동으로 리부팅 됩니다.

&nbsp;

### WiFi 설정
<!-- Blank -->
기본적으로 WPA-PSK 방식의 인증과 2.4GHz를 지원합니다.</br>
SSH 접속 상태에서 다음 명령어를 실행합니다.
<!-- Blank -->

```python
sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
```
아래와 같이 편집기 화면이 나타나는데, network 부분 중 Macroact 네트워크는 향후 Hotspot 또는 A/S를 대비해 그대로 유지하고, 연결이 불가한 네트워크는 삭제하고 새로운 network를 추가합니다.</br>
### <code style="color : red">입력값에 오류가 있는 경우, 모바일 핫스팟 마저 접속이 불가하고 A/S를 받아야만 하니 재차 확인을 해야 합니다.</code>

```python
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=US                      # US 외의 경우에는 몇몇 이슈가 있어 그대로 유지합니다.

# 핫스팟 또는 A/S를 위해 유지해 주세요
network={
        ssid="Macroact"
        psk="20190507"
        key_mgmt=WPA-PSK
        id_str="hq"
}

# 이 부분에 네트워크를 추가하거나 수정합니다
network={
        scan_ssid=1              # (옵션) 숨겨진 WiFi에도 연결 가능
        ssid="YOUR_NETWORK_NAME" # SSID
        psk="YOUR_WIFI_PASSWORD" # 비밀번호
        key_mgmt=WPA-PSK         # 인증 방식
}
```
편집을 완료한 후 <code style="color : red">Ctrl + O</code> 를 누르고 파일명을 확인한 후 <code style="color : red">엔터키</code>를 통해 저장합니다.</br>
이후에 <code style="color : red">Ctrl + X</code> 로 편집기를 종료합니다.</br>
Secure Shell로 연결된 상태이기에 당장 네트워크 테스트를 할 수는 없기 때문에 아래 명령어로 마이캣의 시스템을 종료합니다.
```python
sudo shutdown now
```

1. 마이캣의 눈(디스플레이)이 꺼지면 꼬리쪽 스위치를 눌러 전원을 차단합니다.</br>
2. 모바일 핫스팟을 종료합니다.
3. PC를 일반 무선 네트워크에 연결합니다.
4. 마이캣의 스위치를 눌러 전원을 켜고 눈(디스플레이)이 켜지면, SSH 접속을 시도합니다.

```python
ssh maicat@[UUID].local
```
접속이 가능하면 WiFi 설정이 완료된 것입니다.</br>
접속이 되지 않고 오류 메시지가 발생하면, 아래 링크의 프로그램을 통해 마이캣을 연결 여부를 확인해 주세요.</br>
- https://www.advanced-ip-scanner.com/download
- https://angryip.org/download

호스트명이 나타나지 않는 경우가 가끔 발생하는데, 이 때에는 아래와 같이 검색되는 ip 주소로 접속을 해주세요.
```python
ssh maicat@192.168.0.27  # IP 예시
```
