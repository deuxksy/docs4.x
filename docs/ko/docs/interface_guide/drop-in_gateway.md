# 드롭인 게이트웨이

웹 관리 패널 왼쪽의 **NETWORK** -> **Drop-in Gateway** 로 이동합니다.

드롭인 게이트웨이는 기존 기본 라우터를 교체하거나 재구성하지 않고 기능 확장을 가능하게 하는 확장 기능입니다. GL.iNet 라우터를 이더넷 케이블로 기본 라우터에 연결하여 기존 네트워크 인프라에 고급 네트워크 기능을 추가할 수 있습니다. 예를 들어:

- AdGuard Home을 통한 광고 필터링
- VPN 클라이언트 활성화
- 암호화 DNS 사용

충분한 메모리가 있는 고성능 라우터 또는 보안 게이트웨이(예: GL-MT2500, GL-MT5000)를 사용하고 필요에 따라 추가 트래픽 전달 및 제어 도구를 설치하는 것이 좋습니다.

## 네트워크 토폴로지

드롭인 게이트웨이는 중간 네트워크 시스템으로 작동하며, 클라이언트 기기의 데이터 트래픽을 기본 라우터를 통해 전송하기 전에 GL.iNet 라우터에서 처리하도록 라우팅합니다. 이 과정에서 기존 네트워크 설정(예: SSID 및 비밀번호)을 유지하여 연결된 모든 기기의 연결이 중단되지 않도록 보장할 뿐만 아니라, 필요에 따라 모든 또는 특정 클라이언트 기기의 네트워크 트래픽을 관리할 수 있습니다.

![drop-in gateway mode typology](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/drop-in_gateway_mode_topology.svg){class="glboxshadow gl-60-desktop"}

위 다이어그램은 두 가지 유형의 선으로 구성되어 있습니다: 회색 선과 세 개의 화살표가 있는 녹색 선으로, 각각 해당 번호가 표시되어 있습니다.

1. **회색 선**은 물리적 연결 토폴로지를 보여줍니다: 클라이언트 기기(예: 컴퓨터, 노트북)가 기본 라우터에 연결되고, 기본 라우터의 LAN 포트가 이더넷 케이블을 통해 GL.iNet 라우터(드롭인 게이트웨이 활성화됨)의 WAN 포트에 연결됩니다.

2. **녹색 선**은 드롭인 게이트웨이가 활성화될 때 순차적인 데이터 전송 경로를 나타내며, 번호가 매겨진 화살표는 트래픽 흐름 순서를 나타냅니다:

    1. 클라이언트 기기의 트래픽이 먼저 기본 라우터로 라우팅됩니다.

    2. 기본 라우터가 트래픽을 GL.iNet 라우터로 전달하여 처리합니다(예: 광고 필터링, VPN 암호화).

    3. 처리 후 트래픽은 다시 기본 라우터로 전송되며, 기본 라우터는 최종 데이터를 원래 클라이언트 기기로 전달하거나 인터넷으로 라우팅합니다.

## 설정

다양한 적용 시나리오를 위해 두 가지 배포 모드가 있습니다: 모든 클라이언트 기기가 드롭인 게이트웨이를 통해 네트워킹되거나, 특정 클라이언트 기기만 드롭인 게이트웨이를 통해 네트워킹됩니다.

다음 예에서는 기본 라우터의 게이트웨이 주소가 `192.168.1.1` 입니다.

### 모든 기기가 드롭인 게이트웨이를 통해 네트워킹됨 {all-devices-managed-by-the-drop-in-gateway}

1. 기본 라우터의 LAN 포트를 이더넷 케이블로 GL.iNet 라우터의 WAN 포트에 연결합니다.

2. GL.iNet 라우터의 웹 관리 패널에 로그인하고, 드롭인 게이트웨이를 활성화하면 시스템이 자동으로 해당 구성 매개변수를 생성합니다.

    ![drop-in gateway generated settings](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/drop-in_gateway_all_device_enabled.png){class="glboxshadow"}

    - **IP 주소**는 GL.iNet 라우터의 WAN IP 주소를 나타내며, 기본 라우터에서 동적으로 할당됩니다. 이 WAN IP는 [INTERNET](internet_ethernet.md) 페이지의 이더넷 섹션에서 확인할 수 있습니다.

    - **게이트웨이** 및 **DNS 서버 1** 필드는 기본적으로 기본 라우터의 IP 주소로 자동 채워집니다. 이러한 매개변수가 잘못 구성된 경우 필요에 따라 수동으로 조정할 수 있습니다.

    여기에 IP 주소를 기록해 두세요. 다음 단계에서 사용하게 됩니다.

    첫 번째 구성 방법을 선택하고 **Apply** 를 클릭합니다.

3. 기본 라우터의 웹 관리 패널에 로그인합니다.

    ??? "GL.iNet"

        기본 라우터가 GL.iNet이고 펌웨어 v4.2 이상을 실행하는 경우 아래 단계를 따르세요.

        웹 관리 패널 -> NETWORK -> LAN -> DHCP 서버 -> 고급으로 이동합니다.

        ![glinet lan advanced](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/glinet/lan_advanced.png){class="glboxshadow"}

        2단계의 IP 주소를 DHCP 게이트웨이로 입력합니다(예: `192.168.1.23`). 그런 다음 **Apply** 를 클릭합니다.

        ![glinet lan, dhcp gateway](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/glinet/tips_dhcp_gateway.png){class="glboxshadow"}

        ![glinet lan, dhcp gateway](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/glinet/lan_dhcp_gateway.png){class="glboxshadow"}

    ??? "TP-Link"

        기본 라우터가 TP-Link인 경우 아래 단계를 따르세요(TP-LINK Archer C3150 예시).

        TP-Link 관리 페이지에 로그인하고 **Advanced** -> **Network** -> **DHCP Server** 로 이동한 다음 **DHCP** 를 비활성화합니다.

        ![tplink admin, disable dhcp](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/tplink/tplink_disable_dhcp_1.png){class="glboxshadow"}

        그런 다음 **Save** 를 클릭합니다.

        ![tplink admin, disable dhcp](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/tplink/tplink_disable_dhcp_2.png){class="glboxshadow"}

    ??? "Linksys"

        기본 라우터가 Linksys인 경우 아래 단계를 따르세요(Linksys WHW01 예시)

        Linksys 관리 페이지에 로그인하고 **Router Settings** -> **Connectivity** 로 이동합니다.

        ![linksys admin, connectivity](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/linksys/linksys_connectivity.png){class="glboxshadow"}

        **Local Network** 탭을 클릭하고 **DHCP Server** 를 비활성화한 다음 **OK** 를 클릭합니다.

        ![linksys admin, local network, disable dhcp](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/linksys/linksys_disable_dhcp.png){class="glboxshadow"}

        경고가 표시됩니다. **OK** 를 클릭합니다.

        ![linksys admin, apply changes](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/linksys/linksys_apply_changes.png){class="glboxshadow"}

    ??? "기타"

        기본 라우터의 관리 패널에 로그인하여 DHCP 서버를 비활성화하세요. 해당 제조업체의 사용자 설명서를 참조하거나 지원팀에 문의하세요.

4. GL.iNet 라우터로 돌아와서 [AdGuard Home](adguardhome.md), [암호화 DNS](dns.md), [WireGuard 클라이언트](wireguard_client.md) 및 [OpenVPN 클라이언트](openvpn_client.md)와 같은 기능을 설정합니다.

### 특정 기기만 드롭인 게이트웨이를 통해 네트워킹됨 {some-devices-managed-by-the-drop-in-gateway}

1. 기본 라우터의 LAN 포트를 이더넷 케이블로 GL.iNet 라우터의 WAN 포트에 연결합니다.

2. GL.iNet 라우터의 웹 관리 패널에 로그인하고, 드롭인 게이트웨이를 활성화하면 시스템이 자동으로 해당 구성 매개변수를 생성합니다.

    ![drop-in gateway generated settings](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/drop-in_gateway_some_device_enabled.png){class="glboxshadow"}

    - **IP 주소**는 GL.iNet 라우터의 WAN IP 주소를 나타내며, 기본 라우터에서 동적으로 할당됩니다. 이 WAN IP는 [INTERNET](internet_ethernet.md) 페이지의 이더넷 섹션에서 확인할 수 있습니다.

    - **게이트웨이** 및 **DNS 서버 1** 필드는 기본적으로 기본 라우터의 IP 주소로 자동 채워집니다. 이러한 매개변수가 잘못 구성된 경우 필요에 따라 수동으로 조정할 수 있습니다.

    여기에 IP 주소를 기록해 두세요. 다음 단계에서 사용하게 됩니다.

    두 번째 구성 방법을 선택하고 **Apply** 를 클릭합니다.

3. 드롭인 게이트웨이 기능을 사용하려는 기기에서 게이트웨이와 DNS를 드롭인 게이트웨이 페이지의 IP 주소로 설정합니다.

    ??? "Windows"

        Windows 11의 예시이며, Windows 10도 유사합니다. PC가 기본 라우터에 연결되어 있는지 확인하세요. 여기서는 컴퓨터가 네트워크 케이블로 기본 라우터에 연결되어 있다고 가정하며, Wi-Fi로 연결하는 경우도 유사합니다.

        1. 설정을 엽니다.

        2. **네트워크 및 인터넷** 을 클릭합니다.

        3. **이더넷** 탭을 클릭합니다.

            ![windows 11 ethernet](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/windows/windwos11_ethernet.png){class="glboxshadow"}

        4. 이 PC의 IP 주소를 확인할 수 있습니다. "IP 할당" 섹션에서 **편집** 버튼을 클릭합니다.

            ![windows 11 ethernet edit](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/windows/windwos11_ethernet_ip_assignment_edit.png){class="glboxshadow"}

        5. **수동** 옵션을 선택합니다. **IPv4 토글** 을 켭니다.

        6. **IP 주소** 를 d단계에서 본 IP 주소로 설정하고, **서브넷 마스크** 를 `255.255.255.0` 으로 설정하며, **게이트웨이** 및 **기본 DNS** 를 모두 드롭인 게이트웨이 페이지의 IP 주소로 설정합니다.

            ![windows 11 ethernet edit](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/windows/windwos11_ethernet_edit_ip_settings.png){class="glboxshadow"}

        7. **저장** 버튼을 클릭합니다.

    ??? "Android"

        Samsung S21의 예시입니다. 스마트폰이 기본 라우터에 연결되어 있는지 확인하세요.

        1. 설정을 열고 연결을 클릭합니다.

            ![settings connections](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/android/settings_connections.jpg){class="glboxshadow"}

        2. Wi-Fi를 클릭합니다.

            ![connection wifi](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/android/connections_wifi.jpg){class="glboxshadow"}

        3. 현재 SSID의 톱니바퀴 아이콘을 클릭합니다.

            ![wifi setting](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/android/wifi_cog.jpg){class="glboxshadow"}

        4. **자세히 보기** 를 클릭합니다.

            ![wifi settings, view more](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/android/wifi_view_more.jpg){class="glboxshadow"}

        5. **IP 설정** 을 클릭하고 **고정** 을 선택합니다.

            ![ip settings](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/android/wifi_ip_settings.jpg){class="glboxshadow"}

            ![IP settings, static](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/android/ip_settings_static.jpg){class="glboxshadow"}

        6. **게이트웨이** 및 **DNS 1** 을 드롭인 게이트웨이 페이지의 IP 주소로 설정한 다음 **저장** 을 클릭합니다.

            ![set gateway and dns ip](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/android/set_gateway.jpg){class="glboxshadow"}

    ??? "iOS"

        iPhone 8의 iOS 16.3 예시입니다. 스마트폰이 기본 라우터에 연결되어 있는지 확인하세요.

        1. 설정을 열고 Wi-Fi를 클릭합니다.

            ![settings wifi](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/iphone/setting_wifi.jpg){class="glboxshadow gl-60-desktop"}

        2. SSID를 클릭합니다.

            ![settings wifi](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/iphone/wifi_list.jpg){class="glboxshadow gl-60-desktop"}

        3. 아래로 스크롤하면 **IP 구성** 이 **자동** 인 것을 확인할 수 있습니다. 다음 단계를 위해 **IP 주소** 와 **서브넷 마스크** 를 기록해 두세요.

            ![wifi ipv4](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/iphone/ipv4.jpg){class="glboxshadow gl-60-desktop"}

        4. **IP 구성** 을 **수동** 으로 변경하고, **IP 주소** 와 **서브넷 마스크** 를 이전 단계에서 얻은 것과 동일하게 설정한 다음, **라우터** 를 드롭인 게이트웨이 페이지에 표시된 IP 주소로 설정하고 **저장** 을 클릭합니다.

            ![wifi ipv4 manual](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/iphone/set_ipv4.jpg){class="glboxshadow gl-60-desktop"}

        5. **DNS 구성** 을 클릭하고 **수동** 으로 변경합니다. **서버 추가** 를 클릭하고 DNS 서버 IP 주소를 드롭인 게이트웨이 페이지에 표시된 IP 주소로 설정한 다음 **저장** 을 클릭합니다.

            ![wifi dns](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/iphone/dns.jpg){class="glboxshadow gl-60-desktop"}

            ![wifi set dns](https://static.gl-inet.com/docs/router/en/4/tutorials/drop-in_gateway/iphone/set_dns.jpg){class="glboxshadow gl-60-desktop"}

4. GL.iNet 라우터의 웹 관리 패널로 돌아와서 필요에 따라 [AdGuard Home](adguardhome.md), [암호화 DNS](dns.md), [WireGuard 클라이언트](wireguard_client.md) 및 [OpenVPN 클라이언트](openvpn_client.md)와 같은 기능을 설정합니다.

## 주의사항

1. 드롭인 게이트웨이를 활성화하면 네트워크 지연 시간이 증가합니다.

2. 드롭인 게이트웨이가 활성화되면 선택된 LAN 기기 간의 데이터 전송도 드롭인 게이트웨이를 통해 라우팅됩니다. 따라서 기본 라우터와 드롭인 게이트웨이 간의 대역폭이 전체 LAN 대역폭에 영향을 미칩니다.

---

관련 문서:

- [GL.iNet 라우터에서 드롭인 게이트웨이 설정 방법](../tutorials/how_to_set_up_drop_in_gateway.md)

---

궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하시거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용해 주세요.
