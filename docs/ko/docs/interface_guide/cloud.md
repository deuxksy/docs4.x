# GL.iNet GoodCloud

## 목차

- [소개](#소개)
- [GoodCloud에 기기 등록하기](#goodcloud에-기기-등록하기)
    - [펌웨어 v4.6 이하](#펌웨어-v46-이하)
        - [GoodCloud 활성화](#goodcloud-활성화)
        - [계정 가입](#계정-가입)
        - [기기 추가](#기기-추가)
        - [등록 정보](#등록-정보)
        - [기기 등록 해제](#기기-등록-해제)
    - [펌웨어 v4.7 이상](#펌웨어-v47-이상)
        - [Cloud Service 활성화](#cloud-service-활성화)
        - [등록 정보](#등록-정보_1)
        - [기기 등록 해제](#기기-등록-해제_1)
- [기기 관리](#기기-관리)
    - [시스템 정보 및 작업](#시스템-정보-및-작업)
    - [기기 상세 정보](#기기-상세-정보)
        - [기본 정보](#기본-정보)
        - [통계](#통계)
        - [네트워크 설정](#네트워크-설정)
        - [클라이언트 목록](#클라이언트-목록)
- [원격 접속](#원격-접속)
    - [원격 GUI](#원격-gui)
    - [원격 SSH](#원격-ssh)
- [설정 수정](#설정-수정)
- [이메일 알림](#이메일-알림)
- [Site to Site](#site-to-site)
- [GoodCloud와 VPN](#goodcloud와-vpn)
- [로그 보기](#로그-보기)
- [Cloud 비활성화](#cloud-비활성화)
- [계정 삭제](#계정-삭제)

## 소개

GL.iNet [GoodCloud](https://www.goodcloud.xyz){target="_blank"}는 연결된 기기의 원격 배포 및 관리를 간소화하기 위해 설계된 플랫폼입니다. GL.iNet 라우터에 쉽게 원격으로 접속하고 관리할 수 있는 방법을 제공합니다. 네트워크 기기를 클라우드에 중앙 집중화함으로써 사용자는 네트워크 구성 배포 및 소프트웨어 업그레이드와 같은 일괄 관리 작업을 효율적으로 수행할 수 있습니다. 또한 라우터의 웹 관리 패널에 원격으로 접속하거나 SSH를 통해 라우터의 터미널에 연결하여 지역 간, 종단 간 네트워크 기기 관리를 실현할 수 있습니다.

GoodCloud를 사용하면 다음을 할 수 있습니다:

1. 라우터의 실시간 상태 확인
    - 온라인/오프라인 상태 모니터링
    - 실시간 RAM 사용량 및 부하 평균 확인
    - 온라인/오프라인 상태 변경에 대한 이메일 알림 수신

2. 라우터 원격 설정
    - 라우터 설정 구성 (예: SSID 및 비밀번호)
    - 원격 SSH 접속
    - WebUI 원격 접속
    - 다른 사용자와 라우터 접속 공유

3. 연결된 클라이언트 원격 모니터링
    - 네트워크에 연결된 기기 확인
    - 실시간 트래픽 모니터링 및 클라이언트 차단
    - 새 연결 및 차단 이벤트에 대한 이메일 알림 수신

4. 일괄 작업 수행
    - 일괄 재부팅
    - 일괄 펌웨어 업그레이드

5. Site-to-Site 연결 설정
    - Virtual Office: 사무실 네트워크를 다른 지사로 확장
    - 출장: 사무실 시스템 원격 접속 (예: OA, CRM, MySQL)
    - 스마트 홈: 홈 기기 원격 접속 (예: IP 카메라, NAS)

여러 기기를 관리하고 일괄 작업, 다중 계정 관리, 맞춤형 솔루션과 같은 고급 기능을 사용해야 한다면 유료 플랜을 선택하세요. 자세한 내용은 [여기](https://www.gl-inet.com/solutions/goodcloud/){target="_blank"}를 클릭하고, [support@glinet.biz](mailto:support@glinet.biz)로 문의해 주세요.

## GoodCloud에 기기 등록하기

기기를 클라우드 플랫폼에 성공적으로 연결하려면 펌웨어 버전에 해당하는 등록 절차를 따르세요.

### 펌웨어 v4.6 이하

#### GoodCloud 활성화

라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **GoodCloud**로 이동합니다. 스위치를 토글하여 GoodCloud를 활성화합니다.

![enable goodcloud](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/enable_goodcloud_1.png){class="glboxshadow"}

필요에 따라 **Remote SSH**와 **Remote Web Access**를 활성화하고, 가장 가까운 서버를 선택한 후 **Terms of Service & Privacy Policy**를 읽고 동의한 다음 **Apply**를 클릭합니다.

![enable goodcloud](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/enable_goodcloud_2.png){class="glboxshadow"}

- **Remote SSH**: GoodCloud를 통해 라우터의 터미널에 원격으로 접속합니다.

- **Remote Web Access**: GoodCloud를 통해 라우터의 웹 관리 패널에 원격으로 접속합니다.

- **Data Server**: 기기 위치에서 가장 가까운 서버를 선택하세요. 아시아 태평양(일본), 미국(오레곤), 유럽(아일랜드) 세 가지 옵션이 있습니다.

#### 계정 가입

[GoodCloud 웹사이트](https://www.goodcloud.xyz){target="_blank"}를 방문하여 계정에 가입하고 로그인합니다.

인증 이메일을 받지 못한 경우 스팸 폴더를 확인하거나 몇 분 정도 기다린 후 다시 시도하세요. 가입에 문제가 있으면 [support@glinet.biz](mailto:support@glinet.biz)로 이메일을 보내 도움을 요청하세요.

#### 기기 추가

Cloud 플랫폼에서 **Devices** -> **Bound Devices** -> **Add Devices**로 이동합니다.

![add device](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/add_devices_1.png){class="glboxshadow"}

GoodCloud 계정에 기기를 등록하는 세 가지 방법이 있습니다: Auto Discover, Manually Add, Bulk Import.

??? "Auto Discover"

    GoodCloud 웹사이트에 접속하는 데 사용하는 기기와 라우터가 같은 네트워크에 있는 경우 **Auto discover**를 시도할 수 있습니다.

    드롭다운 목록에서 기기를 선택하고 **DDNS / Device ID**를 입력합니다. 이 정보는 라우터 하단이나 웹 관리 패널의 GoodCloud 페이지에서 찾을 수 있습니다.

    ![add device, auto discover](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/add_devices_auto.jpg){class="glboxshadow"}

    Device ID를 찾으려면 [이 링크](../faq/where_to_find_the_device_id_mac_sn.md)를 참조하세요.

??? "Manually Add"

    기기가 목록에 없으면 **Manually add**를 클릭하고 라우터 정보를 입력합니다. 요청된 모든 정보는 라우터 하단이나 웹 관리 패널의 GoodCloud 페이지에서 찾을 수 있습니다.

    ![manually add device](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/add_devices_manual.jpg){class="glboxshadow"}

??? "Bulk Import"

    **Bulk Import**는 많은 수의 기기를 관리하는 사용자를 위해 설계되었습니다. Microsoft Excel 파일을 통해 여러 기기를 가져올 수 있습니다.

    ![bulk import](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/add_devices_bulk.jpg){class="glboxshadow"}

#### 등록 정보

등록에 성공한 후 라우터의 웹 관리 패널에 다시 로그인하고 **APPLICATIONS** -> **GoodCloud**로 이동합니다. 이 페이지를 새로고침하면 등록된 GoodCloud 사용자 이름과 날짜가 표시됩니다.

![goodcloud bound](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/bind_info_1.png){class="glboxshadow"}

#### 기기 등록 해제

라우터 등록을 해제하려면 라우터의 웹 관리 패널에 로그인하고 **APPLICATION** -> **GoodCloud**로 이동한 다음 **Unbind**를 클릭합니다.

![goodcloud unbind](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/unbind_router_1.png){class="glboxshadow"}

또는 GoodCloud 플랫폼의 Bound Devices 목록에서 해당 기기를 제거할 수 있습니다. 그러면 라우터의 웹 관리 패널이 동기화되어 최신 기기 등록 상태를 반영합니다.

문제가 있으면 [support@glinet.biz](mailto:support@glinet.biz)로 이메일을 보내 도움을 요청하세요.

### 펌웨어 v4.7 이상

#### Cloud Service 활성화

라우터의 웹 관리 패널에 로그인하고 **CLOUD SERVICE** -> **GoodCloud**로 이동합니다.

**Get Started** 버튼을 클릭하면 오른쪽 상단에 Cloud Service 팝업 창이 나타납니다. **Enable**을 클릭하여 Cloud Service를 사용합니다.

![enable cloud service](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/enable_cloud_service.jpg){class="glboxshadow"}

GoodCloud 계정에 로그인합니다.

![log in goodcloud](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/goodcloud_login.png){class="glboxshadow"}

계정이 없으면 가입한 후 로그인하세요. 가입이 완료되면 라우터가 자동으로 이 계정에 등록됩니다.

![sign up goodcloud](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/sign_up.png){class="glboxshadow"}

인증 이메일을 받지 못한 경우 스팸 폴더를 확인하거나 몇 분 정도 기다린 후 다시 시도하세요. 가입에 문제가 있으면 [support@glinet.biz](mailto:support@glinet.biz)로 이메일을 보내 도움을 요청하세요.

#### 등록 정보

등록에 성공한 후 라우터의 웹 관리 패널에 다시 로그인하고 오른쪽 상단의 Cloud 아이콘을 클릭하면 등록된 GoodCloud 사용자 이름과 날짜, Device ID, Device MAC, Device S/N을 확인할 수 있습니다.

![cloud info](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/cloud_info.png){class="glboxshadow"}

웹 관리 패널에서 **CLOUD SERVICES** -> **GoodCloud**로 이동하여 라우터의 원격 접속을 활성화하거나 비활성화할 수 있습니다.

![goodcloud bound](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/bind_info_2.png){class="glboxshadow"}

- **Remote SSH**: GoodCloud를 통해 라우터의 터미널에 원격으로 접속합니다.

- **Remote Web Access**: GoodCloud를 통해 라우터의 웹 관리 패널에 원격으로 접속합니다.

- **View Logs**: GoodCloud의 API 호출 로그를 표시합니다.

#### 기기 등록 해제

라우터 등록을 해제하려면 라우터의 웹 관리 패널에 로그인합니다. 오른쪽 상단의 Cloud 아이콘을 클릭하고 **Unbind**를 클릭합니다.

![goodcloud unbind](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/unbind_router_2.png){class="glboxshadow"}

또는 GoodCloud 플랫폼의 Bound Devices 목록에서 해당 기기를 제거할 수 있습니다. 그러면 라우터의 웹 관리 패널이 동기화되어 최신 기기 등록 상태를 반영합니다.

문제가 있으면 [support@glinet.biz](mailto:support@glinet.biz)로 이메일을 보내 도움을 요청하세요.

## 기기 관리

### 시스템 정보 및 작업

[GoodCloud](https://www.goodcloud.xyz){target="_blank"} -> **Bound Devices**에서 계정에 등록된 모든 기기의 시스템 정보(예: 모델, 버전, MAC 주소, IP 주소)와 상태(예: 온라인, 오프라인)를 확인할 수 있습니다.

![devices info](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/devices_info.png){class="glboxshadow"}

기기를 선택한 후 오른쪽 상단에서 설정 수정, 펌웨어 업데이트, 기기 원격 접속, 재부팅 또는 초기화와 같은 작업을 수행할 수 있습니다.

![device actions1](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/device_actions1.png){class="glboxshadow"}

![device actions2](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/device_actions2.jpg){class="glboxshadow"}

목록 헤더의 가장 오른쪽에 있는 기어 아이콘을 클릭하면 열 표시와 순서를 사용자 지정하여 가장 중요한 기기 정보에 집중할 수 있습니다.

![column display](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/column_display.png){class="glboxshadow"}

### 기기 상세 정보

[GoodCloud](https://www.goodcloud.xyz){target="_blank"} -> **Bound Devices**에서 기기 이름을 클릭하면 기기 상세 정보 페이지로 이동합니다. 이 페이지에는 라우터의 기본 정보, 통계 데이터, 네트워크 설정, 클라이언트 목록 등이 표시됩니다.

![Device detail info](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/device_details.png){class="glboxshadow"}

#### 기본 정보

![basic info](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/basic_info.png){class="glboxshadow"}

#### 통계

![statistics](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/statistics.png){class="glboxshadow"}

#### 네트워크 설정

이 페이지에는 라우터의 네트워크 구성과 Wi-Fi 설정이 표시됩니다.

![status overview](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/device_overview.png){class="glboxshadow"}

#### 클라이언트 목록

![clients list](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/clients_list.png){class="glboxshadow"}

## 원격 접속

[GoodCloud](https://www.goodcloud.xyz){target="_blank"} -> **Bound Devices**에서 접속할 기기 이름을 클릭하여 상세 페이지로 이동하면 오른쪽 상단에 원격 작업이 표시됩니다.

![remote access](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/remote_access.png){class="glboxshadow"}

### 원격 GUI

**Remote GUI**를 클릭하여 라우터의 웹 관리 패널에 원격으로 접속합니다.

![remote access web admin panel](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/remote_web_admin_panel.png){class="glboxshadow"}

이 옵션이 회색으로 표시되거나 사용할 수 없는 경우 이 기능이 비활성화되어 있을 수 있습니다. GoodCloud를 통해 접속하기 전에 라우터의 웹 관리 패널에서 먼저 활성화하세요.

이 옵션을 클릭할 수 있지만 응답이 없는 경우 브라우저의 시크릿/InPrivate 모드를 사용해 보세요.

### 원격 SSH

**Remote SSH**를 클릭하여 SSH를 통해 라우터의 터미널에 원격으로 접속합니다.

![remote access device terminal](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/remote_terminal.png){class="glboxshadow"}

이 옵션이 회색으로 표시되거나 사용할 수 없는 경우 이 기능이 비활성화되어 있을 수 있습니다. GoodCloud를 통해 접속하기 전에 라우터의 웹 관리 패널에서 먼저 활성화하세요.

이 옵션을 클릭할 수 있지만 응답이 없는 경우 브라우저의 시크릿/InPrivate 모드를 사용해 보세요.

## 설정 수정

단일 기기 또는 여러 기기에 대해 여러 매개변수를 구성할 수 있습니다.

[GoodCloud](https://www.goodcloud.xyz){target="_blank"} -> **Bound Devices**에서 구성할 기기를 선택하고 오른쪽 상단의 **Settings** -> **Modify Settings**를 클릭합니다.

![device settings 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/modify_settings_1.png){class="glboxshadow"}

여기서 무선, 이더넷, 보안, 포트 포워딩, LAN 및 시스템 설정을 포함한 라우터의 네트워크 설정을 확인하고 수정할 수 있습니다.

![device settings 2](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/modify_settings_2.png){class="glboxshadow"}

## 이메일 알림

기기 상태가 변경되거나(온라인/오프라인) 새 클라이언트가 연결될 때 이메일 알림을 설정할 수 있습니다.

[GoodCloud](https://www.goodcloud.xyz){target="_blank"} -> **Notifications**에서 오른쪽 상단의 **Add Rule** 버튼을 클릭합니다.

![notifications 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/notifications1.png){class="glboxshadow"}

모니터링할 기기를 선택하고 **Next**를 클릭합니다.

![notifications 2](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/notifications2.png){class="glboxshadow"}

기기 온라인/오프라인 상태와 같은 트리거 이벤트를 선택하고 **Next**를 클릭합니다.

![notifications 3](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/notifications3.png){class="glboxshadow"}

![notifications 4](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/notifications4.png){class="glboxshadow"}

규칙 설정을 확인하고 **Apply**를 클릭합니다.

![notifications 5](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/notifications5.png){class="glboxshadow"}

Notifications 목록에서 생성한 알림 규칙을 볼 수 있습니다. 개인 사용자는 하나의 알림 규칙만 생성할 수 있습니다. 여러 기기를 일괄 관리해야 하는 경우 플랜을 업그레이드하려면 문의해 주세요.

![notifications 6](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/notifications6.png){class="glboxshadow"}

## Site to Site

[GoodCloud Site to Site](../tutorials/goodcloud_site_to_site.md)를 참조하세요.

## GoodCloud와 VPN

라우터에서 **GoodCloud**와 **VPN client**를 동시에 활성화하면 라우터와 GoodCloud 서버 간의 연결은 기본적으로 VPN을 통과하지 않습니다. 이를 통해 GoodCloud 서비스에 더 안정적인 연결을 보장합니다.

하지만 GoodCloud 연결이 VPN을 통과하도록 하려면 라우터의 웹 관리 패널에서 이 설정을 변경할 수 있습니다. VPN -> VPN Dashboard -> VPN Client -> Options로 이동하여 "Services from GL.iNet Use VPN" 옵션을 활성화합니다.

![Services from GL.iNet use VPN](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/goodcloud_vpn.png){class="glboxshadow"}

GoodCloud를 VPN을 통해 라우팅하면 특히 다음과 같은 경우 클라우드 연결의 안정성에 영향을 줄 수 있습니다:

* VPN 연결이 불안정한 경우
* VPN 제공업체가 GoodCloud 트래픽을 필터링하거나 차단하는 경우
* VPN이 연결에 상당한 지연을 추가하는 경우

최적의 성능과 안정성을 위해 GoodCloud가 VPN을 우회하는 기본 설정을 유지하는 것이 일반적으로 권장됩니다.

## 로그 보기

Activity Logs, Device Logs, Upgrade Logs, Alert Logs, Device Settings Logs를 포함한 GoodCloud 로그를 필요에 따라 볼 수 있습니다.

[GoodCloud](https://www.goodcloud.xyz){target="_blank"} -> **Logs**에서 드롭다운 목록에서 보려는 로그를 선택합니다.

![View Logs](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/view_logs.png){class="glboxshadow"}

## Cloud 비활성화

더 이상 기기를 클라우드 플랫폼에 연결하지 않으려면 라우터의 웹 관리 패널에서 Cloud Service를 비활성화할 수 있습니다.

??? "펌웨어 v4.6 이하"

    라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **GoodCloud**로 이동한 다음 스위치를 토글하여 GoodCloud를 비활성화하고 **Apply**를 클릭합니다.

    ![disable cloud 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/disable_cloud_1.jpg){class="glboxshadow"}

    비활성화하면 인터페이스가 다음과 같이 표시됩니다.

    ![disabled cloud 1](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/disabled_cloud.png){class="glboxshadow"}

??? "펌웨어 v4.7 이상"

    라우터의 웹 관리 패널에 로그인하고 오른쪽 상단의 Cloud 아이콘을 클릭합니다.

    ![disable cloud 2](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/disable_cloud_2.png){class="glboxshadow"}

    비활성화하면 인터페이스가 다음과 같이 표시됩니다.

    ![disabled cloud 2](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/disabled_cloud_2.png){class="glboxshadow"}

## 계정 삭제

보안상의 이유로 더 이상 사용하지 않는 계정은 삭제할 수 있습니다.

[GoodCloud](https://www.goodcloud.xyz){target="_blank"} 플랫폼에서 오른쪽 상단의 사용자 이름을 클릭하고 **Personal Center**를 선택합니다. 페이지 하단으로 스크롤하여 **Delete Account**를 클릭합니다.

![delete account](https://static.gl-inet.com/docs/router/en/4/interface_guide/cloud/delete_account.png){class="glboxshadow"}

!!! 참고

    삭제하면 복구 옵션 없이 모든 관련 서비스, 데이터 및 개인 정보가 영구적으로 삭제됩니다.

    계정이 조직에 속해 있는 경우 계정을 삭제하기 전에 먼저 모든 조직에서 탈퇴하세요.

---

여전히 질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
