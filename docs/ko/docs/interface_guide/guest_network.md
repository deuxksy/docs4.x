# 게스트 네트워크

게스트 네트워크 설정은 펌웨어 v4.5부터 [LAN](lan.md)에서 분리되었습니다.

웹 관리 패널 왼쪽에서 **NETWORK** -> **Guest Network**로 이동합니다.

여기에는 게스트 네트워크 기본 설정과 DHCP 서버 설정이 포함됩니다.

## 기본 설정

IPv4 프라이빗 주소 범위 내에서 서브넷을 설정할 수 있습니다: `192.168.0.0/16`, `172.16.0.0/12`, `10.0.0.0/8`

![guest network 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/guest_network/guest_network_1.png){class="glboxshadow"}

임시 사용자를 위해 설계된 별도의 격리된 네트워크를 설정하여, 기본 네트워크와 분리됨으로써 제한된 액세스와 향상된 보안을 제공할 수 있습니다.

**참고**: 일부 모델(예: GL-MT5000, GL-MT2500/GL-MT2500A)은 Wi-Fi를 지원하지 않으므로 웹 관리 패널에서 게스트 네트워크 설정을 사용할 수 없습니다.

- **게이트웨이**

    게스트 네트워크의 **기본 게이트웨이**는 **192.168.9.1**입니다. 로컬 네트워크와 충돌하는 경우 다른 주소로 변경하세요.

- **서브넷 마스크**

    기본값은 **255.255.255.0**입니다. 더 많은 IP 주소가 필요한 더 큰 서브넷이 필요한 경우 **255.255.0.0**을 선택할 수도 있습니다.

- **AP 격리**

    이 기능은 펌웨어 v4.5부터 사용할 수 있습니다

    클라이언트 장치를 별도의 네트워크 세그먼트로 격리할 수 있습니다. 이러한 장치는 동일한 네트워크의 다른 장치와 통신할 수 없게 됩니다.

- **WAN 서브넷 차단**

    이 기능은 펌웨어 v4.8부터 사용할 수 있습니다

    활성화하면 게스트 네트워크에서 업스트림 네트워크와 해당 서브넷에 액세스할 수 없습니다.

## DHCP 서버

게스트 네트워크가 활성화되면 DHCP 서버가 기본적으로 활성화됩니다.

DHCP 서버는 게스트 네트워크에 연결된 각 클라이언트 장치에 IP 주소 및 기타 통신 매개변수를 자동으로 할당합니다. DHCP 서버를 비활성화하면 클라이언트 장치의 네트워크 설정을 수동으로 구성해야 합니다. 수동으로 고정 IP를 구성하는 방법을 알아보려면 [여기](../tutorials/manually_configure_static_ip.md)를 클릭하세요.

네트워크 확장 또는 축소, IP 주소 충돌 발생, 서브넷 마스크 범위 수정 등 필요에 따라 시작 및 종료 IP 주소를 변경할 수 있습니다.

![guest network 2](https://static.gl-inet.com/docs/router/en/4/interface_guide/guest_network/guest_network_2.png){class="glboxshadow"}

필요한 경우 **Advanced**를 클릭하여 추가 구성을 진행하세요.

![dhcp advanced 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/guest_network/dhcp_advanced1.png){class="glboxshadow"}

![dhcp advanced 2](https://static.gl-inet.com/docs/router/en/4/interface_guide/guest_network/dhcp_advanced2.png){class="glboxshadow"}

- **임대 시간**: DHCP가 할당한 IP 주소가 장치에 대해 유효한 기간입니다.

- **게이트웨이**: 게스트 네트워크와 인터넷과 같은 외부 네트워크 간의 트래픽을 라우팅하는 장치입니다.

- **DNS 서버 1**: 도메인 이름을 IP 주소로 변환하는 기본 서버입니다.

- **DNS 서버 2**: 기본 DNS 서버를 사용할 수 없을 때 도메인 이름 확인을 위해 사용되는 보조 서버입니다.

- **LPR 서버**: (Line Printer Remote Server) 인쇄 작업을 관리하고 네트워크 장치가 원격 프린터로 인쇄 요청을 보낼 수 있도록 하는 서비스입니다. 여러 LPR 프린터 포트를 구성할 수 있습니다.

---

관련 문서:

- [GL.iNet 라우터에서 게스트 Wi-Fi 네트워크 설정 방법](../tutorials/how_to_set_up_a_guest_network.md)

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 연락하세요.
