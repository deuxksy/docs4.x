# 토글 버튼 설정

토글 버튼 설정을 사용하면 라우터의 물리적 토글 버튼에 특정 기능을 할당하여 빠른 액세스와 제어를 제공하고 일반적인 작업에 대한 편리한 바로가기를 만들 수 있습니다.

웹 관리 패널에서 버튼 동작을 사용자 정의할 수 있습니다.

## 지원되는 모델

??? "지원되는 모델"
    - GL-MT3600BE (Beryl 7)
    - GL-BE3600 (Slate 7)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-MT1300 (Beryl)
    - GL-SFT1200 (Opal)
    - GL-A1300 (Slate Plus)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-E750V2 (Mudi V2)
    - GL-AR750S (Slate)
    - GL-AR750 (Creta)

??? "지원되지 않는 모델"
    - GL-E5800 (Mudi 7)
    - GL-MT5000 (Brume 3)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-X2000 (Spitz Plus)
    - GL-B3000 (Marble)
    - GL-MT6000 (Flint2)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-AX1800 (Flint)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-XE300 (Puli)
    - GL-B1300 (Convexa-B)
    - GL-AP1300 (Cirrus)
    - GL-X300B (Collie)

## 설정

웹 관리 패널 왼쪽에서 **SYSTEM** -> **Toggle Button Settings**로 이동합니다.

![toggle button settings](https://static.gl.inet.com/docs/router/en/4/interface_guide/toggle_button_settings/toggle_button_settings.jpg){class="glboxshadow"}

펌웨어 v4.8 이전에는 4가지 옵션이 있으며 사용자가 토글 버튼의 기능을 사용자 정의할 수 있습니다.

- No Function
- AdGuard Home
- OpenVPN Client
- Tor
- WireGuard Client

펌웨어 v4.8부터 Repeater, Wi‑Fi, LED와 같은 더 많은 옵션이 도입되었습니다. 사용자는 필요에 따라 토글 버튼을 사용자 정의할 수 있습니다.

- No Function
- Repeater
- Wi-Fi (메인/게스트 Wi-Fi)
- VPN
- Tor
- AdGuard Home
- LED

![toggle button 4.8](https://static.gl.inet.com/docs/router/en/4/interface_guide/toggle_button_settings/toggle_button_4.8.png){class="glboxshadow"}

설정을 적용할 때 토글 스위치의 켜짐/꺼짐(왼쪽/오른쪽) 위치에 따라 선택한 기능을 즉시 활성화/비활성화할지 결정할 수 있습니다.

**참고**: 장치를 재시작한 후 시스템은 토글 스위치 위치에 따라 기능 상태를 자동으로 적용합니다.

예를 들어 WireGuard Client가 토글 스위치로 제어되도록 구성한 경우: 스위치가 왼쪽(ON)이면 WireGuard Client가 자동으로 시작됩니다. 스위치가 오른쪽(OFF)이면 WireGuard Client가 비활성화된 상태로 유지됩니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
