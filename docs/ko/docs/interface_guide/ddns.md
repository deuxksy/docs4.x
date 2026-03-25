# 동적 DNS

동적 도메인 이름 서비스(Dynamic DNS 또는 DDNS)는 도메인 이름을 네트워크 장치의 동적 IP 주소에 매핑하는 데 사용되는 서비스입니다. 동적 DNS를 사용하면 라우터에 원격으로 액세스할 수 있습니다. 이 기능을 사용하려면 인터넷 공용 IP 주소가 필요합니다.

## DDNS 활성화

웹 관리 패널 왼쪽의 **APPLICATIONS** -> **Dynamic DNS** 로 이동합니다.

![ddns](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/ddns.png){class="glboxshadow"}

**Enable DDNS** 를 켜고, **Terms of Services & Privacy Policy** 에 동의한 후 **Apply** 를 클릭합니다.

![enable ddns](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/enable_ddns.png){class="glboxshadow"}

오른쪽 하단의 **Security Settings** 를 클릭합니다.

![security settings](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/security_settings-1.png){class="glboxshadow"}

팝업 창에서 적용하려는 원격 액세스 프로토콜이 활성화되어 있는지 확인합니다. 활성화되어 있지 않으면 SYSTEM -> Security -> Remote Access Control로 이동하여 활성화합니다.

![security settings](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/security_settings-2.png){class="glboxshadow"}

원하는 원격 액세스 프로토콜을 활성화하고 **Apply** 를 클릭합니다.

![security remote access](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/remote_access_enabled.jpg){class="glboxshadow"}

DNS 서버 간의 레코드 동기화에는 최대 10분까지 지연이 발생할 수 있습니다. 이로 인해 DDNS를 활성화한 직후나 공용 IP가 변경될 때 DDNS 도메인 이름을 통해 즉시 액세스하지 못할 수 있습니다.

**참고**: DDNS와 VPN 클라이언트를 동시에 활성화하는 경우 **Services From GL.iNet Use VPN** 이 비활성화되어 있는지 확인하세요. 이 기능은 VPN 대시보드의 [VPN 클라이언트 옵션](vpn_dashboard.md#tunnel-options)에서 찾을 수 있습니다.

## DDNS 작동 여부 확인

DDNS 테스트 도구를 사용하거나 명령어를 사용하여 수동으로 DDNS 작동 여부를 확인할 수 있습니다.

=== "DDNS 테스트 도구 사용"

    동적 DNS 페이지에서 **DDNS Test** 를 클릭합니다.

    ![ddns test](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/ddns_test.png){class="glboxshadow"}

    DDNS 도메인 확인에서 얻은 IP 주소가 라우터의 WAN IP와 일치하는지 확인하세요.

    일치하지 않으면 상단에 노란색 프롬프트가 나타나며, 라우터가 NAT 뒤에 있을 수 있음을 나타내고 상위 라우터에서 포트 포워딩을 설정해야 합니다.

    ![ddns test prompt](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/ddns_test_no_public_ip.png){class="glboxshadow"}

=== "수동으로 확인"

    1. `nslookup` 명령어를 사용하여 도메인 이름과 IP 주소 간의 매핑을 가져옵니다. 아래와 같습니다.

        ![nslookup 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/nslookup1.jpg){class="glboxshadow"}

        위 이미지에서 "xxxxxxx.glddns.com"을 본인의 호스트 이름으로 바꾸세요.

        위 이미지에서 "8.8.8.8"은 Google DNS입니다. 이를 사용하거나 다른 DNS로 바꾼 후 Enter를 누르세요.

    2. 라우터에 연결된 기기에서 브라우저로 "what is my ip address"를 검색하거나 [What Is My IP Address](https://whatismyipaddress.com){target="_blank"}와 같은 웹사이트를 방문하세요. 그러면 공용 IP 주소를 얻을 수 있습니다. 1단계와 2단계에서 얻은 두 IP 주소를 비교하세요. 같다면 DDNS가 작동하는 것이고, 다르면면 작동하지 않는 것입니다.

    3. 아래와 같이 `** server can't find xxxxxxx.glddns.com: NXDOMAIN` 메시지가 나타나면 도메인 확인에 실패했음을 의미하며, DDNS 도메인이 공용 IP 주소에 성공적으로 매핑되지 않았다는 것입니다.

        ![nslookup 3](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/nslookup3.png){class="glboxshadow"}

## HTTPS 원격 액세스

!!! 참고

    1. HTTPS 원격 액세스에는 **공용 IP** 주소가 필요합니다.

        인터넷 서비스 제공업체(ISP)에서 공용 IP 주소를 할당받았는지 확인하려면 [여기](../tutorials/how_to_check_if_isp_assigns_you_a_public_ip_address.md)를 클릭하세요.

    2. 라우터가 NAT 뒤에 있는 경우 HTTPS 액세스를 위해 상위 라우터에서 포트 포워딩(포트 **443**)을 구성하세요.

다음 단계에 따라 라우터에 HTTPS 원격 액세스를 활성화합니다.

1. 동적 DNS 페이지에서 **Enable DDNS** 를 켜고, **Terms of Services & Privacy Policy** 에 동의한 후 **Apply** 를 클릭합니다.

    ![enable ddns](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/enable_ddns.png){class="glboxshadow"}

2. 웹 관리 패널에서 SYSTEM -> Security -> Remote Access Control로 이동합니다.

    ![remote access control](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/remote_access_disabled.png){class="glboxshadow"}

3. **HTTPS Remote Access** 를 활성화하고 **Apply** 를 클릭합니다.

    ![enable https remote access](https://static.gl-inet.com/docs/router/en/4/interface_guide/ddns/enable_https_remote_access.png){class="glboxshadow"}

4. 이제 DDNS 도메인 이름을 통해 HTTPS를 사용하여 웹 관리 패널에 원격으로 액세스할 수 있습니다. 예: `https://xxxxxxx.glddns.com`.

---

궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하시거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용해 주세요.