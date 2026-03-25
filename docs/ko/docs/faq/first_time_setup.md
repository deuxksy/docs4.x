# 초기 설정

GL.iNet 라우터의 초기 설정은 매우 유사합니다. 대부분 모델에는 Wi-Fi 모듈이 있지만 일부 모델에는 없습니다.

따라서 다음 안내는 Wi-Fi 모듈 유무에 따라 두 가지 경우로 나뉩니다.

* [Wi-Fi가 있는 모델](#wi-fi가-있는-모델)
* [Wi-Fi가 없는 모델](#wi-fi가-없는-모델)

## Wi-Fi가 있는 모델

GL-AXT1800 (Slate AX)을 예로 듭니다.

패키지에 포함된 다음 항목을 준비하세요.

- GL-AXT1800
- 전원 어댑터
- 이더넷 케이블

비디오 가이드를 시청하거나 아래 단계를 따르세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/WW8wGk68lEU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<small>(이 비디오는 다른 GL.iNet 라우터를 사용하여 설정을 시연합니다. 대부분의 라우터 모델에서 단계가 동일합니다.)</small>

1. 전원 켜기

    TF 카드를 사용하려면 라우터 전원을 켜기 전에 삽입하세요. TF 카드 핫 스왑핑은 지원되지 않습니다.

    전원 어댑터의 한쪽 끝을 라우터에 연결하고 다른 쪽 끝을 콘센트에 연결하세요. 자동으로 전원이 켜집니다.

2. 라우터에 연결

    이더넷 케이블 또는 Wi-Fi를 통해 라우터에 연결할 수 있습니다.

    * 케이블로 연결

        이더넷 케이블을 통해 컴퓨터를 라우터의 LAN 포트에 연결하세요.

    * Wi-Fi로 연결

        Wi-Fi SSID는 라우터 하단 라벨에 다음 형식으로 인쇄되어 있습니다.

        **GL-AXT1800-XXX** 또는 **GL-AXT1800-XXX-5G**

        기본 Wi-Fi 키는 SSID 아래에 있습니다.

        컴퓨터, 폰 또는 태블릿에서 라우터의 SSID를 검색한 후 Wi-Fi 키를 입력하세요. 일부 모델의 경우 라벨에서 Wi-Fi 비밀번호를 찾을 수 없는 경우 "**goodlife**"를 시도하세요.

        **팁:** 하단 라벨의 QR 코드에는 기본 Wi-Fi 정보가 포함되어 있습니다. 폰의 QR 코드 스캐너로 스캔하여 빠르게 연결할 수 있습니다.

        **참고:** Wi-Fi에 연결한 후 즉시 인터넷에 액세스하지 못할 수 있습니다. 인터넷에 액세스하기 전에 다음 단계에 따라 네트워크를 먼저 구성하세요.

3. 웹 관리 패널에 로그인

    웹 브라우저를 열고(Chrome, Edge 또는 Safari 권장) [http://192.168.8.1](http://192.168.8.1)을 방문하세요. 웹 관리 패널의 초기 설정으로 리디렉션됩니다.

    웹 관리 패널에 액세스하지 못하는 경우 [여기](cannot_access_web_admin_panel.md)를 확인하세요.

    언어를 선택하고 **Next**를 클릭하여 계속합니다.

    ![Admin Panel](https://static.gl.inet.com/docs/router/en/4/tutorials/first_time_setup/admin_panel_first_time_login.png){class="glboxshadow"}

    관리자 비밀번호를 설정하세요. 강력한 비밀번호 사용을 권장합니다. **Apply**를 클릭하여 계속합니다.

    **참고**: 초기화 중 Wi-Fi가 꺼질 수 있으니 라우터에 다시 연결하세요.

    ![set up admin password](https://static.gl.inet.com/docs/router/en/4/tutorials/first_time_setup/set_up_your_admin_password_gl-mt2500.png){class="glboxshadow"}

    초기 설정 후 라우터의 웹 관리 패널에 들어갑니다.

    ![admin panel of gl-axt1800](https://static.gl.inet.com/docs/router/en/4/tutorials/first_time_setup/admin_panel_gl-axt1800.png){class="glboxshadow"}

4. 인터넷에 연결

    * [이더넷 케이블을 통해 인터넷에 연결](../interface_guide/internet_ethernet.md)
    * [기존 Wi-Fi를 통해 인터넷에 연결](../interface_guide/internet_repeater.md)
    * [USB 테더링을 통해 인터넷에 연결](../interface_guide/internet_tethering.md)
    * [USB 모뎁을 통해 인터넷에 연결](../interface_guide/internet_cellular.md)

## Wi-Fi가 없는 모델

GL-MT2500A (Brume 2)를 예로 듭니다.

1. 전원 켜기

    전원 어댑터의 한쪽 끝을 라우터에 연결하고 다른 쪽 끝을 콘센트에 연결하세요. 라우터가 자동으로 전원이 켜집니다.

2. 라우터에 연결

    이더넷 케이블 또는 Wi-Fi를 통해 라우터에 연결할 수 있습니다.

    * 이더넷 케이블을 통한 직접 연결

        이더넷 케이블을 사용하여 컴퓨터를 라우터의 LAN 포트에 연결하세요. 간단하고 명확하기 때문에 권장되는 구성 방법입니다.

    * 다른 라우터의 Wi-Fi를 통해 연결

        GL-MT2500A에는 내장 Wi-Fi 모듈이 없으므로 Wi-Fi 기능이 있는 다른 라우터를 사용하여 GL-MT2500A를 초기화할 수 있습니다.

        * 방법 1: 두 번째 라우터를 AP(액세스 포인트) 모드로 설정한 다음 GL-MT2500A의 LAN 포트를 두 번째 라우터의 WAN 포트에 연결합니다.

        * 방법 2: 두 번째 라우터를 기본 라우터 모드로 유지하지만 192.168.8.1/24와 충돌하지 않는 다른 라우터 IP 주소(예: 192.168.10.1)를 사용합니다. 그런 다음 GL-MT2500A의 LAN 포트를 두 번째 라우터의 WAN 포트에 연결합니다.

        컴퓨터나 스마트폰을 사용하여 두 번째 라우터의 Wi-Fi에 연결하세요.

        !!! Note

            여기서 언급한 두 번째 라우터는 GL.iNet GL-AXT1800, TP-LINK 또는 Netgear 라우터와 같은 일반 라우터입니다. 모뎀, 광 네트워크 단말 또는 ISP에서 제공하는 장치는 이 시나리오에서 작동하지 않을 수 있습니다.

3. 웹 관리 패널에 액세스

    웹 브라우저를 열고(Chrome, Edge, Safari 권장) [http://192.168.8.1](http://192.168.8.1)을 방문하세요. 웹 관리 패널의 초기 설정으로 리디렉션됩니다. 웹 관리 패널에 액세스하지 못하는 경우 [여기](cannot_access_web_admin_panel.md)를 확인하세요.

    언어를 선택하고 **Next**를 클릭하여 계속합니다.

    ![Admin Panel](https://static.gl.inet.com/docs/router/en/4/tutorials/first_time_setup/admin_panel_first_time_login_gl-mt2500.png){class="glboxshadow"}

    관리자 비밀번호를 설정하세요. 강력한 비밀번호 사용을 권장합니다. **Submit**를 클릭하여 계속합니다.

    ![set up admin password](https://static.gl.inet.com/docs/router/en/4/tutorials/first_time_setup/set_up_your_admin_password_gl-mt2500.png){class="glboxshadow"}

    초기 설정 후 라우터의 웹 관리 패널에 들어갑니다.

    ![admin panel of gl-mt2500](https://static.gl.inet.com/docs/router/en/4/tutorials/first_time_setup/admin_panel_gl-mt2500.png){class="glboxshadow"}

4. 인터넷에 연결

    * [이더넷 케이블을 통해 인터넷에 연결](../interface_guide/internet_ethernet.md)
    * [USB 테더링을 통해 인터넷에 연결](../interface_guide/internet_tethering.md)
    * [USB 모뎁을 통해 인터넷에 연결](../interface_guide/internet_cellular.md)

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
