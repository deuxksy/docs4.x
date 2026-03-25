# 방화벽

이 가이드는 펌웨어 v4.5 이전 버전에 적용됩니다.

v4.6부터 방화벽 페이지가 분리되었습니다. 포트 포워딩 및 DMZ 기능은 [포트 포워딩](port_forwarding.md)으로 이동되었습니다. 열린 포트 기능은 [보안](security.md)으로 이동되었습니다.

---

웹 관리 패널 왼쪽의 **NETWORK** -> **Firewall** 로 이동합니다.

방화벽 페이지에서 **포트 포워딩**, **라우터에서 포트 열기**, **DMZ** 와 같은 방화벽 규칙을 설정할 수 있습니다.

## 포트 포워딩

포트 포워딩을 사용하면 원격 컴퓨터가 라우터의 방화벽 뒤에 있는 LAN의 로컬 컴퓨터 또는 서버(예: 웹 서버, FTP 서버)에 연결할 수 있습니다.

포트 포워딩을 설정하려면 **Port Forwards** 탭을 클릭한 다음 **Add** 를 클릭합니다.

![firewall page](https://static.gl-inet.com/docs/router/en/4/tutorials/firewall/firewall.png){class="glboxshadow"}

팝업 창에서 새 포트 포워딩 규칙을 추가하고 **Apply** 를 클릭합니다.

![add new port forward rule](https://static.gl-inet.com/docs/router/en/4/tutorials/firewall/add_new_port_forward_rule.png){class="glboxshadow"}

**이름:** 규칙의 이름입니다.

**프로토콜:** 사용할 프로토콜로, TCP, UDP 또는 TCP와 UDP 모두를 선택할 수 있습니다.

**외부 영역:** 외부 영역 옵션은 `WAN`, `wgclient`, `wgserver`, `ovpnclient`, `ovpnserver` 입니다.

**외부 포트:** 외부 포트 번호입니다. 여기에 특정 포트 번호를 입력할 수 있습니다.

**내부 영역:** 내부 영역 옵션은 `WAN`, `wgclient`, `wgserver`, `ovpnclient`, `ovpnserver` 입니다.

**내부 IP:** 원격으로 액세스해야 하는 장치에 라우터가 할당한 IP 주소입니다.

**내부 포트:** 장치의 내부 포트 번호입니다. 특정 포트 번호를 입력할 수 있습니다. 외부 포트와 동일한 경우 비워두세요.

**활성화:** 규칙을 활성화하거나 비활성화합니다.

## 라우터에서 포트 열기

라우터의 웹 및 FTP와 같은 서비스는 공개적으로 액세스할 수 있도록 하려면 라우터에서 각각의 포트를 열어야 합니다.

포트를 열려면 **Open Ports on Router** 탭으로 전환한 다음 **Add** 를 클릭합니다.

![open Ports on router](https://static.gl-inet.com/docs/router/en/4/tutorials/firewall/open_ports_on_router.png){class="glboxshadow"}

팝업 창에서 새 포트를 열고 **Apply** 를 클릭합니다.

![open Ports on router](https://static.gl-inet.com/docs/router/en/4/tutorials/firewall/add_new_open_port.png){class="glboxshadow"}

**이름:** 사용자가 지정할 수 있는 규칙 이름입니다.

**프로토콜:** 사용할 프로토콜로, TCP, UDP 또는 TCP와 UDP 모두를 선택할 수 있습니다.

**포트:** 열려는 포트 번호입니다.

**활성화:** 규칙을 활성화하거나 비활성화합니다.

## DMZ

DMZ를 사용하면 한 대의 컴퓨터를 인터넷에 노출시킬 수 있으며, 모든 인바운드 패킷이 이 컴퓨터로 리디렉션됩니다.

**Enable DMZ** 를 켭니다. 모든 인바운드 패킷을 수신할 호스트 장치의 내부 IP 주소를 선택합니다.

![Port Forwards](https://static.gl-inet.com/docs/router/en/4/tutorials/firewall/dmz.png){class="glboxshadow"}

---

궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하시거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용해 주세요.
