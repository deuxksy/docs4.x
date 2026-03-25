# GL.iNet 라우터에서 전용 IP로 NordVPN에 연결하는 방법

이 문서에서는 GL.iNet 라우터에서 전용 IP로 NordVPN 연결을 설정하는 단계를 소개합니다.

GL-AXT1800을 예로 사용합니다.

1. Nord 계정에 로그인하여 전용 IP 세부 정보를 확인합니다. 아래와 같이 할당된 IP는 **193.32.211.142**이고 서버는 **United Kingdom #1625**입니다.

    ![nordvpn 전용 ip 정보](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_nordvpn_dedicated_ip/dedicated_ip_info.png){class="glboxshadow"}

2. [https://nordvpn.com/ovpn/](https://nordvpn.com/ovpn/)로 이동하여 **United Kingdom #1625**의 구성 파일을 찾습니다. UDP 또는 TCP 구성 파일을 다운로드합니다.

    ![nordvpn 전용 ip 정보 다운로드](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_nordvpn_dedicated_ip/download_dedicated_ip_config.png){class="glboxshadow"}

3. Nord 계정 페이지로 돌아가 **Manual Setup**으로 이동한 후 **Set up NordVPN Manually**를 클릭하여 서비스 자격 증명을 가져옵니다.

    ![nordvpn 수동 설정](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_nordvpn_dedicated_ip/nordvpn_manual_setup.png){class="glboxshadow"}

    ![nordvpn 수동 설정 서비스 자격 증명](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_nordvpn_dedicated_ip/nordvpn_manual_setup_service_credential.png){class="glboxshadow"}

4. 라우터의 웹 관리 패널에 로그인한 후 **VPN** > **OpenVPN Client**로 이동합니다. 2단계에서 다운로드한 구성 파일을 업로드할 새 그룹을 만듭니다. 그런 다음 3단계에서 가져온 서비스 자격 증명을 입력합니다.

    ![glinet 라우터에 nordvpn 설정](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_nordvpn_dedicated_ip/set_up_nordvpn_on_glinet_router.png){class="glboxshadow"}

    유효한 구성 파일 1개가 감지되었습니다. 사용자 이름과 비밀번호를 입력하세요. 이러한 구성이 서로 다른 비밀번호를 사용하는 경우 각 구성 파일에 해당하는 비밀번호를 입력해야 합니다.

5. 오른쪽의 세 점 아이콘을 클릭하여 연결합니다. **VPN Dashboard**로 이동하여 구성 파일을 선택하고 **Apply**를 클릭하여 연결을 설정할 수도 있습니다.

6. 연결되면 [여기](https://whatismyipaddress.com/)에서 공용 IP를 확인하고 NordVPN의 전용 IP와 일치하는지 확인하세요.

    ![연결 후 ip 확인](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_nordvpn_dedicated_ip/check_ip_after_connected.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
