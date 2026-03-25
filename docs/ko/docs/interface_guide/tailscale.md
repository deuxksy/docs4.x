# Tailscale

Tailscale은 소유한 장치와 애플리케이션을 전 세계 어디서나 안전하고 간편하게 액세스할 수 있는 VPN 서비스입니다. Tailscale에 대한 자세한 정보는 [Tailscale 공식 웹사이트](https://tailscale.com/)를 방문하세요.

GL.iNet 라우터의 Tailscale 기능은 펌웨어 V4.2부터 사용할 수 있으며 라우터가 Tailscale 가상 네트워크에 연결할 수 있습니다. 연결되면 WAN 및 LAN 리소스를 포함하여 라우터를 원격으로 액세스할 수 있습니다.

**참고**:

1. Tailscale은 WireGuard를 기반으로 하므로 다음 기능이나 서비스와 동시에 사용하면 라우팅 충돌이 발생할 수 있으므로 권장하지 않습니다: OpenVPN Client, WireGuard Client, GoodCloud Site to Site, ZeroTier, AstroWarp.

2. 이 기능은 현재 베타이며 일부 버그가 있을 수 있습니다.

3. GL.iNet 라우터는 아직 **종료 노드로 사용할 수 없습니다**.

## 지원되는 모델

??? "지원되는 모델"
    - GL-E5800 (Mudi 7)
    - GL-MT5000 (Brume 3)
    - GL-MT3600BE (Beryl 7)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-BE3600 (Slate 7)
    - GL-X2000 (Spitz Plus)
    - GL-B3000 (Marble)
    - GL-MT6000 (Flint2)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-AX1800 (Flint)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-A1300 (Slate Plus)

??? "지원되지 않는 모델"
    - GL-SFT1200 (Opal)
    - GL-MT1300 (Beryl)
    - GL-E750/E750V2 (Mudi)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-AR750S (Slate)
    - GL-XE300 (Puli)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-AP1300 (Cirrus)
    - GL-S1300 (Convexa-S)
    - GL-X300B (Collie)

## Tailscale 네트워크 설정

다음은 GL-MT2500의 예입니다.

1. 장치 바인딩

    먼저 Tailscale 계정을 등록한 다음 테스트 목적으로 하나 또는 두 개의 장치(예: 스마트폰, 노트북)를 Tailscale 계정에 바인딩하세요.

    바인딩 후 Tailscale 관리 콘솔에서 장치와 상태를 볼 수 있습니다.

    ![tailscale admin console](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_admin_console_1.png){class="glboxshadow"}

2. GL.iNet 라우터에서 Tailscale 활성화

    라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **Tailscale**로 이동합니다.

    ![glinet tailscale disabled](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_disabled.png){class="glboxshadow"}

    토글을 전환하여 Tailscale를 활성화한 다음 **Apply**를 클릭하세요.

    ![glinet enable tailscale](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/enable_tailscale.png){class="glboxshadow"}

3. 잠시 후 인터페이스에 **장치 바인딩 링크**가 표시됩니다. 장치 바인딩 링크를 클릭하세요.

    ![glinet bind link](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_bind_link_1.png){class="glboxshadow"}

    팝업 창에 Tailscale 링크가 표시됩니다. 링크를 클릭하여 Tailscale 웹사이트로 리디렉션하고 로그인하세요.

    ![glinet bind link](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_bind_link_2.png){class="glboxshadow"}

    로그인하면 연결할 장치를 확인하라는 메시지가 표시됩니다. **Connect**를 클릭하세요.

    ![tailscale confirm connect device](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_connect_device.png){class="glboxshadow gl-70-desktop"}

    연결에 성공하면 Tailscale 관리 콘솔로 자동으로 리디렉션됩니다. GL-MT2500의 IP 주소가 `100.88.54.21`인 것을 볼 수 있습니다. 이제 이 IP를 사용하여 라우터에 액세스할 수 있습니다.

    ![tailscale admin console](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_admin_console_2.png){class="glboxshadow"}

3. 연결성 테스트

    동일한 Tailscale 네트워크에 연결된 장치에서 다음 세 가지 방법으로 연결성을 테스트할 수 있습니다.

    * ping 명령어 사용

        ![ping](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/ping.png){class="glboxshadow"}

    * 라우터에 SSH 접속

        ![ssh](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/ssh.png){class="glboxshadow"}

    * 웹 관리 패널 액세스

        ![web admin panel](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/web_admin_panel.png){class="glboxshadow gl-80-desktop"}

## 원격 액세스 WAN 허용

이 옵션을 활성화하면 장치의 WAN 측 리소스를 Tailscale 가상 네트워크를 통해 액세스할 수 있습니다.

예를 들어 아래 토폴로지와 같이 이 기능을 활성화하면 `leo-phone`에서 `GL-AXT1800`의 IP 주소(`192.168.29.1`)를 통해 액세스할 수 있습니다. 이는 GL-AXT1800가 `GL-MT2500`의 상위 장치이며 후자가 leo-phone과 동일한 Tailscale 네트워크에 연결되어 있기 때문입니다.

![tailscale, remote access wan topology](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_access_wan_topology.png){class="glboxshadow"}

작업 단계는 다음과 같습니다.

1. 라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **Tailscale**로 이동합니다.

    **Allow Remote Access WAN**을 활성화하고 **Apply**를 클릭하세요.

    ![enable allow remote access wan](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/enable_allow_remote_access_wan.png){class="glboxshadow"}

2. Tailscale 관리 콘솔로 이동하면 GL-MT2500에 서브넷이 있다는 알림이 표시됩니다.

    GL-MT2500 오른쪽의 점 3개 아이콘을 클릭하고 **Edit route settings**를 선택하세요.

    ![tailscale subnet alert](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_subnet_alert_wan.png){class="glboxshadow"}

3. 서브넷 경로를 활성화합니다.

    ![tailcale, enable subnet route](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_enable_subnet_routes.png){class="glboxshadow"}

4. 이제 다른 장치에서 GL-AXT1800의 IP 주소(`192.168.29.1`)를 통해 액세스할 수 있습니다. 실제로는 `192.168.29.0/24` 서브넷 내의 모든 장치에 액세스할 수 있습니다.

    ![tailscale, access axt1800](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_access_axt1800.jpg){class="glboxshadow gl-50-desktop"}

## 원격 액세스 LAN 허용

이 옵션을 활성화하면 장치의 LAN 측 리소스를 Tailscale 가상 네트워크를 통해 액세스할 수 있습니다.

예를 들어 아래 토폴로지와 같이 이 기능을 활성화하면 `leo-phone`에서 `Ubuntu`의 IP 주소(`192.168.8.110`)를 통해 SSH 로그인할 수 있습니다. 이는 `Ubuntu`가 `GL-MT2500`의 하위 장치이며 후자가 leo-phone과 동일한 Tailscale 네트워크에 연결되어 있기 때문입니다.

![tailscale, remote access lan topology](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_access_lan_topology.png){class="glboxshadow"}

작업 단계는 다음과 같습니다.

1. 라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **Tailscale**로 이동합니다.

    **Allow Remote Access LAN**을 활성화하고 **Apply**를 클릭하세요.

    ![enable remote access lan](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/enable_allow_remote_access_lan.png){class="glboxshadow"}

2. Tailscale 관리 콘솔로 이동하면 GL-MT2500에 서브넷이 있다는 알림이 표시됩니다.

    GL-MT2500 오른쪽의 점 3개 아이콘을 클릭하고 **Edit route settings**를 선택하세요.

    ![tailscale subnet alert](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_subnet_alert_lan.png){class="glboxshadow"}

3. 서브넷 경로를 활성화합니다.

    ![tailscale, enable subnet route](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_enable_subnet_routes_lan.png){class="glboxshadow"}

4. 이제 다른 장치에서 Ubuntu의 IP 주소(`192.168.8.110`)를 통해 ping하거나 SSH 로그인할 수 있습니다. 실제로는 `192.168.8.0/24` 서브넷 내의 모든 장치에 액세스할 수 있습니다.

    ![tailscale, access ubuntu](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/tailscale_access_ubuntu.png){class="glboxshadow gl-80-desktop"}

## 사용자 정의 종료 노드

종료 노드 기능을 사용하면 Tailscale가 아닌 모든 인터넷 트래픽을 네트워크의 특정 장치를 통해 라우팅할 수 있습니다. 트래픽을 라우팅하는 장치를 "종료 노드"라고 합니다.

![exitnode](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/custom_exit_nodes/exitnode.jpg){class="glboxshadow"}

**참고**: 라우터의 DNS 서버가 로컬 네트워크에서만 액세스할 수 있는 사설 IP 주소인 경우 종료 노드를 실행할 때 인터넷 액세스가 손실될 수 있습니다. 해결 방법으로 Network > DNS 메뉴로 이동하여 8.8.8.8과 같은 수동 공개 DNS 서버를 설정하세요.

설정 단계:

1. 종료 노드로 사용할 장치에서 **Run exit node**를 선택하세요. Windows에서는 다음 단계를 따르세요.

    ![tailscale windows, run exit node](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/custom_exit_nodes/tailscale_run_exit_node.png){class="glboxshadow"}

    **Yes**를 클릭하세요.

    ![tailscale windows, run exit ndoe alert](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/custom_exit_nodes/tailscale_run_exit_node_alert.png){class="glboxshadow"}

2. 관리 콘솔에서 장치를 종료 노드로 설정합니다.

    ![tailscale exit node alert](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/custom_exit_nodes/tailscale_exit_node_alert.png){class="glboxshadow"}

    ![tailscale use as exit node](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/custom_exit_nodes/tailscale_use_as_exit_node.png){class="glboxshadow"}

3. GL 라우터에서 **Custom Exit Nodes**를 활성화하고 새로고침 버튼을 클릭한 다음 드롭다운 메뉴에서 종료 노드로 설정된 장치의 IP를 선택하고 **Apply**를 클릭하세요. 이것으로 완료입니다.

    ![glinet tailscale, custom exit node](https://static.gl.inet.com/docs/router/en/4/tutorials/tailscale/custom_exit_nodes/custom_exit_node.png){class="glboxshadow"}

4. 해당 GL 라우터 아래의 장치들은 **종료 노드**의 홈 IP를 사용합니다.

[참조 링크: Exit Nodes (route all traffic)](https://tailscale.com/kb/1103/exit-nodes/)

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
