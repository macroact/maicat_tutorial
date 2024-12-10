# 마이캣(Maicat) 튜토리얼
## 네트워크 설정:

### (기관 사전 세팅의 경우 생략) 블루투스 연결
마이캣이 켜진 상태에서 앱에 로그인을 하면 가까운 마이캣을 찾게 됩니다.
앱 화면에 나타나는 마이캣을 선택하면 블루투스 연결을 진행합니다.

### (기관 사전 세팅의 경우 생략) 와이파이(Wi-Fi) 설정
앱 화면에서 검출되는 네트워크 목록 중 마이캣에 연결할 네트워크를 선택한 후 와이파이 비밀번호를 정확히 입력하세요.
잠시 후 마이캣은 해당 네트워크에 접속하게 되며 이후에는 별도의 설정이 필요하지 않습니다.

https://github.com/macroact/maicat_tutorial/assets/103547322/32a52cf4-bc47-4de6-a12d-e5fdab67b557

### 마이캣의 IP주소 확인
앱 화면에서 IP 주소를 확인한 후에 블록 코딩 또는 SSH 접속에 사용합니다.
![ip_address](https://github.com/user-attachments/assets/ea20e087-247a-4dfb-9ae8-8320393a7b24)

#### 블록 코딩의 경우
앱 화면에서 확인한 IP주소를 블록 코딩 화면의 IP주소창에 입력합니다.
![textField](https://github.com/user-attachments/assets/92f6ab1b-0e13-429e-bfc1-2efc0ff545fc)

IP주소가 정확하게 입력된 경우 아래 그림과 같이 마이캣에 연결됩니다. 
![textField-connect](https://github.com/user-attachments/assets/1a1485f5-f473-4cef-8411-65b22147e6ec)

이후에 보유하신 마이캣의 시리얼넘버(UUID)를 블록 코딩 화면의 ID창에 입력합니다.
![textField-connect](https://github.com/user-attachments/assets/1a1485f5-f473-4cef-8411-65b22147e6ec)
![textField-id](https://github.com/user-attachments/assets/983fad1d-9ba0-4675-a62d-0c7e8b5fe229)

#### 우분투의 경우
터미널창을 열고 IP주소 "ssh maicat@IP주소" 또는 호스트명 "ssh maicat@maibot1.local"을 입력하고 엔터키를 누릅니다.
일반적으로 호스트명은 시리얼넘버(UUID)의 끝자리 번호가 사용되어 maibot(끝자리 번호).local로 설정되어 배송됩니다.
```
ssh maicat@192.168.0.1
```
또는
```
ssh maicat@maibot1.local
```

&nbsp;
[Next - 눈 디스플레이](../02_maicat_eyes/README.md)
