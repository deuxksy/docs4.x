# 포트 포워딩

이 페이지는 펌웨어 v4.6부터 사용할 수 있습니다. 이전 버전은 [Firewall](firewall.md)을 참조하세요.

---

웹 관리 패널 왼쪽에서 **NETWORK** -> **Port Forwarding**으로 이동합니다.

이 페이지에서 **DMZ** 및 **Port Forwarding**와 같은 방화벽 규칙을 설정할 수 있습니다.

**Open Ports on Router** 설정은 SYSTEM -> Security로 이동하세요.

## DMZ

DMZ를 사용하면 한 대의 컴퓨터를 인터넷에 노출할 수 있으므로 모든 인바운드 패킷이 이 컴퓨터로 리디렉션됩니다.

**Enable DMZ**를 토글합니다. 모든 인바운드 패킷을 받을 호스트 장치의 내부 IP 주소를 선택합니다.

DMZ의 우선 순위를 설정할 수 있습니다. DMZ 우선 순위가 포트 포워딩 규칙보다 높으면 모든 포트 포워딩 규칙이 무효화됩니다. 그렇지 않으면 액세스된 포트에 해당하는 포트 포워딩 규칙이 없는 경우에만 요청이 DMZ 호스트 장치로 전달됩니다.

![dmz](https://static.gl.inet.com/docs/router/en/4/interface_guide/port_forwarding/dmz.png){class="glboxshadow"}

## 포트 포워딩

포트 포워딩을 사용하면 원격 컴퓨터가 라우터 방화벽� 뒤의 LAN에 있는 로컬 컴퓨터나 서버(예: 웹 서버, FTP 서버 등)에 연결할 수 있습니다.

포트 포워딩을 설정하려면 Port Forwarding 섹션에서 **Add**를 클릭합니다.

![port forwarding add](https://static.gl.inet.com/docs/router/en/4/interface_guide/port_forwarding/port_forwarding_add1.png){class="glboxshadow"}

팝업 창에서 새 포트 포워딩 규칙을 추가하고 **Apply**를 클릭합니다.

![add new port forwarding rule](https://static.gl.inet.com/docs/router/en/4/interface_guide/port_forwarding/port_forwarding_add2.png){class="glboxshadow"}

**Protocol:** 사용되는 프로토콜입니다. TCP, UDP 또는 둘 다 선택할 수 있습니다.

**External Zone:** 외부 존의 옵션은 `WAN`, `WireGuard Client`, `WireGuard Server`, `OpenVPN Client`, `OpenVPN Server`, `LAN`, `Guest`입니다.

**External Port:** 외부 포트 번호입니다. 특정 포트 번호를 입력할 수 있습니다. 포트 범위는 1에서 65535까지입니다. 단일 포트를 설정하거나 - 기호로 첫 번째와 마지막 포트 번호를 연결하여 포트 범위를 설정할 수 있습니다(예: 501-510).

**Internal Zone:** 내부 존의 옵션은 `LAN`, `Guest`, `WireGuard Client`, `WireGuard Server`, `OpenVPN Client`, `OpenVPN Server`, `WAN`입니다.

**Internal IP:** 라우터가 원격 액세스가 필요한 장치에 할당한 IP 주소입니다. **External Port**에 단일 포트를 설정한 경우 여기에 단일 포트를 설정해야 합니다. **External Port**에 포트 범위를 설정한 경우 여기에 해당 포트 범위를 설정해야 합니다.

**Internal Port:** 장치의 내부 포트 번호입니다. 특정 포트 번호를 입력할 수 있습니다. 외부 포트와 동일한 경우 비워 두세요.

**Description:** 포트 포워딩 규칙의 이름을 설정하거나 설명을 추가합니다(선택 사항).

**Enable:** 규칙을 활성화 또는 비활성화합니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
