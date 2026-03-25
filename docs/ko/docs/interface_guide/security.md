# 보안

이 기능은 펌웨어 v4.5부터 사용할 수 있습니다.

웹 관리 패널 왼쪽에서 **SYSTEM** -> **Security**로 이동합니다.

이 페이지에서 무단 액세스로부터 네트워크와 라우터를 보호하기 위한 다양한 보안 설정을 구성할 수 있습니다.

## 관리자 비밀번호

여기서 웹 관리 패널의 로그인 비밀번호를 변경할 수 있습니다.

![admin password](https://static.gl.inet.com/docs/router/en/4/interface_guide/security/admin_password.jpg){class="glboxshadow"}

관리자 비밀번호는 다음 요구 사항을 충족해야 합니다.

- 최소 10자, 최대 63자.
- 문자(대소문자 구분), 숫자 및 기호 `` ! @ # $ % ^ & * ( ) _ + - = , . > < | ? / \ [ ] { } : ; " ' ` ~ ``가 허용됩니다.
- 대문자, 소문자, 숫자, 기호 중 최소 두 가지가 필요합니다.

## 액세스 제어

액세스 제어는 펌웨어 v4.7 이전에서 로컬 액세스 제어라고도 하며, 라우터의 다양한 관리 인터페이스에 대한 액세스를 관리합니다.

기본 포트에 대한 스캔 및 침입 시도를 방지하고 포트 충돌로 인한 네트워크 문제를 방지할 수 있습니다.

**참고**: 펌웨어에서 포트 번호를 수정한 경우 올바른 포트 번호를 입력해야 관리 패널에 액세스할 수 있습니다. 포트 번호를 잊어버린 경우 라우터를 기본 포트 번호로 재설정하세요.

![security_access_control](https://static.gl.inet.com/docs/router/en/4/interface_guide/security/access_control_4.8.png){class="glboxshadow"}

### 관리 패널

- **HTTP 포트**: 기본값은 80이며, 웹 관리 패널에 대한 암호화되지 않은 HTTP 액세스에 사용됩니다.

- **HTTPS 포트**: 기본값은 443이며, 웹 관리 패널에 대한 보안 HTTPS 액세스에 사용됩니다.

- **강제 HTTPS**: 활성화하면 웹 관리 패널 액세스가 보안 HTTPS 연결을 사용하도록 강제됩니다.

- **자동 로그아웃 시간**: 기본값은 5분이며, 보안을 위해 이 시간 동안 유휴 상태인 관리자 세션을 자동으로 로그아웃합니다. 자동 로그아웃 시간을 1분에서 3시간까지 사용자 정의할 수 있습니다.

### LuCI

- **HTTP 포트**: 기본값은 8080이며, LuCI 인터페이스에 대한 암호화되지 않은 HTTP 액세스에 사용됩니다.

- **HTTPS 포트**: 기본값은 8443이며, LuCI 인터페이스에 대한 보안 HTTPS 액세스에 사용됩니다.

- **강제 HTTPS**: 활성화하면 LuCI 인터페이스 액세스가 보안 HTTPS 연결을 사용하도록 강제됩니다.

### SSH

- **SSH 활성화**: 라우터에 대한 SSH 액세스 허용 여부를 제어합니다. 기본적으로 활성화되어 있습니다.

- **SSH 포트**: 기본값은 22이며, 라우터에 대한 SSH 액세스에 사용되는 포트입니다.

### 금지된 포트 {#prohibited-port}

예약된 포트(또는 브라우저/네트워크 규칙에 따라 특정 서비스용으로 예약된 포트)와 충돌하는 포트 번호를 할당하면 "이 포트는 브라우저에서 금지되어 있습니다"라는 메시지가 나타납니다.

![http_https_port_forbidden](https://static.gl.inet.com/docs/router/en/4/interface_guide/security/http_https_port_forbidden.png){class="glboxshadow"}

??? "브라우저에서 금지된 포트 번호 목록"

    | 포트   | 설명                                     |
    | :----- | :--------------------------------------: |
    | 1      | tcpmux                                   |
    | 7      | echo                                     |
    | 9      | discard                                  |
    | 11     | systat                                   |
    | 13     | daytime                                  |
    | 15     | netstat                                  |
    | 17     | qotd                                     |
    | 19     | chargen                                  |
    | 20     | ftp data                                 |
    | 21     | ftp access                               |
    | 22     | ssh                                      |
    | 23     | telnet                                   |
    | 25     | smtp                                     |
    | 37     | time                                     |
    | 42     | name                                     |
    | 43     | nicname                                  |
    | 53     | domain                                   |
    | 69     | tftp                                     |
    | 77     | priv-rjs                                 |
    | 79     | finger                                   |
    | 87     | ttylink                                  |
    | 95     | supdup                                   |
    | 101    | hostriame                                |
    | 102    | iso-tsap                                 |
    | 103    | gppitnp                                  |
    | 104    | acr-nema                                 |
    | 109    | pop2                                     |
    | 110    | pop3                                     |
    | 111    | sunrpc                                   |
    | 113    | auth                                     |
    | 115    | sftp                                     |
    | 117    | uucp-path                                |
    | 119    | nntp                                     |
    | 123    | NTP                                      |
    | 135    | loc-srv /epmap                           |
    | 137    | netbios                                  |
    | 139    | netbios                                  |
    | 143    | imap2                                    |
    | 161    | snmp                                     |
    | 179    | BGP                                      |
    | 389    | ldap                                     |
    | 427    | SLP (Apple Filing Protocol에서도 사용)   |
    | 465    | smtp+ssl                                 |
    | 512    | print / exec                             |
    | 513    | login                                    |
    | 514    | shell                                    |
    | 515    | printer                                  |
    | 526    | tempo                                    |
    | 530    | courier                                  |
    | 531    | chat                                     |
    | 532    | netnews                                  |
    | 540    | uucp                                     |
    | 548    | AFP (Apple Filing Protocol)              |
    | 554    | rtsp                                     |
    | 556    | remotefs                                 |
    | 563    | nntp+ssl                                 |
    | 587    | smtp (rfc6409)                           |
    | 601    | syslog-conn (rfc3195)                    |
    | 636    | ldap+ssl                                 |
    | 989    | ftps-data                                |
    | 990    | ftps                                     |
    | 993    | ldap+ssl                                 |
    | 995    | pop3+ssl                                 |
    | 1719   | h323gatestat                             |
    | 1720   | h323hostcall                             |
    | 1723   | pptp                                     |
    | 2049   | nfs                                      |
    | 3659   | apple-sasl / PasswordServer              |
    | 4045   | lockd                                    |
    | 5060   | sip                                      |
    | 5061   | sips                                     |
    | 6000   | X11                                      |
    | 6566   | sane-port                                |
    | 6665   | 대체 IRC [Apple 추가]                    |
    | 6666   | 대체 IRC [Apple 추가]                    |
    | 6667   | 표준 IRC [Apple 추가]                    |
    | 6668   | 대체 IRC [Apple 추가]                    |
    | 6669   | 대체 IRC [Apple 추가]                    |
    | 6697   | IRC + TLS                                |
    | 10080  | Amanda                                   |

## 원격 액세스 제어

원격 액세스를 활성화한 후 액세스를 허용할 특정 위치를 설정할 수 있습니다. 예를 들어 사무실에서만 가정 장치에 대한 원격 액세스를 활성화하여 편의성을 희생하고 보안을 향상시킬 수 있습니다.

![security_remote_access_control](https://static.gl.inet.com/docs/router/en/4/interface_guide/security/security_remote_access_control.png){class="glboxshadow"}

- **WAN에서 Ping 허용**: 네트워크 문제가 발생한 경우 WAN 포트에서 Ping을 허용하면 사용자나 네트워크 관리자가 라우터가 제대로 연결되어 있는지 확인하고 네트워크 대기 시간과 패킷 손실을 확인하는 데 도움이 됩니다.

- **HTTPS 원격 액세스**: HTTPS 프로토콜은 주로 웹 브라우저와 웹 서버 간의 통신에 사용되며 안전한 데이터 전송을 보장합니다. 따라서 사용자가 웹 브라우저를 통해 서버를 원격으로 관리하거나 웹 애플리케이션에 액세스해야 할 때 HTTPS 프로토콜을 사용하여 데이터 전송의 보안과 신뢰성을 보장할 수 있습니다.

- **SSH 원격 액세스**: SSH 프로토콜은 주로 원격 컴퓨터와 서버에 안전하게 액세스하고 관리하며 파일 전송 작업을 수행하는 데 사용됩니다. 사용자가 명령줄이나 스크립트를 통해 서버에 원격으로 로그인하여 시스템 관리, 파일 전송 및 기타 작업을 수행해야 할 때 SSH 프로토콜을 사용하여 보안 터널을 설정하고 데이터 전송의 보안과 개인정보를 보장할 수 있습니다.

- **특정 IP에서 원격 액세스 허용**: 이 기능은 **WAN에서 Ping 허용**, **HTTPS 원격 액세스** 또는 **SSH 원격 액세스**와 함께 사용됩니다. 여러 지정된 IP 주소를 추가하여 이러한 지정된 IP 주소가 있는 장치에서 라우터를 원격으로 관리할 수 있습니다.

![add_ip_address_1](https://static.gl.inet.com/docs/router/en/4/interface_guide/security/add_ip_address_1.png){class="glboxshadow"}

![add_ip_address_2](https://static.gl.inet.com/docs/router/en/4/interface_guide/security/add_ip_address_2.png){class="glboxshadow"}

---

## 라우터에서 포트 열기

라우터의 웹 및 FTP와 같은 서비스는 공개적으로 액세스 가능하려면 라우터에서 각각의 포트를 열어야 합니다.

포트를 열려면 **추가**를 클릭하세요.

![open Ports on router](https://static.gl.inet.com/docs/router/en/4/interface_guide/security/open_ports_on_router.png){class="glboxshadow"}

![open Ports on router](https://static.gl.inet.com/docs/router/en/4/interface_guide/security/add_new_open_port.png){class="glboxshadow"}

**이름:** 사용자가 지정할 수 있는 규칙의 이름입니다.

**프로토콜:** 사용되는 프로토콜이며 TCP, UDP 또는 TCP와 UDP를 모두 선택할 수 있습니다.

**포트:** 열려는 포트 번호입니다.

**활성화:** 규칙을 활성화하거나 비활성화합니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
