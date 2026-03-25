# 클라이언트 장치에서 고정 IP 수동으로 설정하는 방법

=== "Windows 11"

    Windows 11에서는 설정 앱에서 무선 및 유선 어댑터에 대한 고정 IP 주소 구성을 설정할 수 있습니다.

    **Wi-Fi 어댑터에 고정 IP 주소 설정**

    Wi-Fi 어댑터에 고정 IP 주소 구성을 할당하려면 다음 단계를 따르세요:

    1. Windows 11에서 설정 열기 -> 네트워크 및 인터넷 -> Wi-Fi 탭 -> 현재 네트워크 연결 선택.

    2. "IP 설정" 섹션에서 편집 버튼을 클릭합니다.

        ![Windows 11 edit IP address](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/Windows_11_edit_IP_address.webp){class="glboxshadow"}

    3. 아래 단계에 따라 설정하세요:

        ![Settings_app_set_static_IP_address](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/Settings_app_set_static_IP_address.webp){class="glboxshadow"}

        - 수동 옵션을 선택하고 IPv4 토글 스위치를 켭니다.

        - Windows 11용 고정 IP 주소 설정 – 예: 10.1.4.119.

        - 서브넷 마스크 지정 – 예: 255.255.255.0.

        - 기본 게이트웨이 주소 지정.

        - 기본 DNS 주소 지정 (필수).

        - (선택 사항) "보조 DNS" 주소 지정.

        - "HTTPS를 통한 DNS" 드롭다운 메뉴를 사용하고 기본 및 보조 주소에 대해 꺼짐 옵션을 선택하지만, 다음 옵션으로 DoH를 활성화할 수 있습니다:

            - 꺼짐: 모든 DNS 트래픽을 암호화 없이 전송합니다.

            - 켜짐 (자동 템플릿): 모든 DNS 트래픽을 암호화하여 전송합니다.

            - 켜짐 (수동 템플릿): 특정 템플릿을 지정할 수 있습니다. DNS 서비스가 자동으로 작동하지 않거나 예상대로 작동하는 템플릿이 있는 경우에만 필요합니다.

        - "일반 텍스트 대체" 토글 스위치를 끕니다 (DoH를 활성화한 경우).

            - 빠른 팁: 이 기능을 활성화하면 시스템이 DNS 트래픽을 암호화하지만, 암호화 없이 쿼리를 보낼 수 있습니다.

    4. 저장 버튼을 클릭합니다.

        단계를 완료하면 컴퓨터에 고정 네트워크 구성이 적용됩니다. 웹 브라우저를 열어 웹사이트를 로드하여 새 설정을 테스트할 수 있습니다.


    ## **Ethernet 어댑터에 고정 IP 주소 설정**

    Windows 11의 Ethernet (유선) 어댑터에 고정 IP 주소를 할당하려면 다음 단계를 따르세요:

    1. 설정 열기 -> 네트워크 및 인터넷 -> Ethernet 탭.

    2. "IP 설정" 섹션에서 편집 버튼을 클릭합니다.

        ![Edit_TCP/IP_Ethernet_settings](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/Edit_TCP_IP_Ethernet_settings.webp){class="glboxshadow"}

    3. 아래 단계에 따라 설정하세요:

        ![Settings_app_set_static_IP_address](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/Settings_app_set_static_IP_address.webp){class="glboxshadow"}

        - 수동 옵션을 선택합니다.

        - IPv4 토글 스위치를 켭니다.

        - Windows 11용 고정 IP 주소 설정 – 예: 10.1.4.119.

        - 서브넷 마스크 지정 – 예: 255.255.255.0.

        - 기본 게이트웨이 주소 지정.

        - 기본 DNS 주소 지정 (필수).

        - (선택 사항) "보조 DNS" 주소 지정.

        - "HTTPS를 통한 DNS" 드롭다운 메뉴를 사용하고 기본 및 보조 주소에 대해 꺼짐 옵션을 선택하지만, 다음 옵션으로 DoH를 활성화할 수 있습니다:

            * 꺼짐: 모든 DNS 트래픽을 암호화 없이 전송합니다.

            * 켜짐 (자동 템플릿): 모든 DNS 트래픽을 암호화하여 전송합니다.

            * 켜짐 (수동 템플릿): 특정 템플릿을 지정할 수 있습니다. DNS 서비스가 자동으로 작동하지 않거나 예상대로 작동하는 템플릿이 있는 경우에만 필요합니다.

        - "일반 텍스트 대체" 토글 스위치를 끕니다 (DoH를 활성화한 경우).

    4. 저장 버튼을 클릭합니다.

        단계를 완료한 후 웹 브라우저를 사용하여 웹사이트를 열어 설정을 테스트할 수 있습니다.


=== "macOS"

    macOS에서 고정 IP 주소를 설정하는 방법은 다음과 같습니다:

    MacBook을 소유하고 있는 경우 새로운 네트워크 위치를 만들고 싶을 수 있습니다. 이를 통해 특정 네트워크에 대해서만 고정 IP 주소를 사용하고 다른 네트워크에서는 사용하지 않을 수 있습니다.

    Apple 메뉴에서 시스템 환경설정을 선택합니다.

    네트워크를 선택합니다. 아래와 같은 창이 나타납니다.

    ![Mac_network_settings](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/Mac_network_settings.webp){class="glboxshadow"}

    사이드바에서 활성 네트워크 인터페이스를 선택합니다. 이 예에서는 무선 네트워크에 연결되어 있으므로 Wi-Fi를 선택합니다.

    Mac에 할당된 현재 IP 주소를 기억해 두세요. 나중에 나열된 개인 IP 주소 범위 내에서 새 IP 주소를 선택해야 합니다. 자세한 내용은 잠시 후에 설명합니다.

    고급을 클릭합니다.

    TCP/IP를 선택합니다. 아래와 같은 창이 나타납니다.

    ![Mac_Wi-Fi_settings](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/Mac_Wi-Fi_settings.webp){class="glboxshadow"}

    IPv4 구성 메뉴에서 수동을 선택합니다.

    IPv4 주소 필드에 고정 IP 주소를 입력합니다. 어떤 숫자를 입력해야 할까요? 한 가지 방법은 현재 IP 주소를 가져와서 숫자의 마지막 부분을 변경하는 것입니다. 이 예에서는 192.168.7.0부터 192.168.7.255 사이의 주소 중 다른 장치에 이미 할당되지 않은 주소를 선택할 수 있었습니다.

    확인을 클릭 -> 적용을 클릭합니다.


=== "Android"

    단계는 Android 버전에 따라 다릅니다. 이 문서는 Android 버전 11을 기준으로 합니다.

    1. 설정으로 이동 -> 네트워크 및 인터넷 선택,然后 Wi-Fi -> 현재 연결된 네트워크를 탭하여 설정 메뉴를 엽니다.

    ![list_available_networks](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/list_available_networks.png){class="gl-50-desktop"}
    {class="glboxshadow"}

    2. 고정 IP 주소를 설정하려면 다음을 수행합니다:

    - 네트워크 설정에 액세스하려면 오른쪽 상단의 연필 아이콘을 선택합니다.

        ![pencil_icon](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/pencil_icon.png){class="gl-50-desktop"}
        {class="glboxshadow"}

    - 고급 옵션을 선택합니다.

        ![advanced_options](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/advanced_options.png){class="gl-50-desktop"}
        {class="glboxshadow"}

    - IP 설정을 선택합니다.

    - 설정을 DHCP에서 정적(Static)으로 변경합니다.

        ![DHCP_to_Static](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/DHCP_to_Static.png){class="gl-50-desktop"}
        {class="glboxshadow"}

    - 가정 및 기타 개인 네트워크에서 고정 IP 주소를 사용하는 경우 나열된 표준 개인 IP 주소 범위 내에서 선택해야 합니다:10.0.0.0부터 10.255.255.255, 172.16.0.0부터 172.31.255.255, 192.168.0.0부터 192.168.255.255

    - 이제 IP 주소를 입력합니다.
        -이 단계는 각 네트워크에 따라 다릅니다. 예: 192.168.1.128

    - 게이트웨이는 IP 주소를 기반으로 자동으로 채워져야 합니다. 그렇지 않은 경우 IP 주소를 복사하고 마지막 숫자를 1로 바꿉니다.
        -예: 이전 예를 기준으로: 192.168.1.1

    3. 저장을 탭하고 네트워크가 다시 연결될 때까지 기다립니다.

=== "iOS"

    가정 및 기타 개인 네트워크에서 고정 IP 주소를 사용하는 경우 나열된 표준 개인 IP 주소 범위 내에서 선택해야 합니다:

    10.0.0.0부터 10.255.255.255
    172.16.0.0부터 172.31.255.255
    192.168.0.0부터 192.168.255.255

    고정 IP 주소를 설정하려면 다음을 수행합니다:

    - 설정 아이콘을 탭합니다.

    - Wi-Fi로 이동합니다.

    - Wi-Fi 네트워크 이름 옆에 있는 파란색 정보 아이콘 (i)을 탭합니다
         - iOS 7보다 오래된 버전을 사용하는 경우 파란색 오류일 수 있습니다.

    - 아래와 같은 정적(Static) 탭으로 이동합니다.


    ![IP_Settings_Screen_iOS](https://static.gl-inet.com/docs/router/en/4/tutorials/manually_configure_static_ip/IP_Settings_Screen_iOS.png){class="glboxshadow"}

    - IP 주소 필드를 탭합니다.

    - iPhone/iPad에서 사용하려는 고정 IP 주소를 입력합니다.

    - 라우터 필드를 탭합니다.

    - 라우터의 IP 주소를 입력합니다.

    - 서브넷 마스크를 탭하고 정보를 입력합니다

        - 일반적으로 225.225.0.0입니다.

    - 설정을 저장하려면 화면 왼쪽 상단의 Wi-Fi 버튼을 탭합니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
