# U-Boot를 사용하여 라우터 벽돌 해제

DIY 프로젝트나 잘못된 펌웨어를 플래시하여 라우터가 벽돌(bricked)된 경우 라우터에 액세스하지 못할 수 있습니다. 이 경우 U-Boot failsafe를 사용하여 펌웨어를 재설치할 수 있습니다.

**참고:** U-Boot 작업은 라우터의 설정과 설치된 플러그인을 제거합니다.

---

## 준비

이더넷 포트가 있는 컴퓨터를 준비하세요. 컴퓨터에 이더넷 포트가 없는 경우 추가 USB 이더넷 어댑터를 준비하세요.

## 벽돌 해제 단계

비디오 튜토리얼을 참조하거나 아래 절차에 따라 U-Boot Web UI에 액세스하고 펌웨어를 재설치하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/pz0DidfIXRk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<small>U-Boot를 사용하여 펌웨어를 재설치하는 단계는 대략적으로 동일하며 이 비디오는 Mudi/Mudi V2를 예로로 사용합니다. 다른 모델의 경우 아래 절차를 따르세요.</small>

1. 컴퓨터에 펌웨어를 [다운로드](https://dl.gl-inet.com/){target="_blank"}하세요.

    GL-AR750S-EXT와 같은 일부 모델은 두 가지 형식의 펌웨어를 제공합니다. U-Boot용 펌웨어(파일 이름 확장자가 **.img**)를 사용하세요.

2. 라우터의 전원을 제거하세요. 컴퓨터를 라우터의 **이더넷 LAN 포트**에 연결하세요. 다른 모든 포트는 **연결하지 마세요**.

    !!! note

        일부 모델에서는 개별 LAN 포트와 WAN 포트가 상호 교체 가능합니다. 이 LAN 포트를 사용하지 마세요. 예를 들어 GL-MT6000 (Flint 2)에서는 LAN 1을 사용하지 마세요. 대신 LAN 2, LAN 3 또는 LAN 4를 사용하세요.

3. Reset 버튼을 단단히 누른 상태에서 **동시에 라우터의 전원을 켜세요**. 라우터에 전원 버튼이 없는 경우 전원을 연결하면 자동으로 켜집니다.

    그러면 LED가 몇 번 정기적인 순서로 깜빡이게 됩니다. 순서가 바뀐 때 손가락을 놓으세요.

    각 모델의 LED 깜빡임 순서에 대한 설명은 다음과 같습니다.

    **참고:** 제조일이 다른 동일한 라우터 모델은 LED 색상이나 깜빡임 순서가 다를 수 있으며 U-Boot 과정에 영향을 주지 않습니다. 깜빡이는 LED의 변화에 더 주의하세요.

    - **GL-BE9300(Flint 3)**의 경우 파란색 LED가 6번 깜빡이고 then 흰색으로 켜집니다.

    - **GL-BE3600(Slate 7)**의 경우 Reset 버튼을 약 5초간 누르고 있으면 LED 디스플레이에 5초 카운트다운이 표시됩니다. 다음 단계가 화면에 표시될 때까지 Reset 버튼을 계속 누르고 있세요:

        1. 컴퓨터의 IP 주소를 192.168.1.2로 수동 설정하세요
        2. 브라우저를 사용하여 http://192.168.1.1에 방문하세요

        추가 지침은 4단계로 이동하세요.

    - **GL-B3000(Marble)**의 경우 파란색 LED가 7번 깜빡이고 then 흰색으로 켜집니다.

    - **GL-MT6000(Flint 2)**의 경우 파란색 LED가 6번 깜빡이고 then 흰색으로 켜집니다.

    - **GL-MT3000(Beryl AX)**의 경우 파란색 LED가 6번 깜빡이고 then 흰색으로 켜집니다.

    - **GL-MT2500/GL-MT2500A(Brume 2)**의 경우 파란색 LED가 5번 깜빡이고 then 흰색으로 켜집니다.

    - **GL-S200**의 경우 청록색 LED가 5번 깜빡이고 then 잠시 자주색이 된 후 청록색으로 켜집니다.

    - **GL-A1300(Slate Plus)**의 경우 LED가 5번 천천히 깜빡이고 then 잠시 켜져 있는 상태를 유지하다가 계속 빠르게 깜빡입니다.

    - **GL-AR150**, **GL-AR300M**, **GL-USB150(Microuter)**, **GL-AR750(Creta)**, **GL-AR750S-EXT(Slate)**, **GL-X750(Spitz)**, **GL-MT300N-V2(Mango)** 및 **microuter-N300**의 경우 LED가 5번 깜빡입니다.

    - **GL-E750(Mudi)**의 경우 화면에 먼저 "Booting"이 표시되고 "Reset Counting 1 to 4"가 이어지며 마지막으로 "Please Open Web 192.168.1.1"이 표시됩니다.

    - **GL-S1300(Convexa-S)** 및 **GL-B1300(Convexa-B)**의 경우 LED가 4번 깜빡입니다.

        가장 왼쪽의 Power LED는 계속 켜져 있을 수 있고 가장 오른쪽의 Wi-Fi LED가 4번 깜빡인 후 가운데 Mesh LED가 켜진 채로 유지됩니다.

        (일부 오래된 GL-B1300의 경우 가장 왼쪽의 Power LED가 계속 켜져 있고 중간 LED와 오른쪽� LED가 동시에 5번 깜빡인 후 켜진 상태를 유지합니다.)

    - **GL-SF1200**의 경우 5G LED가 5번 깜빡이고 then 켜진 상태를 유지합니다.

    - **GL-AX1800(Flint)**의 경우 파란색 LED가 5번 깜빡이고 then 흰색으로 켜집니다.

    - **GL-AXT1800(Slate AX)**의 경우 파란색 LED가 5번 깜빡이고 then 켜진 상태를 유지합니다.

    - **GL-XE300(Puli)**의 경우 LAN LED가 5번 깜빡이고 Wi-Fi LED가 켜진 상태를 유지합니다.

    - **GL-X300B(Collie)**의 경우 WAN LED가 5번 깜빡이고 Wi-Fi LED가 켜진 상태를 유지합니다.

    - **GL-X3000(Spitz AX)**의 경우 WAN LED가 5번 깜빡이고 Wi-Fi LED가 켜진 상태를 유지합니다.

    - **GL-XE3000(Puli AX)**의 경우 WAN LED가 5번 깜빡이고 Wi-Fi LED가 켜진 상태를 유지합니다.

    - **GL-SFT1200(Opal)**의 경우 파란색 LED가 5번 깜빡이고 then 흰색으로 켜집니다.

    - **GL-AP1300(Cirrus)**의 경우 Power LED가 5번 천천히 깜빡이고 잠시 켜져 있다가 계속 빠르게 깜빡입니다.

    - **GL-MT1300(Beryl)**의 경우 LED가 파란색으로 시작되어 2번 천천히 깜빡이고 5번 더 빠르게 깜빡인 후 흰색으로 켜집니다.

    - **GL-B2200(Velica)**의 경우 두 LED가 파란색으로 시작되고 흰색으로 바뀌며 5번 깜빡인 후 파란색으로 켜집니다.

    - **GL-MV1000/GL-MV1000W(Brume)**의 경우 반복적인 LED 깜빡임 신호가 없습니다. (Power 및 WAN LED가 계속 켜져 있습니다.)

    - **GL-MiFi**의 경우 LED가 6번 깜빡입니다.

    - **GL-MT300N**, **GL-MT300A**의 경우 LED가 3번 깜빡입니다.

4. 컴퓨터의 IP 주소를 **192.168.1.2**로 수동 설정하세요. 다른 운영체제에 대한 단계별 가이드는 아래와 같습니다:

    ??? "Windows 7 / Windows 10"

        1. **Control Panel** -> **Network and Internet** -> **Network and Sharing Center** -> **Change adapter settings**로 이동하세요.

        2. **Local Area Connection** -> **Properties**를 마우스 오른쪽 버튼으로 클릭하세요.

        3. **Internet Protocol Version 4 (TCP/IPv4)** -> **Properties**를 클릭하세요.

        4. **IP adress**를 `192.168.1.2`로 수동 설정하세요.

        5. **Subnet mask**를 `255.255.255.0`으로 설정하세요.

            ![ipv4 properties](https://static.gl.inet.com/docs/router/en/2/troubleshooting/src/debrick/set_ip.jpg){class="glboxshadow"}

        6. **OK** 버튼을 클릭하세요.

    ??? "Windows 11"

        7. Settings를 엽니다.

        8. **Network & Internet**을 클릭합니다.

        9. **Ethernet** 탭을 클릭합니다.

            ![windows 11 ethernet](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/windwos11_ethernet.png){class="glboxshadow"}

        10. "IP assignment" 섹션에서 **Edit** 버튼을 클릭합니다.

            ![windows 11 ethernet edit](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/windows11_ethernet_ip_assignment_edit.png){class="glboxshadow"}

        11. **Manual** 옵션을 선택합니다.

            ![windows 11 ethernet edit](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/windows11_ethernet_edit_ip_settings.png){class="glboxshadow"}

        12. **IPv4 토글** 스위치를 켭니다.

        13. static **IP address**를 **192.168.1.2**로 설정합니다.

            ![windows 11 ethernet edit](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/windows11_ethernet_edit_ip_settings_2.png){class="glboxshadow"}

        14. **Subnet mask**를 **255.255.255.0**로 지정합니다.

        15. **Save** 버튼을 클릭합니다.

    ??? "macOS"

        16. 화면 왼쪽 상단의 **Apple** 아이콘을 클릭하고 **System Preferences**를 선택합니다.

            ![macos system preferences](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/macos_system_preferences.png){class="glboxshadow"}

        17. **Network**를 클릭합니다.

            ![macos system preferences network](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/macos_system_preferences_network.png){class="glboxshadow"}

        18. 왼쪽에서 **Ethernet**을 클릭한 후 **Configure IPv4** 옆의 드롭다운 상자를 클릭하고 **Manually**를 선택합니다. USB Ethernet Adapter를 사용하는 경우 Ethernet을 찾을 수 없고 USB Ethernet Adapter의 이름으로 표시될 수 있습니다.

            ![macos ip manually](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/macos_ip_manually_1.png){class="glboxshadow"}

        19. **IPv4 Address**를 `192.168.1.2`, **Subnet Mask**를 `255.255.255.0`, **Router**를 `192.168.1.1`로 입력한 후 우측 하단의 Apply 버튼을 클릭합니다.

            ![macos ip manually](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/macos_ip_manually_2.png){class="glboxshadow"}

5. 브라우저를 사용하여 **http://192.168.1.1**을 방문하세요. 이것이 U-Boot Web UI입니다.

    ![Uboot web ui](https://static.gl.inet.com/docs/router/en/4/tutorials/debrick/uboot_ui.png){class="glboxshadow" width="700"}

    !!! Note

        - U-Boot Web UI에 액세스하지 못하는 경우 VPN 또는 프록시 소프트웨어가 실행 중인지 확인하세요. Tailscale 및 ZeroTier를 포함한 모든 VPN 또는 프록시 소프트웨어를 비활성화하세요.

        - 위의 U-Boot Web UI는 생산일에 따라 다를 수 있어 실제와 완전히 동일하지 않을 수 있습니다. 일부 극단적인 경우 U-Boot 버전을 업그레이드하는 것이 좋습니다. [여기](upgrade_uboot_version.md) 튜토리얼을 참조하세요.

6. **Choose file** 버튼을 클릭하여 펌웨어 파일을 찾으세요. 그런 다음 **Update firmware** 버튼을 클릭하세요.

7. 약 3분 정도 기다리세요. 업데이트 중에는 장치의 전원을 끄지 마세요. 전원 및 Wi-Fi LED가 모두 켜져 있거나 장치에서 SSID를 찾을 수 있으면 라우터가 준비된 것입니다.

8. 4단계에서 수행한 IP 설정을 되돌리고 장치를 라우터의 LAN 또는 Wi-Fi에 연결하세요. 다시 **192.168.8.1**을 통해 라우터에 액세스할 수 있어야 합니다.

    **참고:** 라우터에 액세스하려면 시크릿 모드를 사용하거나 브라우저 캐시와 쿠키를 삭제해야 할 수도 있습니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
