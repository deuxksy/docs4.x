# VPN 클라이언트가 활성화된 경우 WAN 접근을 허용하는 방법

GL.iNet 라우터에서 VPN 클라이언트가 활성화된 경우, 기본 글로벌 모드에서는 DNS 유출을 방지하기 위해 LAN의 모든 트래픽이 상위 네트워크(WAN)가 아닌 VPN 터널을 통해 라우팅되므로 LAN 기기에서 로컬 WAN 기기나 서비스에 접근할 수 없습니다.

이 튜토리얼에서는 VPN 클라이언트의 LAN 기기에서 로컬 WAN 서비스(예: 프린터, NAS 등)에 접근할 수 있도록 하는 단계를 소개합니다.

![allow acdess wan diagram](https://static.gl-inet.com/docs/router/en/4/tutorials/vpn_dashboard/allow_access_wan_diagram.jpg){class="glboxshadow gl-90-desktop"}

## 펌웨어 v4.7 이전 버전의 경우

VPN 클라이언트의 웹 관리 패널에 로그인하고 **VPN** -> **VPN Dashboard** -> **VPN Client**로 이동합니다. 오른쪽 상단의 **Global Options**를 클릭합니다.

![global options](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/4.7-global-options.png){class="glboxshadow"}

**Allow Access WAN**을 활성화하고 **Apply**를 클릭합니다.

![allow access](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/4.7-allow-access-wan.png){class="glboxshadow"}

이 옵션이 활성화되면 VPN이 연결된 동안에도 클라이언트 기기는 상위 서브넷의 WAN 서비스(예: 프린터, NAS 등)에 계속 접근할 수 있습니다.

## 펌웨어 v4.8 이상의 경우

**Allow Access WAN** 옵션은 펌웨어 v4.8의 VPN Dashboard에서 제거되었습니다. 하지만 VPN 정책을 통해 로컬 WAN 접근을 구현할 수 있습니다.

아래 단계를 따르세요.

1. VPN 클라이언트의 웹 관리 패널에 로그인하고 **VPN** -> **VPN Dashboard**로 이동합니다.

    오른쪽 상단의 모드를 클릭합니다.

    ![switch mode](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/switch-mode-1.png){class="glboxshadow"}

    **Policy Mode**로 전환하고 **Apply**를 클릭합니다.

    ![switch mode](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/switch-mode-2.png){class="glboxshadow"}

    페이지가 새로고침되고 아래와 같이 표시됩니다.

    ![policy mode](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/primary-tunnel.png){class="glboxshadow"}

2. 가운데 상자를 클릭하여 터널 대상을 설정합니다.

    ![tunnel target](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/select-target.png){class="glboxshadow"}

    **Exclude Specified Domain / IP**를 선택하고 라우터의 WAN 서브넷을 입력한 다음 **Apply**를 클릭합니다.

    이렇게 하면 WAN 서브넷으로 가는 모든 트래픽이 VPN 터널이 아닌 로컬 WAN을 통해 라우팅됩니다.

    ![exclude target](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/exclude-target.png){class="glboxshadow"}

    여기서는 서브넷 192.168.0.1/24를 예로 들었습니다. 이 서브넷을 입력하고 적용하면 VPN 터널이 아래와 같이 표시됩니다.

    ![exclude target apply](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/target-apply.png){class="glboxshadow"}

    ??? "GL.iNet 라우터의 WAN 서브넷을 어떻게 알 수 있나요?"

        GL.iNet 라우터의 WAN 서브넷은 일반적으로 INTERNET 페이지에서 찾을 수 있습니다. 이는 라우터의 WAN 인터페이스가 연결된 상위 기기(예: ISP 모뎀 또는 상위 게이트웨이)에 의해 결정됩니다.

        예를 들어, 라우터가 보조 라우터로 작동하는 경우(WAN 포트가 ISP 모뎀이나 메인 라우터의 LAN 포트와 같은 다른 로컬 네트워크에 연결됨) 라우터의 WAN IP가 192.168.1.165, 게이트웨이가 192.168.1.1, 서브넷 마스크가 255.255.255.0(소규모 네트워크의 일반적인 마스크)이라면 해당 WAN 서브넷은 192.168.1.0/24입니다. 이는 상위 기기의 LAN 서브넷이기도 합니다.

        ![check wan subnet](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/local-wan-details.png){class="glboxshadow gl-80-desktop"}

        **참고**: 192.168.1.0/24의 접두사 길이는 24이며 서브넷 마스크 255.255.255.0에 해당합니다. 라우터의 WAN 서브넷 마스크가 255.255.255.0이 아니라면 WAN 서브넷의 접두사 길이는 "/24"가 아닙니다. 실제 WAN 설정에 따라 WAN 서브넷을 확인하세요.

3. 오른쪽 상자를 클릭하여 터널 동작(VPN 사용 또는 미사용)을 설정합니다.

    ![exclude target](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/select-config-1.png){class="glboxshadow"}

    **Use VPN**을 선택하고 VPN 설정 파일을 선택합니다. 그런 다음 **Apply**를 클릭합니다.

    사용 가능한 설정이 없는 경우 먼저 설정을 업로드하여 라우터를 VPN 클라이언트로 설정합니다. 그런 다음 이 페이지로 돌아와 Use VPN을 선택하고 VPN 설정 파일을 선택합니다. 그런 다음 Apply를 클릭합니다.

    ![exclude target](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/select-config-2.jpg){class="glboxshadow"}

4. 오른쪽 상단의 스위치를 토글하여 이 VPN 터널을 활성화합니다. 연결이 시작됩니다.

    ![enable vpn](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/enable_vpn.png){class="glboxshadow"}

    몇 분 정도 기다립니다. 연결이 성공하면 녹색으로 바뀝니다.

    ![vpn connected](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/vpn_connected.png){class="glboxshadow"}

    공인 IP를 검색하여 VPN 연결을 테스트합니다. 예를 들어 브라우저를 열고 [whatismyip](https://whatismyipaddress.com/){target="_blank"}를 방문합니다. 아래와 같이 공인 IP 주소와 위치가 표시됩니다.

    ![vpn test](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/ipcheck.png){class="glboxshadow"}

5. WAN 서브넷의 기기나 서비스에 접근하여 성공적으로 접근할 수 있는지 확인합니다.

    ping 명령을 사용하여 연결을 테스트할 수 있습니다.

    ![ping test](https://static.gl-inet.com/docs/router/en/4/tutorials/allow_access_to_vpn_server_wan/ping-test.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
