# Repeater를 통해 기존 Wi-Fi에 연결하여 인터넷 사용

<iframe width="560" height="315" src="https://www.youtube.com/embed/7mZtz8u8--E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Repeater를 사용한다는 것은 라우터를 다른 기존 무선 네트워크에 연결하는 것을 의미합니다. 예를 들어 호텔이나 카페에서 무료 Wi-Fi를 사용할 때입니다.

기본적으로 WISP(Wireless Internet Service Provider) 모드로 작동하며, 이는 라우터가 자체 서브넷을 생성하고 방화벽으로 작동하여 공용 네트워크로부터 사용자를 보호합니다.

## 기본 단계

라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Repeater** 섹션으로 이동한 후 **Connect**를 클릭합니다.

![repeater section](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/repeater_section.png){class="glboxshadow"}

사용 가능한 네트워크 목록에서 연결할 Wi-Fi 네트워크를 선택합니다.

![join wifi 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/join_wifi_1.png){class="glboxshadow"}

**참고**: 이 페이지에는 라우터가 지원하는 Wi-Fi 채널이 표시됩니다. 연결하려는 Wi-Fi 네트워크가 이 채널 중 하나를 사용하는지 확인하세요. 그렇지 않으면 사용 가능한 네트워크 목록에 표시되지 않을 수 있습니다.

올바른 Wi-Fi 비밀번호를 입력하고 **Apply**를 클릭합니다.

![join wifi 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/join_wifi_2.png){class="glboxshadow"}

연결하려는 Wi-Fi SSID가 사용 가능한 네트워크 목록에 없으면 오른쪽 상단의 **Join Other Network**를 클릭하여 Wi-Fi SSID 및 기타 필요한 정보를 수동으로 입력합니다. 자세한 단계는 [여기](#join-other-network)를 참조하세요.

![join other network](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/join_other_network_1.png){class="glboxshadow"}

호텔/공항/쇼핑몰에서 제공하는 공용 핫스팟에 연결하려면 [공용 핫스팟](#for-public-hotspot)을 참조하세요.

기타 설정은 [고급 설정](#advanced-settings)을 참조하세요.

잠시 후, 비밀번호 입력이 올바르면 연결이 성공합니다.

![repeater connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/repeater_connected.png){class="glboxshadow"}

## 공용 핫스팟용

캡티브 포털이 있는 공용 핫스팟에 라우터를 연결할 때 다음 기능을 활성화하면 연결 성공률을 높이는 데 도움이 됩니다.

![repeater settings for public hotspot](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/repeater_settings_for_public_hotspot.png){class="glboxshadow"}

- **공용 핫스팟용 로그인 모드 자동 활성화**

    이 기능은 v4.6부터 사용할 수 있습니다.

    이 옵션을 활성화하면 라우터가 핫스팟에 성공적으로 연결되었지만 인터넷에 연결되지 않은 경우 공용 핫스팟용 로그인 모드로 자동 전환됩니다. **이 모드에서는 일부 서비스가 일시 중단되고 DNS 모드가 자동으로 전환되며, 핫스팟 제공자(예: 호텔 또는 쇼핑몰)에 네트워크 활동이 유출될 수 있습니다.**

    이 옵션을 활성화하지 않더라도 라우터는 핫스팟에서 캡티브 포털을 감지하고 로그인에 실패하면 이 모드로 전환하라는 메시지를 표시합니다.

    ![login mode for public hotspots](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/login_mode_for_public_hotspots.png){class="glboxshadow"}

- **위장 활성화**

    활성화하면 라우터는 관리 패널에 액세스하는 데 사용하는 클라이언트 장치의 MAC 주소를 에뮬레이션하여 해당 장치로 위장합니다.

- **MAC 모드**

    라우터가 공용 핫스팟에 연결하는 데 사용할 MAC를 선택할 수 있습니다.

    - **공장**: 장치의 원래 공장 할당 MAC 주소를 사용합니다.

    - **복제**: 연결을 위해 클라이언트 장치의 MAC 주소를 복제합니다. 원하는 MAC가 나열되어 있지 않으면 복제할 주소를 수동으로 입력합니다.

        참고: 많은 최신 장치는 Wi-Fi 네트워크에 연결할 때 무작위 MAC 주소(일반적으로 프라이빗 Wi-Fi 주소 또는 무작위 하드웨어 주소라고 함)를 사용합니다. 따라서 여기에 표시된 MAC 주소는 장치의 실제 물리적 MAC와 일치하지 않을 수 있습니다.

    - **무작위**: 연결을 위해 무작위 MAC 주소를 자동으로 생성합니다.

    네트워크 구성을 저장할 때 MAC 모드(복제/무작위 MAC 주소 포함)는 저장하는 특정 SSID에 연결됩니다. 언제든지 각 SSID에 대해 이 설정을 수동으로 변경할 수 있습니다.

- **MAC 자동 업데이트**: 이 옵션을 활성화하면 MAC이 자동으로 업데이트될 수 있습니다.

## 고급 설정

네트워크에 참가할 때 몇 가지 추가 옵션이 있습니다.

![advanced settings](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/repeater_advanced_settings.png){class="glboxshadow"}

* **기억**: 이를 활성화하여 현재 반복된 Wi-Fi 네트워크를 기억합니다.

* **BSSID 잠금**: 활성화하면 라우터는 다른 AP가 동일한 SSID를 공유하더라도 선택한 BSSID에 해당하는 특정 액세스 포인트(AP)에만 연결합니다.

* **수동으로 고정 IP 설정**: 활성화하면 설정을 자동으로 가져오는 대신 라우터의 Repeater 연결에 대해 고정 IPv4 주소, 넷마스크, 게이트웨이 및 DNS 서버를 수동으로 구성할 수 있습니다.

    ![set static ip](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/manually_set_static_ip.png){class="glboxshadow"}

* **TTL**: TTL(Time To Live)은 패킷이 네트워크에서 존재할 수 있는 최대 시간을 설정하며 통신 사업자의 요구 사항에 따라 입력됩니다. 기본적으로 라우터는 들어오는 클라이언트 장치의 TTL을 1씩 줄여 포워딩합니다. 위장이 필요한 경우 여기에 고정 값을 설정할 수 있습니다. TTL은 IPv4에만 유효합니다.

* **HL**: IPv6에서 HL(Hop Limit) 필드는 네트워크에서 데이터 패킷의 전송 홉 수를 제한하며 IPv4의 TTL과 동일합니다.

* **MTU**: 기본값은 1500입니다.

## Repeater 옵션

Repeater 옵션을 보려면 연결된 Repeater 섹션의 오른쪽 상단에 있는 기어 아이콘을 클릭합니다.

![repeater options](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/repeater_connected.png){class="glboxshadow"}

**펌웨어 v4.8의 경우** Repeater 옵션 페이지는 다음과 같이 표시됩니다.

![v4.8 repeater options 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/4.8/repeater_options_1.png){class="glboxshadow"}

- **다른 네트워크 모드로 전환 허용**:

    - 전환 없음 모드: 전환 없음 모드를 활성화하면 현재 Wi-Fi가 연결 해제될 때 다른 저장된 네트워크에 자동으로 연결되지 않습니다.

    - 자동 전환 모드: 자동 전환 모드를 활성화하면 현재 Wi-Fi가 연결 해제될 때 라우터가 다른 저장된 네트워크에 연결을 시도합니다.

    - 네트워크 없이 자동 전환: 네트워크 없이 자동 전환 모드를 활성화하면 라우터는 Repeater가 아닌 모드에서 성공적으로 네트워킹될 때 네트워크를 자동으로 스캔하지 않으며, 라우터에 네트워크가 없을 때만 다른 저장된 네트워크로 자동 전환을 시도하므로 통신 패킷 손실을 방지할 수 있습니다.

- **대역 선택**: 자동, 5GHz 및 2.4GHz의 세 가지 옵션에서 선택할 수 있습니다.

    대역을 수동으로 선택하면 라우터는 다른 대역을 사용하는 Wi-Fi를 스캔하거나 연결하지 않습니다.

**펌웨어 v4.7 이전의 경우** Repeater 옵션 페이지는 아래와 같이 표시됩니다.

![repeater options](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/repeater_options.png){class="glboxshadow"}

* **다른 저장된 네트워크로 전환 허용**. 이 옵션을 활성화하면 라우터가 현재 Wi-Fi 네트워크에 연결할 수 없을 때 다른 저장된 네트워크에 자동으로 연결합니다.

* **대역 선택**. 대역을 수동으로 선택하면 라우터는 다른 대역의 Wi-Fi를 스캔하거나 연결하지 않습니다.

## 알려진 네트워크 관리

알려진 네트워크를 삭제하려면 **Switch Network**를 클릭합니다.

![switch network](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/repeater_connected.png){class="glboxshadow"}

또는 연결된 네트워크가 없으면 Repeater 섹션에서 **Connect**를 클릭합니다.

![repeater section](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/repeater_section.png){class="glboxshadow"}

**알려진 네트워크** 섹션에서 휴지통 아이콘을 클릭하여 알려진 네트워크를 삭제하거나 기어 아이콘을 클릭하여 네트워크를 구성합니다.

![manage known network](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/manage_known_networks.png){class="glboxshadow"}

## 다른 네트워크 참여

SSID가 사용 가능한 네트워크 목록에 없거나 SSID가 숨겨진 경우 **Join Other Network**를 클릭할 수 있습니다.

![join other network 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/join_other_network_1.png){class="glboxshadow"}

SSID를 입력하고 보안을 선택한 다음 비밀번호(필요한 경우)를 입력합니다.

![join other network 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/join_other_network_2.png){class="glboxshadow"}

**보안** 설정에는 모델에 따라 두세 가지 옵션이 있습니다.

* 없음, 비밀번호가 필요하지 않음을 의미합니다.
* WPA/WPA2/WPA3, 거의 모든 Wi-Fi 네트워크에서 지원하는 일반적인 보안입니다.
* WPA/WPA2/WPA3 Enterprise, 인증을 위해 확장 가능한 인증 프로토콜(EAP)이 필요합니다. 연결하려면 유효한 사용자 이름과 비밀번호가 필요합니다(일반적으로 비즈니스 또는 캠퍼스 네트워크에서 사용).

    ![join other network, eap](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/join_other_network_eap.jpg){class="glboxshadow"}

    EAP 네트워크 반복에 대한 자세한 지침은 [여기](../tutorials/eap.md){target="_blank"}를 클릭하세요.

## 재연결

다음 경우 라우터는 일정 시간마다 Wi-Fi에 자동으로 재연결을 시도합니다. 필요한 경우 수동으로 비활성화할 수 있습니다. SSID/비밀번호 오류의 경우 알려진 네트워크에서 네트워크를 제거하여 해결하세요.

1. Repeater 설정 중에 잘못된 SSID/비밀번호를 입력했습니다.

2. 초기 연결 후 상위 라우터의 범위를 벗어났습니다.

3. 상위 라우터가 SSID/비밀번호를 변경하거나 연결 후 액세스를 제한합니다.

재연결 프로세스에는 대기, 스캔, 연결의 세 가지 고유한 단계가 있습니다.

1. 대기 단계: 문제 없음 - 라우터가 재연결 조건을 기다립니다.

2. 스캔 단계: 스캔된 주파수 대역에서 패킷 손실이 발생할 수 있습니다. 새 장치는 연결 문제에 직면할 수 있습니다. GL-AXT1800/GL-AX1800 모델의 경우 게스트 Wi-Fi가 일시적으로 비활성화됩니다.

3. 연결 단계: 대상 대역의 메인 Wi-Fi가 재설정 중에 몇 초 동안 끊길 수 있습니다.

**참고**: 문제는 일반적으로 스캔 및 연결 단계에서 발생합니다.

## 문제 해결

라우터가 Repeater로 Wi-Fi 네트워크에 연결되어 있지만 인터넷을 사용할 수 없는 경우 아래와 같이 노란색 메시지가 표시됩니다.

**"인터페이스는 연결되었지만 인터넷에 액세스할 수 없습니다."**

![connect but no internet](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_repeater/interface_connected_no_internet.png){class="glboxshadow"}

이 문제를 해결하려면:

1. 상위 장치(즉, 라우터가 연결된 Wi-Fi 네트워크)에 인터넷 액세스가 있는지 확인하세요.

2. [Multi-WAN](multi-wan.md) 페이지로 이동하여 Repeater 인터페이스 상태를 확인하세요.

## DFS

상위 5G Wi-Fi에 연결할 때 라우터의 Wi-Fi는 상위 Wi-Fi에 따라 DFS 채널을 사용하거나 사용하지 않습니다.

* 상위 Wi-Fi가 DFS 채널을 사용하고 스캔 가능한 경우 라우터의 5G Wi-Fi는 동일한 채널을 사용합니다.

* 상위 Wi-Fi가 스캔 가능하지 않거나 연결이 실패하면 라우터의 5G Wi-Fi는 비DFS 채널로 전환됩니다.

??? "지원되는 모델"

    - GL-E5800 (Mudi 7)
    - GL-MT3600BE (Beryl 7)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-BE3600 (Slate 7)
    - GL-B3000 (Marble)
    - GL-MT6000 (Flint 2)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)

??? "지원되지 않는 모델"

    - GL-MT5000 (Brume 3)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-AX1800 (Flint)
    - GL-A1300 (Slate Plus)
    - GL-SFT1200 (Opal)
    - GL-MT1300 (Beryl)
    - GL-AR750S (Slate)
    - GL-AR750 (Creta)
    - GL-AR300M Series (Shadow)
    - GL-MT300N-V2 (Mango)
    - GL-XE300 (Puli)
    - GL-X750 (Spitz)
    - GL-X300B (Collie)
    - GL-S1300 (Convexa-S)
    - GL-B1300 (Convexa-B)
    - GL-AP1300 (Cirrus)
    - GL-MV1000/GL-MV1000W (Brume)

---

관련 문서

- [인터넷 페이지](internet.md)
- [각 인터넷 액세스 방법의 우선 순위를 설정하는 방법](multi-wan.md)
- [여러 인터넷 액세스 방법을 동시에 사용할 때 로드 밸런스를 설정하는 방법](multi-wan.md)
- [LAN 및 Wi-Fi MAC 주소를 알 수 있는 방법](../faq/how_can_i_know_the_lan_wifi_mac.md)

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
