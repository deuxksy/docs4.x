# 공용 IP 주소가 있는지 확인하는 방법

공용 주소는 사설 IP 주소와 달리 인터넷에 연결된 장치에 할당된 고유한 숫자 식별자입니다. 웹사이트를 호스팅하거나 VPN 서버를 설정하거나 온라인 서비스를 제공하려면 공용 IP 주소가 필요합니다. 인터넷 서비스 제공업체에서 일반적으로 하나를 제공합니다.

공용 IP 주소가 있는지 확실하지 않은 경우 다음 방법 중 하나를 사용하여 확인하세요.

**방법 1: 인터넷 서비스 제공업체에 직접 문의**

**방법 2: 라우터 관리 패널과 인터넷에서 IP 주소 확인**

1. 라우터 관리 패널에 로그인합니다.
    * GL.iNet 라우터의 경우 웹 브라우저에 `192.168.8.1`을 입력하고 로그인합니다.
    * 설정에 라우터가 두 개 이상 있는 경우 기본 라우터의 관리 패널에 로그인합니다.
2. 라우터 관리 패널에서 WAN IP 주소를 찾습니다 (예: 42.XXX.XX.)
![IP 주소 찾기](https://static.gl-inet.com/docs/router/en/4/tutorials/how_to_check_if_isp_assigns_you_a_public_ip_address/locate-ip-address.png){class="glboxshadow"}
3. 웹 브라우저에서 "what is my ip"를 검색합니다.
![내 IP 주소](https://static.gl-inet.com/docs/router/en/4/tutorials/how_to_check_if_isp_assigns_you_a_public_ip_address/search-what-is-my-ip.png){class="glboxshadow"}

두 IP 주소가 일치하면 공용 IP 주소가 있는 것입니다.
![두 IP 주소 일치](https://static.gl-inet.com/docs/router/en/4/tutorials/how_to_check_if_isp_assigns_you_a_public_ip_address/two-ip-addresses-match.png){class="glboxshadow"}

공용 IP 주소가 없는 경우 인트라넷 침투 도구를 사용하는 것이 좋습니다. 공용 IP 주소가 없더라도 웹사이트, VPN 서버 또는 서비스를 인터넷에서 액세스할 수 있도록 합니다.

---

관련 문서

- [GL.iNet 라우터에 WireGuard 서버 설정](../interface_guide/wireguard_server.md)
- [GL.iNet 라우터에 OpenVPN 서버 설정](../interface_guide/openvpn_server.md)
- [포트 포워딩](../interface_guide/port_forwarding.md)

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
