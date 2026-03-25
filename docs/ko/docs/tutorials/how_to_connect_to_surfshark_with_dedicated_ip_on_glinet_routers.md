# GL.iNet 라우터에서 전용 IP로 Surfshark에 연결하는 방법

이 문서에서는 GL.iNet 라우터에서 전용 IP로 Surfshark 연결을 설정하는 단계를 소개합니다.

GL-AXT1800을 예로 사용합니다.

1. Surfshark 계정에 로그인한 후 **Dedicated IP**를 선택합니다.

    ![manualdip](https://static.gl-inet.com/docs/router/en/4/interface_guide/openvpn_client/manualdip.jpg){calss="glboxshadow"}

2. Dedicated IP 섹션에서 **Settings**를 클릭합니다.

    ![setting](https://static.gl-inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark_dip/setting.jpg){calss="glboxshadow"}

3. 프로토콜(WireGuard 또는 OpenVPN)을 선택하고 수동 연결용 구성 파일을 다운로드합니다.

    ![protocol](https://static.gl-inet.com/docs/router/en/4/interface_guide/openvpn_client/protocol.jpg){calss="glboxshadow"}

    WireGuard 구성의 경우 다운로드 페이지에 아래와 같이 Server IP와 Server Public Key가 표시됩니다.

    ![loadwg](https://static.gl-inet.com/docs/router/en/4/interface_guide/wireguard_client/set_up_surfshark_dip/loadwg.jpg){calss="glboxshadow"}

    OpenVPN 구성의 경우 다운로드 페이지에 아래와 같이 Server IP와 자격 증명(Username & Password)이 표시됩니다. 자격 증명을 복사하여 나중에 사용하세요.

    ![loadovpn](https://static.gl-inet.com/docs/router/en/4/interface_guide/openvpn_client/loadovpn.jpg){calss="glboxshadow"}

4. 아래 링크를 참조하여 구성 파일을 GL.iNet 라우터에 업로드합니다. 필요한 경우 자격 증명을 입력합니다.

    - [Wireguard 구성 업로드](../interface_guide/wireguard_client.md#set-up-wireguard-client-manually-for-other-providers)

    - [OpenVPN 구성 업로드](../interface_guide/openvpn_client.md#set-up-openvpn-client-manually-for-other-providers)

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
