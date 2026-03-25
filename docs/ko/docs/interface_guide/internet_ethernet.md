# 이더넷 케이블을 통해 인터넷에 연결

WAN 포트에 연결된 이더넷 케이블을 통해 라우터를 광대역 네트워크에 연결합니다. 일반적으로 IP 주소(DHCP)를 자동으로 획득합니다. 사용자는 수동으로 고정 IP 또는 PPPoE를 구성할 수도 있습니다. 이 방법은 높은 안정성과 빠른 속도를 제공하며 고정 광대역 액세스가 있는 가정 및 사무실 환경에 이상적입니다.

다음 단계에 따라 이더넷 케이블을 통해 라우터를 인터넷에 연결하세요.

1. 라우터의 WAN 포트를 이더넷 케이블을 통해 상위 장치(예: ISP 모뎀, 라우터, 네트워크 스위치 또는 이더넷 잭)에 연결합니다.

2. 라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Ethernet** 섹션으로 이동합니다.

    연결이 성공하면 Ethernet 섹션에 프로토콜, IP 주소, 게이트웨이 및 DNS 서버를 포함한 네트워크 세부 정보가 표시됩니다.

    ![ethernet](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_ethernet/ethernet_1.png){class="glboxshadow"}

**팁**: 이더넷 케이블을 라우터의 WAN 포트에 꽂기 전에 **Change to LAN**을 클릭하여 [WAN 포트를 LAN 포트로 설정](../faq/change_wan_to_lan.md)할 수 있습니다. 이는 라우터를 [중계기](internet_repeater.md)로 사용할 때 유용합니다. 물리적 WAN 포트가 유휴 상태이기 때문입니다. 따라서 사용하지 않는 WAN 포트를 LAN 포트로 용도 변경하면 LAN 포트가 하나 더 늘어납니다.

## 프로토콜

DHCP, Static, PPPoE의 3가지 유형의 프로토콜이 있습니다. **Modify**를 클릭하여 변경합니다.

![modify](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_ethernet/ethernet_2.png){class="glboxshadow"}

* DHCP

    DHCP는 기본이며 가장 일반적인 프로토콜로 IP 네트워크에서 클라이언트-서버 아키텍처를 통해 네트워크 장치에 IP 주소 및 기타 통신 매개변수를 자동으로 할당합니다.

    ![ethernet dhcp](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_ethernet/ethernet_3.png){class="glboxshadow"}

* Static

    ISP(인터넷 서비스 제공자)가 고정 IP 주소를 제공하거나 IP 주소, 게이트웨이, 넷마스크와 같은 네트워크 정보를 수동으로 구성하려는 경우 Static이 필요합니다.

    ![ethernet static](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_ethernet/ethernet_4.png){class="glboxshadow"}

* PPPoE

    PPPoE는 대부분의 ISP에서 사용하는 프로토콜입니다. 일반적으로 모뎀과 사용자 이름 및 비밀번호를 제공하며 인터넷 설정에 필요합니다.

    ![ethernet pppoe](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_ethernet/ethernet_5.png){class="glboxshadow"}

## 고급 설정

필수 설정 외에도 위 세 가지 프로토콜에 대한 선택적 고급 설정이 있습니다.

* **VLAN ID**: 공급자 서버가 인터페이스에 특정 태그가 지정된 VLAN ID를 사용하도록 요구하는 경우에만 이 설정 항목이 필요합니다.

* **TTL**: TTL(Time To Live)은 패킷이 네트워크에서 존재할 수 있는 최대 시간을 정의합니다. 기본적으로 라우터는 클라이언트 장치에서 들어오는 패킷의 TTL을 1씩 줄인 후 포워딩합니다. 재정의해야 하는 경우 여기에 고정 값을 설정할 수 있습니다. TTL 설정은 IPv4에만 유효합니다.

* **HL**: IPv6에서 HL(Hop Limit) 필드는 네트워크에서 데이터 패킷의 전송 홉 수를 제한하며 IPv4의 TTL과 동일합니다.

* **MTU**: 기본 MTU 값은 1500바이트입니다.

## 이더넷 포트

오른쪽 상단의 기어 아이콘을 클릭하여 [이더넷 포트](ethernet_port.md)로 들어갑니다.

![ethernet port 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_ethernet/ethernet_6.png){class="glboxshadow"}

**WAN** 페이지는 포트 역할(즉, WAN 또는 LAN으로 사용), MAC 모드 및 MAC 주소, 협상된 네트워크 포트 속도를 표시합니다.

![ethernet port 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/ethernet_port/wan.png){class="glboxshadow"}

**LAN** 페이지는 포트 역할 및 협상된 네트워크 포트 속도를 표시합니다.

![ethernet port 3](https://static.gl.inet.com/docs/router/en/4/interface_guide/ethernet_port/lan.png){class="glboxshadow"}

자세한 내용은 이 [링크](ethernet_port.md)를 참조하세요.

## 문제 해결

이더넷 케이블이 WAN 포트에 꽂혀 있지만 인터넷을 사용할 수 없는 경우 아래와 같은 노란색 메시지가 표시됩니다.

**"인터페이스는 연결되었지만 인터넷에 액세스할 수 없습니다."**

![ethernet caution](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_ethernet/ethernet_9.jpg){class="glboxshadow gl-90-desktop"}

이 문제를 해결하려면:

1. 상위 장치에 인터넷 액세스가 있는지 확인하세요.

2. [Multi-WAN](multi-wan.md) 페이지로 이동하여 Ethernet 인터페이스 상태를 확인하세요.

---

관련 문서

- [Internet 페이지](internet.md)
- [각 인터넷 액세스 방법의 우선 순위를 설정하는 방법](multi-wan.md)
- [여러 인터넷 액세스 방법을 동시에 사용할 때 로드 밸런스를 설정하는 방법](multi-wan.md)

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
