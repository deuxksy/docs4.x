# GoodCloud Site to Site

## 소개

GoodCloud Site to Site를 사용하면 여러 위치에 있는 사무실이 인터넷을 통해 서로 안전하게 연결할 수 있습니다. 회사 네트워크를 확장하여 한 위치의 컴퓨터 리소스를 네트워크를 통해 다른 위치의 직원이 사용할 수 있게 합니다.

![site to site](https://static.gl-inet.com/goodcloud/docs/tutorials/site_to_site/s2s-main.png){class="glboxshadow"}

**시나리오 1**: 같은 회사 산하의 수십 개 지사를 통합된 사설 네트워크로 연결하여 모든 위치에서 원활한 리소스 공유를 가능하게 합니다.

**시나리오 2**: 긴밀한 파트너십을 맺은 두 회사가 비즈니스 협업을 해야 할 때, Site to Site를 통해 공유된 안전한 네트워크 환경에서 업무를 수행할 수 있습니다.

**시나리오 3**: IP 카메라가 있는 가정의 경우, Site to Site를 통해 구성원이 집을 비운 상태에서도 기기에 원격으로 접속하여 어디서나 쉽게 모니터링할 수 있습니다.

## 조건

1. Site to Site 네트워크를 구축하려면 최소 두 대의 GL.iNet 라우터가 필요합니다.

2. 메인 노드로 설정하기 위해 최소 한 대의 라우터에는 공인 IP 주소가 있어야 합니다. [ISP로부터 공인 IP 주소를 할당받았는지 확인하기](how_to_check_if_isp_assigns_you_a_public_ip_address.md).

    성능이 좋고 네트워크 속도가 가장 빠른 라우터를 메인 노드로 선택하는 것이 좋습니다.

3. 서브 노드에서 VPN 클라이언트 / Tailscale / ZeroTier / AstroWarp도 실행하면서 Site to Site를 실행하는 것은 **권장하지 않습니다**. 네트워크 설정이 특히 복잡해질 수 있기 때문입니다.

## Site to Site 네트워크 구축

1. 라우터를 GoodCloud 계정에 바인딩합니다. [방법](../interface_guide/cloud.md/#setup-your-goodcloud-account)?

2. [GoodCloud](https://www.goodcloud.xyz/#/login)에 로그인하고 왼쪽 사이드바의 **Site to Site**로 이동합니다. 오른쪽 상단의 **Create Network**를 클릭합니다.

    ![create network](https://static.gl-inet.com/goodcloud/docs/tutorials/site_to_site/create-network.png){class="glboxshadow"}

3. 왼쪽 체크박스를 선택하여 최소 두 대의 기기를 선택합니다.

    ![select devices](https://static.gl-inet.com/goodcloud/docs/tutorials/site_to_site/select-devices.png){class="glboxshadow"}

    선택된 기기는 페이지 하단에 표시됩니다.

    Site to Site의 기본 포트는 **51830**입니다. 다른 포트를 사용하려면 왼쪽 하단의 **Advanced**를 클릭하여 수정합니다. 그런 다음 **Next**를 클릭합니다.

    ![two devices selected](https://static.gl-inet.com/goodcloud/docs/tutorials/site_to_site/two-devices-selected.png){class="glboxshadow"}

    Site to Site 네트워크는 안정적인 성능을 보장하기 위해 최대 10대의 기기를 가질 수 있습니다.

4. 네트워크 이름을 입력하고 **Next**를 클릭합니다.

    ![name network](https://static.gl-inet.com/goodcloud/docs/tutorials/site_to_site/name-network.png){class="glboxshadow"}

5. Node Usability Testing이 시작되어 어떤 기기를 메인 노드로 설정할 수 있는지 확인합니다.

    ![node testing](https://static.gl-inet.com/goodcloud/docs/tutorials/site_to_site/node-testing.png){class="glboxshadow"}

    어떤 기기도 메인 노드로 사용할 수 없는 경우 다음을 확인하세요:

    - 최소 한 대의 라우터에 공인 IP(고정 또는 동적 공인 IP)가 있는지 확인합니다.
    - 포트가 열려 있는지 확인합니다. Site to Site의 기본 포트는 51830입니다. 포트를 변경하고 다시 시도할 수도 있습니다.
    - 메인 노드로 설정하려는 라우터가 NAT 뒤에 있는 경우 포트 포워딩을 설정해야 할 수 있습니다.

    ![testing failed](https://static.gl-inet.com/goodcloud/docs/tutorials/site_to_site/testing-failed.png){class="glboxshadow"}

    두 대 이상의 기기를 메인 노드로 설정할 수 있는 경우 하나를 선택하여 계속합니다. 성능이 좋고 네트워크 속도가 가장 빠른 라우터를 메인 노드로 선택하는 것을 권장합니다.

    ![testing success](https://static.gl-inet.com/goodcloud/docs/tutorials/site_to_site/testing-success.jpg){class="glboxshadow"}

    메인 노드로 설정할 수 있는 기기가 한 대뿐인 경우 Site to Site 상세 페이지로 바로 이동합니다.

6. 네트워크는 기본적으로 비활성화되어 있습니다. 모든 노드의 LAN IP 주소가 서로 충돌하지 않는지 확인합니다. 필요한 경우 톱니바퀴 아이콘을 클릭하여 LAN IP를 변경하고 **Start**를 클릭합니다.

    ![detail s2s](https://static.gl-inet.com/goodcloud/docs/detail-s2s-00.png){class="glboxshadow"}

7. 몇 분 정도 기다립니다. 점선이 실선으로 바뀌면 Site to Site 네트워크가 성공적으로 구축된 것입니다.

    ![detail s2s](https://static.gl-inet.com/goodcloud/docs/detail-s2s-01.png){class="glboxshadow"}

## Site to Site 연결 테스트

1. PC나 스마트폰을 이 Site to Site 네트워크의 노드 중 하나에 연결합니다.

2. 웹 브라우저를 실행하여 다른 노드의 LAN IP에 접속합니다. 로그인 페이지에 접근할 수 있으면 두 노드 간의 연결이 정상 작동하는 것입니다.

## 라우트 및 기타 옵션

기본적으로 각 노드는 다른 노드의 LAN에 접근할 수 있습니다. 보안상의 이유로 특정 서비스의 IP 주소만 개방하는 것을 권장합니다.

예를 들어, 노드 1의 서브넷에 서버 A (172.30.97.100)가 있다고 가정합니다. 다른 노드가 노드 1의 서비스 A에만 접근하도록 하려면 다음과 같이 설정합니다:

![LAN IP and routes](https://static.gl-inet.com/goodcloud/docs/lanip-routes-s2s-02.png){class="glboxshadow"}

노드의 상위 라우트도 추가할 수 있습니다.

각 서브 노드는 메인 노드와 암호화된 터널 네트워크를 구축합니다. 터널 서브넷의 IP를 변경하려면 **IP Address Range**를 클릭하여 수정합니다.

IP 주소 범위 변경을 적용하면 몇 분간 네트워크 연결이 끊깁니다.

![Tunnel IP Address Range](https://static.gl-inet.com/goodcloud/docs/tunnel-ip-address-range-s2s.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
