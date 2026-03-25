# GL.iNet 라우터를 EAP 네트워크에 연결하기

일부 GL.iNet 라우터는 EAP (Extensible Authentication Protocol) Wi-Fi 네트워크 연결을 지원합니다.

EAP는 **WPA2‑Enterprise / WPA3‑Enterprise** 네트워크를 위한 **802.1X 인증**에 일반적으로 사용되는 인증 프레임워크입니다. 대표적인 예로 802.1X와 EAP를 기반으로 하는 교육 및 연구 기관을 위한 글로벌 Wi-Fi 로밍 서비스인 **eduroam**이 있습니다.

이 가이드에서는 관리 패널과 LuCI를 통해 GL.iNet 라우터를 EAP Wi-Fi 네트워크에 연결하는 두 가지 방법을 소개합니다.

## 지원 모델

??? "지원 모델"
    - GL-MT3600BE (Beryl 7)
    - GL-E5800 (Mudi 7)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-BE3600 (Slate 7)
    - GL-X2000 (Spitz Plus)
    - GL-B3000 (Marble)
    - GL-AX1800 (Flint)
    - GL-AXT1800 (Slate AX)
    - GL-A1300 (Slate Plus)
    - GL-XE300 (Puli)
    - GL-E750/GL-E750V2 (Mudi)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-AR750S (Slate)
    - GL-AR750 (Creta)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-AP1300 (Cirrus)
    - GL-X300B (Collie)
    - ※GL-MT6000 (Flint 2)
    - ※GL-MT3000 (Beryl AX)
    - ※GL-SFT1200 (Opal)

    **참고:**

    1. GL-MT6000 (Flint 2)과 GL-MT3000 (Beryl AX)은 기본 펌웨어가 설치된 상태에서는 EAP 네트워크 연결을 지원하지 않지만, GL.iNet에서 이 모델들을 위해 EAP 네트워크 연결을 지원하는 네이티브 OpenWrt 24 펌웨어를 제공합니다. [다운로드 센터](https://dl.gl-inet.com/){target="_blank"}에서 모델을 검색하고 OPENWRT 24 탭에서 자세한 내용을 확인하세요.

    2. GL-SFT1200 (Opal)은 펌웨어 v4.8부터 EAP 네트워크 연결을 지원합니다.

??? "미지원 모델"
    - GL-MT5000 (Brume 3)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT1300 (Beryl)
    - GL-MT300N-V2 (Mango)

## 웹 관리 패널을 통한 연결

1. 웹 관리 패널에 로그인하고 **INTERNET** -> **Repeater** 섹션으로 이동한 다음 **Connect**를 클릭합니다.

    ![repeater connect](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/repeater_connect.png){class="glboxshadow"}

    사용 가능한 네트워크를 스캔합니다. 연결할 EAP SSID를 찾아 선택합니다.

    ![scan available networks](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/scan_available_wifi.png){class="glboxshadow"}

    또는 오른쪽 상단의 **Join Other Network**를 클릭하여 수동으로 EAP 네트워크에 연결합니다.

    ![join other network](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/join_other_network.png){class="glboxshadow"}

2. **SSID**를 입력합니다.

    ![input ssid](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/ssid.png){class="glboxshadow"}

3. **Security**를 WPA/WPA2/WPA3 Enterprise로 선택합니다.

    ![select security](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/select_security.jpg){class="glboxshadow"}

4. **Username**과 **Password**를 입력한 다음 **Apply**를 클릭하여 연결합니다.

    ![input username and Password](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/username_and_password.jpg){class="glboxshadow"}

## LuCI를 통한 연결

GL.iNet 웹 관리 패널은 제한된 수의 EAP 유형만 지원합니다.

대상 EAP 네트워크가 웹 관리 패널을 통해 연결할 수 없는 경우 LuCI 인터페이스를 통해 연결을 시도해 보세요.

1. 웹 관리 패널에 로그인하고 **SYSTEM** -> **Advanced Settings**로 이동합니다. LuCI를 설치하고 **Go to LuCI**를 클릭합니다.

    ![gotoluci](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/gotoluci.png){class="glboxshadow"}

2. 동일한 관리 비밀번호로 LuCI 인터페이스에 로그인하고 Network -> Wireless로 이동합니다.

    ![wireless](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/luci_network_wireless.png){class="glboxshadow"}

3. 2.4G 섹션 또는 5G 섹션에서 **Scan**을 클릭합니다.

    ![scan](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/luci_wireless_scan.png){class="glboxshadow"}

4. 원하는 네트워크에 연결합니다.

    ![join network](https://static.gl-inet.com/docs/router/en/4/tutorials/eap/luci_join_network.png){class="glboxshadow"}

## 문제 해결

대상 EAP 네트워크에 EAP 유형(예: PEAP, TTLS), 도메인 접미사 일치, 아이덴티티, 익명 아이덴티티 등과 같은 추가 매개변수가 필요한 경우, 웹 관리 패널을 통한 EAP 연결이 실패할 수 있습니다.

![connection failed](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/connection_failed.png){class="glboxshadow"}

아래 단계에 따라 LuCI 인터페이스를 통해 고급 설정이 필요한 EAP 네트워크에 GL.iNet 라우터를 연결하세요.

1. 설정 정보 확인

    대상 EAP 네트워크의 설정 매개변수를 미리 확인합니다. 예:

    - EAP Type (예: PEAP, TTLS, TLS)
    - 인증 도메인 접미사 (예: @company.com)
    - Identity (보통 전체 사용자 이름)
    - Anonymous Identity (선택 사항)
    - 내부 인증 유형 (예: MSCHAPv2, PAP)
    - CA 인증서 (필요한 경우 .crt 형식 파일 준비)

    참고용으로 Xfinity Mobile Wi-Fi의 예시입니다.

    ![xfinity wifi configs](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/xfinity_mobile_config.png){class="glboxshadow gl-50-desktop"}

2. LuCI에 로그인

    라우터의 웹 관리 패널에 로그인합니다. 로그인 후, 이전에 WebGUI를 통해 대상 EAP 네트워크에 연결을 시도했지만 실패한 경우 연결을 중단하세요.

    ![abort connection](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/abort_connection.png){class="glboxshadow"}

    그런 다음 **SYSTEM** -> **Advanced Settings** -> **Go to LuCI**로 이동합니다. 동일한 관리 비밀번호로 LuCI에 로그인합니다.

    ![luci login](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/luci_login.jpg){class="glboxshadow gl-70-desktop"}

3. LuCI에서 리피터 설정

    LuCI 인터페이스에서 Network -> Wireless로 이동합니다.

    ![xfinity wifi configs](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/wireless.png){class="glboxshadow"}

    5G 또는 2.4G 섹션에서 **Scan** 버튼을 클릭하여 사용 가능한 Wi-Fi 네트워크를 검색합니다.

    ![wireless scan](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/wireless_scan.png){class="glboxshadow"}

    검색 결과에서 대상 EAP 네트워크를 찾아 **Join Network**를 클릭합니다.

    ![scan results](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/scan_results.png){class="glboxshadow"}

    "Joining Network" 페이지에서 **WPA passphrase**를 입력하고 **Submit** 버튼을 클릭합니다.

    ![joining network](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/joining_network.png){class="glboxshadow"}

    Wireless Client 설정 페이지로 이동합니다.

4. **Interface Configuration** -> **Wireless Security**를 찾습니다.

    ![wireless security](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/wireless_security.jpg){class="glboxshadow"}

    아래와 같이 대상 EAP 네트워크에 맞는 올바른 설정 매개변수를 선택/입력합니다. **아직 Save를 클릭하지 마세요**.

    ![wireless security example](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/wireless_security_example.png){class="glboxshadow"}

5. **Advanced Settings** 탭으로 전환하고 인터페이스 이름(예: **wlan0**)을 지정합니다. 그런 다음 오른쪽 하단의 **Save**를 클릭합니다.

    ![advanced settings](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/advanced_settings.png){class="glboxshadow"}

6. Wireless 페이지로 돌아가면 보류 중인 변경 사항이 표시됩니다. 오른쪽 하단의 **Save & Apply** 버튼을 클릭합니다.

    ![save abd apply](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/save_apply.png){class="glboxshadow"}

    라우터가 대상 EAP 네트워크에 성공적으로 연결됩니다.

7. 연결 확인

    ??? "WebGUI에서 연결 확인"

        라우터가 대상 EAP 네트워크에 성공적으로 연결되면 아래와 같이 WebGUI에 리피터 아이콘이 켜집니다.

        ![connected status](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/connected_status.png){class="glboxshadow"}

        **참고**: LuCI의 설정은 WebGUI와 동기화되지 않으므로 리피터 인터페이스의 세부 정보(예: 연결된 IP, 게이트웨이 등)는 WebGUI에 표시되지 않습니다.

        이미지와 같이 하단의 리피터 섹션이 비어 있습니다. 그러나 상단의 리피터 아이콘이 켜져 있으므로 라우터는 이미 리피터로 대상 EAP 네트워크에 연결되어 있습니다.

    ??? "SSH를 통한 연결 확인"

        1. [SSH](../tutorials/ssh_log_in_to_the_router.md){target="_blank"}로 라우터에 로그인합니다.

        2. **ifconfig**를 입력하고 Enter를 클릭합니다.

            ![ifconfig](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/ifconfig.png){class="glboxshadow"}

            **wlan0** 인터페이스 상태를 확인할 수 있습니다.

            ![ifconfig](https://static.gl-inet.com/docs/router/en/4/tutorials/connect_to_eap_network_with_advanced_settings/ifconfig_2.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
