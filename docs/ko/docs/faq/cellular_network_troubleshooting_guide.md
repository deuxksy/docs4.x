# 셀룰러 네트워크 문제 해결 가이드

셀룰러 연결을 설정할 수 없는 경우 다음 문제를 확인하세요.

??? "장치 하드웨어 확인"

    **1.1** 장치에 표준 전원 어댑터를 사용하세요. 비표준 전원 어댑터는 전원 공급이 불충분할 수 있습니다.

    **1.2** **Modem name**, **IMEI**, **SIM ICCID**가 웹 관리 패널에 표시되는지 확인하세요.

    ![modem name](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/no_sim.png){class="glboxshadow"}

    펌웨어 ver.4.8 이상에서는 **View More Information**을 클릭하여 SIM ICCID를 찾으세요.

    표시되지 않는 경우 라우터를 재시작하세요. 모뎬 이름과 IMEI를 여전히 인식하지 못하는 경우 [support@gl-inet.com](mailto:support@gl-inet.com)으로 문의하세요.

    **1.3** **View More**를 클릭하여 **Cells Info**를 확인하고 신호가 안정적인지 확인하세요. 신호가 매우 약한 경우 안테나가 올바르게 설치되어 있는지 확인하거나 라우터를 신호가 좋은 지역으로 옮겨서 다시 테스트하세요.

    ![cells info](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/cells_info.png){class="glboxshadow"}

    **1.4** **View More**를 클릭하여 장치에서 지원하는 주파수 대역이 지역과 호환되는지 확인하세요.

    ![frequency band](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/frequency_band.png){class="glboxshadow"}

??? "소프트웨어 설정 확인"

    **2.1** 웹 관리 패널에 로그인하여 셀룰러 연결 프로그램이 시작되었는지 확인하세요. **Abort**를 클릭한 후 **Connect**를 클릭할 수도 있습니다.

    ![](https://static.gl.inet.com/docs/router/en/4/faq/x3000_xe3000_connection/2.png){class="glboxshadow gl-90-desktop"}

    **2.2** 일부 네트워크 통신사는 연결에 **3G 프로토콜**을 필요로 할 수 있습니다. 3G 프로토콜로 전환하고 다시 테스트하세요.

    펌웨어 ver.4.7 이전에서는 **Manual Setup** -> **Protocol**로 이동하여 **3G**를 선택한 후 **Apply**를 클릭하세요.

    ![](https://static.gl.inet.com/docs/router/en/4/faq/x3000_xe3000_connection/3.png){class="glboxshadow gl-90-desktop"}

    ![](https://static.gl.inet.com/docs/router/en/4/faq/x3000_xe3000_connection/4.png){class="glboxshadow gl-90-desktop"}

    펌웨어 ver.4.8 이상에서는 **SIM Card Settings** -> **Protocol**로 이동하여 **3G**를 선택한 후 **Apply**를 클릭하세요.

    ![](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/sim_settings_protocol.png){class="glboxshadow gl-90-desktop"}

    장치가 자동으로 재연결됩니다. 연결이 성공적인지 확인하기 위해 몇 분 정도 기다리세요.

    **2.3** 일부 SIM 카드는 특정 APN이 필요합니다. SIM 카드가 등록되지 못하는 경우 통신사에 문의하여 제한 사항이 있는지 확인하세요. 필요한 경우 라우터에 올바른 APN을 구성한 후 **Apply**를 클릭하세요.

    ![](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/sim_settings_apn.png){class="glboxshadow gl-90-desktop"}

    **2.4** **Band Masking**을 활성화하고 다시 테스트하세요. 펌웨어 ver.4.7 이전에서는 [이 링크](../interface_guide/internet_cellular_v4.7.md/#band-masking)를 참조하세요. 펌웨어 ver.4.8 이상에서는 [이 링크](../interface_guide/internet_cellular.md/#band-masking)를 참조하세요.

    **2.5** 기지국 타워를 잠금 또는 잠금 해제하고 다시 테스트하세요. 이 기능은 GL-X3000 (Spitz AX), GL-XE3000 (Puli AX) 및 GL-X2000 (Spitz Plus)에서만 사용할 수 있습니다. 자세한 지침은 [여기](../interface_guide/internet_cellular.md/#lock-tower)를 클릭하세요.

    특정 기지국 타워에 잠금하면 라우터가 고품질 네트워크 리소스에 액세스하고 안정적인 셀룰러 연결을 유지할 수 있습니다.

    그러나 일단 타워가 잠금되면 라우터는 새로운 위치로 이동하더라도 재시작 후 해당 타워에 계속 연결을 시도합니다. 이로 인해 라우터가 셀룰러 네트워크에 자동으로 연결하지 못할 수 있습니다. 이 경우 라우터의 웹 관리 패널을 통해 현재 타워의 잠금을 해제하거나 새로운 타워에 수동으로 잠금할 수 있습니다.

    **참고:** 잠금된 타워는 통신사와 장치에서 지원하는 주파수 대역과 일치해야 합니다. 그렇지 않으면 연결이 실패할 수 있습니다.

??? "SIM 호환성 확인"

    **3.1** SIM 유형을 확인하세요. GL.iNet 셀룰러 라우터는 IoT 장치로 인증됩니다. 이론적으로 장치는 IoT 유형 SIM 카드만 지원합니다. SIM 유형이 확실하지 않은 경우 통신사에 문의하세요.

    일반적인 SIM 유형은 다음과 같습니다: data‑only, data‑only + voice, IoT, hotspot. IoT 또는 hotspot SIM 카드 사용을 권장합니다. data-only 또는 data-only + voice SIM 카드는 작동이 보장되지 않습니다.

    **3.2** 일부 SIM 카드는 먼저 활성화해야 합니다. SIM 카드를 휴대폰에 넣었을 때 인터넷에 액세스할 수 있는지 확인한 후 라우터로 옮기세요.

    **3.3** 일부 맞춤형 SIM 카드는 휴대폰 또는 특정 장치에서만 사용할 수 있습니다. SIM 카드가 특정 장치로 잠금되어 있는지 확인하세요.

    **3.4** 미국의 일부 주나 도시(예: 시애틀의 AT&T)에서 장치 IMEI를 통신사에 등록해야 할 수 있습니다. 등록이 확실하지 않은 경우 통신사에 문의하세요.

    **3.5** 웹 관리 패널에 "SIM card not registered"가 표시되는 경우 먼저 위 단계를 시도해 보세요.

    라우터의 전원을 끄고 SIM 카드를 넣은 후 라우터를 재시작하는 것이 좋습니다. 일부 모델은 핫 스왑핑을 지원하지 않아 전원이 켜진 상태에서 넣으면 SIM 카드를 감지하지 못할 수 있습니다.

    모든 안테나가 올바르게 설치되어 있는지 확인하고 셀룰러 신호가 강한 야외 지역에서 다시 테스트하세요. 신호가 약하면 SIM 카드가 네트워크에 등록되지 못할 수 있습니다.

    문제가 지속되면 SIM 카드가 라우터와 호환되지 않을 수 있습니다. 추가 지원을 위해 네트워크 통신사에 문의하세요.

    통신사에서 문제가 SIM 카드와 관련이 없다고 확인하는 경우 [support@gl-inet.com](mailto:support@gl-inet.com)로 지원팀에 문의하세요.

    **3.6** SIM 카드가 등록되고 IP 주소를 얻을 수 있지만 인터넷에 액세스할 수 없는 경우(업로드는 작동하지만 다운로드는 안 됨), SIM 카드가 네트워크 통신사에서 제한되었을 가능성이 높습니다. 통신사에 문의하여 제한을 해제하거나 아래와 같이 TTL을 65로 설정하고 다시 테스트하세요.

    ![](https://static.gl.inet.com/docs/router/en/4/faq/x3000_xe3000_connection/5.png){class="glboxshadow gl-90-desktop"}

    ![](https://static.gl.inet.com/docs/router/en/4/faq/x3000_xe3000_connection/6.png){class="glboxshadow gl-90-desktop"}

    네트워크 통신사에 문의할 때 장치 모뎬 이름, IMEI, SIM ICCID 및 라우터 모델을 제공하세요.

위의 방법으로도 문제가 해결되지 않으면 [support@gl-inet.com](mailto:support@gl-inet.com)로 지원팀에 문의하세요.
