# 셀룰러를 통해 인터넷에 연결

**참고**: 이 가이드는 펌웨어 v4.8을 기준으로 합니다. 이전 버전은 [여기](internet_cellular_v4.7.md)를 참조하세요.

---

대부분의 GL.iNet 라우터는 셀룰러 연결을 지원합니다. 이 가이드에서는 세 가지 유형의 모델을 다룹니다.

1. **내장 4G 단일 SIM 모델**

    GL-E750 (Mudi)와 같이 단일 SIM 카드 슬롯이 있는 내장 4G 모듈이 포함된 일부 모델입니다. [단일 SIM 모델 설정](#setup-for-single-sim-models)을 참조하세요.

2. **내장 5G 듀얼 SIM 모델**

    GL-X3000 (Spitz AX)와 같이 듀얼 SIM 카드 슬롯이 있는 내장 5G 모듈이 포함된 일부 모델입니다. 웹 관리 패널의 셀룰러 설정은 약간 다를 수 있습니다. [듀얼 SIM 모델 설정](#setup-for-dual-sim-models)을 참조하세요.

3. **USB 모뎀 호환 모델**

    GL-MT3000 (Beryl AX)와 같이 내장 SIM 카드 슬롯은 없지만 USB 포트가 있어 USB 모뎀을 통해 셀룰러 연결을 지원하는 일부 모델입니다. [USB 모뎀 설정](#setup-for-usb-modem)을 참조하세요.

**참고:** 일부 SIM 카드는 처음 사용하기 전에 활성화가 필요할 수 있습니다. 호환성을 위해 라우터에 SIM 카드를 삽입하기 전에 스마트폰에서 SIM 카드를 활성화하세요.

## 단일 SIM 모델 설정

다음 단계는 내장 셀룰러 모뎀과 단일 SIM 카드 슬롯이 있는 모델에 적용됩니다.

여기서는 **GL-E750 (Mudi)**를 예로 들어 설명합니다.

라우터의 전원을 먼저 끄고, 미리 활성화된 SIM 카드를 슬롯에 삽입한 다음 전원을 켜는 것을 권장합니다. 라우터가 부팅된 후에 SIM 카드를 삽입하면 웹 관리 패널이 자동으로 업데이트되지 않을 수 있습니다. 이 경우 페이지를 새로고침하거나 라우터를 재시작하세요.

### 자동 설정

라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Cellular**로 이동합니다.

1. SIM 카드가 삽입되지 않은 경우 "SIM 카드가 감지되지 않았습니다"라는 메시지가 표시됩니다.

    ![single no sim](https://static.gl-inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/single_no_sim.png){class="glboxshadow"}

2. SIM 카드를 삽입합니다. 아래와 같이 연결을 시작합니다.

    ![single sim connecting](https://static.gl-inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/single_sim_connecting.png){class="glboxshadow"}

    자동으로 연결되지 않은 경우 **Connect** 버튼을 클릭합니다.

    SIM 카드가 감지되지 않은 경우 라우터를 재시작하여 감지되는지 확인하세요.

3. 셀룰러 네트워크에 연결되면 페이지에 녹색 점과 함께 네트워크 세부 정보가 표시되어 연결이 성공했음을 나타냅니다.

    ![single sim connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/single_sim_connected.png){class="glboxshadow"}

자동 설정이 실패하면 [수동 설정](#manual-setup-single-sim)을 시도하세요.

### 수동 설정 {#manual-setup-single-sim}

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular**로 이동한 다음 **SIM Card Settings**를 클릭합니다.

![sim card settings](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/single_sim_settings_1.png){class="glboxshadow"}

현재 SIM 카드의 셀룰러 설정을 보거나 수정할 수 있습니다.

**참고**: 일부 SIM 카드는 특정 APN이 필요할 수 있습니다. SIM 카드가 등록되지 않으면 이동통신사에 문의하여 제한 사항이 있는지 확인하세요. 필요한 경우 라우터에 올바른 APN을 구성하세요.

변경 사항을 적용하면 재연결이 트리거됩니다.

![single sim card settings 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/single_sim_settings_2.png){class="glboxshadow"}

- **APN**: APN (Access Point Name)은 셀룰러 네트워크 연결에 필요한 게이트웨이 매개변수입니다. 라우터가 이동통신사가 제공하는 인터넷에 연결할 수 있도록 합니다. 기본 APN을 사용하거나 이동통신사가 제공하는 사용자 지정 APN을 설정할 수 있습니다.

- **Protocol**: 셀룰러 통신 프로토콜(예: 3G, QMI 또는 QCM). 일반적으로 자동 감지되며 모뎀과 이동통신사 요구 사항에 맞게 변경할 수 있습니다.

- **Port**: 셀룰러 모뎀과 통신하는 데 사용되는 시리얼 포트입니다. 일반적으로 자동 감지되며 수동 조정이 필요하지 않습니다.

- **TTL**: TTL(Time To Live)은 패킷이 네트워크에서 존재할 수 있는 최대 시간을 정의합니다. 기본적으로 라우터는 클라이언트 장치에서 들어오는 패킷의 TTL을 1씩 줄인 후 포워딩합니다. 재정의해야 하는 경우 여기에 고정 값을 설정할 수 있습니다. TTL 설정은 IPv4에만 유효합니다.

- **HL**: IPv6에서 HL(Hop Limit)은 네트워크에서 데이터 패킷의 전송 홉 수를 제한하며 IPv4의 TTL과 동일한 역할을 합니다.

- **MTU**: 기본 MTU 값은 1500바이트입니다.

- **Authentication**: 이동통신사가 요구하는 인증 방법(예: NONE, PAP, CHAP)을 선택합니다. 자격 증명이 필요하지 않은 경우 일반적으로 NONE으로 설정됩니다.

- **Band Masking**: 라우터가 특정 대역을 차단하거나 특정 셀룰러 대역만 사용하도록 하려면 Band Masking을 활성화할 수 있습니다. 자세한 내용은 [여기](#band-masking)를 클릭하세요.

## 듀얼 SIM 모델 설정

다음 단계는 듀얼 SIM 카드를 지원하는 내장 셀룰러 모뎀이 있는 모델에 적용됩니다. 페이지는 단일 SIM 모델과 약간 다를 수 있습니다.

여기서는 **GL-X3000 (Spitz AX)**를 예로 들어 설명합니다. 듀얼 SIM, 단일 대기 모드를 지원합니다. 즉, 셀룰러 액세스를 위해 두 개의 SIM 카드를 장착할 수 있지만 한 번에 하나의 SIM 카드만 활성화할 수 있습니다. 두 SIM 카드 간에 수동으로 전환할 수 있습니다.

라우터의 전원을 먼저 끄고, 미리 활성화된 SIM 카드를 슬롯에 삽입한 다음 전원을 켜는 것을 권장합니다. 라우터가 부팅된 후에 SIM 카드를 삽입하면 웹 관리 패널이 자동으로 업데이트되지 않을 수 있습니다. 이 경우 페이지를 새로고침하거나 라우터를 재시작하세요.

### 자동 설정

라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Cellular**로 이동합니다.

1. SIM 카드가 삽입되지 않은 경우 "SIM 카드가 감지되지 않았습니다"라는 메시지가 표시됩니다.

    ![no sim](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/no_sim.png){class="glboxshadow"}

2. SIM 카드가 삽입되면 페이지가 아래와 같이 표시됩니다. **Connect**를 클릭합니다.

    ![cellular unconnected](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/cellular_unconnected.png){class="glboxshadow"}

    SIM 카드가 감지되지 않은 경우 라우터를 재시작하여 감지되는지 확인하세요.

3. 셀룰러 네트워크에 연결되면 페이지에 녹색 점과 함께 네트워크 세부 정보가 표시되어 연결이 성공했음을 나타냅니다.

    ![cellular connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/cellular_connected.png){class="glboxshadow"}

4. **View More Information**을 클릭하여 모뎀 세부 정보, SIM 카드 세부 정보, 인터넷 세부 정보, 셀룰러 신호를 포함한 더 많은 셀룰러 정보를 표시합니다.

    ![view more info](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/view_more_info.png){class="glboxshadow"}

    ![cellular info](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/cellular_info.jpg){class="glboxshadow gl-90-desktop"}

자동 설정이 실패하면 [수동 설정](#manual-setup-dual-sim)을 시도하세요.

### 수동 설정 {#manual-setup-dual-sim}

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular**로 이동한 다음 **SIM Card Settings**를 클릭합니다.

![sim card settings 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/sim_card_settings_1.png){class="glboxshadow"}

현재 SIM 카드의 셀룰러 설정을 보거나 수정할 수 있습니다.

**참고**: 일부 SIM 카드는 특정 APN이 필요할 수 있습니다. SIM 카드가 등록되지 않으면 이동통신사에 문의하여 제한 사항이 있는지 확인하세요. 필요한 경우 라우터에 올바른 APN을 구성하세요.

변경 사항을 적용하면 재연결이 트리거됩니다.

![sim card settings 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/sim_card_settings_2.png){class="glboxshadow"}

- **APN**: APN (Access Point Name)은 셀룰러 네트워크 연결에 필요한 게이트웨이 매개변수입니다. 라우터가 이동통신사가 제공하는 인터넷에 연결할 수 있도록 합니다. 기본 APN을 사용하거나 이동통신사가 제공하는 사용자 지정 APN을 설정할 수 있습니다.

- **Protocol**: 모뎀과 이동통신사에 따라 자동 감지되는 셀룰러 통신 프로토콜(예: QMI 또는 QCM).

- **Port**: 셀룰러 모뎀과 통신하기 위해 자동 감지되는 시리얼 포트.

- **TTL**: TTL(Time To Live)은 패킷이 네트워크에서 존재할 수 있는 최대 시간을 정의합니다. 기본적으로 라우터는 클라이언트 장치에서 들어오는 패킷의 TTL을 1씩 줄인 후 포워딩합니다. 재정의해야 하는 경우 여기에 고정 값을 설정할 수 있습니다. TTL 설정은 IPv4에만 유효합니다.

- **HL**: IPv6에서 HL(Hop Limit)은 네트워크에서 데이터 패킷의 전송 홉 수를 제한하며 IPv4의 TTL과 동일한 역할을 합니다.

- **MTU**: 기본 MTU 값은 1500바이트입니다.

- **Authentication**: 이동통신사가 요구하는 인증 방법(예: NONE, PAP, CHAP)을 선택합니다. 자격 증명이 필요하지 않은 경우 일반적으로 NONE으로 설정됩니다.

- **Band Masking**: 라우터가 특정 대역을 차단하거나 특정 셀룰러 대역만 사용하도록 하려면 Band Masking을 활성화할 수 있습니다. 자세한 내용은 [여기](#band-masking)를 클릭하세요.

### SIM 카드 슬롯 설정

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular**로 이동한 다음 **SIM Card Switch**를 클릭합니다.

![sim card switch](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/slot_settings_0.png){class="glboxshadow"}

자동 전환 버튼, 활성 SIM 카드, ICCID 및 네트워크 운영자가 표시됩니다.

![slot_settings_1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/slot_settings_1.png){class="glboxshadow"}

두 개의 SIM 카드가 삽입된 경우 **Auto Switch**를 활성화할 수 있습니다.

![slot_settings_2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/slot_settings_2.png){class="glboxshadow"}

- **Auto Switch**: SIM 1과 SIM 2 간의 자동 전환을 활성화합니다. SIM 자동 전환의 네트워크 감지 방법은 Multi-WAN 페이지에서 구성된 방법과 동일합니다.

- **Preferred SIM Card Slot**: 선호 SIM 카드를 SIM 1 또는 SIM 2로 설정하세요.

- **Failover Interval**: 사용 가능한 값은 5분에서 24시간까지입니다.

    장애 조치 후에도 인터넷 연결을 사용할 수 없는 경우 장치는 선호 SIM 슬롯으로 다시 전환하고 장애 조치를 재시도하기 전에 이 간격 동안 기다립니다.

    이 옵션은 선호 SIM 카드와 백업 SIM 카드 모두 신호가 없는 경우 적용됩니다. 장치는 SIM 카드 간에 전환하여 하나의 카드가 유효한 신호를 얻을 때까지 기다립니다.

    ![failover interval](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/sim_failover_interval.png){class="glboxshadow"}

- **Checking Preferred Slot Status Scheduled**

    활성화하면 장치는 매일 구성된 시간에 선호 SIM 슬롯을 확인하고 선호 SIM이 인터넷 액세스를 다시 얻으면 전환을 시도합니다.

    이렇게 하면 백업 SIM이 과도한 데이터를 소비하는 것을 방지할 수 있습니다. 선호 SIM에 여전히 신호가 없으면 장치는 백업 SIM을 계속 사용합니다.

    ![checking preferred slot status scheduled](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/check_preferred_slot_status.png){class="glboxshadow"}

**참고**: 자동 전환 기능은 즉시 다른 SIM 카드로 전환하지 않습니다. 첫째, 장치는 현재 SIM이 인터넷에 액세스할 수 없다는 것을 확인하는 데 시간이 필요합니다. 둘째, 다른 SIM은 대기 모드가 아니며 활성화하는 데 시간이 필요합니다.

## USB 모뎀 설정

다음 단계는 내장 SIM 카드 슬롯은 없지만 USB 모뎀 연결을 위한 USB 포트가 있는 모델에 적용됩니다.

여기서는 외장 USB 모뎀 **SIMPoYo uFi**가 있는 **GL-MT3000 (Beryl AX)**를 예로 들어 설명합니다.

라우터의 전원을 먼저 끄고, 미리 활성화된 SIM 카드를 USB 모뎀에 삽입하고 모뎀을 라우터의 USB 포트에 연결한 다음 라우터의 전원을 켜는 것을 권장합니다. 라우터가 부팅된 후에 USB 모뎀을 연결하면 웹 관리 패널이 자동으로 업데이트되지 않을 수 있습니다. 이 경우 페이지를 새로고침하거나 라우터를 재시작하세요.

### 빠른 설정

1. 라우터의 전원을 먼저 끕니다. SIM 카드를 USB 모뎀에 삽입하고 모뎀을 라우터의 USB 포트에 연결한 다음 라우터의 전원을 켭니다.

2. 라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Tethering**로 이동한 다음 **Connect**를 클릭합니다.

    ![usb modem 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/usb_modem_1.png){class="glboxshadow"}

    고급 설정(TTL, HL, MTU 등)을 설정해야 하는 경우 **Advanced**를 클릭하여 사용자 지정한 다음 **Connect**를 클릭합니다.

    ![usb modem 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/usb_modem_2.png){class="glboxshadow"}

    연결을 시작합니다.

    ![usb modem 3](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/usb_modem_3.png){class="glboxshadow"}

3. 연결되면 페이지에 녹색 점과 함께 네트워크 세부 정보가 표시되어 연결이 성공했음을 나타냅니다.

    ![usb modem 4](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/usb_modem_4.png){class="glboxshadow"}

    **참고:** 초기 설정 후 USB 모뎀이 연결된 상태로 라우터를 재시작하거나 모뎀을 다시 연결하면 자동으로 인식되며 연결 버튼을 다시 클릭하지 않아도 네트워크 연결이 설정됩니다.

### 호환 모뎀

여기서는 이전에 테스트한 지원 모뎀 목록입니다.

**SIMPoYo uFi**는 Wi-Fi 핫스팟이 있는 컴팩트한 플그 앤 플레이 USB 동글로, 어디서나 빠르고 안정적인 연결을 위해 설계되었습니다. 대부분의 GL.iNet 라우터는 물론 노트북, 배터리 팩, 자동차 USB 포트 및 기타 USB 전원 공급 장치와도 원활하게 작동합니다. 영국 및 34개 유럽 국가에서 30일간 유효한 10GB 무료 데이터가 포함되어 있습니다.

| Model                                  | Cellular | Tested | Tested by       | Comments* |
| -------------------------------------- | -------- | ------ | --------------- | --------- |
| [SIMPoYo 5G uFi](https://www.gl-inet.com/campaign/simpoyo-5g-ufi/)                        | 5G    | Yes    | GL.iNet         |           |
| [SIMPoYo 4G uFi (SP-N150C4)](https://www.gl-inet.com/campaign/simpoyo-ufi/)               | 4G    | Yes    | GL.iNet         |           |
| Quectel EC20-E, EC20-A, EC20-C         | 4G       | Yes    | GL.iNet         |           |
| Quectel EC25-E, EC25-A, EC25-V, EC25-C | 4G       | Yes    | GL.iNet         |           |
| Quectel EC200A series                  | 4G       | Yes    | akw2312         | Host-less |
| Quectel EP06-E, EP06-A                 | 4G       | Yes    | akw2312         |           |
| Quectel EM060K-GL, EM120K-GL           | 4G       | Yes    | akw2312         |           |
| Quectel EM120R-GL, EM160R-GL           | 4G       | Yes    | akw2312         |           |
| Quectel RM520N-GL                      | 5G       | Yes    | akw2312         |           |
| Quectel UC20-E                         | 3G       | Yes    | GL.iNet         |           |
| ZTE ME909s-821                         | 4G       | Yes    | GL.iNet         |           |
| Huawei E1550                           | 3G       | Yes    | GL.iNet         |           |
| Huawei E3276                           | 4G       | Yes    | GL.iNet         |           |
| Huawei E3372                           | 4G       | Yes    | anonymous       |           |
| Huawei E3372h-320 (Ukraine)            | 4G       | Yes    | anonymous       | Host-less |
| TP-Link MA260                          | 3G       | Yes    | GL.iNet         |           |
| ZTE M823                               | 4G       | Yes    | Arnas Risqianto |           |
| ZTE MF190                              | 3G       | Yes    | Arnas Risqianto |           |
| Pantech UML290VW (Verizon)             | 4G       | Yes    | GL.iNet/steven  | QMI       |
| Pantech UML295 (Verizon)               | 4G       | Yes    | GL.iNet/steven  | Host-less |
| Novatel USB551L (Verizon)              | 4G       | Yes    | GL.iNet/steven  | QMI       |
| Verizon U620L (Verizon)                | 4G       | Yes    | anonymous       | Host-less |

- **QMI**: 이 모뎀은 QMI 모드를 지원합니다. SIM 카드 설정에서 셀룰러 통신 프로토콜로 QMI를, 시리얼� 포트로 **/dev/cdc-wdm0**를 선택하세요.

- **Host-less**: 이 모뎀은 Tethering 모드를 지원합니다. Cellular 인터페이스가 아닌 라우터의 Tethering 인터페이스를 통해 연결을 관리하세요.

## 트래픽 통계

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular**로 이동한 다음 **Data Used**를 클릭합니다.

![traffic statistics](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/traffic_statistics_0.png){class="glboxshadow"}

트래픽 통계 페이지로 이동합니다. SIM 카드의 사용된 데이터를 표시하고 데이터 제한 설정을 제공합니다.

![traffic statistics 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/traffic_statistics_1.png){class="glboxshadow"}

사용된 데이터가 데이터 제한량을 초과하면 **Data Cap Amount** 또는 **Data Used**를 수동으로 수정하세요. 그렇지 않으면 네트워크 연결이 끊어지거나 SIM 카드가 자동 전환될 수 있습니다(듀얼 SIM 모델의 경우).

- **Data Used 수정**

    SIM 1/2 Data Used 오른쪽의 **Modify**를 클릭합니다.

    ![traffic statistics 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/traffic_statistics_2.jpg){class="glboxshadow"}

    그런 다음 사용된 데이터를 수정하거나 재설정할 수 있습니다.

    ![traffic statistics 3](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/traffic_statistics_3_new.png){class="glboxshadow"}

- **SIM 데이터 제한 설정**

    SIM 데이터 제한을 설정하려면 먼저 **Save data when power off**를 활성화하세요. 이는 장치 전원을 꺼도 데이터가 저장됨을 의미합니다.

    ![traffic statistics 4](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/traffic_statistics_4.png){class="glboxshadow"}

    그런 다음 SIM 1 또는 SIM 2 제한 설정을 활성화합니다.

    ![traffic statistics 5](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/traffic_statistics_5.jpg){class="glboxshadow"}

듀얼 SIM 모델의 경우 동시에 **SIM Card Slot Auto Switch**를 활성화하는 것을 권장합니다. SIM 1 데이터 제한량이 설정되어 있고 SIM Card Slot Auto Switch가 활성화되어 있으면 SIM 1의 데이터가 데이터 제한량을 초과할 때 SIM 1은 자동으로 SIM 2로 전환되며 SIM 1은 비활성화됩니다.

## 과거 신호 기록

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular**로 이동한 다음 **Historical Signal Record**를 클릭합니다.

![historical signal record](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/historical_signal_record_0.png){class="glboxshadow"}

여기서 셀룰러 연결 품질을 확인할 수 있습니다. 신호가 약한 경우 기지국을 전환하여 더 나은 신호를 시도하세요.

![historical signal record 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/historical_signal_record_1.png){class="glboxshadow"}

![historical signal record 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/historical_signal_record_2.png){class="glboxshadow"}

오른쪽 상단에서 다른 시간 프레임을 선택하여 신호 강도 기록을 봅니다.

![historical signal record 3](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/historical_signal_record_3.png){class="glboxshadow"}

## Band Masking

Band Masking을 사용하면 특정 대역을 차단하거나 선호하는 셀룰러 대역만 사용하여 약한 셀룰러 신호를 개선할 수 있습니다.

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular** -> **SIM Card Settings**로 이동하고 **Enable Band Masking**을 토글합니다.

![single sim band masking](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/single_sim_band_masking.png){class="glboxshadow"}

**Masking Mode**(Block 또는 Open)를 선택한 다음 LTE Bands, 5G NSA Bands 및 5G SA Bands를 선택합니다.

## SMS

[SMS 튜토리얼](sms.md)을 참조하세요.

## SMS 전달

[SMS 전달 튜토리얼](../tutorials/sms_forwarding.md)을 참조하세요.

## 기지국 잠금

!!! note "지원 모델"

    - GL-E5800 (Mudi 7)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-X2000 (Spitz Plus)*

    *GL-X2000 (Spitz Plus)는 펌웨어 4.7 이상에서 이 기능을 지원합니다.

고품질 신호를 수신하고 안정적인 셀룰러 연결을 보장하려면 기지국 잠금을 시도할 수 있습니다.

**참고:** 잠긴 기지국은 이동통신사와 장치가 지원하는 주파수 대역과 일치해야 합니다. 그렇지 않으면 연결이 실패할 수 있습니다.

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular**로 이동합니다. 오른쪽 상단의 세 점 아이콘을 클릭한 다음 **Lock Tower**를 선택합니다.

![lock tower 0](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/lock_tower_0.png){class="glboxshadow"}

**Scan**을 클릭하여 셀룰러 신호 기지국 스캔을 시작합니다. 몇 분 정도 소요됩니다. 스캔 중에는 페이지를 새로고침하지 마세요.

![lock tower 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/lock_tower_1.png){class="glboxshadow"}

사용 가능한 기지국이 표시됩니다.

![lock tower 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/lock_tower_2.png){class="glboxshadow"}

기지국을 클릭하여 세부 정보를 보고 잠급니다.

![lock tower 3](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/lock_tower_3.png){class="glboxshadow"}

**참고**:

1. Cellular 인터페이스가 활성화되어 있으면 장치가 모든 기지국을 스캔하지 못할 수 있습니다.

2. 잠긴 기지국이 셀룰러 설정의 Band Masking 또는 APN 매개변수와 일치하지 않으면 라우터가 셀룰러 네트워크에 연결할 수 없습니다.

3. 기지국을 잠근 후 라우터를 다른 위치로 이동하면 재부팅 후에도 잠긴 기지국에 다시 연결을 시도합니다. 이로 인해 라우터가 새 위치에서 자동으로 셀룰러 네트워크에 연결하지 못할 수 있습니다. 이 경우 현재 기지국을 잠금 해제하거나 새 기지국에 수동으로 잠급니다.

## 운영자 잠금

이 기능은 GL-X3000, GL-XE3000 및 GL-X2000(펌웨어 4.8 이상)에서만 사용할 수 있습니다.

특정 이동통신사에 잠그면 라우터는 해당 운영자의 네트워크만 사용하며 안정적인 연결을 보장하고 의도하지 않은 로밍 요금을 방지합니다. 특히 장치가 외국 네트워크에 연결될 수 있는 국경 지역에서 유용합니다.

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular**로 이동합니다. 오른쪽 상단의 세 점 아이콘을 클릭한 다음 **Lock Operator**를 선택합니다.

![lock operator 0](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/lock_operator_0.png){class="glboxshadow"}

세 가지 잠금 모드가 있습니다:

- **Auto**: 사용 가능한 운영자 네트워크에 자동으로 연결합니다.
- **Manual**: 특정 운영자에 수동으로 잠급니다.
- **Manual-Auto**: 수동 잠금이 실패하면 사용 가능한 운영자 네트워크로 자동 전환됩니다.

![lock operator 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/lock_operator_1.png){class="glboxshadow"}

## 모뎀 AT 명령

모뎀 AT 명령은 셀룰러 모뎀과 통신하는 데 사용되는 표준 명령입니다. 이 기능을 사용하면 명령을 보내고 모뎀 상태를 확인할 수 있습니다.

라우터의 웹 관리 패널에서 **INTERNET** -> **Cellular**로 이동합니다. 오른쪽 상단의 세 점 아이콘을 클릭한 다음 **Modem AT Command**를 선택합니다.

![AT command 0](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_0.jpg){class="glboxshadow"}

AT 명령 페이지로 이동합니다.

![AT command 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_1.png){class="glboxshadow"}

Shortcut이 **Manual command**로 설정된 경우 AT 명령 필드에 원하는 명령을 입력할 수 있습니다.

Shortcut 드롭다운을 클릭하여 **미리 설정된 명령** 목록에서 선택할 수도 있습니다.

![AT command 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_2.png){class="glboxshadow}

다음 명령을 미리 설정으로 사용할 수 있습니다:

* Request IMEI
* Request QCCID
* Request IMSI
* Check Signal Quality
* Reset modem
* Operator Names
* Request SIM card status

예로 "Request IMEI" 바로가기를 선택했습니다. "Send"를 클릭하면 아래와 같은 결과를 얻을 수 있습니다.

![AT command 3](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_3.png){class="glboxshadow"}

오른쪽 하단에서 **Export Debug Info**를 클릭하여 .json 파일을 다운로드할 수 있습니다.

![AT command 4](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/at_command_4.png){class="glboxshadow"}

## 문제 해결

셀룰러 연결 설정에 실패하면 아래 오류 메시지를 클릭하여 관련 솔루션을 확인하세요.

??? note "SIM 없음 / SIM 카드가 감지되지 않았습니다"

    ![no sim](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/no_sim.png){class="glboxshadow"}

    문제 해결을 위한 몇 가지 제안 사항입니다.

    1. 페이지를 새로고침하고 몇 분 기다려 SIM 카드가 감지되는지 확인하세요.

    2. SIM 카드가 올바르게 설치되었는지 확인하세요. SIM 카드의 노치를 카드 슬롯의 해당 마크와 정렬하여 올바른 삽입 방향을 확인하세요.

    3. 라우터 전원을 끄고 SIM 카드를 제거한 다음 다시 삽입한 후 라우터 전원을 다시 켭니다.

    4. 가능한 경우 다른 SIM 카드를 사용해 보세요.

    문제가 지속되면 로그를 다운로드하여 [support@gl-inet.com](mailto:support@gl-inet.com)으로 보내세요.

??? note "SIM 카드가 등록되지 않음 / 인터페이스는 연결되었지만 인터넷에 액세스할 수 없음"

    이 문제에는 두 가지 유형의 오류 메시지가 있습니다:

    - SIM 카드가 등록되지 않음

        ![sim not registered](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/sim_not_registered.png){class="glboxshadow"}

    - 인터페이스는 연결되었지만 인터넷에 액세스할 수 없음

        ![connected no internet](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/connected_no_internet.png){class="glboxshadow"}

    문제 해결을 위한 몇 가지 제안 사항입니다.

    1. 페이지를 새로고침하고 몇 분 기다려 오류가 사라지는지 확인하세요.

    2. **Disconnect**/**Abort**를 클릭한 다음 **Connect**를 클릭하여 재연결을 시도하세요.

    3. 라우터를 재시작하세요.

    4. SIM 카드 상태를 확인하고 활성화되었는지 확인하세요. 활성화된 모바일 데이터 요금제로 정상적으로 인터넷에 액세스할 수 있는지 확인하기 위해 스마트폰에 SIM 카드를 삽입하여 테스트하거나 네트워크 운영자에 문의하여 확인하세요.

    5. 일부 네트워크 운영자는 네트워크 연결을 위해 3G 프로토콜을 요구할 수 있습니다. **SIM Card Settings** -> **Protocol**로 이동하여 **3G**를 선택한 다음 **Apply**를 클릭하세요.

        ![sim protocol](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/sim_settings_protocol.png){class="glboxshadow gl-80-desktop"}

        장치가 자동으로 재연결됩니다. 연결이 성공적인지 확인하기 위해 몇 분 기다리세요.

        ![connecting](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/connecting.png){class="glboxshadow"}

        연결이 성공하면 페이지가 아래와 같이 표시됩니다.

        ![connected](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/connected.png){class="glboxshadow"}

    6. 일부 SIM 카드에는 특정 사용 제한이 있을 수 있습니다(예: 특정 APN 필요). SIM 카드가 등록되지 않으면 운영자에 문의하여 제한 사항이 있는지 확인하세요.

        필요한 경우 **SIM Card Settings** -> **APN**으로 이동하여 라우터에 올바른 APN을 구성한 다음 **Apply**를 클릭하세요.

        ![sim apn](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/sim_settings_apn.png){class="glboxshadow gl-80-desktop"}

    7. **View More Information**을 클릭하여 셀룰러 신호 강도를 확인하세요. 신호가 약한 경우 안테나가 올바르게 설치되었는지 확인하세요. 더 나은 신호 수신을 위해 라우터를 열리고 장애물이 없는 위치로 이동하세요.

        ![cells signal](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/4.8/troubleshoot/cells_info.png){class="glboxshadow gl-80-desktop"}

    8. **Band Masking** 또는 **Lock Tower**가 활성화되어 있는지 확인하세요. 활성화된 경우 기능을 비활성화하고 재연결을 시도하세요.

    문제가 지속되면 로그를 다운로드하여 [support@gl-inet.com](mailto:support@gl-inet.com)으로 보내세요.

## IoT 인증 {#iot-certification}

### AT&T 인증

[att device certification](https://iotdevices.att.com/certified-devices.aspx#) 링크를 클릭하고 장치 이름을 입력하면 찾을 수 있습니다.

![bandmasking](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/certification/at&t_certification.png){class="glboxshadow"}

![bandmasking](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/certification/at&t_certification_2.png){class="glboxshadow"}

### T-Mobile 인증

[t-mobile device certification](https://www.t-mobile.com/business/solutions/iot/device-certification) 링크를 클릭하고 **Filter**에서 5G를 선택하면 찾을 수 있습니다.

![bandmasking](https://static.gl.inet.com/docs/router/en/4/interface_guide/internet_cellular/certification/t-mobile_certification.png){class="glboxshadow"}


---

관련 문서

- [Internet 페이지](internet.md)
- [각 인터넷 액세스 방법의 우선 순위를 설정하는 방법](multi-wan.md)
- [여러 인터넷 액세스 방법을 동시에 사용할 때 로드 밸런스를 설정하는 방법](multi-wan.md)

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
