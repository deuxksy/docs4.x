# WireGuard 서비스 제공업체에서 구성 파일 가져오기

??? "AzireVPN"
    ### AzireVPN

    [공식 웹사이트](https://www.azirevpn.com/aff/9x7wisg4){target="_blank"}

    1. [AzireVPN 공식 웹사이트](https://www.azirevpn.com/aff/9x7wisg4){target="_blank"}에 접속하여 로그인한 후 [WireGuard Configuration generator](https://www.azirevpn.com/cfg/wireguard){target="_blank"}에 접속하세요

        ![azirevpn wireguard configuration generator](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/azirevpn/azirevpn_wireguard_generator.png){class="glboxshadow"}

    2. IP 옵션에서 **IPv4**를 선택합니다. 그런 다음 **Download Configuration**을 클릭합니다.

        ![azirevpn wireguard configuration generator](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/azirevpn/azirevpn_wireguard_generator_ip.png){class="glboxshadow"}

    3. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-azirevpn)를 따라 계속하세요.

    4. [모바일 앱](../faq/mobile_app.md)을 사용하여 AzireVPN을 설정할 수도 있습니다.

??? "Hide.me VPN"
    ### Hide.me VPN

    [공식 웹사이트](https://hide.me/?friend=glinet){target="_blank"}

    Hide.me VPN은 GL.iNet 라우터에서 자신들의 WireGuard 서비스를 사용하는 간단한 방법을 제공합니다.

    1. 라우터에 [SSH](https://docs.gl-inet.com/router/en/3/tutorials/ssh/){target="_blank"}로 접속하세요.

    2. 아래 설치 URL을 복사한 후 터미널에 붙여넣고 Enter 키를 누르세요. (마우스 오른쪽 버튼을 클릭하면 붙여넣기 됩니다.)

        `curl -fsSL https://raw.githubusercontent.com/eventure/hide.client.routers/master/glinet_v4/hidemevpn | sh -s install`

    3. 설치가 시작되면 사용자 이름과 비밀번호를 묻습니다. 비밀번호를 입력하거나 붙여넣을 때 터미널에는 변경 사항이 표시되지 않으므로 입력 후 Enter 키를 누르세요.

    4. 완료되면 웹 관리 패널로 이동하면 hide.me VPN 그룹이 생성되었고 구성 파일이 이미 포함되어 있는 것을 볼 수 있습니다. 다른 구성 파일과 마찬가지로 연결하면 됩니다.

    **참고**: Hide.me VPN 구성 파일의 키는 연결하기 전에 다시 생성되며 연결 해제 후 유효하지 않으므로 이 구성 파일을 다른 장치에 복사해도 연결되지 않습니다.

    [참조 링크](https://github.com/eventure/hide.client.routers){target="_blank"}

??? "Mullvad"
    ### Mullvad

    [공식 웹사이트](https://mullvad.net/){target="_blank"}

    1. [Mullvad 공식 웹사이트](https://mullvad.net/){target="_blank"}에 접속하여 로그인한 후 [WireGuard configuration file generator](https://mullvad.net/en/account/#/wireguard-config){target="_blank"}에 접속하세요

    2. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md/#set-up-mullvad)를 따라 계속하세요.

    3. [모바일 앱](../faq/mobile_app.md)을 사용하여 Mullvad를 설정할 수도 있습니다.

??? "PIA (Private Internet Access)"
    ### PIA (Private Internet Access)

    [공식 웹사이트](https://privateinternetaccess.com/offer/GLiNET_71dx4t8bl){target="_blank"}

    웹사이트에서 WireGuard 구성을 다운로드할 수 없으므로 [모바일 앱](../faq/mobile_app.md)을 사용하여 PIA VPN을 설정하세요.

    <iframe width="560" height="315" src="https://www.youtube.com/embed/Fc7NTdQ9QFo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

??? "Surfshark"
    ### Surfshark

    [공식 웹사이트](https://get.surfshark.net/aff_c?offer_id=926&aff_id=1400){target="_blank"}

    1. [Surfshark](https://get.surfshark.net/aff_c?offer_id=926&aff_id=1400){target="_blank"}를 사용하는 경우 로그인한 후 [이 페이지](https://my.surfshark.com/vpn/manual-setup/router){target="_blank"}로 이동하여 **Router**를 클릭하고 **WireGuard**를 선택하세요.

        ![surfshark wireguard manual setup](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/surfshark/surfshark_wireguard_manual_setup_1.png){class="glboxshadow"}

    2. 다음 창에서 **I don't have a key pair**를 선택하세요.

        ![surfshark wireguard manual setup](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/surfshark/surfshark_wireguard_manual_setup_2.png){class="glboxshadow"}

    3. **Generate a new key pair**를 선택하세요.

        ![surfshark wireguard manual setup](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/surfshark/surfshark_wireguard_manual_setup_3.png){class="glboxshadow"}

    4. 키가 생성되면 **Choose a location**를 선택하세요.

        ![surfshark wireguard manual setup](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/surfshark/surfshark_wireguard_manual_setup_4.png){class="glboxshadow"}

    5. 마지막으로 설정하려는 위치를 선택하고 위치 옆의 **download** 버튼을 누르세요. 구성 파일을 다운로드할 수 있습니다.

        ![surfshark wireguard manual setup](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/surfshark/surfshark_wireguard_manual_setup_5.png){class="glboxshadow"}

    6. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-surfshark)를 따라 계속하세요.

    [참조 링크](https://support.surfshark.com/hc/en-us/articles/6585805139474-How-to-set-up-a-manual-WireGuard-connection-on-Android-){target="_blank"}

??? "AirVPN"
    ### AirVPN

    [공식 웹사이트](https://airvpn.org/?referred_by=402389){target="_blank"}

    1. [AirVPN](https://airvpn.org/?referred_by=402389){target="_blank"}을 사용하는 경우 웹사이트에 로그인한 후 [Client Area](https://airvpn.org/client/){target="_blank"}로 이동하여 [Config Generator](https://airvpn.org/generator/){target="_blank"}를 클릭하세요

        ![airvpn configuration generator](https://static.gl.inet.com/docs/router/en/4/tutorials/get_wg_configs/airvpn/airvpn_config_generator.png){class="glboxshadow" width="400"}

    2. Config Generator 페이지에서 Protocols 섹터에서 WireGuard를 선택하세요.

        ![airvpn protocols](https://static.gl.inet.com/docs/router/en/4/tutorials/get_wg_configs/airvpn/airvpn_protocols.png){class="glboxshadow" width="600"}

    3. 서버를 선택한 후 맨 아래로 스크롤하고 **Generate** 버튼을 클릭하세요. 구성 파일이 다운로드됩니다.

        ![airvpn select server](https://static.gl.inet.com/docs/router/en/4/tutorials/get_wg_configs/airvpn/airvpn_select_server.png){class="glboxshadow" width="600"}

    4. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "Astrill"
    ### Astrill

    [공식 웹사이트](https://www.astrill.com/a/dik2masnw6ig){target="_blank"}

    [Astrill](https://www.astrill.com/a/dik2masnw6ig){target="_blank"}을 사용하는 경우 로그인한 후 [이 페이지](https://www.astrill.com/member-zone/tools/wireguard-configuration){target="_blank"}에 접속하여 WireGuard 구성을 생성하세요.

    그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "IVPN"
    ### IVPN

    [공식 웹사이트](https://www.ivpn.net/){target="_blank"}

    [IVPN](https://www.ivpn.net/){target="_blank"}을 사용하는 경우 WireGuard 구성을 수동으로 생성해야 합니다. OS에 따라 가이드를 따르세요.

    [Windows](https://www.ivpn.net/setup/windows-10-wireguard/){target="_blank"}, [macOS](https://www.ivpn.net/setup/macos-wireguard/){target="_blank"}, [Linux](https://www.ivpn.net/setup/linux-wireguard/){target="_blank"}

    그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "NVPN"
    ### NVPN

    [공식 웹사이트](https://www.nvpn.net/){target="_blank"}

    [여기](https://support.nvpn.net/Knowledgebase/Article/View/428/0/how-to-use-our-wireguard#windows){target="_blank"} 가이드를 따라 구성을 생성하세요.

    그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "OVPN"
    ### OVPN

    [공식 웹사이트](https://www.ovpn.com/en?ref=glinet){target="_blank"}

    1. [www.ovpn.com](https://www.ovpn.com/en?ref=glinet){target="_blank"}에 로그인하고 아래 메뉴에서 WireGuard 구성 파일을 찾으세요.

        ![ovpn dashboard](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/ovpn/get_wireguard_configuration_files.jpg){class="glboxshadow"}

    2. **Generate WireGuard keys**를 클릭하고 원하는 서버를 선택한 후 구성을 다운로드하세요.

        ![ovpn generate wireguard keys](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/ovpn/download_wireguard_configuration_files.jpg){class="glboxshadow"}

    3. 텍스트 편집 소프트웨어로 구성을 열고 내용을 복사하세요.

        구성에 IPv6 내용이 포함될 수 있습니다. GL.iNet 라우터는 IPv6를 충분히 지원하지 않으므로 IPv6 내용을 삭제하세요. 아래에 예시가 있으며 강조 표시된 부분이 IPv6 내용입니다.

        ![remove wireguard ipv6 content](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/ovpn/remove_wireguard_ipv6_content.jpg){class="glboxshadow"}

    4. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

    5. [모바일 앱](../faq/mobile_app.md)을 사용하여 OVPN을 설정할 수도 있습니다.

??? "PrivateVPN"
    ### PrivateVPN

    [공식 웹사이트](https://affiliate.privatevpn.com/scripts/click.php?a_aid=5e3a511658bc3){target="_blank"}

    1. 로그인한 후 [Control panel](https://privatevpn.com/control-panel){target="_blank"}에 접속하세요

        ![PrivateVPN Control panel](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/privatevpn/privatevpn_wireguard_1.jpg){class="glboxshadow"}

    2. 서버를 선택하세요

        ![select a server](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/privatevpn/privatevpn_wireguard_2.jpg){class="glboxshadow"}

    3. **GENERATE CONFIG**를 클릭한 후 구성을 복사하세요

        ![generate config](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/privatevpn/privatevpn_wireguard_3.jpg){class="glboxshadow"}

    4. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "PrivadoVPN"
    ### PrivadoVPN

    [공식 웹사이트](https://privadovpn.com/#a_aid=GLINET){target="_blank"}

    PrivadoVPN 웹사이트에 접속한 후 로그인하세요.

    대시보드에서 Manual Configuration 섹션을 찾고 WireGuard를 클릭하세요. 연결하려는 서버를 선택한 후 Download Configration을 클릭하세요.

    ![privadovpn wireguard manual configuration](https://static.gl.inet.com/docs/router/en/4/tutorials/get_wg_configs/privadovpn/privadovpn_wireguard_manual_configuration.png){class="glboxshadow"}

    ![privadovpn wireguard manual configuration download](https://static.gl.inet.com/docs/router/en/4/tutorials/get_wg_configs/privadovpn/privadovpn_wireguard_manual_configuration_download.png){class="glboxshadow"}

    그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "Proton VPN"
    ### Proton VPN

    [공식 웹사이트](https://go.getproton.me/aff_c?offer_id=26&aff_id=1612){target="_blank"}

    [Proton VPN](https://go.getproton.me/aff_c?offer_id=26&aff_id=1612){target="_blank"}을 사용하는 경우 [여기](https://protonvpn.com/support/wireguard-configurations/){target="_blank"} 가이드를 따라 WireGuard 구성 파일을 생성하세요.

    그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "PureVPN"
    ### PureVPN

    [공식 웹사이트](https://billing.purevpn.com/aff.php?aff=35535){target="_blank"}

    [이 가이드](https://support.purevpn.com/router/how-to-setup-purevpn-on-glinet-router){target="_blank"}를 참조하거나 다음 단계에 따라 WireGuard 구성 파일을 수동으로 가져오세요.

    1. [Member Area](https://my.puremember.com/){target="_blank"}에 로그인한 후 **Manual Configuration**을 클릭하세요.

        ![purevpn wireguard manual configuration](https://static.gl.inet.com/docs/router/en/4/tutorials/get_wg_configs/purevpn/manual-purevpn1.png){class="glboxshadow"}

    2. Member Area로 이동하여 WireGuard 구성 파일을 다운로드하세요.

        ![purevpn wireguard manual configuration](https://static.gl.inet.com/docs/router/en/4/tutorials/get_wg_configs/purevpn/manual-purevpn2.png){class="glboxshadow"}

    **참고**: 프로필을 다운로드한 후 30분 이내에 파일을 복사하고 연결을 활성화하세요. 그렇지 않으면 구성이 만료되어 새 구성 파일을 다시 다운로드해야 합니다.

    그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

    [참조 링크](https://support.purevpn.com/router/how-to-setup-purevpn-on-glinet-router){target="_blank"}

??? "SpiderVPN"
    ### SpiderVPN

    [공식 웹사이트](https://spidervpn.org/#a_aid=5ddfa0372e7ff){target="_blank"}

    1. [www.spidervpn.org](https://spidervpn.org/#a_aid=5ddfa0372e7ff)에 로그인하고 VPN 구성을 가져오는 섹션을 찾으세요. 구성을 가져오는 단계를 따르세요.

        ![get spider vpn configuration](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/spidervpn/spidervpn_config_1.jpg){class="glboxshadow"}

    2. vpn 구성 다운로드

        ![download spider vpn configuration](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/spidervpn/spidervpn_config_2.jpg){class="glboxshadow"}

    3. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "StarVPN"
    ### StarVPN

    [공식 웹사이트](https://www.starvpn.com/dashboard/aff.php?aff=91){target="_blank"}

    1. **StarVPN 계정 등록**

        [pricing plan](https://www.starvpn.com/#pricing){target="_blank"} 옵션으로 이동하여 필요에 맞는 VPN 요금제를 선택하세요. 결제 시 등록하거나 [여기](https://www.starvpn.com/dashboard/register.php){target="_blank"}에서 직접 등록할 수 있습니다.

    2. **Wireguard 구성 다운로드**

        StarVPN 회원 영역 [dashboard](https://www.starvpn.com/dashboard){target="_blank"}에 로그인하세요. Wireguard Config를 클릭하여 구성 파일을 다운로드하세요. 각 슬롯에는 고유한 wireguard 구성 파일이 포함되어 있습니다.

        ![starvpn download wireguard config](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/starvpn/download-config_edited.jpg){class="glboxshadow"}

    3. 구성에 IPv6 내용이 포함될 수 있습니다. GL.iNet 라우터는 IPv6를 충분히 지원하지 않으므로 IPv6 내용을 삭제하세요.

        ![startvpn wireguard configuration remove ipv6 content](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/starvpn/starvpn_wireguard_configuration_remove_ipv6.jpg){class="glboxshadow"}

    4. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

    [참조 링크](https://www.starvpn.com/wireguard-setup-on-gl-inet-router/){target="_blank"}

??? "StrongVPN"
    ### StrongVPN

    [공식 웹사이트](https://strongvpn.com/?tr_aid=5ac44bd241ca7){target="_blank"}

    1. [StrongVPN](https://strongvpn.com/?tr_aid=5ac44bd241ca7){target="_blank"}을 사용하는 경우 [https://wg.strongvpn.com](https://wg.strongvpn.com){target="_blank"}에 로그인하세요

    2. 드롭다운 메뉴에서 위치를 선택하고 **GENERATE**를 클릭한 후 다운로드한 텍스트 파일을 엽니다.

        ![strongvpn wireguard configuration generator](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/strongvpn/strongvpn_wireguard_configuration_generator.png){class="glboxshadow"}

    3. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

    4. [모바일 앱](../faq/mobile_app.md)을 사용하여 StrongVPN을 설정할 수도 있습니다.

??? "TRUST.ZONE"
    ### TRUST.ZONE

    [공식 웹사이트](https://trustzonevpn.info/r.php?RID=B-byr1v-MDAxNzE3NjgxMjM4){target="_blank"}

    1. [https://trust.zone/setup](https://trust.zone/setup)에 접속하여 로그인하세요.

    2. WireGuard 섹션까지 아래로 스크롤하고 원하는 포트를 선택한 후 특정 서버의 구성 또는 모든 구성의 zip 파일을 다운로드하세요.

    3. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "VPN.AC"
    ### VPN.AC

    [공식 웹사이트](https://vpn.ac/aff.php?aff=1424){target="_blank"}

    1. [VPN.AC](https://vpn.ac/aff.php?aff=1424){target="_blank"}을 사용하는 경우 제어 패널에 로그인한 후 "Services" 메뉴에서 WireGuard Manager를 찾으세요.

        ![VPN.AC WireGuard Manager](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/vpnac/vpn.ac_wireguard_manager.jpg){class="glboxshadow"}

    2. 구성을 생성하고 다운로드하세요.

        ![VPN.AC create wireguard profiles](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/vpnac/vpn.ac_create_wireguard_profiles.jpg){class="glboxshadow"}

    3. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

??? "VPN Unlimited(KeepSolid)"
    ### VPN Unlimited(KeepSolid)

    [공식 웹사이트](https://keepsolid.g2afse.com/click?pid=270&offer_id=7){target="_blank"}

    1. [VPN Unlimited](https://keepsolid.g2afse.com/click?pid=270&offer_id=7){target="_blank"}을 사용하는 경우 [User Office](https://my.keepsolid.com/){target="_blank"}에 로그인한 후 VPN Unlimited® 애플리케이션을 선택하고 **Manage**를 클릭하세요.

        ![vpn unlimited setup on gl.inet router](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/vpnunlimited/01.jpg){class="glboxshadow"}

    2. **Device** 아래 필드을 누르고 **Manually create a new device…**를 클릭한 후 사용자 정의 이름(예: WireGuard)을 설정하고 **Server**의 적절한 위치를 선택한 후 드롭다운 메뉴에서 **WireGuard**® 프로토콜을 선택하고 **Generate**를 클릭하세요.

        ![vpn unlimited setup on gl.inet router](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/vpnunlimited/02.jpg){class="glboxshadow"}

    3. 그러면 구성 매개변수가 아래 텍스트 형식으로 표시됩니다.

        ![vpn unlimited setup on gl.inet router](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/vpnunlimited/03.jpg){class="glboxshadow"}

        아래와 같이 구성을 결합하세요.

        <p>
        [Interface]</br>
        PrivateKey = <i>User Office에서 PrivateKey를 붙여넣으세요</i></br>
        ListenPort = <i>ListenPort 정보를 붙여넣으세요</i></br>
        Address = <i>Address 정보를 붙여넣으세요</i></br>
        DNS = <i>User Office에서 DNS 정보를 붙여넣으세요</i></br>
        </br>
        [Peer]</br>
        PublicKey = <i>User Office에서 PublicKey를 붙여넣으세요</i></br>
        PresharedKey = <i>PresharedKey 정보를 붙여넣으세요</i></br>
        AllowedIPs = <i>AllowedIPs 정보를 붙여넣으세요</i></br>
        Endpoint = <i>Endpoint 정보를 붙여넣으세요</i></br>
        </p>

    4. 그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

    [참조 링크 1](https://www.vpnunlimited.com/help/manuals/wireguard-setup-on-glinet-router){target="_blank"}

    [참조 링크 2](https://www.vpnunlimited.com/help/manuals/wireguard/windows){target="_blank"}

??? "Windscribe"
    ### Windscribe

    [공식 웹사이트](https://windscribe.com/yo/1u2h9ndl){target="_blank"}

    1. [여기](https://windscribe.com/login?auth_required){target="_blank"}에서 Windscribe 회원 계정에 로그인한 후 [WireGuard Config Generator](https://windscribe.com/getconfig/wireguard){target="_blank"}에 접속하세요.

    2. 사용하려는 서버 위치와 포트를 선택한 후 **Download Config**를 클릭하세요.

        ![windscribe WireGuard Config Generator](https://static.gl.inet.com/docs/router/en/3/tutorials/wireguard_client/windscribe/windscribe_01.jpg){class="glboxshadow"}

    3. [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따르세요.

??? "12VPX"
    ### 12VPX

    [공식 웹사이트](https://12vpx.com/?aff=1174){target="_blank"}

    [12VPX](https://12vpx.com/?aff=1174){target="_blank"}을 사용하는 경우 로그인한 후 [이 페이지](https://12vpx.com/setup/wireguard){target="_blank"}에 접속하면 모든 서버의 구성을 볼 수 있습니다.

    그런 다음 [이 가이드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)를 따라 계속하세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
