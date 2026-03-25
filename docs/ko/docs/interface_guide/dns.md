# DNS

웹 관리 패널 왼쪽의 **NETWORK** -> **DNS** 로 이동합니다.

라우터의 DNS 설정은 도메인 이름이 IP 주소로 변환되는 방식을 제어합니다. 이 페이지에서는 상위 장치에서 자동으로 얻은 DNS 서버를 사용하거나 사용자 지정 DNS를 설정하고, DNS 우선순위를 구성할 수 있습니다.

사용자 지정 DNS 서버를 설정하면 상위 네트워크 인터페이스에서 얻은 DNS 서버 대신 지정된 DNS 서버를 통해 모든 DNS 쿼리가 해결됩니다. 이를 통해 네트워크의 모든 클라이언트가 각 인터페이스에 대해 구성된 DNS 설정을 사용하게 됩니다.

![dns](https://static.gl-inet.com/docs/router/en/4/interface_guide/dns/dns_page.png){class="glboxshadow"}

- **DNS Rebinding Attack Protection:** 이 옵션을 켜면 개인 DNS 조회가 실패할 수 있습니다. 네트워크에 캡티브 포털이 있는 경우 이 옵션을 비활성화하세요.

- **Override DNS Settings for All Clients:** 활성화하면 라우터가 모든 클라이언트에 대해 암호화되지 않은 DNS 설정을 재정의합니다.
- **Allow Custom DNS to Override VPN DNS:** 활성화하면 사용자 지정 DNS를 설정한 후 VPN 터널을 통해 전송되는 패킷이 VPN 연결의 DNS 서버 설정 대신 사용자 지정 DNS 재정의를 사용하여 해결됩니다.

## DNS 서버 설정

자동, 암호화 DNS, 수동 DNS, DNS 프록시의 네 가지 모드가 있습니다.

- **자동**: 라우터는 상위 장치(예: ISP 모뎀, 기본 라우터)에서 제공하는 DNS 서버 또는 각 네트워크 인터페이스에 해당하는 DNS 설정을 자동으로 사용합니다.

    ![automatic](https://static.gl-inet.com/docs/router/en/4/interface_guide/dns/dns_auto.png){class="glboxshadow"}

- **암호화 DNS**: DNS over TLS, DNSCrypt-Proxy, DNS over HTTPS, Oblivious DNS over HTTPS의 네 가지 암호화 유형을 사용할 수 있습니다.

    ![encrypted dns types](https://static.gl-inet.com/docs/router/en/4/interface_guide/dns/encrypted_types.png){class="glboxshadow"}

    - DNS over TLS의 경우 Control D, NextDNS, Cloudflare 중에서 DNS 제공업체를 선택합니다.

        ![dns over tls](https://static.gl-inet.com/docs/router/en/4/interface_guide/dns/encrypted_tls.png){class="glboxshadow"}

    - 나머지 세 가지(예: DNSCrypt-Proxy, DNS over HTTPS, Oblivious DNS over HTTPS)의 경우 저장소에서 하나 이상의 DNS 서버를 선택합니다.

        ![dnscrypt-proxy](https://static.gl-inet.com/docs/router/en/4/interface_guide/dns/dnscrypt-proxy.png){class="glboxshadow"}

- **수동 DNS**: 드롭다운 목록에서 라우터에 사용할 DNS 서버를 하나 이상 선택합니다.

    ![manual dns](https://static.gl-inet.com/docs/router/en/4/interface_guide/dns/manual_dns.png){class="glboxshadow"}

- **DNS 프록시**: 라우터는 모든 LAN DNS 쿼리를 구성된 DNS 서버로 라우팅합니다. 네트워크에 로컬 DNS 서버를 사용하려는 경우 유용합니다.

    ![dns proxy](https://static.gl-inet.com/docs/router/en/4/interface_guide/dns/dns_proxy.png){class="glboxshadow"}

## 호스트 편집

DNS 서버 섹션 하단에서 **Edit Hosts** 를 클릭하여 정적 DNS 레코드를 추가, 편집 또는 삭제할 수 있습니다. 이를 통해 클라이언트가 로컬 이름으로 로컬 IP 주소에 액세스할 수 있습니다.

![hosts](https://static.gl-inet.com/docs/router/en/4/interface_guide/dns/edit_hosts.png){class="glboxshadow"}

---

궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하시거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용해 주세요.