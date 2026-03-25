# 웹 관리 패널에 액세스할 수 없음

때로는 [http://192.168.8.1](http://192.168.8.1)에 액세스하지 못해 웹 관리 패널에 로그인하지 못할 수 있습니다. 여러 가지 원인이 있을 수 있습니다.

![can't access admin](https://static.gl.inet.com/docs/router/en/4/tutorials/cannot_access_web_admin_panel/cantaccessadmin.jpg){class="glboxshadow"}

## 가능한 원인

* 컴퓨터 또는 모바일 폰이 라우터에 연결되지 않음.
* `192.168.8.1`은 라우터의 기본 IP 주소입니다. 이 IP를 변경했을 수 있습니다.
* 브라우저의 캐시 또는 확장 프로그램으로 인해 관리 패널에 액세스하지 못할 수 있습니다.
* VPN 또는 프록시 소프트웨어가 트래픽을 처리하여 관리 패널에 액세스하지 못할 수 있습니다.
* 라우터가 벽돌(bricked)됨.

## 웹 관리 패널에 액세스하기 위한 일반 단계 확인

1. 장치 연결 없이 라우터의 전원을 켭니다.
2. 모바일/랩톱을 라우터의 Wi-Fi에 연결하고 라우터 라벨에 인쇄된 Wi-Fi 키를 입력합니다.
3. 2단계가 실패하면 컴퓨터/랩톱에서 Wi-Fi를 끕니다. 대신 이더넷 케이블을 통해 라우터의 LAN 포트에 연결합니다.
4. 브라우저를 열고 주소 표시줄에 `192.168.8.1`을 입력하고 Enter를 클릭합니다. GL.iNet 웹 관리 패널에 액세스할 수 있어야 합니다.

또는 [앱](mobile_app.md)을 사용하여 라우터에 액세스할 수 있습니다.

## 이 문제를 해결하기 위한 기타 단계

1. [연결 확인](#check-the-connection)
2. [라우터 IP 주소 확인](#check-routers-ip-address)
3. [라우터 IP 주소에 액세스](#access-the-routers-ip-address)

---

### 연결 확인

이더넷 케이블로 연결한 경우 라우터의 WAN/LAN 포트 연결이 올바른지 확인하세요.

- WAN 포트는 모뎀 또는 기본 라우터와 같은 인터넷 소스에 연결됩니다.
- LAN 포트는 랩톱과 같은 터미널 장치에 연결됩니다.

Wi-Fi로 연결한 경우 장치에서 올바른 SSID를 선택하여 연결하고 올바른 비밀번호를 입력했는지 확인하세요.

### 라우터 IP 주소 확인

아래 단계에 따라 라우터의 IP 주소를 확인하세요.

=== "Windows 10 / Windows 11"

    Control Panel에 액세스하고 오른쪽 상단이 Large icons 또는 Small icons로 보기되어 있는지 확인하세요.

    ![control panel](https://static.gl.inet.com/docs/router/en/3/tutorials/cannot_access_web_panel/control_panel_view_by.png){class="glboxshadow"}

    Control Panel -> Network and Share Center -> 연결을 클릭하세요. 여러 연결이 있을 수 있으니 확인하려는 라우터의 해당 연결을 선택하세요.

    ![network and sharing center, connections](https://static.gl.inet.com/docs/router/en/3/tutorials/cannot_access_web_panel/network_and_sharing_center_connections.png){class="glboxshadow"}

    연결 상태 대화 상자가 팝업됩니다. 세부 정보 버튼을 클릭하세요.

    ![network and sharing center, connections status](https://static.gl.inet.com/docs/router/en/3/tutorials/cannot_access_web_panel/network_and_sharing_center_connections_status.png){class="glboxshadow"}

    네트워크 연결 세부 정보 대화 상자가 팝업됩니다. 라우터의 IP 주소는 **IPv4 Default Gateway**입니다.

    ![network and sharing center, connections status detail](https://static.gl.inet.com/docs/router/en/3/tutorials/cannot_access_web_panel/network_and_sharing_center_connections_status_detail.png){class="glboxshadow"}

=== "Windows 7"

    Control Panel -> Network and Internet -> Network and Sharing Center -> Change adapter settings

    네트워크 마우스 오른쪽 버튼 클릭 -> Status -> Details

    라우터의 IP 주소는 **IPv4 Default Gateway**입니다.

    ![property of network on windows 7](https://static.gl.inet.com/docs/router/en/3/tutorials/cannot_access_web_panel/property_of_network_win7.jpg){class="glboxshadow"}

=== "macOS"

    1. System Preferences -> Network

    2. 왼쪽 열에서 네트워크 연결을 클릭합니다. 이더넷 연결의 경우 라우터 IP 주소가 표시됩니다.

    ![router ip of ethernet on mac os](https://static.gl.inet.com/docs/router/en/3/tutorials/cannot_access_web_panel/router_ip_of_ethernet_on_mac_os.jpg){class="glboxshadow"}

    Wi-Fi 연결의 경우 "Advanced..." 버튼을 클릭한 후 창 상단의 "TCP/IP" 탭을 클릭합니다. 라우터 IP 주소가 표시됩니다.

    ![router ip of Wi-Fi on mac os](https://static.gl.inet.com/docs/router/en/3/tutorials/cannot_access_web_panel/router_ip_of_wifi_on_mac_os.jpg){class="glboxshadow"}

=== "iOS"

    1. Settings -> Wi-Fi
    2. 현재 연결된 Wi-Fi의 정보 아이콘(파란색 원형 i)을 탭합니다. 라우터 IP 주소가 표시됩니다.

    ![router ip address on iphone](https://static.gl.inet.com/docs/router/en/3/tutorials/cannot_access_web_panel/router_ip_address_on_iphone.jpg){class="glboxshadow"}

=== "Android"

    이것은 Android 장치마다 다를 수 있습니다.

    1. Settings -> Network & internet
    2. Wi-Fi를 탭하고 연결된 네트워크를 찾은 후 설정 아이콘을 클릭하여 설정을 관리합니다.
    3. Advanced 드롭다운을 탭합니다. Static 또는 Dynamic IP 옵션을 제공하는 경우 Static을 선택합니다.
    4. 어떤 경우든 Gateway 아래에서 라우터의 IP를 볼 수 있어야 합니다.

### 라우터 IP 주소에 액세스

1. 더 나은 호환성을 위해 Chrome/Edge/Safari를 사용하여 라우터의 관리 패널에 액세스하세요.

2. 브라우저 캐시 및 확장 프로그램으로 인한 문제를 피하기 위해 시크릿 창을 연 다음 라우터의 IP 주소에 다시 액세스해 보세요.

3. Tailscale 및 ZeroTier를 포함한 모든 VPN 또는 프록시 소프트웨어를 비활성화하세요.

4. 모바일 폰을 사용하는 경우 모바일 데이터를 끄세요.

    일부 스마트폰은 라우터에 인터넷이 없음을 감지하면 라우터의 Wi-Fi 연결을 끊고 대신 모바일 데이터를 사용합니다. 그러나 라우터 연결이 끊어지면 웹 관리 패널에 액세스할 수 없습니다.

5. 위 단계가 실패하면 [재설정](repair_network_or_reset_firmware.md#reset-to-factory)하여 라우터를 공장 기본값으로 초기화해 보세요.

6. 재설정으로도 해결되지 않으면 [U-Boot를 통해 벽돌 해제](debrick.md)를 시도하세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
