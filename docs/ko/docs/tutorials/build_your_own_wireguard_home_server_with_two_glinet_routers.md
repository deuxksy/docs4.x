# 두 대의 GL.iNet 라우터로 나만의 WireGuard 홈 서버 구축하기

이 글에서는 홈 라우터를 WireGuard VPN 서버로, 트래블 라우터를 WireGuard VPN 클라이언트로 설정하여 원격으로 연결하는 방법을 소개합니다. 이를 통해 어디서든 트래블 라우터로 홈 IP 주소를 사용할 수 있습니다.

아래 동영상을 시청하거나 단계를 참조하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/7mJXA5MfMb8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<small>(이 동영상은 GL-MT5000 (Brume 3)과 GL-MT3600BE (Beryl 7)을 사용하여 VPN 설정을 시연합니다.)</small>

다음 단계에서는 GL-MT6000 (Flint 2)과 GL-MT3000 (Beryl AX)을 예로 사용합니다:

- GL-MT6000은 홈 라우터로, WireGuard VPN 서버로 설정됩니다. 무선 기능이 필요하지 않은 경우 보안 게이트웨이인 GL-MT2500 또는 다른 모델도 고려할 수 있습니다.

- GL-MT3000은 트래블 라우터로, 집의 VPN 서버에 원격으로 연결하기 위해 WireGuard VPN 클라이언트로 설정됩니다.

## 나만의 WireGuard 홈 서버를 구축해야 하는 이유

1. 홈 IP 주소를 인터넷 주소로 사용하여, 집에 있는 것처럼 행동할 수 있습니다.
2. 제3자 VPN 서비스와 비교할 때 월 요금을 지불할 필요가 없습니다.
3. 암호화된 VPN 터널을 통해 모든 인터넷 트래픽을 홈 네트워크로 라우팅하여 개인정보를 보호합니다.
4. 내부 리소스 및 로컬 스트리밍에 쉽게 접근할 수 있습니다.

## 준비 사항

### 공인 IP가 있는지 확인

먼저 GL-MT6000이 WAN 측에서 공인 IP 주소를 가지고 있는지 확인해야 합니다. 그래야 전 세계적으로 접근할 수 있습니다. 그렇지 않으면 여행 중에 트래블 라우터가 VPN 연결을 설정할 수 없습니다.

공인 IP 주소가 있는지 확인하려면 웹 브라우저를 열고 주소 표시줄에 [what is my ip](https://whatismyipaddress.com/){target="_blank"}을 입력하세요.

![whatismyip](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/whatismyip.jpg){class="glboxshadow"}

공인 IP 주소가 표시됩니다. ISP가 GL-MT6000에 제공한 WAN IP와 일치하면 공인 IP 주소가 있는 것입니다.

공인 IP 주소가 없다면 다음 방법들을 참고하세요.

1. 메인 라우터가 있다면 로그인하여 ISP로부터 공인 IP를 받았는지 확인하세요.
2. ISP에 공인 IP 주소를 요청하세요. 추가 비용이 발생할 수 있습니다.
3. 위의 두 가지 방법이 작동하지 않는 경우(예: CGNAT 환경), [Astrorelay](how_to_set_up_wireguard_server_via_astrorelay.md)와 같은 리버스 프록시 방법을 사용할 수 있습니다. 또는 SDWAN 솔루션인 [AstroWarp](https://www.astrowarp.net/)를 사용해 볼 수도 있습니다.

### 포트 포워딩이 필요한지 확인

??? "GL.iNet이 메인 라우터인 경우"

    GL.iNet 라우터가 이더넷 케이블로 ISP 모뎀에 직접 연결된 경우, GL.iNet 라우터가 메인 라우터입니다.

    **GL.iNet 라우터가 ISP 모뎀에 직접 연결되어 있는지 확인하는 방법**

    단계:

    1. GL.iNet 관리 패널에 로그인합니다.

    2. 왼쪽 사이드바에서 INTERNET을 선택합니다. 토폴로지 및 연결 세부 정보를 확인합니다:

        이더넷으로 직접 연결된 경우 프로토콜, IP 주소, 게이트웨이 등의 세부 정보가 포함된 "Ethernet" 섹션이 표시됩니다.

        아래 이미지를 예로 들면, 표시된 IP 주소는 ISP가 이 GL-iNet 라우터에 제공한 WAN IP입니다.

        ![mt6000-home](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/mt6000_home.png){class="glboxshadow"}

        이 WAN IP는 공인 IP 주소이므로, 메인 라우터 역할을 하는 이 GL.iNet 라우터는 공인 IP를 가지고 있으며 **포트 포워딩을 설정할 필요가 없습니다**.

        이 GL.iNet 라우터를 WireGuard 서버로, 트래블 라우터를 WireGuard 클라이언트로 설정하기만 하면 됩니다. 그러면 둘 사이에 VPN 터널이 생성됩니다.

        ![topologywg](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/topologywg.jpg){class="glboxshadow"}

??? "GL.iNet이 서브 라우터인 경우"

    GL.iNet 라우터가 NAT 뒤에 있는 경우 메인 라우터에서 **포트 포워딩**을 설정하세요.

    토폴로지

    ![togologywgtp](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/topologywgtp.jpg){class="glboxshadow"}

    예: TP-Link 라우터를 홈 메인 라우터로 사용하는 경우.

    홈 라우터의 Wi-Fi 또는 LAN에 연결합니다. 그런 다음 웹 관리 패널에 로그인합니다. ISP로부터 받은 WAN IP 주소를 확인합니다. 아래 이미지에서 공인 IP가 **42.200.00.00**임을 확인할 수 있습니다.

    ![tp_home](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/tp_home.png){class="glboxshadow"}

    **포트 포워딩을 설정하기 전에 메인 라우터에서 GL.iNet 라우터의 IP 주소를 예약하여 고정 IP를 할당하는 것을 권장합니다.** 그렇지 않으면 메인 라우터 또는 GL.iNet 라우터가 재시작될 때 메인 라우터가 GL.iNet 라우터에 다른 IP 주소를 할당하여 포트 포워딩 규칙이 실패할 수 있습니다.

    그런 다음 메인 라우터에서 GL.iNet 라우터에 대한 포트 포워딩을 설정합니다.

    1. "Advanced"로 이동하여 "Virtual Server"를 클릭한 다음 "Add"를 클릭합니다.

    2. Internal IP (Device IP): GL.iNet 라우터에 할당된 IP 주소입니다. TP-Link의 클라이언트 목록에서 찾을 수 있습니다.

    3. External/Internal port: 둘 다 "51820"을 입력하세요.

    4. Protocol: "All" 또는 "UDP" 또는 "TCP/UDP"를 선택할 수 있습니다.

    ![tp_port1](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/tp_port1.jpg){class="glboxshadow"}

    **더 많은 [포트 포워딩](how_to_set_up_port_forwarding.md) 예제**

## WireGuard 서버 설정

### DDNS 활성화 (선택 사항)

고정 공인 IP가 없고 동적 공인 IP만 있는 경우 DDNS 기능을 활성화하세요.

GL-MT6000의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **Dynamic DNS**로 이동합니다. **Enable DDNS** 스위치를 켭니다.

**Terms of Service & Privacy Policy** 체크박스를 선택하고 **Apply**를 클릭합니다.

![ddnsapply](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/enable_ddns.jpg){class="glboxshadow"}

그런 다음 **WireGuard Server** -> Configuration 탭으로 이동하여 Listen Port가 51820인지 확인한 후 **Apply**를 클릭합니다.

![wgserver](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/wgserver-apply.png){class="glboxshadow"}

### 설정 생성

같은 페이지에서 Configuration 탭 옆에 있는 **Profiles** 탭을 클릭한 다음 **Add**를 클릭합니다 (아래 이미지에서 1로 표시).

클라이언트 설정이 자동으로 생성됩니다. **앞으로 아이콘**을 클릭합니다 (2로 표시).

팝업 창에서 DDNS Domain을 활성화하려면 슬라이드합니다 (3으로 표시, 동적 공인 IP가 있는 경우에만 선택 사항).

![wgservergen](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/wgconfiggen.jpg){class="glboxshadow"}

그런 다음 WireGuard [모바일 앱](https://www.wireguard.com/install/)을 사용하여 QR 코드를 스캔하여 서버를 테스트할 수 있습니다. 자세한 내용은 [여기](../interface_guide/wireguard_server.md/#check-if-wireguard-server-is-working-properly)를 클릭하세요.

또는 VPN 클라이언트 연결을 위해 텍스트 형식의 설정을 내보낼 수 있습니다.

**Configuration File** 탭을 클릭하여 QR 코드에서 텍스트 형식으로 설정을 전환합니다.

클라이언트용 텍스트를 복사하거나 다운로드 버튼을 클릭하여 나중에 사용할 수 있도록 저장합니다.

![configload](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/configload.jpg){class="glboxshadow"}

## WireGuard 클라이언트 설정

### LAN IP 변경

이 튜토리얼에서는 GL-MT6000과 GL-MT3000을 예로 사용하며, 두 기본 LAN IP는 모두 **192.168.8.1**입니다. 충돌을 피하기 위해 둘 중 하나를 다른 LAN IP로 변경해야 합니다.

GL-MT3000 (WireGuard 클라이언트)의 LAN IP를 변경하는 단계는 다음과 같습니다.

GL-MT3000의 웹 관리 패널에 로그인한 다음 왼쪽 사이드바의 **NETWORK** -> **LAN**으로 이동하여 LAN IP를 변경합니다. 예를 들어 기본 192.168.8.1에서 `192.168.10.1`로 LAN IP를 변경할 수 있습니다.

![change lan](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/change_lan_ip.png){class="glboxshadow"}

LAN 인터페이스에 대한 자세한 내용은 [여기](../interface_guide/lan.md)를 클릭하세요.

### 설정 추가

GL-MT3000의 웹 관리 패널에서 **VPN** -> **WireGuard Client**로 이동하고 **Add Manually**를 클릭합니다.

![addwgclient1](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/addwgclient-1.png){class="glboxshadow"}

왼쪽에 그룹을 만들고 이름을 설정한 다음 설정 파일을 선택하여 업로드하거나 오른쪽 업로드 상자로 드래그합니다.

![addwgclient2](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/addwgclient-2.png){class="glboxshadow"}

파일이 검증을 통과하면 **Apply**를 클릭합니다.

![addwgclient3](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/addwgclient-3.png){class="glboxshadow"}

**Manually Add Configuration**을 클릭하고 설정 텍스트를 붙여넣은 다음 **Apply**를 클릭할 수도 있습니다.

![addwgclient4](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/addwgclient-4.png){class="glboxshadow"}

![addwgclient5](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/addwgclient-5.jpg){class="glboxshadow"}

설정 파일이 성공적으로 업로드되면 WireGuard Client 페이지에 표시됩니다.

![addwgclient6](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/addwgclient-6.png){class="glboxshadow"}

### 연결 시작

세 점 아이콘을 클릭하고 **Start**를 클릭합니다.

![wgstart](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/wgclientstart.png){class="glboxshadow"}

몇 분 정도 기다립니다. 연결이 성공하면 녹색 점이 켜집니다.

![wgconnected](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/wgclient_connected.png){class="glboxshadow"}

**VPN Dashboard**로 이동하면 클라이언트가 홈 공인 IP로 서버에 연결되어 있는 것을 볼 수 있습니다. 펌웨어 버전에 따라 페이지가 약간 다를 수 있습니다.

![clientup](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/wgclientup.jpg){class="glboxshadow"}

GL-MT6000 (WireGuard 서버)의 웹 관리 패널에 다시 로그인하고 **VPN** -> **WireGuard Server**로 이동합니다 (펌웨어 v4.7 이전 버전을 사용하는 경우 **VPN** -> **VPN Dashboard**로 이동). 클라이언트가 연결되어 있음을 나타내는 연결 상태를 볼 수 있습니다.

![servercon](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/wgservercon-4.8.png){class="glboxshadow"}
<small>(FW v4.8의 WireGuard Server 페이지)</small>

![servercon](https://static.gl-inet.com/docs/router/en/4/tutorials/build_your_own_wireguard_server/wgservercon-4.7.jpg){class="glboxshadow"}
<small>(FW v4.7 이전 버전의 VPN Dashboard 페이지)</small>

## 원격 VPN 문제 해결을 위한 사전 준비

여행 중 예기치 못한 문제가 발생할 경우, 원격 VPN 문제 해결을 위해 두 라우터를 모두 GoodCloud 계정에 미리 바인딩하세요.

때때로 정전 등의 이유로 서버가 다운될 수 있습니다. 서버의 접근성을 유지하기 위해 GL.iNet GoodCloud에 바인딩하세요.

---

관련 문서

- [GL.iNet GoodCloud](../interface_guide/cloud.md)

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
