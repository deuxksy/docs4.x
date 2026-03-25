# 클라이언트

웹 관리 패널 왼쪽에서 **CLIENTS**로 이동합니다.

클라이언트 페이지에는 연결된 기기에 대한 정보가 표시되며, 왼쪽에서 오른쪽으로 기기 이름, 연결 유형, IP 주소, MAC 주소, 속도, 트래픽이 나열됩니다.

## 기기 이름

첫 번째 열에는 기기 이름과 기기 유형이 표시되며, 이는 기기 운영자의 호스트 이름에 따라 달라집니다.

![device name](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/device_name.png){class="glboxshadow"}

기기 이름과 유형을 수정하려면 Action 열의 점 세 개 아이콘을 클릭하고, 드롭다운 메뉴에서 **Modify**를 클릭합니다.

![modify](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/modify.png){class="glboxshadow"}

![modify client device](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/modify_client_device.png){class="glboxshadow"}

## 연결 유형

기기 이름 오른쪽의 파란색 아이콘은 기기의 연결 유형/방법을 나타냅니다.

기기가 네트워크에 연결된 방식(Wi-Fi 또는 이더넷 케이블)을 나타냅니다.

![connection type](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/connection_type.png){class="glboxshadow"}

## IP 및 MAC 주소

두 번째 열에는 연결된 기기의 IP 및 MAC 주소가 나열됩니다.

![ip and mac](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/ip_mac.png){class="glboxshadow"}

많은 기기에서 무작위 MAC 주소를 사용합니다. 연결된 기기에서 무작위 MAC 주소를 사용하는 경우 다음 프롬프트가 나타납니다.

![random mac prompt](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/randomized_mac.png){class="glboxshadow"}

**참고**: 여기서 규칙은 MAC 주소의 두 번째 문자가 2, 6, A 또는 E(대소문자 구분 없음)인 경우 무작위 MAC 주소로 간주된다는 것입니다. 하지만 일부 기기는 다른 규칙을 사용하여 무작위 MAC 주소를 생성할 수 있으므로 이 감지 방법이 정확하지 않을 수 있습니다.

## 속도

세 번째 열에는 연결된 기기의 인터넷 속도가 표시됩니다.

![speed](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/speed.png){class="glboxshadow"}

이 속도는 3분간의 평균 속도입니다.

- 현재 페이지를 10초 동안 열어두면 마지막 10초의 평균 속도가 표시됩니다.
- 현재 페이지를 30초 동안 열어두면 마지막 30초의 평균 속도가 표시됩니다.
- 현재 페이지를 60초 동안 열어두면 마지막 60초의 평균 속도가 표시됩니다.
- 현재 페이지를 3분 동안 열어두면 마지막 3분의 평균 속도가 표시됩니다.
- 현재 페이지를 10분 동안 열어두면 마지막 3분의 평균 속도가 표시됩니다.

## 트래픽

네 번째 열에는 연결된 기기의 인터넷 트래픽이 표시됩니다.

![traffic](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/traffic.png){class="glboxshadow"}

## 고정 IP

다섯 번째 열에서는 연결된 특정 기기에 IP 주소를 한 번의 클릭으로 예약할 수 있습니다.

이 기능은 v4.8부터 사용할 수 있습니다.

LAN 내의 클라이언트에 고정 IP 주소를 지정하면, 해당 클라이언트는 라우터의 DHCP 서버에 액세스할 때마다 항상 동일한 IP 주소를 받습니다.

영구 IP 설정이 필요한 컴퓨터나 서버에 고정 IP 주소를 할당할 수 있습니다.

![reserved ip](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/reserved_ip.png){class="glboxshadow"}

## 차단 목록 {#blocklist}

여섯 번째 열에서는 특정 연결된 기기를 한 번의 클릭으로 차단할 수 있습니다.

액세스 제어 규칙은 기본적으로 차단 목록이며, 필요한 경우 상단에서 허용 목록으로 전환할 수 있습니다.

![blocklist](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/blocklist.jpg){class="glboxshadow"}

![access control](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/blocklist_allowlist.jpg){class="glboxshadow"}

- **차단 목록**: 차단 목록에 있는 MAC 주소를 가진 기기는 이 라우터에 연결할 수 없습니다.

- **허용 목록**: 특정 MAC 주소를 가진 기기만 연결할 수 있으며, IoT 기기 및 기업 네트워크 관리에 적합합니다.

차단 목록을 생성하려면 **(1)**에서 엑셀 형식의 차단 목록을 업로드하거나, **(2)**에서 MAC 주소를 수동으로 입력할 수 있습니다.

![create blocklist](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/create_blocklist.png){class="glboxshadow"}

**방법 1. 클라이언트 가져오기**

액세스 제어 페이지에서 **Import Clients**를 클릭합니다.

![import clients](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/import_clients.png){class="glboxshadow"}

**Download Import Template**를 클릭하면 "mac-template.csv"라는 XLS 워크시트가 다운로드됩니다.

![download template](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/download_template.png){class="glboxshadow"}

파일을 열고 MAC 주소를 가져온 후 저장합니다.

![import csv](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/importcsv.jpg){class="glboxshadow gl-80-desktop"}

저장한 파일을 선택하거나 업로드 영역으로 드래그합니다.

![upload csv](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/dragcsv.jpg){class="glboxshadow  gl-80-desktop"}

업로드가 성공하면 **Import**를 클릭하여 MAC 주소 일괄 가져오기를 완료합니다.

![upload successful](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/upload_successful.png){class="glboxshadow"}

**방법 2. 수동 입력**

액세스 제어 페이지에서 차단하려는 기기의 MAC 주소를 수동으로 입력하고 **Apply**를 클릭합니다.

![input mac manually](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/input_mac_manually.png){class="glboxshadow"}

**참고**: 클라이언트 차단은 기기의 MAC 주소를 기반으로 합니다. 차단된 기기가 다음에 다른 MAC 주소를 사용하면 여전히 라우터에 연결할 수 있습니다.

## 정렬

현재 정렬 유형은 오른쪽 상단에 표시되며, 다른 정렬 유형으로 전환할 수 있습니다.

기본 정렬 유형은 다음과 같습니다:

- 자신의 기기는 항상 맨 위에 표시됩니다.
- 온라인 클라이언트 섹션에서는 기기가 연결된 시간이 늦을수록 목록 상단에 표시됩니다.

![sort](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/sort.png){class="glboxshadow"}

## 작업

### 클라이언트 상세 정보

클라이언트 기기의 상세 정보를 확인하려면 오른쪽 끝 Action 열의 점 세 개 아이콘을 클릭한 다음 드롭다운 메뉴에서 **View Details**를 클릭합니다.

![view details](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/details.png){class="glboxshadow"}

열린 하위 페이지에서 클라이언트 기기에 대한 모든 정보를 확인할 수 있으며, 있는 경우 기기의 모든 IPv6 주소도 포함됩니다.

![client details](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/client_detail.png){class="glboxshadow"}

### 수정

Action 열의 점 세 개 아이콘을 클릭하고, 드롭다운 메뉴에서 **Modify**를 클릭합니다.

![modify](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/modify.png){class="glboxshadow"}

![modify client device](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/modify_client_device.png){class="glboxshadow"}

### 속도 제한

Action 열의 점 세 개 아이콘을 클릭하고, 드롭다운 메뉴에서 **Limit Speed**를 클릭합니다.

![limit speed](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/limit_speed.png){class="glboxshadow"}

![limit speed settings](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/clients_limit_speed_settings.png){class="glboxshadow"}

클라이언트에 속도 제한이 적용되면 속도의 위쪽 화살표와 아래쪽 화살표가 노란색으로 변합니다.

![limited speed](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/limit_speed.jpg){class="glboxshadow"}

Action 열의 점 세 개 아이콘을 클릭하여 속도 제한을 비활성화합니다.

### VPN 터널 사용

**참고**: 이 옵션은 펌웨어 v4.8부터 사용할 수 있으며, MAC 기반 정책이 구성된 경우에만 Action 메뉴에 나타납니다.

MAC 기반 정책으로 클라이언트를 VPN 터널 목록에 추가합니다. 터널에 대한 세부 조정이 필요한 경우 VPN 대시보드로 이동하여 관리합니다.

![use vpn tunnel](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/use-vpn-tunnel.png){class="glboxshadow"}

## 오프라인 클라이언트 제거

오프라인 클라이언트 섹션에서 오른쪽 상단의 **Delete All**을 클릭하여 모든 오프라인 클라이언트를 삭제할 수 있습니다.

특정 클라이언트를 제거하려면 Action 열의 점 세 개 아이콘을 클릭하고, 드롭다운 메뉴에서 **Remove Client**를 클릭합니다.

![remove offline clients](https://static.gl-inet.com/docs/router/en/4/interface_guide/clients/remove_offline.png){class="glboxshadow"}

---

궁금한 점이 있으시면 [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
