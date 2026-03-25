# VPN 클라이언트 DNS 쿼리를 VPN 서버의 업스트림 DNS로 라우팅하는 방법은 무엇인가요?

이 튜토리얼에서는 VPN 클라이언트의 모든 DNS 쿼리를 기본 라우터의 LAN 측에 있는 자체 호스팅 DNS 서버, VPN 서버의 업스트림으로 리디렉션하는 단계를 소개합니다.

## 토폴로지

이 튜토리얼에서는 **Flint 3 (GL-BE9300)**과 **Slate 7 (GL-BE3600)**을 예로 사용합니다.

Flint 3은 VPN 서버이며 업스트림 네트워크에 기본 라우터가 있고, Slate 7은 Flint 3에 연결된 VPN 클라이언트입니다.

VPN 서버와 클라이언트 간에 VPN 터널이 설정되면 기본적으로 VPN 클라이언트의 DNS 쿼리는 먼저 VPN 서버로 전송된 다음 기본 라우터로 전달되고 마지막으로 기본 라우터의 WAN에 구성된 ISP 할당 DNS 서버에 의해 해결됩니다.

![topology 1](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/topology-1.jpg){class="glboxshadow"}

그러나 기본 라우터에 자체 호스팅 DNS 서버(IP 주소 `192.168.1.13`)를 배포한 경우 DNS 쿼리를 자체 호스팅 DNS 서버로 라우팅하려면 추가 구성이 필요합니다.

![topology 2](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/topology-2.jpg){class="glboxshadow"}

## 설정

1. Flint 3의 웹 관리 패널에 로그인하고 **NETWORK** -> **DNS**로 이동합니다. DNS 서버 모드를 **Manual DNS**로 전환하고 DNS 서버의 IP 주소를 입력합니다.

    ![manual dns](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/manual_dns.png){class="glboxshadow"}

2. **VPN** -> **WireGuard Server** -> **Configuration** 탭으로 이동하여 IPv4 주소를 기록해 둡니다. 일반적으로 모델과 펌웨어 버전에 따라 `10.0.0.1/24` 또는 `10.1.0.1/24`입니다.

    ![server ip](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/server_ip.png){class="glboxshadow"}

3. **Profiles** 탭으로 전환하고 클라이언트 구성을 추가한 다음 Slate 7용 프로필을 내보냅니다.

    ![add profile](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/add_profile.png){class="glboxshadow"}

4. 프로필을 열고 DNS가 2단계에서 얻은 VPN 서버 IP 주소인지 확인합니다.

    DNS 확인 실패를 방지하려면 "64.6.64.6"이 있으면 삭제하고 변경 사항을 저장하세요.

    ![edit config](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/edit_config.png){class="glboxshadow"}

5. Flint 3의 웹 관리 패널에서 **WireGuard Server** 페이지 상단의 **Start** 버튼을 클릭하여 서버를 실행합니다.

    ![start server](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/start_server.png){class="glboxshadow"}

6. Slate 7의 웹 관리 패널에 로그인하고 **VPN** -> **WireGuard Client**로 이동합니다.

    **Add Manually**를 클릭하고 편집한 프로필을 업로드합니다.

    ![upload config](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/upload_config.png){class="glboxshadow"}

7. 세 점 아이콘을 클릭하여 VPN 연결을 시작합니다. 상태 표시기가 녹색으로 바뀌면 VPN 연결이 성공한 것입니다.

    ![start client](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/start_client.png){class="glboxshadow"}

## DNS 확인 검증

다음 명령을 실행하여 VPN 클라이언트의 DNS 트래픽을 캡처합니다. 모든 VPN 클라이언트 DNS 트래픽이 VPN 서버(이 예에서는 `10.0.0.1`)로 이동하는 것을 보여줍니다.

![client dns traffic](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/client_dns_traffic.png){class="glboxshadow"}

다음 명령을 실행하여 VPN 서버의 DNS 트래픽을 캡처합니다. 모든 VPN 클라이언트 DNS 트래픽이 마지막으로 자체 호스팅 DNS 서버(이 예에서는 `192.168.1.13`)로 이동하는 것을 보여줍니다.

![server dns traffic](https://static.gl-inet.com/docs/router/en/4/tutorials/route_vpn_dns_to_server_upstream_dns/server_dns_traffic.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
