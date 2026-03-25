# 기본 라우터에 포트 포워딩 설정하기

GL.iNet 라우터에 서버([OpenVPN 서버](how_to_set_up_openvpn_server.md) 또는 [WireGuard 서버](build_your_own_wireguard_home_server_with_two_glinet_routers.md) 등)를 설정하고 있고 기본 라우터에 연결되어 있는 경우 기본 라우터에 포트 포워딩을 설정해야 합니다. 이렇게 하면 서버가 제대로 액세스할 수 있습니다.

기본 라우터와 GL.iNet 라우터 사이에 다른 라우터가 있는 경우 이러한 모든 라우터에 포트 포워딩을 설정해야 합니다.

## 준비

포트 포워딩을 구성하기 전에 기본 라우터에서 GL.iNet 라우터용 **고정 IP 주소 예약**을 권장합니다. 이렇게 하면 GL.iNet 라우터에 항상 고정 IP 주소가 할당됩니다.

그렇지 않으면 기본 라우터 또는 GL.iNet 라우터가 다시 시작되면 기본 라우터가 GL.iNet 라우터에 새 IP 주소를 할당하여 포트 포워딩 규칙이 실패할 수 있습니다.

다음으로 기본 라우터에서 GL.iNet 라우터용 포트 포워딩을 설정합니다.

포트 포워딩 구성 단계는 라우터 브랜드와 모델에 따라 다릅니다. 아래 해당 섹션을 참조하세요.

## 기본 라우터로 GL.iNet 라우터 사용

[이 링크](../interface_guide/port_forwarding.md){target="_blank"}를 참조하세요.

## 다른 라우터 브랜드를 기본 라우터로 사용

!!! note "포트 포워딩 설정 시 다음 정보를 입력하세요"

    포트 포워딩을 구성할 때 다음 정보가 제공되는지 확인하세요. 라우터 브랜드와 모델에 따라 용어가 다를 수 있습니다.

    * **외부 포트/내부 포트:** 사용 중인 포트를 입력합니다. 예를 들어 기본 포트는 **1194**(OpenVPN 서버용)와 **51820**(WireGuard 서버용)입니다.
    * **프로토콜:** **All** 또는 **UDP/TCP**를 선택하세요.
    * **내부 IP**(또는 **Host IP**로 표시): 2차 라우터의 WAN IP 주소를 입력하거나 드롭다운에서 2차 라우터를 선택합니다.

일반적인 기본 라우터 브랜드와 모델에 포트 포워딩을 설정하는 단계별 지침입니다.

기본 라우터 브랜드나 모델이 아래에 나열되어 있지 않은 경우 라우터 설명서를 참조하거나 지원 팀에 문의하세요.

### AT&T

* [NVG589](https://www.att.com/support/article/u-verse-high-speed-internet/KM1010280/){target="_blank"}
* [Pace 5031](https://www.att.com/support/article/u-verse-high-speed-internet/KM1010292/){target="_blank"}
* [Peace 5268](https://www.att.com/support/article/u-verse-high-speed-internet/KM1123072){target="_blank"}

### Comcast (Xfinity)

* [Xfinity Gateway](https://www.xfinity.com/support/articles/xfi-port-forwarding){target="_blank"}

### TP-Link

* [Deco 시리즈](https://www.tp-link.com/us/support/faq/1797/){target="_blank"}
* [무선 라우터 시리즈](https://www.tp-link.com/us/support/faq/1379/){target="_blank"}

### Eero

[이 링크](https://support.eero.com/hc/en-us/articles/207908443-How-do-I-configure-port-forwarding){target="_blank"}를 참조하세요.

### Linksys

[이 링크](https://support.linksys.com/kb/article/318-en/){target="_blank"}를 참조하세요.

### Netgear

[이 링크](https://kb.netgear.com/24290/How-do-I-add-a-custom-port-forwarding-service-on-my-NETGEAR-router){target="_blank"}를 참조하세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
