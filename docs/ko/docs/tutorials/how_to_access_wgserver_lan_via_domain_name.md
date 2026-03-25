# 도메인 이름을 통해 클라이언트에서 WireGuard 서버 LAN 기기에 접근하는 방법

이 튜토리얼은 클라이언트에서 도메인 이름을 사용하여 WireGuard 서버의 LAN에 있는 홈 기기(예: NAS, IP 카메라 등)에 접근하는 방법을 설명합니다.

## 토폴로지

아래와 같이 클라이언트 LAN의 PC에서 WireGuard 서버 LAN에 있는 NAS, IP 카메라 등의 기기에 각각의 도메인 이름을 사용하여 접근할 수 있습니다.

![topology](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/topology_be9300_be3600.png){class="glboxshadow"}

## 설정 단계

### 1. 서버에서 Hosts 편집 (선택 사항)

이 단계는 VPN 서버가 로컬 도메인 이름을 올바르게 확인할 수 없는 경우에 적용됩니다. 확실하지 않은 경우 이 단계를 건너뛰세요.

VPN 서버 라우터의 웹 관리 패널에 로그인하고 **NETWORK** -> **DNS** -> **Edit Hosts**로 이동합니다.

![edit hosts](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/edit_hosts.png){class="glboxshadow"}

접근하려는 홈 기기의 IP와 도메인 이름을 입력한 다음 **Apply**를 클릭합니다.

![input ip domain](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/input_ip_domain.png){class="glboxshadow gl-80-desktop"}

### 2. 서버에서 원격 LAN 접근 허용

??? "서버 라우터가 펌웨어 v4.8을 실행 중인 경우"

    서버의 웹 관리 패널에서 **VPN** -> **WireGuard Server**로 이동합니다. 오른쪽 상단의 **Options**를 클릭합니다.

    ![server options 4.8](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/server_options_4.8.png){class="glboxshadow gl-90-desktop"}

    **Allow Remote Access the LAN Subnet**을 활성화하고 **Apply**를 클릭합니다.

    ![server allow access lan 4.8](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/server-allow-access-lan-4.8.png){class="glboxshadow"}

    **활성화하면 이 라우터와 LAN 기기에 VPN을 통해 원격으로 접근할 수 있습니다.**

??? "서버 라우터가 펌웨어 v4.7 이전 버전을 실행 중인 경우"

    서버의 웹 관리 패널에서 **VPN** -> **VPN Dashboard** -> **VPN Server** 섹션으로 이동합니다. WireGuard 서버 오른쪽의 톱니바퀴 아이콘을 클릭합니다.

    ![server options 4.7](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/server_options_4.7.png){class="glboxshadow gl-90-desktop"}

    **Remote Access LAN**을 활성화하고 **Apply**를 클릭합니다.

    ![server allow access lan 4.7](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/server-allow-access-lan-4.7.png){class="glboxshadow"}

    **활성화하면 이 라우터와 LAN 기기에 VPN을 통해 원격으로 접근할 수 있습니다.**

### 3. VPN 설정 내보내기

서버의 관리 패널에서 **VPN** -> **WireGuard Server** -> **Profiles** 탭으로 이동하고 **Add**를 클릭하여 설정 프로필을 내보냅니다.

![export config](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/export_config.png){class="glboxshadow"}

아래와 같이 **.conf** 파일을 얻게 됩니다.

![downloads](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/downloads.png){class="glboxshadow"}

이 파일을 엽니다. 파일의 DNS 필드가 서버의 터널 IP를 가리키는지 확인합니다. 이 IP는 아래와 같이 WireGuard Server 페이지의 **Configuration** 탭 아래에 표시됩니다. 동시에 DNS 확인 실패를 방지하기 위해 DNS 필드에 "64.6.64.6"이 있는 경우 삭제합니다.

![dns field](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/dns_field.png){class="glboxshadow"}

![wg tunnel ip](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/wg_tunnel_ip.png){class="glboxshadow"}

**참고**: WireGuard 서버의 터널 IP는 펌웨어 버전에 따라 다릅니다. 서버의 터널 IP를 확인하세요.

### 4. VPN 서버 활성화

**WireGuard Server** 페이지에서 오른쪽 상단의 **Start** 버튼을 클릭하여 서버를 시작합니다.

![start server](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/start_server.png){class="glboxshadow"}

### 5. VPN 설정 업로드

VPN 클라이언트 라우터의 웹 관리 패널에 로그인하고 **VPN** -> **WireGuard Client**로 이동한 다음 **Add Manually**를 클릭합니다.

![add manually](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/wgclient_add_manually.png){class="glboxshadow"}

이 그룹의 이름을 만들고 설정 파일을 업로드합니다.

![add manually](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/wgclient_add_manually-2.png){class="glboxshadow"}

업로드가 완료되면 **Apply**를 클릭합니다.

![apply](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/wgclient_add_apply.png){class="glboxshadow"}

설정 파일이 여기에 표시됩니다.

![applied](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/wgclient_add_applied.png){class="glboxshadow"}

### 6. VPN 클라이언트 연결 시작

세 점 아이콘을 클릭하여 VPN 연결을 시작합니다.

![start client](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/start_client.png){class="glboxshadow"}

회색 점이 녹색으로 바뀌면 WireGuard 클라이언트가 서버에 성공적으로 연결된 것입니다.

![wgclient connected](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/wg_client_connected.png){class="glboxshadow"}

이제 클라이언트 LAN의 PC에서 도메인 이름을 사용하여 서버 LAN에 있는 홈 기기(예: NAS)에 접근할 수 있습니다.

![ping test](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/ping_nas.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
