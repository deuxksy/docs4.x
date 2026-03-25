# 도메인 이름을 통해 클라이언트에서 OpenVPN 서버 LAN 기기에 접근하는 방법

이 튜토리얼은 클라이언트에서 도메인 이름을 사용하여 OpenVPN 서버의 LAN에 있는 홈 기기(예: NAS, IP 카메라 등)에 접근하는 방법을 설명합니다.

## 토폴로지

아래와 같이 클라이언트 LAN의 PC에서 OpenVPN 서버 LAN에 있는 NAS, IP 카메라 등의 기기에 각각의 도메인 이름을 사용하여 접근할 수 있습니다.

![topology](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/topology_be9300_be3600.png){class="glboxshadow"}

## 설정 단계

### 1. 서버에서 Hosts 편집 (선택 사항)

이 단계는 VPN 서버가 로컬 도메인 이름을 올바르게 확인할 수 없는 경우에 적용됩니다. 확실하지 않은 경우 이 단계를 건너뛰세요.

VPN 서버 라우터의 웹 관리 패널에 로그인하고 **NETWORK** -> **DNS** -> **Edit Hosts**로 이동합니다.

![edit hosts](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/edit_hosts.png){class="glboxshadow"}

접근하려는 홈 기기의 IP와 도메인 이름을 입력한 다음 **Apply**를 클릭합니다.

![input ip domain](https://static.gl-inet.com/docs/router/en/4/tutorials/access_server_lan_via_domain_names/input_ip_domain.png){class="glboxshadow gl-80-desktop"}

### 2. 서버에서 원격 LAN 접근 허용

서버의 웹 관리 패널에서 **VPN** -> **OpenVPN Server**로 이동합니다. 오른쪽 상단의 **Options**를 클릭합니다.

![ovpnserver options 4.8](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnserver_options.png){class="glboxshadow"}

**Allow Remote Access the LAN Subnet**을 활성화하고 **Apply**를 클릭합니다.

![ovpnserver allow access lan 4.8](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/allow_remote_access_lan.png){class="glboxshadow"}

활성화하면 VPN을 통해 라우터와 LAN 기기에 원격으로 접근할 수 있습니다.

### 3. VPN 설정 내보내기

서버의 관리 패널에서 **VPN** -> **OpenVPN Server** -> **Configuration** 탭으로 이동하고 하단의 **Export Client Configuration**을 클릭합니다.

![export config](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/export1.png){class="glboxshadow"}

팝업 창에서 **Export**를 클릭합니다.

**참고**: 서버의 공인 IP 주소가 동적이고 자주 변경되는 경우 클라이언트 설정을 내보내기 전에 **APPLICATIONS** -> **Dynamic DNS**로 이동하여 **DDNS**를 활성화하세요.

![export config](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/export2.png){class="glboxshadow"}

아래와 같이 **.ovpn** 파일을 얻게 됩니다.

![downloads](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/download.png){class="glboxshadow"}

서버 라우터가 펌웨어 v4.8 이상을 실행 중인 경우 설정 파일을 편집할 필요가 없으며 다음 단계로 진행하세요.

서버 라우터가 펌웨어 v4.7 이전 버전을 실행 중인 경우 이 파일을 열고 다음 줄을 추가하여 DNS 서버를 OpenVPN 서버의 터널 IP로 설정한 다음 변경 사항을 저장합니다.

`dns server 1 address 10.8.0.1`

![edit config](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/edit_config.png){class="glboxshadow"}

팁: OpenVPN 서버의 터널 IPv4 서브넷은 아래와 같이 OpenVPN Server 페이지의 **Configuration** 탭에서 찾을 수 있습니다. 펌웨어 버전에 따라 다릅니다. OpenVPN 서버의 터널 IP를 확인하세요.

![ovpnserver tunnel ip](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnserver_tunnel_ip.png){class="glboxshadow"}

### 4. VPN 서버 활성화

**OpenVPN Server** 페이지에서 오른쪽 상단의 **Start** 버튼을 클릭하여 서버를 시작합니다.

![start server](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnserver_start.png){class="glboxshadow"}

### 5. VPN 설정 업로드

VPN 클라이언트 라우터의 웹 관리 패널에 로그인하고 **VPN** -> **OpenVPN Client**로 이동한 다음 **Add Manually**를 클릭합니다.

![add manually](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnclient_upload1.png){class="glboxshadow"}

이 그룹의 이름을 만들고 설정 파일을 업로드합니다.

![add manually](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnclient_upload2.png){class="glboxshadow"}

업로드가 완료되면 **Apply**를 클릭합니다.

![apply](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnclient_upload3.png){class="glboxshadow"}

설정 파일이 여기에 표시됩니다.

![applied](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnclient_upload4.png){class="glboxshadow"}

### 6. VPN 클라이언트 연결 시작

세 점 아이콘을 클릭하여 VPN 연결을 시작합니다.

![start client](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnclient_start.png){class="glboxshadow"}

회색 점이 녹색으로 바뀌면 OpenVPN 클라이언트가 서버에 성공적으로 연결된 것입니다.

![ovpnclient connected](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ovpnclient_connected.png){class="glboxshadow"}

이제 클라이언트 LAN의 PC에서 도메인 이름을 사용하여 서버 LAN에 있는 홈 기기(예: NAS)에 접근할 수 있습니다.

![ping test](https://static.gl-inet.com/docs/router/en/4/tutorials/access_ovpnserver_lan_via_domain_names/ping_test.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
