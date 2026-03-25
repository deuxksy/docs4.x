# OpenVPN 서버에서 클라이언트 LAN 측 액세스하는 방법

이 튜토리얼에서는 OpenVPN 서버 측에서 OpenVPN 클라이언트의 LAN 서브넷(NAS, IP 카메라 등)에 액세스하는 단계를 소개합니다.

## 토폴로지

아래와 같이 GL-AXT1800은 OpenVPN 서버이고 GL-MT2500은 이에 연결된 OpenVPN 클라이언트입니다. 서버 측에서 GL-MT2500의 LAN 측 장치(NAS 또는 GL-MT3000 서브 라우터 등)에 액세스할 수 있습니다.

![topology](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/ovpnlantop.jpg){class="glboxshadow"}

## 1. 서버에 라우팅 규칙 추가

??? "펌웨어 v4.7 이하"

    <u>OpenVPN 서버</u>의 웹 관리 패널에 로그인하고 **VPN** -> **VPN Dashboard** -> **VPN Server**로 이동합니다.

    오른쪽의 경로 아이콘을 클릭하여 라우팅 규칙을 입력합니다.

    ![ovpnserver route rule](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.7-ovpn-route-rule-1.jpg){class="glboxshadow"}

    팝업 창에서 오른쪽의 **라우팅 규칙 추가** 버튼을 클릭하고 액세스하려는 서브넷을 입력합니다.

    ![ovpnserver route rule](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.7-ovpn-route-rule-2.png){class="glboxshadow"}

    예를 들어 OpenVPN 클라이언트 GL-MT2500의 LAN 서브넷은 **192.168.48.0/24**이므로 대상 주소는 **192.168.48.0/24**입니다.

    게이트웨이는 OpenVPN 서버가 이 OpenVPN 클라이언트에 대해 생성한 클라이언트 IP입니다. 여기서 게이트웨이를 **10.8.0.1**로 설정한 다음 **Apply**를 클릭합니다.

    ![ovpnserver route rule](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.7-ovpn-route-rule-3.jpg){class="glboxshadow"}

    참고: 여러 OpenVPN 클라이언트의 LAN 서브넷에 액세스해야 하는 경우 라우팅 규칙을 설정하기 전에 [이 링크](reserve_fixed_IP_for_ovpn_client.md)를 참조하여 각 OpenVPN 클라이언트에 대한 클라이언트 IP를 예약하세요.

??? "펌웨어 v4.8 이상"

    <u>OpenVPN 서버</u>의 웹 관리 패널에 로그인하고 **VPN** -> **OpenVPN Server**로 이동합니다.

    **라우팅 규칙** 탭을 클릭한 다음 오른쪽의 **라우팅 규칙 추가** 버튼을 클릭합니다.

    ![ovpnserver route rule](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.8-ovpn-route-rule-1.png){class="glboxshadow"}

    팝업 창에서 액세스하려는 서브넷을 입력합니다.

    ![ovpnserver route rule](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.8-ovpn-route-rule-2.png){class="glboxshadow"}

    예를 들어 OpenVPN 클라이언트 GL-MT2500의 LAN 서브넷은 **192.168.48.0/24**이므로 대상 주소는 **192.168.48.0/24**입니다.

    게이트웨이는 OpenVPN 서버가 이 OpenVPN 클라이언트에 대해 생성한 클라이언트 IP입니다. 여기서 게이트웨이를 **10.8.0.2**로 설정한 다음 **Apply**를 클릭합니다.

    ![ovpnserver route rule](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.8-ovpn-route-rule-3.jpg){class="glboxshadow"}

    참고: 여러 OpenVPN 클라이언트의 LAN 서브넷에 액세스해야 하는 경우 라우팅 규칙을 설정하기 전에 [이 링크](reserve_fixed_IP_for_ovpn_client.md)를 참조하여 각 OpenVPN 클라이언트에 대한 클라이언트 IP를 예약하세요.

## 2. 클라이언트 LAN에 대한 원격 액세스 허용

??? "펌웨어 v4.7 이하"

    <u>OpenVPN 클라이언트</u>의 웹 관리 패널에 로그인하고 **VPN** -> **VPN Dashboard** -> **VPN Client**로 이동합니다.

    기어 아이콘을 클릭하여 클라이언트 옵션을 입력합니다.

    ![ovpnclient options](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.7-client-options.png){class="glboxshadow"}

    팝업 창에서 **Remote Access LAN**을 활성화한 다음 **Apply**를 클릭합니다.

    ![allow remote access lan](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.7-allow-remote-access-lan.jpg){class="glboxshadow"}

??? "펌웨어 v4.8 이상"

    <u>OpenVPN 클라이언트</u>의 웹 관리 패널에 로그인하고 **VPN** -> **VPN Dashboard**로 이동합니다.

    VPN 터널의 왼쪽 상단 모서리에서 기어 아이콘을 클릭하여 터널 옵션을 입력합니다.

    ![ovpnclient options](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.8-client-tunnel-options.png){class="glboxshadow"}

    팝업 창에서 **Allow Remote Access the LAN Subnet**을 활성화한 다음 **Apply**를 클릭합니다.

    ![allow remote access lan](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/4.8-allow-remote-access-lan.png){class="glboxshadow"}

## 3. 연결 테스트

다음은 IP **192.168.48.211**을 사용하는 GL-MT3000(OpenVPN 클라이언트 LAN의 장치)에 액세스하는 예입니다.

OpenVPN 서버에 연결된 장치에서 GL-MT3000의 IP 주소 **192.168.48.211**을 ping합니다. 이는 OpenVPN 클라이언트(GL-MT2500)가 자신의 LAN에서 GL-MT3000에 할당한 IP 주소입니다.

ping에 성공하면 설정이 올바른 것입니다. OpenVPN 클라이언트 LAN 서브넷 내의 다른 모든 장치에 IP 주소를 통해 액세스할 수 있습니다.

![ping test](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_server-access_client_lan_side/ping-test.jpg){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
