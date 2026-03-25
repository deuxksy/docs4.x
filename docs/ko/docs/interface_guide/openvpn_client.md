# GL.iNet 라우터에서 OpenVPN 클라이언트 설정

OpenVPN은 가상 사설망 기술을 사용하여 보안 사이트 간 또는 지점 간 연결을 설정하는 오픈 소스 VPN 프로토콜입니다.

GL.iNet 라우터에 OpenVPN 클라이언트를 설정하려면 이 동영상을 보시거나 아래 단계를 참조하십시오.

<iframe width="560" height="315" src="https://www.youtube.com/embed/04sW3l6_rDM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

시작하기 전에 OpenVPN 수동 구성을 지원하는 VPN 서비스 제공업체와 활성 구독이 있는지 확인하십시오. GL.iNet과 호환되는 OpenVPN 제공업체를 보려면 [여기](https://www.gl-inet.com/solutions/vpn/){target="_blank"}를 클릭하십시오.

일반적으로 먼저 구독한 VPN 서비스 제공업체의 공식 웹사이트를 방문하여 구성 파일을 가져온 다음 라우터에 업로드하여 OpenVPN 클라이언트로 설정해야 합니다. 구성 파일을 가져오는 방법을 모르는 경우 [이 링크](#openvpn-service-providers에서-구성-파일-가져오기)를 참조하거나 지원팀에 문의하십시오.

웹 관리 패널 또는 [모바일 앱](../faq/mobile_app.md)을 통해 OpenVPN 클라이언트를 설정할 수 있습니다. 다음은 웹 관리 패널을 통해 설정하는 단계입니다.

---

웹 관리 패널에서 **VPN** -> **OpenVPN Client**로 이동합니다.

NordVPN 구독이 있는 경우 **NordVPN**을 클릭하여 로그인합니다. 그렇지 않은 경우 **Add Manually**를 클릭하여 OpenVPN 구성 파일을 업로드합니다.

![openvpn client](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_client/openvpn_client_initial.png){class="glboxshadow"}

## NordVPN 설정 {#set-up-nordvpn}

[NordVPN](https://go.nordvpn.net/aff_c?offer_id=15&amp;aff_id=12016&amp;url_id=902){target="_blank"}은 속도와 보안을 위한 인기 있는 온라인 VPN 서비스입니다.

NordVPN 빠른 설정은 GL.iNet 라우터의 관리 패널에 통합되어 있습니다. 라우터의 웹 관리 패널 또는 모바일 앱에서 계정 자격 증명(NordVPN 대시보드에서 가져옴)을 입력하여 모든 NordVPN 서버에 대한 구성 파일을 온라인으로 가져올 수 있으므로 수동 파일 업로드가 필요 없습니다.

1. [여기](https://my.nordaccount.com/){target="_blank"}에서 NordVPN 웹 계정에 로그인합니다.

    ![nord login](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_client/nord_login.png){class="glboxshadow"}

    로그인 후 Nord 대시보드에서 **NordVPN**을 클릭한 다음 **Set up NordVPN manually**를 클릭합니다.

    ![nord dashboard](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_client/nord_dashboard.png){class="glboxshadow"}

    ![nord setup manually](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_client/nord_setup_manually.png){class="glboxshadow"}

    **서비스 자격 증명**을 찾을 수 있습니다. 나중에 사용할 수 있도록 복사합니다.

    ![nordvpn service credential](https://static.gl-inet.com/docs/router/en/4/tutorials/openvpn_client/nord_service_credentials.jpg){class="glboxshadow"}

2. 라우터의 웹 관리 패널에 로그인하고 VPN -> OpenVPN Client -> NordVPN으로 이동합니다. 1단계에서 얻은 **서비스 자격 증명**을 입력합니다(참고: 로그인 계정 이메일/비밀번호가 **아닙니다**). 그런 다음 **Save and Continue**를 클릭합니다.

    ![input nordvpn service credentials](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn1.png){class="glboxshadow"}

3. 프로토콜, 각 위치의 최대 서버 수 및 위치를 선택한 다음 **Apply**를 클릭합니다.

    ![select nordvpn servers](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn2.png){class="glboxshadow"}

    구성 파일을 다운로드합니다.

    ![nordvpn configuration files](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn3.png){class="glboxshadow"}

4. 연결을 시작합니다.

    원하는 서버를 선택하고 오른쪽의 세 점 아이콘을 클릭하여 연결을 시작합니다.

    ![nordvpn start connect](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn4.png){class="glboxshadow"}

5. 연결되면 구성 파일 옆에 녹색 점이 나타납니다.

    ![nordvpn connected](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn5.png){class="glboxshadow"}

    그리고 VPN 연결 세부 정보가 **VPN Dashboard**에 표시됩니다.

    ![vpn dashboard nordvpn connected](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn6.png){class="glboxshadow"}

6. 서버 업데이트.

    **Update Servers**를 클릭하여 최신 사용 가능한 서버 목록을 가져와 서버 유지 관리 또는 종료로 인한 연결 실패를 방지할 수 있습니다.

    ![nordvpn update servers](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn7.png){class="glboxshadow"}

7. 자격 증명 편집.

    기어 아이콘을 클릭하여 로그인 자격 증명을 편집합니다.

    ![nordvpn edit credentials](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn8.png){class="glboxshadow"}

8. 모든 파일 삭제.

    **Delete All**을 클릭하여 모든 구성 파일을 한 번에 삭제할 수 있습니다.

    ![nordvpn delete all](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nordvpn9.png){class="glboxshadow"}

## OpenVPN 클라이언트 수동 설정(다른 제공업체)

OpenVPN 서비스 제공업체가 우리 관리 패널에 통합되어 있지 않은 경우 먼저 구독한 서비스 제공업체의 공식 웹사이트를 방문하여 구성 파일을 가져오십시오. 다음으로 라우터에 업로드하여 OpenVPN 클라이언트를 설정합니다.

다음 단계에서는 [PIA (Private Internet Access)](https://privateinternetaccess.com/offer/GLiNET_71dx4t8bl){target="_blank"}를 예로 사용합니다.

1. Private Internet Access 공식 웹사이트에서 구성 파일을 다운로드합니다.

2. 라우터의 웹 관리 패널에 로그인하고 VPN -> OpenVPN Client로 이동한 다음 **Add Manually**를 클릭합니다.

    ![add manually](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/manual1.png){class="glboxshadow"}

3. 왼쪽 사이드바에 그룹이 만들어집니다.

    ![add a new group](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/manual2.png){class="glboxshadow"}

4. 그룹의 설명이 되는 이름을 설정합니다(예: private internet access).

    ![set the new group name](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/manual3.png){class="glboxshadow"}

5. OpenVPN 구성 파일을 업로드합니다. 필요한 경우 자격 증명을 입력한 다음 **Apply**를 클릭합니다.

    ![manual upload files](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/manual4.png){class="glboxshadow"}

    - 인증에 4가지 유형의 자격 증명이 있습니다:

        1. 인증 없음.

        2. 사용자 이름 및 비밀번호만.

        3. 암호만.

        4. 사용자 이름, 비밀번호 및 암호.

    그러면 업로드된 구성 파일이 표시됩니다.

    ![manual upload files](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/manual5.png){class="glboxshadow"}

6. 오른쪽의 세 점 아이콘을 클릭하여 연결을 시작합니다.

    ![start connect](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/manual6.png){class="glboxshadow"}

7. 연결되면 구성 파일 옆에 녹색 점이 나타납니다.

    ![openvpn connected](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/manual7.png){class="glboxshadow"}

    그리고 VPN 연결 세부 정보가 **VPN Dashboard**에 표시됩니다.

    ![vpn dashboard openvpn status](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/manual8.png){class="glboxshadow"}

## GL.iNet 라우터에서 OpenVPN 서버 설정

GL.iNet 라우터가 두 대 있는 경우 하나를 OpenVPN 서버(공용 IP 필요)로, 다른 하나를 OpenVPN 클라이언트로 설정할 수 있습니다. 이렇게 하면 타사 VPN 서비스를 구독하지 않고 자체 VPN 연결을 설정할 수 있습니다.

OpenVPN 서버 설정은 [여기](openvpn_server.md)를 확인하십시오.

## OpenVPN 서비스 제공업체에서 구성 파일 가져오기 {#openvpn-service-providers에서-구성-파일-가져오기}

30개 이상의 OpenVPN 서비스 제공업체를 테스트하고 구성 파일을 가져오는 단계를 문서화했습니다. 구성 파일을 가져오는 방법을 잘 모르는 경우 아래 단계를 참조하십시오.

구독한 서비스 제공업체가 아래에 나열되어 있지 않은 경우 지원팀에 추가 지원을 문의하십시오.

??? "NordVPN"
    ### NordVPN

    [공식 웹사이트](https://go.nordvpn.net/aff_c?offer_id=15&amp;aff_id=12016&amp;url_id=902){target="_blank"}

    1. **NordVPN 계정에 로그인**

        [공식 웹사이트](https://go.nordvpn.net/aff_c?offer_id=15&amp;aff_id=12016&amp;url_id=902){target="_blank"}에 로그인하고 Nord 계정 대시보드로 이동하여 서비스 자격 증명을 찾습니다.

        ![nordvpn login](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nord_login.png){class="glboxshadow"}

        Nord 대시보드에 로그인한 후 왼쪽에서 NordVPN을 클릭한 다음 **Set up NordVPN manually**를 클릭합니다.

        ![nordvpn dashboard](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nord_dashboard.png){class="glboxshadow"}

        ![nordvpn setup manually](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nord_setup_manually.png){class="glboxshadow"}

        **Service credentials**를 찾습니다. 구성 업로드에 사용해야 할 수 있으므로 복사합니다.

        ![nordvpn service credential](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nord_service_credentials.jpg){class="glboxshadow"}

    2. **NordVPN 서버를 선택하고 구성 파일 다운로드**

        **Server recommendation** 탭으로 이동합니다. 네트워크를 기반으로 서버를 추천하고 다운로드할 수 있는 사용 가능한 프로토콜을 제공합니다. 계속하려면 **Get setup configuration**을 클릭합니다.

        ![nordvpn config download](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nord_config_download.png){class="glboxshadow"}

        팝업 창에서 **OpenVPN** 프로토콜을 선택하고 UDP 또는 TCP 구성을 다운로드합니다.

        ![nordvpn select protocol](https://static.gl.inet.com/docs/router/en/4/tutorials/openvpn_client/nord_select_protocol.png){class="glboxshadow"}

    [여기](https://downloads.nordcdn.com/configs/archives/servers/ovpn.zip)에서 모든 서버 구성을 다운로드할 수 있습니다.

    팁: zip 파일이 너무 커서 업로드할 수 없는 경우 .zip 파일에서 일부 .ovpn을 삭제하거나 단일 .ovpn 파일을 업로드하십시오.

    [참조 링크](https://support.nordvpn.com/Connectivity/Router/1047409122/GL-iNet-setup-with-NordVPN.htm){target="_blank"}

    [모바일 앱](../faq/mobile_app.md)을 사용하여 NordVPN을 설정할 수도 있습니다.

??? "AirVPN"
    ### AirVPN

    [공식 웹사이트](https://airvpn.org/?referred_by=402389){target="_blank"}

    1. AirVPN 계정에 로그인

        ![airvpn client detail](https://static.gl-inet.com/docs/router/en/3/tutorials/openvpn_client/airvpn/airvpn1.png){class="glboxshadow"}

    2. 왼쪽에서 Config Generator를 선택한 다음 운영 체제로 Linux를 선택합니다. 다음으로 원하는 서버를 선택합니다.

        ![openvpn config generator](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/airvpn/airvpn2.png){class="glboxshadow"}

    3. 구성 파일의 다운로드 페이지를 볼 수 있습니다.

        ![download config](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/airvpn/airvpn3.png){class="glboxshadow"}

??? "Astrill"
    ### Astrill

    [공식 웹사이트](https://www.astrill.com/a/dik2masnw6ig){target="_blank"}

    [Astrill 공식 지침](https://wiki.astrill.com/Astrill_Setup_Manual:How_to_configure_OpenVPN_with_OpenVPN_application_on_Windows){target="_blank"}에서 인용한 정보

    1. Astrill Openvpn 구성 ZIP 생성 및 다운로드

        ![astrill vpn tools](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/astrillvpn/astrill1.png){class="glboxshadow"}

        ![create new certificate](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/astrillvpn/astrill2.png){class="glboxshadow"}

    2. OPENVPN_GUI와 같은 설명을 입력합니다.

    3. ADD to my certificates 버튼을 클릭합니다.

        ![create new certificate](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/astrillvpn/astrill3.png){class="glboxshadow"}

    4. OpenVPN 인증서가 추가되면 다운로드 버튼을 클릭합니다.

        ![download certificate](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/astrillvpn/astrill4.png){class="glboxshadow"}

??? "BolehVPN"
    ### BolehVPN

    [공식 웹사이트](https://www.bolehvpn.net/){target="_blank"}

    [대시보드](https://users.bolehvpn.net/){target="_blank"}에 로그인하고 구성 파일을 다운로드한 다음 [Linux_iOS inline](https://users.bolehvpn.net/download/inline/6){target="_blank"} 형식을 선택합니다. 다운로드가 완료된 후 zip 파일을 압축 해제합니다.

    팁: zip 파일이 너무 커서 업로드할 수 없는 경우 .zip 파일에서 일부 .ovpn을 삭제하거나 단일 .ovpn 파일을 업로드하십시오.

    [참조 링크](https://www.bolehvpn.net/clients-installations/#1487691248224-0c435dba-d612){target="_blank"}

??? "CactusVPN"
    ### CactusVPN

    [공식 웹사이트](https://billing.cactusvpn.com/aff.php?aff=2310){target="_blank"}

    [다운로드](https://www.cactusvpn.com/downloads/){target="_blank"} 페이지에서 직접 다운로드하십시오.

    ![download cactusvpn openvpn profiles](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/cactusvpn/cactusvpn1.jpg){class="glboxshadow"}

??? "Cryptostorm"
    ### Cryptostorm

    [공식 웹사이트](https://cryptostorm.is/){target="_blank"}

    [여기](https://cryptostorm.is/configs/ecc/){target="_blank"}에서 직접 다운로드하십시오.

??? "CyberGhost"
    ### CyberGhost

    [공식 웹사이트](https://www.cyberghostvpn.com/offer/GLiNet_rem6fdij){target="_blank"}

    [CyberGhost 공식 지침](https://support.cyberghostvpn.com/hc/en-us/articles/213811885-Router-How-to-configure-OpenVPN-for-flashed-DD-WRT-routers){target="_blank"}에서 인용한 정보

    1. CyberGhost VPN 온라인 계정에 로그인합니다.

        ![login](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/cyberghost/cyberghost1.png){class="glboxshadow"}

    2. 왼쪽 메뉴에서 "**VPN**"을 선택한 다음 "**Configure Device**"를 클릭하고 아래와 같이 서버 구성을 만듭니다:

        ![config device](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/cyberghost/cyberghost2.jpg){class="glboxshadow"}

        ![save config](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/cyberghost/cyberghost3.jpg){class="glboxshadow"}

    3. 이제 다음과 같이 서버 구성을 만듭니다:

        * **프로토콜** : **OpenVPN**
        * **국가** : 기본 프로토콜 연결은 정확히 하나의 서버에서만 사용할 수 있으므로 이제 탐색하려는 국가를 선택해야 합니다. 이 국가에서 사용할 서버는 CyberGhost가 자동으로 선택합니다.
        * **서버 그룹** : 사용하려는 서버 그룹과 OpenVPN 프로토콜(UDP 또는 TCP)을 선택합니다

        **OpenVPN UDP**는 TCP 버전보다 더 높은 속도를 허용하지만 경우에 따라 다운로드가 중단될 수 있습니다. 이것이 기본 설정입니다.

        **OpenVPN TCP**는 UDP 버전보다 더 안정적인 연결을 허용하지만 약간 느립니다. 갑작스러운 연결 끊김과 같은 반복적인 연결 문제가 있는 경우 이 버전을 선택하십시오.

        원하는 매개 변수를 선택한 후 **Save Configuration**으로 저장합니다

    4. 구성 대시보드에서 생성된 **OpenVPN** 자격 증명을 보려면 **View Configuration**을 누릅니다.

        ![view configuration](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/cyberghost/cyberghost4.png){class="glboxshadow"}

    5. 연결 기본 설정을 완료한 후 다음 사항을 참고하십시오:

        * **Server Group** : 연결하려는 국가(서버)의 주소입니다(예: '12345-1-ca.cg-dialup.net'). 이 주소는 이전 단계에서 선택한 모든 국가마다 변경됩니다. 사용할 실제 단일 서버는 CyberGhost가 자동으로 선택합니다.
        * **Username** : 이 프로토콜용으로만 생성된 사용자 이름입니다. 이것은 일반 CyberGhost 계정 사용자 이름이 아닙니다. 수동 구성을 통해 CyberGhost 서버에 인증하는 데만 사용됩니다. GL.iNet 라우터에서 OpenVPN을 설정할 때 필요합니다.
        * **Password** : 프로토콜 사용만 위해 생성된 비밀번호입니다. 이것은 일반 CyberGhost 계정 비밀번호가 아닙니다. 수동 구성을 통해 CyberGhost 서버에 인증하는 데만 사용됩니다. GL.iNet 라우터에서 OpenVPN을 설정할 때 필요합니다.

        완료되면 구성 파일을 다운로드하십시오. 이렇게 하려면 *Download Configuration*을 클릭하고 구성 파일을 컴퓨터에 다운로드합니다

        ![save config](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/cyberghost/cyberghost5.png){class="glboxshadow"}

??? "ExpressVPN"
    ### ExpressVPN

    [공식 웹사이트](https://go.expressvpn.com/c/4130682/1645813/16063){target="_blank"}

    [Expressvpn 공식 지침](https://www.expressvpn.com/support/vpn-setup/manual-config-for-linux-with-openvpn/#download){rel="sponsored" target="_blank"}에서 인용한 정보

    1. [ExpressVPN](https://go.expressvpn.com/c/4130682/1645813/16063){rel="sponsored" target="_blank"} 웹사이트로 이동하여 ExpressVPN 자격 증명으로 로그인합니다.

        ![expressvpn account click sign in](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/expressvpn/expressvpn-account-click-sign-in.jpg){target="_blank"}

        이메일로 전송된 **확인 코드**를 입력합니다.

    2. "Set up your devices" 섹션에서 **More**를 클릭합니다.

        ![expressvpn, set up your devices, more](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/expressvpn/set_up_your_devices_more.png){class="glboxshadow"}

    3.  **Manual Configuration**을 클릭합니다.

        ![expressvpn, set up your devices, manual configuration](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/expressvpn/set_up_your_devices_manual_configuration.png){class="glboxshadow"}

    4.  **사용자 이름**, **비밀번호** 및 **OpenVPN 구성 파일** 목록을 볼 수 있습니다.

        ![expressvpn, setup info](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/expressvpn/setup_info.png){class="glboxshadow"}

        원하는 위치를 클릭하여 .ovpn 파일을 다운로드합니다.

        나중에 설정에 필요하므로 이 브라우저 창을 **열어 두십시오**.

    [참조 링크](https://www.expressvpn.com/support/vpn-setup/manual-config-for-linux-with-openvpn/#download){rel="sponsored" target="_blank"}

??? "FastestVPN"
    ### FastestVPN

    [공식 웹사이트](https://go.fastestvpn.com/affiliate/pap?a_aid=5ffd2a3e9d687){target="_blank"}

    [여기](https://support.fastestvpn.com/download/fastestvpn_ovpn/)에서 OpenVPN TCP 및 UDP용 FastestVPN 구성 파일 zip 폴더를 다운로드하십시오

    팁: zip 파일이 너무 커서 업로드할 수 없는 경우 .zip 폴더에서 일부 .ovpn 파일을 삭제하거나 단일 .ovpn 파일을 업로드하십시오.

    [참조 링크](https://support.fastestvpn.com/tutorials/routers/gl-inet/openvpn){target="_blank"}

??? "FinchVPN"
    ### FinchVPN

    [공식 웹사이트](https://www.finchvpn.com/){target="_blank"}

    1. FinchVPN 계정에 로그인합니다.

        ![finchvpn login](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/finchvpn/finchvpn1.jpg){class="glboxshadow"}

    2. 다운로드 페이지로 이동하여 FinchVPN OpenVPN Config 아래에서 다운로드를 클릭합니다.

        ![finchvpn download page](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/finchvpn/finchvpn2.jpg){class="glboxshadow"}

    3. Linux를 선택합니다

        ![finchvpn](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/finchvpn/finchvpn3.jpg){class="glboxshadow"}

    4. 기본 설정에 따라 프로토콜을 선택합니다. 일반적으로 첫 번째 **Port 8484 over UDP**를 선택할 수 있습니다

        ![finchvpn](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/finchvpn/finchvpn4.jpg){class="glboxshadow"}

    5. 파일을 다운로드하기 전에 사용자 이름과 비밀번호를 포함하도록 확인란을 선택하는 것을 기억하십시오.

        ![finchvpn](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/finchvpn/finchvpn5.jpg){class="glboxshadow"}

??? "HideIPVPN"
    ### HideIPVPN

    [공식 웹사이트](https://www.hideipvpn.com/){target="_blank"}

    1. HideIPVPN 계정에 로그인합니다.

    2. 왼쪽에서 Package를 클릭하고 패키지를 클릭하여 활성 상태인지 확인합니다.

        ![hideipvpn client area](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/hideipvpn/package.jpg){class="glboxshadow"}

    3. VPN 탭에는 사용자 이름과 비밀번호의 VPN 로그인 세부 정보가 있습니다. 이것은 OpenVPN 연결 시 로그인에 사용됩니다

        ![hideipvpn client area](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/hideipvpn/vpn_username_password.jpg){class="glboxshadow"}

    4. 아래로 스크롤하여 OpenVPN 구성 파일을 다운로드합니다.

        ![hideipvpn client area](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/hideipvpn/openvpn_config_files.jpg){class="glboxshadow"}

??? "Hide.me VPN"
    ### Hide.me VPN

    [공식 웹사이트](https://hide.me/?friend=glinet){target="_blank"}

    1. Hide.me 계정에 로그인하고 왼쪽에서 Server Locations를 찾습니다.

    2. Windows용 OpenVPN 구성을 다운로드합니다.

        ![hide.me vpn dashboard](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/hideme/hideme_dashboard.jpg){class="glboxshadow"}

??? "Hotspot Shield"
    ### Hotspot Shield

    [공식 웹사이트](https://trk.aclktrkr.com/aff_c?offer_id=59&aff_id=3722){target="_blank"}

    **참고: Hotspot Shield 라우터 구성 파일은 더 이상 사용할 수 없거나 지원되지 않습니다. 다음 단계는 여전히 파일을 설치한 사용자를 위해 레거시 목적으로 제공됩니다.**

    1. [https://www.hotspotshield.com/](https://www.hotspotshield.com/)로 이동하여 Account를 클릭합니다. 메시지가 표시되면 로그인합니다.

        ![hotspot shield login](https://static.gl.inet.com/docs/router/en/4/interface_guide/openvpn_client/hotspot_shield/hotspotshield_front_page.png){class="glboxshadow"}

    2. [https://app.hotspotshield.com/app/hotspotshield/router](https://app.hotspotshield.com/app/hotspotshield/router)로 이동합니다

        Select location 드롭다운으로 이동하여 라우터가 사용할 가상 위치를 선택합니다. 이제 "Download file"를 클릭합니다. 구성 파일(config.ovpn)이 컴퓨터에 다운로드됩니다. 라우터에서 OpenVPN 클라이언트를 설정할 때 사용자 이름과 비밀번호를 입력해야 합니다.

        ![hotspot shield link router](https://static.gl.inet.com/docs/router/en/4/interface_guide/openvpn_client/hotspot_shield/link_router.png){class="glboxshadow"}

    [참조 링크](https://support.hotspotshield.com/hc/en-us/articles/360038538012-How-do-I-install-Hotspot-Shield-on-my-GL-iNet-router)

??? "IPVANISH"
    ### IPVANISH

    [공식 웹사이트](https://affiliate.ipvanish.com/aff_c?offer_id=1&aff_id=3073){target="_blank"}

    - [여기](https://configs.ipvanish.com/configs/configs.zip)에서 모든 서버의 모든 구성 파일을 다운로드할 수 있습니다. 모든 서버 구성 파일(.ovpn)과 인증서 파일(.crt)이 포함되어 있습니다. .zip 파일은 일부 모델에서 약간 클 수 있으므로 사용하지 않을 서버의 구성(.ovpn)을 삭제하십시오.

        ![ipvanish all openvpn configs](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/ipvanish/ipvanish_all_openvpn_configs.png){class="glboxshadow"}

    - [여기](https://www.ipvanish.com/software/configs/)에서 개별 서버 구성 파일을 다운로드할 수도 있지만 **ca.ipvanish.com.crt**도 다운로드해야 합니다. 라우터에 업로드하기 전에 **ca.ipvanish.com.crt**와 .ovpn 구성 파일을 .zip 아카이브로 압축해야 합니다.

        ![ipvanish openvpn config file with certificate file](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/ipvanish/ipvanish_openvpn_config_file_with_certificate_file.png){class="glboxshadow"}

    [참조 링크](https://support.ipvanish.com/hc/en-us/articles/360001329813-Android-OpenVPN-Setup)

??? "IVACY"
    ### IVACY

    [공식 웹사이트](https://billing.ivacy.com/page/22852){target="_blank"}

    Ivacy를 사용하여 OpenVPN 클라이언트를 설정하려면 다음이 필요합니다:

    - "Download Configuration" 프롬프트에 표시된 OpenVPN 수동 구성용 사용자 이름
     ![ivacy openvpn username](https://static.gl-inet.com/docs/router/en/4/interface_guide/openvpn_client/ivacy-username.png){class="glboxshadow"}
    - 비밀번호(Ivacy 계정에 로그인할 때 사용한 비밀번호와 동일)
    - OpenVPN 구성 파일

    [참조 링크](https://support.ivacy.com/setup_guide/how-to-setup-ivacy-on-gl-inet-router/)

??? "IVPN"
    ### IVPN

    [공식 웹사이트](https://www.ivpn.net/){target="_blank"}

    1. [OpenVPN 구성 파일](https://www.ivpn.net/releases/config/ivpn-openvpn-config.zip)을 다운로드합니다.

    2. [IVPN Client Area](https://www.ivpn.net/clientarea/login){target="_blank"}에서 계정 ID를 찾습니다.

    3. 구성 파일을 새 OpenVPN 구성으로 끌어 놓으면 사용자 이름과 비밀번호를 입력하라는 메시지가 표시됩니다. 사용자 이름은 **ivpn** 문자로 시작하는 계정 ID입니다. 비밀번호는 **ivpn**과 같이 모든 것이 될 수 있습니다

        ![ivpn set up on gl.inet router](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/ivpn/ivpn_set_up_openvpn_client.png){class="glboxshadow"}

    [참조 링크](https://www.ivpn.net/setup/gnu-linux-terminal.html)

??? "Mullvad"
    ### Mullvad

    [공식 웹사이트](https://mullvad.net/en){target="_blank"}

    1. [Mullvad](https://mullvad.net/en){rel="sponsored" target="_blank"} 웹사이트로 이동하여 Mullvad 자격 증명으로 로그인합니다.

    2. OpenVPN Configuration을 선택합니다

    ![ovpnconfig](https://static.gl.inet.com/docs/router/en/4/interface_guide/openvpn_client/ovpnconfig.jpg){class="glboxshadow"}

    3. **Linux**를 선택하고 서버 위치를 선택합니다

        ![linux](https://static.gl.inet.com/docs/router/en/4/interface_guide/openvpn_client/linux.jpg){class="glboxshadow"}

??? "OVPN"
    ### OVPN

    [공식 웹사이트](https://www.ovpn.com/en?ref=glinet){target="_blank"}

    로그인만 하면 아래 메뉴를 클릭하여 쉽게 OpenVPN 구성 파일을 가져올 수 있습니다.

    ![get ovpn configuration files](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/ovpn/get_ovpn_configuration_files.jpg){class="glboxshadow"}

    서버를 선택하고 다운로드합니다.

    ![download ovpn openvpn configuration files](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/ovpn/download_configuration_files.jpg){class="glboxshadow"}

    사용자 이름과 비밀번호는 OVPN에 로그인할 때와 동일합니다.

??? "OysterVPN"
    ### OysterVPN

    [공식 웹사이트](https://go.oystervpn.net?a_aid=glinet){target="_blank"}

    1. [OysterVPN 서버 목록 페이지](https://support.oystervpn.com/server-list/){target="_blank"}에 액세스하여 **Download .ovpn file**을 클릭하여 구성 파일을 다운로드합니다.

        ![download oystervpn .ovpn file](https://static.gl.inet.com/docs/router/en/4/interface_guide/openvpn_client/oystervpn/download_ovpn_file.png){class="glboxshadow"}

    2. OpenVPN 연결용 사용자 이름과 비밀번호는 OysterVPN에 로그인할 때 사용하는 것과 동일합니다.

    팁: zip 파일이 너무 커서 업로드할 수 없는 경우 .zip 파일에서 일부 .ovpn을 삭제하거나 단일 .ovpn 파일을 업로드하십시오.

??? "PIA (Private Internet Access)"
    ### PIA

    [공식 웹사이트](https://privateinternetaccess.com/offer/GLiNET_71dx4t8bl){target="_blank"}

    [여기](https://www.privateinternetaccess.com/openvpn/openvpn.zip)에서 직접 다운로드하십시오.

    팁: zip 파일이 너무 커서 업로드할 수 없는 경우 .zip 파일에서 일부 .ovpn을 삭제하거나 단일 .ovpn 파일을 업로드하십시오.

??? "PrivadoVPN"
    ### PrivadoVPN

    [공식 웹사이트](https://privadovpn.com/#a_aid=GLINET){target="_blank"}

    로그인만 하면 **Download VPN Configuration**을 쉽게 찾을 수 있습니다.

    ![PrivadoVPN OpenVPN configuration](https://static.gl-inet.com/docs/router/en/3/tutorials/openvpn_client/privadovpn/privadovpn_openvpn_configuration.png){class="glboxshadow"}

    팁: zip 파일이 너무 커서 업로드할 수 없는 경우 .zip 파일에서 일부 .ovpn을 삭제하거나 단일 .ovpn 파일을 업로드하십시오.

??? "PrivateVPN"
    ### PrivateVPN

    [공식 웹사이트](https://affiliate.privatevpn.com/scripts/click.php?a_aid=5e3a511658bc3){target="_blank"}

    [여기](https://static.gl-inet.com/docs/router/en/3/tutorials/openvpn_client/privatevpn/PrivateVPN-TUN.zip){target="_blank"}에서 직접 다운로드하십시오.

    [여기](https://privatevpn.com/client/PrivateVPN-TUN.zip)가 공식 다운로드 링크입니다. 라우터로 가져오는 동안 발생한 버그로 인해 내부의 파일 이름에 'Bogotá' 특수 문자가 포함되어 있습니다. 우리는 이것의 이름을 변경하고 위에서 다운로드 링크를 제공했습니다. 우리는 향후 버전에서 이 버그를 수정할 것입니다.

    팁: zip 파일이 너무 커서 업로드할 수 없는 경우 .zip 파일에서 일부 .ovpn을 삭제하거나 단일 .ovpn 파일을 업로드하십시오.

??? "Proton VPN"
    ### Proton VPN

    [공식 웹사이트](https://go.getproton.me/aff_c?offer_id=26&aff_id=1612){target="_blank"}

    **Proton VPN은 WireGuard 서비스를 제공하므로 WireGuard 사용을 권장합니다. [여기](wireguard_client.md#wireguard-providers)**를 확인하십시오.

    1. [Proton VPN](https://go.getproton.me/aff_c?offer_id=26&aff_id=1612){target="_blank"} 계정에 로그인합니다.

    2. 왼쪽에서 **Download**를 클릭합니다.

    3. 라우터 플랫폼, 프로토콜 등을 선택하고 대상 국가를 찾아 구성 파일을 다운로드합니다.

        ![protonvpn openvpn configuration file](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/protonvpn/proton_openvpn_configuration_file.jpg){class="glboxshadow"}

    4. OpenVPN 연결용 자격 증명은 Proton 웹사이트 대시보드에 로그인하는 자격 증명이 아닙니다. **Account -> OpenVPN/IKEv2 username**에서 자격 증명을 찾을 수 있습니다

        ![protonvpn openvpn credential](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/protonvpn/protonvpn_openvpn_credential.jpg){class="glboxshadow"}

??? "PureVPN"
    ### PureVPN

    [공식 웹사이트](https://billing.purevpn.com/aff.php?aff=35535){target="_blank"}

    PureVPN을 사용하여 OpenVPN 클라이언트를 설정하려면 OpenVPN 사용자 이름과 비밀번호 및 PureVPN 계정에서 찾을 수 있는 구성 파일이 필요합니다.

    1. [PureVPN 계정에 로그인합니다.](https://my.purevpn.com/)
    2. 왼쪽 사이드바에서 **Subscriptions**를 클릭합니다.
    3. 아래로 스크롤하여 OpenVPN 사용자 이름과 비밀번호를 찾습니다.
        ![purevpn username and password](https://static.gl.inet.com/docs/router/en/4/interface_guide/openvpn_client/purevpn-vpn-username-vpn-password.png){class="glboxshadow"}
    4. 왼쪽 사이드바에서 **Manual Configuration**을 클릭합니다.
    5. VPN 위치를 선택하고 **Download**를 클릭하여 구성 파일을 다운로드합니다.

    [참조 링크](https://support.purevpn.com/openvpn-files)

    GL.iNet 라우터는 PPTP가 필요하므로 PureVPN의 [전용 IP](https://www.purevpn.com/dedicated-ip){target="_blank"} 기능을 지원하지 않습니다.

??? "SaferVPN"
    ### SaferVPN

    [공식 웹사이트](https://safervpn.com/?a_aid=563){target="_blank"}

    [여기](https://support.safervpn.com/hc/en-us/articles/360035425314-What-are-SaferVPN-s-OpenVPN-configuration-ovpn-files-for-manual-setup)에서 직접 다운로드하십시오.

    ![safervpn openvpn config](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/safervpn/safervpn1.png){class="glboxshadow"}

??? "StarVPN"
    ### StarVPN

    [공식 웹사이트](https://www.starvpn.com/dashboard/aff.php?aff=91){target="_blank"}

    StarVPN은 WireGuard 서비스를 제공하므로 WireGuard 사용을 권장합니다. [여기](wireguard_client.md#starvpn)를 확인하십시오.

    1. **StarVPN으로 계정 등록**

        [가격 정책](https://www.starvpn.com/#pricing){target="_blank"} 옵션으로 이동하여 필요에 맞는 VPN 요금제를 선택합니다. 결제 시 등록하거나 [여기](https://www.starvpn.com/dashboard/register.php){target="_blank"}에서 직접 등록할 수 있습니다

    2. VPN 로그인 정보

        [대시보드](https://www.starvpn.com/dashboard){target="_blank"}에 StarVPN 회원 영역으로 로그인합니다. Manage Slots 섹션 또는 대시보드 영역에서 각 슬롯의 VPN 사용자 이름과 비밀번호를 찾을 수 있습니다.

        ![starvpn credential](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/starvpn/vpn-username_edited-2.jpg){class="glboxshadow"}

        여러 슬롯의 경우 VPN 구성 설정 및 자격 증명은 "Manage Slots" 섹션에 위치할 수 있습니다.

        ![starvpn credential](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/starvpn/vpn-username_slots_edited-1024x355.jpeg){class="glboxshadow"}

    3. OpenVPN 구성 파일 다운로드

        다음 단계에서는 OpenVPN 소프트웨어가 연결할 위치를 알 수 있도록 필요한 VPN 서버 구성 파일을 다운로드해야 합니다. 회원 영역 대시보드에서 구성 파일을 다운로드합니다.

        ![download starvpn config](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/starvpn/download-ovpn_edited.jpg){class="glboxshadow"}

        일부 GL.iNet 라우터는 IPv6 또는 DNS 누수 방지를 지원하지 않으므로 IP 또는 연결 오류가 발생할 수 있습니다. ovpn 구성 파일을 편집하고 다음 간단한 작업을 수행하여 IPv6를 비활성화합니다.

        ![troubleshooting](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/starvpn/troubleshooting.jpg){class="glboxshadow"}

??? "StreamVPN"
    ### StreamVPN

    [공식 웹사이트](https://billing.streamvpn.com/account/signup?aff_t=aaf341756f7b94ed3f040f78292b80f1db1adf3318eacb87dd9c4ad4e08fde11a%3A2%3A%7Bs%3A6%3A%22aff_id%22%3Bs%3A6%3A%22645311%22%3Bs%3A6%3A%22off_id%22%3Bi%3A10%3B%7D){target="_blank"}

    1. [StreamVPN](https://billing.streamvpn.com/account/signup?aff_t=aaf341756f7b94ed3f040f78292b80f1db1adf3318eacb87dd9c4ad4e08fde11a%3A2%3A%7Bs%3A6%3A%22aff_id%22%3Bs%3A6%3A%22645311%22%3Bs%3A6%3A%22off_id%22%3Bi%3A10%3B%7D){target="_blank"} 계정으로 로그인하면 구독 정보를 볼 수 있습니다. **Install & Guides**를 클릭합니다.

        ![streamvpn subscription info](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/streamvpn/streamvpn_subscription.png){class="glboxshadow"}

    2. **VPN Router**를 클릭하면 `StreamVPN.zip`이라는 .zip 아카이브 파일이 다운로드됩니다.

        ![streamvpn guide, vpn router](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/streamvpn/streamvpn_guide_router.png){class="glboxshadow"}

        **참고:** 구성 파일 이름에 "Primary"가 포함된 것만 작동합니다.

??? "StrongVPN"
    ### StrongVPN

    [공식 웹사이트](https://strongvpn.com/?tr_aid=5ac44bd241ca7){target="_blank"}

    1. [StrongVPN](https://strongvpn.com/?tr_aid=5ac44bd241ca7){target="_blank"} 계정으로 로그인하면 VPN Accounts Summary를 볼 수 있습니다. **Account Setup Instructions**를 클릭합니다.

        ![strongvpn setup 1](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/strongvpn/strong_vpn_setup_01.jpg){class="glboxshadow"}

    2. Manual setup 섹션을 찾고 단계를 따라 구성을 가져옵니다.

        ![strongvpn get config](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/strongvpn/strong_vpn_setup_02.jpg){class="glboxshadow"}

??? "Surfshark"
    ### Surfshark

    [공식 웹사이트](https://get.surfshark.net/aff_c?offer_id=926&aff_id=1400){target="_blank"}

    1. **로그인 세부 정보 찾기**

        Surfshark 서비스 자격 증명은 Surfshark 계정 자격 증명(이메일 주소 및 비밀번호)과 다릅니다. 라우터에서 수동 OpenVPN 구성 방법을 사용하여 VPN에 연결하려면 Surfshark 서비스 자격 증명이 필요합니다.

        [공식 웹사이트](https://get.surfshark.net/aff_c?offer_id=926&aff_id=1400){target="_blank"}에 로그인하고 [이 페이지](https://my.surfshark.com/vpn/manual-setup/router){target="_blank"}로 이동하여 수동 연결에 필요한 모든 세부 정보를 찾습니다.

        ![surfshark service credential](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/surfshark/surfshark_service_credential.png){class="glboxshadow"}

    2. **Surfshark 서버 선택**

        **Locations** 탭을 선택하면 모든 Surfshark 서버가 표시됩니다.

        ![surfshark locations](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/surfshark/surfshark_locations.png){class="glboxshadow"}

        TCP 또는 UDP를 선택하라는 메시지가 표시됩니다. 차이점을 보려면 [여기](../faq/openvpn_tcp_udp.md)를 클릭하십시오.

        ![surfshark tcp udp](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/surfshark/surfshark_udp_tcp.png){class="glboxshadow" width="400"}

    [여기](https://api.surfshark.com/v1/server/configurations)에서 모든 구성을 직접 다운로드할 수 있습니다.

    팁: zip 파일이 너무 커서 업로드할 수 없는 경우 .zip 파일에서 일부 .ovpn을 삭제하거나 단일 .ovpn 파일을 업로드하십시오.

    [참조 링크](https://support.surfshark.com/hc/en-us/articles/360011856259-How-to-set-up-Surfshark-on-GL-iNet-router-3-x-firmware-){target="_blank"}

??? "VPN.AC"
    ### VPN.AC

    [공식 웹사이트](https://vpn.ac/aff.php?aff=1424){target="_blank"}

    [여기](https://vpn.ac/ovpn/)에서 다운로드하십시오.

    <img class="glboxshadow" alt="vpn.ac donwoad configuration" src="https://static.gl-inet.com/docs/router/en/3/tutorials/openvpn_client/vpn.ac/vpn.ac1.png" />

??? "VPNGate"
    ### VPNGate

    [공식 웹사이트](https://www.vpngate.net/en/){target="_blank"}

    OpenVPN 구성 파일은 [VPN Gate 웹사이트](https://www.vpngate.net/en/)에 서버 위치별로 나열되어 있습니다.

    1. **OpenVPN** 열 아래에서 OpenVPN Config 파일을 클릭합니다.

        ![VPNGate server list](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/vpngate/vpngate1.png){class="glboxshadow"}

    2. 다운로드 페이지가 표시됩니다.

        ![VPNGate download page](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/vpngate/vpngate2.png){class="glboxshadow"}

??? "VPN Unlimited(KeepSolid)"
    ### VPN Unlimited(KeepSolid)

    [공식 웹사이트](https://keepsolid.g2afse.com/click?pid=270&offer_id=7){target="_blank"}

    [VPN unlimited 공식 지침](https://www.vpnunlimitedapp.com/en/info/manuals/how-to-manually-create-vpn-conf){target="_blank"}에서 인용한 정보

    사용자 오피스에 로그인하여 시작하고 VPN Unlimited 서비스에 대해 Manage를 누른 다음 몇 가지 간단한 단계를 따르십시오:

    1. 장치 선택

        목록에서 장치를 선택하거나 새 장치를 만듭니다. 무료 슬롯이 없는 경우 오래된 장치를 삭제하거나 추가 슬롯을 구매하십시오.

        ![vpn unlimited openvpn config](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/vpnunlimited/keepsolid1.png){class="glboxshadow"}

    2. 원하는 서버 위치 선택

        VPN Unlimited은 70개 이상의 위치에서 400개 이상의 서버를 제공합니다. 이 경우 독일로 하겠습니다.

    3. VPN 프로토콜 선택

        OpenVPN 프로토콜을 선택합니다.

        ![vpn unlimited select protocol](https://static.gl-inet.com/docs/router/en/3/tutorials/openvpn_client/vpnunlimited/keepsolid2.png){class="glboxshadow"}

    4. 구성 생성

        Generate를 누르면 VPN 연결을 설정하는 데 필요한 모든 데이터를 얻을 수 있습니다.

        ![vpn unlimited generate configuration](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/vpnunlimited/keepsolid3.png){class="glboxshadow"}

??? "VyprVPN"
    ### VyprVPN

    VyprVPN는 여기서 OpenVPN 파일을 제공합니다: [Where can I find the OpenVPN files? – VyprVPN Support](https://support.vyprvpn.com/hc/en-us/articles/360038096131-Where-can-I-find-the-OpenVPN-files-){target="_blank"}

    제공된 zip 파일에는 .ovpn 파일이 있는 두 개의 폴더가 포함되어 있습니다. 하나는 OpenVPN160 다른 하나는 OpenVPN256입니다. zip 파일에서 OpenVPN160 폴더를 삭제한 다음 평소대로 GL.iNet 라우터에 업로드하십시오.

??? "Windscribe"
    ### Windscribe

    [공식 웹사이트](https://windscribe.com/yo/1u2h9ndl){target="_blank"}

    1. [여기](https://windscribe.com/login?auth_required){target="_blank"}에서 Windscribe 회원 계정에 로그인한 다음 [OpenVPN Config Generator](https://windscribe.com/getconfig/openvpn){target="_blank"}에 액세스합니다.

    2. 사용하려는 서버 위치, 프로토콜(UDP/TCP), 포트(예: 1194) 및 OpenVPN 버전(가급 최신 버전)을 선택한 다음 **Download Config**를 클릭합니다. 그러면 접미사 ".ovpn"이 있는 파일이 로컬 장치에 다운로드됩니다.

        ![windscribe OpenVPN Config Generator](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/windscribe/ovpn-config-generator.png){class="glboxshadow"}

    3. 동일 페이지에서 **Get Credentials** 버튼을 클릭합니다. 그러면 나중에 구성 파일을 라우터에 업로드할 때 라우터의 웹 관리 패널에서 인증에 사용할 해당 자격 증명을 받게 됩니다. 자격 증명을 복사하거나 이 웹페이지를 열어두십시오.

    4. 그런 다음 [이 가이드](../interface_guide/openvpn_client.md#set-up-openvpn-client-manually-for-other-providers)를 따라 계속합니다.

??? "ZoogVPN"
    ### ZoogVPN

    [공식 웹사이트](https://zoogvpn.com/pricing?ref=xrsyzx){target="_blank"}

    [공식 웹사이트](https://zoogvpn.com/pricing?ref=xrsyzx){target="_blank"}에 로그인한 다음 [OpenVPN 구성 파일 페이지](https://app.zoogvpn.com/setup/configuration-files){target="_blank"}에 액세스하여 여기에서 모든 서버를 찾을 수 있습니다. TCP 열 또는 UDP 열에서 구성 파일을 다운로드합니다.

    ![zoogvpn openvpn configuration files](https://static.gl.inet.com/docs/router/en/3/tutorials/openvpn_client/zoogvpn/zoogvpn_openvpn_config_files.png)

    그런 다음 [GL.iNet 라우터에서 OpenVPN 클라이언트 설정 가이드](#setup-openvpn-client)를 따르십시오. 사용자 이름과 비밀번호는 ZoogVPN 웹사이트에 로그인할 때 사용하는 것과 동일합니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 연락하세요.
