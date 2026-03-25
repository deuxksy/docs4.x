# 장치의 모든 MAC 주소를 찾는 방법은 무엇인가요?

## 사용 시나리오

GL.iNet 장치의 MAC 주소는 WAN 1, WAN 2, LAN 포트, 2.4G Wi-Fi 및 5G Wi-Fi와 같은 각 네트워크 인터페이스마다 고유합니다.

호텔, 캠핑장 또는 캠퍼스에 연결할 때 네트워크 관리자가 인터넷 액세스 권한을 얻기 위해 장치의 MAC 주소를 요청할 수 있습니다.

다음 방법으로 장치의 정확한 MAC 주소를 찾을 수 있습니다.

## 방법 1. 제품 라벨 통한 확인 (WAN MAC만 해당)

하단 라벨에서 **WAN MAC 주소**를 찾으세요.

아래 이미지에서 WAN MAC은 E4:95:6E:40:DB:A9입니다.

![wan_lan_wifi](https://static.gl.inet.com/docs/router/en/4/tutorials/where_to_find_the_device_id_mac_sn/wan_lan_wifi.png){class="glboxshadow"}

## 방법 2. SSH를 통한 확인

SSH 사용 방법은 [여기](https://docs.gl-inet.com/router/en/4/tutorials/ssh_log_in_to_the_router/)를 확인하세요.

SSH에서 **ifconfig**를 입력하면 br-lan, ethx, wlanx 등의 인터페이스가 순서대로 표시되는 데이터 출력을 받게 됩니다.

### 이더넷 포트의 MAC 찾기

다음 이미지를 예로 듭니다.

![ifconfigwan](https://static.gl.inet.com/docs/router/en/4/tutorials/where_to_find_the_device_id_mac_sn/ifcongwan.jpg){class="glboxshadow"}

- **eth0**는 WAN 포트이며 MAC 주소는 **94:83:C4:19:19:08**입니다.

    WAN 포트가 하나 더 있는 경우(예: GL-MT6000) WAN MAC 주소가 하나 더 있습니다.

- **eth1**, **eth2** 등은 LAN 포트이며 MAC 주소는 **94:83:C4:19:19:09**입니다.

    LAN 포트가 여러 개 있어도 MAC 주소는 하나만 있습니다.

### 무선 포트의 MAC 찾기

다음 이미지를 예로 듭니다.

![ifconfigwifi](https://static.gl.inet.com/docs/router/en/4/tutorials/where_to_find_the_device_id_mac_sn/ifcongwifi.jpg){class="glboxshadow"}

- **wlan0-1**은 2.4G Wi-Fi이며 MAC 주소는 **96:83:C4:19:19:0B**입니다.

- **wlan1**은 5G Wi-Fi이며 MAC 주소는 **94:83:C4:19:19:0A**입니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
