# Captive Portal가 있는 공용 핫스팟에 GL.iNet 라우터 연결

## Captive Portal이란 무엇인가요?

Captive Portal은 공용 핫스팟에서 인터넷 액세스가 허용되기 전에 사용자가 웹 페이지를 보고 상호 작용하도록 요구하는 페이지입니다.

## 공용 핫스팟에 라우터를 사용하는 이유는 무엇인가요?

* 공용 Wi-Fi는 안전하지 않습니다

    공용 Wi-Fi의 위험은 아무리 강조해도 지나치지 않습니다. GL.iNet 라우터를 공용 Wi-Fi에 연결하면 라우터의 관리 패널을 통해 VPN 계정에 직접 로그인할 수 있습니다. 로컬 네트워크의 모든 연결된 장치를 자동으로 암호화하여 모든 단일 장치에 VPN을 설정하는 번거로움을 덜어줍니다.

* 리피터로 사용하여 여러 장치 연결 가능

    게다가 일부 공용 Wi-Fi 네트워크(예: 호텔 Wi-Fi)는 예를 들어 두 개의 장치로 액세스를 제한합니다. 그룹으로 여행할 때 이는 비현실적입니다. 대신 여행용 라우터를 호텔 Wi-Fi에 연결하고 리피터로 사용하여 랩톱, 스마트폰, 태블릿 등 모든 장치에 Wi-Fi 신호를 브로드캐스트할 수 있습니다. 호텔 Wi-Fi는 여행용 라우터를 단일 장치로 인식하지만 무료 Wi-Fi에 원하는 만큼 많은 장치를 연결할 수 있습니다.

## Captive Portal가 있는 공용 핫스팟에 라우터를 연결하는 방법은 무엇인가요?

동영상을 시청하거나 아래 단계를 따르세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/CM4_soLf9fw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

1. 스마트폰 또는 컴퓨터를 라우터에 연결하세요.

    라우터의 전원을 켜세요. 스마트폰 또는 컴퓨터에서 라우터의 SSID를 검색하고 Wi-Fi 비밀번호를 입력하세요. 기본 SSID와 비밀번호는 라우터 하단에 인쇄되어 있습니다.

2. 라우터의 웹 관리 패널에 로그인하세요.

    스마트폰 또는 컴퓨터에서 웹 브라우저를 열고 주소 표시줄에 라우터 IP 주소(기본 IP: `192.168.8.1`)를 입력하세요. 라우터의 웹 관리 패널에 액세스할 수 있습니다.

    처음 로그인하는 경우 언어를 선택하고 라우터 웹 관리 패널의 로그인 비밀번호를 생성하세요.

3. 라우터를 공용 핫스팟에 연결하세요. [Repeater](../interface_guide/internet_repeater.md/) 튜토리얼을 참조하세요.

## 문제 해결

Captive Portal에 들어갈 수 없는 경우 라우터가 인터넷에 액세스하지 못할 수 있습니다. 문제 해결을 위해 다음 방법을 시도해 보세요.

### 방법 1: 공용 핫스팟 로그인 모드 및 위장 활성화

**참고**: 이 두 기능은 펌웨어 v4.6 이상에서만 사용할 수 있습니다.

라우터를 공용 핫스팟에 연결할 때 **Join Network** 페이지에서 다음 기능을 활성화하면 연결 성공률을 높이는 데 도움이 될 수 있습니다.

![hotspot login mode & camouflage](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/hotspot_login_mode_camouflage.png){class="glboxshadow"}

- 공용 핫스팟용 로그인 모드 자동 활성화

    이 옵션을 활성화하면 라우터가 핫스팟에는 성공적으로 연결되었지만 인터넷에는 연결되지 않을 때 자동으로 공용 핫스팟용 로그인 모드로 들어갑니다. 이 모드에서 일부 서비스가 일시 중단되며 DNS 모드가 자동으로 전환되어 핫스팟 제공업체(예: 호텔 또는 쇼핑몰)에 네트워크 활동이 유출될 수 있습니다.

- 위장 활성화

    활성화하면 라우터가 관리 패널에 액세스하는 데 사용하는 클라이언트 장치의 MAC 주소를 에뮬레이션하여 해당 장치인 것처럼 위장합니다.

---

### 방법 2: 라우터 설정 변경

1. 웹 관리 패널에 로그인하고 NETWORK -> DNS로 이동하세요. **DNS Rebinding Attack Protection**가 비활성화되어 있고 **Mode**가 **Automatic**으로 설정되어 있는지 확인하세요.

    ![dns rebinding attack protection](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/dns_rebinding_attack_protection.png){class="glboxshadow" width="600"}

2. 웹 관리 패널에서 VPN -> VPN Dashboard로 이동하세요. 모든 VPN 연결이 비활성화되어 있는지 확인하세요.

    **펌웨어 v4.7 이전**, 페이지는 아래와 같이 표시됩니다.

    ![vpn client disabled v4.7](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/vpn_client_is_disable.png){class="glboxshadow" width="600"}

    **펌웨어 v4.8 이상**, 페이지는 아래와 같이 표시됩니다.

    ![vpn client disabled v4.8](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/vpn_disabled_4.8.png){class="glboxshadow" width="600"}

3. 웹 관리 패널에서 APPLICATIONS -> AdGuard Home으로 이동하세요. AdGuard Home이 비활성화되어 있는지 확인하세요.

    ![adguard home is stopped](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/adguardhome_init.png){class="glboxshadow"}

4. 웹 브라우저를 열고 captive portal 웹페이지를 다시 입력하거나 새로고침하세요. 1분 정도 기다린 후 자동으로 captive portal 인증 페이지로 리디렉션되는지 확인하세요.

    스마트폰을 사용 중인데 웹 브라우저가 captive portal로 리디렉션되지 않는 경우 스마트폰의 Wi-Fi를 끄고 켠진 다음 라우터의 Wi-Fi에 다시 연결하세요. Wi-Fi 비밀번호를 입력한 후 직접 captive portal가 팝업되어야 합니다.

    ![connected](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/connected.png){class="glboxshadow"}

---

### 방법 3: MAC 복제

일부 호텔은 MAC 주소를 인식하여 각 고객이 호텔 Wi-Fi에 연결할 수 있는 장치 수를 제한하며 처음 연결할 때 장치의 MAC 주소를 기록합니다. 이 경우 휴대폰이 호텔 Wi-Fi에 연결하는 데 사용하는 MAC 주소를 라우터에 복제하여 라우터가 해당 MAC 주소를 사용하여 호텔 Wi-Fi에 액세스할 수 있도록 할 수 있습니다.

1. 휴대폰을 호텔 Wi-Fi에 연결하세요. 휴대폰이 호텔 Wi-Fi에 연결하는 데 사용하는 MAC 주소를 찾으세요.

    iPhone (iOS 16.1.2)의 예: Settings -> Wi-Fi -> 호텔 Wi-Fi를 선택하고 Wi-Fi Address를 찾을 수 있습니다. 이 주소를 기록하세요.

    ![iphone wifi private address](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/iphone_wifi_private_address.png){class="glboxshadow" width="350"}

    일부 구형 모델에서는 Wi-Fi 설정에서 MAC 주소를 사용할 수 없을 수 있습니다. 이 경우 장치는 공용 Wi-Fi에 연결할 때 실제 MAC 주소를 사용할 수 있으며 이는 휴대폰의 Settings > About(또는 "About Phone")에서 찾을 수 있습니다.

2. 휴대폰 또는 컴퓨터를 라우터에 연결하세요. 라우터의 웹 관리 패널에 로그인한 후 이 MAC 액세스를 복제하거나 수동으로 입력하세요.

    **펌웨어 v4.5 이전**, 왼쪽에서 NETWORK -> MAC Address를 선택하세요.

    Manual Mode를 선택하고 1단계에서 얻은 MAC 주소를 입력한 후 Apply를 클릭하세요.

    ![MAC manual](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/mac_address_manual.png){class="glboxshadow"}

    **펌웨어 v4.6 이상**, 왼쪽에서 INTERNET -> Repeater 섹션을 선택하고 Modify를 클릭하세요.

    ![repeater modify](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/repeater_modify.png){class="glboxshadow gl-90-desktop"}

    팝업 창에서 MAC Mode를 Clone로 전환하고 MAC 주소를 수동으로 입력한 후 Apply를 클릭하세요.

    ![repeater clone mac](https://static.gl.inet.com/docs/router/en/4/tutorials/connect_to_a_hotspot_with_captive_portal/repeater_clone_mac.png){class="glboxshadow gl-90-desktop"}

3. 적용하려면 라우터를 재부팅해야 할 수 있습니다.

---

### 방법 4: 호텔 직원에게 도움 요청

일부 호텔은 네트워크에 대해 매우 엄격한 검증 정책을 가지고 있습니다. 위의 방법이 작동하지 않는 경우 호텔 직원에게 문의하여 라우터의 MAC 주소(임의의 것이 아닌 공장 기본 MAC 주소 사용)를 호텔 네트워크의 허용 목록에 직접 추가해 달라고 요청해 보세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
