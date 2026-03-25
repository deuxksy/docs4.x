# 직접 구축한 OpenVPN 연결에서 OpenVPN 클라이언트용 고정 IP를 예약하는 방법은 무엇인가요?

이 튜토리얼에서는 서버에 연결하는 OpenVPN 클라이언트용 고정 IP를 예약하는 방법을 보여드립니다. 아래 단계를 따르기 전에 GL.iNet 라우터를 OpenVPN 서버로 설정하세요.

1. OpenVPN 서버의 웹 관리 패널에 로그인하고 왼쪽 사이드바에서 **VPN** -> **OpenVPN Server**로 이동합니다.

    **Configuration** 탭에서 **IPv4 서브넷**(아래 이미지에서는 10.8.0.0/24)을 기록해 두고 인증 모드를 **Username and Password Only**로 전환합니다.

    ![ovpn configuration](https://static.gl-inet.com/docs/router/en/4/tutorials/reserve_fixed_ip_for_ovpn_client/ovpn_server_config.png){class="glboxshadow"}

2. **Users** 탭으로 전환하고 아래와 같이 사용자 이름과 비밀번호를 만듭니다.

    ![ovpn users](https://static.gl-inet.com/docs/router/en/4/tutorials/reserve_fixed_ip_for_ovpn_client/ovpn_server_users.png){class="glboxshadow"}

3. SSH로 라우터에 로그인하고 다음 명령을 실행하여 OpenVPN 서버 구성 스크립트 파일을 엽니다:

    `vi /lib/netifd/proto/openserver.sh`

    열린 파일에서 스크립트에 "*client-config-dir /etc/openvpn/ccd*" 줄이 있는지 확인합니다.

    ![check config line](https://static.gl-inet.com/docs/router/en/4/tutorials/reserve_fixed_ip_for_ovpn_client/check_config_line.png){class="glboxshadow"}

    없으면 수동으로 추가한 다음 파일을 저장하고 종료합니다.

4. `/etc/openvpn/`로 이동하여 ccd 폴더를 추가합니다 `mkdir ccd`.

    ![add ccd folder](https://static.gl-inet.com/docs/router/en/4/tutorials/reserve_fixed_ip_for_ovpn_client/add_ccd_folder.png){class="glboxshadow"}

5. "GLsupport" 파일을 추가하고 `ifconfig-push 10.8.0.10 255.255.255.0`을 입력한 다음 파일을 저장하고 종료합니다.

    `cat GLsupport`로 내용을 확인합니다

    ![ifconfig-push](https://static.gl-inet.com/docs/router/en/4/tutorials/reserve_fixed_ip_for_ovpn_client/ifconfig-push.png){class="glboxshadow"}

    - GLsupport를 사용하여 OpenVPN 서버에 연결하면 이 GLsupport 사용자에게 고정 IP 10.8.0.10이 할당됩니다.

    - "255.255.255.0"은 서브넷 마스크이며 OpenVPN 서버 서브넷 마스크로 바꿀 수 있습니다.

    **참고**: 여러 OpenVPN 클라이언트에 대한 IP 주소를 고정하려면 2단계에서 여러 사용자 이름과 비밀번호를 만든 다음 5단계를 반복하여 CCD 폴더에 사용자 순서대로 파일(user_1, user_2, user_3 등)을 추가하고 그 뒤에 "ifconfig push" 명령과 해당 고정 IP 및 서브넷 마스크를 추가합니다.

    예를 들어 `ifconfig-push 10.8.0.20 225.225.225.0`, `ifconfig-push 10.8.0.30 225.225.225.0`, `ifconfig-push 10.8.0.40 225.225.225.0`

6. 마지막으로 OVPN 클라이언트로 테스트하고 클라이언트 가상 IP(IPv4)가 예약된 것인지 확인합니다.

    예를 들어 OpenVPN 클라이언트가 GL.iNet 라우터인 경우 OpenVPN 클라이언트 라우터의 웹 관리 패널에 로그인하고 VPN Dashboard로 이동하여 클라이언트 가상 IP(IPv4)를 확인할 수 있습니다.

    ![ovpn client test v4.7](https://static.gl-inet.com/docs/router/en/4/tutorials/reserve_fixed_ip_for_ovpn_client/ovpn_client_test_4.7.png){class="glboxshadow"}
    <small>(펌웨어 v4.7 이하의 VPN Dashboard)</small>

    ![ovpn client test v4.8](https://static.gl-inet.com/docs/router/en/4/tutorials/reserve_fixed_ip_for_ovpn_client/ovpn_client_test_4.8.png){class="glboxshadow"}
    <small>(펌웨어 v4.8의 VPN Dashboard)</small>

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
