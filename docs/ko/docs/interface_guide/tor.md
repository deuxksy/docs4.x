# Tor

Tor(**The Onion Router**에서 파생됨)는 익명 통신을 활성화하는 무료 오픈 소스 소프트웨어입니다. 사용자가 개인정보를 보호하며 인터넷을 탐색할 수 있도록 도와줍니다. [Tor에 대한 자세한 정보](https://www.torproject.org/){target="_blank"}.

**참고**: 이 기능은 현재 베타 버전이며 일부 국가에서 문제가 발생할 수 있습니다. Tor가 활성화되면 다음 기능이 제대로 작동하지 않습니다:

 - VPN
 - DNS
 - IPv6
 - ADGuard Home.

## 지원되는 모델

??? "지원되는 모델"
    - GL-MT3600BE (Beryl 7)
    - GL-E5800 (Mudi 7)
    - GL-MT5000 (Brume 3)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-BE3600 (Slate 7)
    - GL-B3000 (Marble)
    - GL-MT6000 (Flint2)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-AX1800 (Flint)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-A1300 (Slate Plus)
    - GL-AP1300 (Cirrus)
    - GL-S1300 (Convexa-S)
    - *GL-SFT1200 (Opal)
    - *GL-MT1300 (Beryl)
    - *GL-E750/E750V2 (Mudi)

    **참고**: * 표시가 있는 모델은 Tor를 기본적으로 지원하지 않지만 사용자가 플러그인을 통해 Tor를 수동으로 설치할 수 있습니다. 자세한 내용은 [여기](#manual-install)를 클릭하세요.

??? "지원되지 않는 모델"
    - GL-X2000 (Spitz Plus)
    - GL-AR750S (Slate)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-XE300 (Puli)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-X300B (Collie)

## 빠른 설정

웹 관리 패널 왼쪽에서 **VPN** -> **Tor**로 이동합니다.

펌웨어 ver.4.8.4 이상에서는 **APPLICATIONS** -> **Tor**로 이동합니다.

토글 스위치를 클릭하여 활성화하고 필요한 경우 **Custom Exit Nodes**를 활성화한 다음 **Apply**를 클릭하세요.

![enable tor](https://static.gl.inet.com/docs/router/en/4/tutorials/tor/enable_tor.png){class="glboxshadow"}

연결을 시작합니다. 네트워크가 요구 사항을 충족하면 연결됨을 표시합니다.

![tor connected](https://static.gl.inet.com/docs/router/en/4/tutorials/tor/connected.png){class="glboxshadow" width="672"}

## 수동 설치

**참고**: 일부 모델은 플러그인을 통해 Tor를 수동으로 설치할 수 있지만 CPU 부하가 증가하고 시스템 응답 속도가 느려질 수 있습니다.

웹 관리 패널 왼쪽에서 **APPLICATIONS** -> **Plug-ins**로 이동합니다.

**gl-sdk4-ui-torview**를 검색하여 설치하세요.

![torview](https://static.gl.inet.com/docs/router/en/4/tutorials/tor/torview.jpg){class="glboxshadow"}

![torpage](https://static.gl.inet.com/docs/router/en/4/tutorials/tor/torpage.jpg){class="glboxshadow"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
