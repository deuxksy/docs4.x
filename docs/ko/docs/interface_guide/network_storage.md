# 네트워크 스토리지

## 목차

- [소개](#소개)
- [지원 모델](#지원-모델)
- [저장 장치 연결](#저장-장치-연결)
- [Samba 설정](#samba-설정)
- [WebDAV 설정](#webdav-설정)
- [DLNA 설정](#dlna-설정)
- [Samba 클라이언트](#samba-클라이언트)
- [WebDAV 클라이언트](#webdav-클라이언트)

## 소개

네트워크 스토리지를 사용하면 USB 드라이브나 SD 카드를 라우터에 연결하여 장치 간에 무선 파일 공유가 가능해집니다. 라우터는 저장 장치를 공유 네트워크 드라이브로 변환하여 Wi-Fi에 연결된 모든 장치에서 액세스할 수 있습니다.

일부 GL.iNet 모델에는 MicroSD(TF) 카드 슬롯이 있고 일부 모델에는 USB 포트가 있어 USB 플래시 드라이브와 휴대용 외장 하드 드라이브를 지원합니다. 이러한 저장 장치에 대해 Samba, WebDAV, DLNA를 구성할 수 있으며 NTFS, FAT32, EXT4와 같은 일반적인 형식을 지원합니다.

!!! 참고

    1. USB 하드 드라이브의 소비 전력은 상당히 높습니다. 외부 전원 공급 장치와 함께 사용하십시오. 그렇지 않으면 오작동을 일으킬 수 있습니다.

    2. 일부 모델에는 USB 포트 또는 MicroSD 슬롯이 있지만 저장 공간이 제한적이어서 네트워크 스토리지를 지원하지 않습니다.

    3. 웹 관리 패널에서는 공유 폴더만 관리할 수 있습니다. 저장 장치의 파일을 관리하려면 [모바일 앱](https://www.gl-inet.com/app/#download-app-glinet){target="_blank"}을 사용하십시오.

## 지원 모델

일반적으로 USB 포트나 MicroSD(TF) 슬롯이 있는 모델은 네트워크 스토리지(즉, 파일 공유)를 지원합니다.

플래시 저장 공간이 32MB 이하인 장치는 네트워크 스토리지 기능을 아직 지원하지 않습니다.

| 라우터 모델                           | Samba | Webdav | DLNA | USB 포트 | MicroSD 카드 |
| :------------------------------------- | :---: | :---: | :---: | :------: | :----------: |
| GL-E5800 (Mudi 7)                      | √     | √     | √     | √        | -            |
| GL-MT5000 (Brume 3)                    | √     | √     | √     | √        | -            |
| GL-BE3600 (Slate 7)                    | √     | √     | √     | √        | -            |
| GL-X2000 (Spitz Plus)                  | √     | √     | √     | √        | -            |
| GL-MT6000 (Flint 2)                    | √     | √     | √     | √        | -            |
| GL-XE3000 (Puli AX)                    | √     | √     | √     | √        | √            |
| GL-X3000 (Spitz AX)                    | √     | √     | √     | √        | √            |
| GL-MT3000 (Beryl AX)                   | √     | √     | √     | √        | -            |
| GL-MT2500/GL-MT2500A (Brume 2)         | √     | √     | √     | √        | -            |
| GL-AXT1800 (Slate AX)                  | √     | √     | √     | √        | √            |
| GL-AX1800 (Flint)                      | √     | √     | √     | √        | -            |
| GL-A1300 (Slate Plus)                  | √     | √     | √     | √        | -            |
| GL-S1300 (Convexa-S)                   | √     | √     | √     | √        | -            |
| GL-SFT1200 (Opal)</br>***FW 4.7.2**    | √     | -     | -     | √        | -            |
| GL-E750V2 (Mudi V2)</br>***FW 4.7.2**  | √     | -     | -     | √        | √            |
| GL-AR750S-EXT (Slate)</br>***FW 4.7.2**| √     | -     | -     | √        | √            |

## 저장 장치 연결

TF 카드의 경우 라우터의 전원을 먼저 끄고, TF 카드를 삽입한 다음 라우터의 전원을 켭니다.

USB 드라이브의 경우 USB 포트에 직접 꽂을 수 있습니다. 휴대용 외장 하드 드라이브의 경우 별도의 전원 공급 장치가 있으면 전원 공급 장치에 연결하십시오.

라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **Network Storage**로 이동합니다.

![network storage](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/network_storage_init.png){class="glboxshadow"}

저장 장치를 연결합니다. 감지되면 페이지가 아래와 같이 표시됩니다.

![network storage, disk found](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/disk_found.png){class="glboxshadow"}

## Samba 설정 {#samba-설정}

1. **Enable Samba**를 토글하고 **Apply**를 클릭합니다.

    * Allow Access Samba from WAN: 상위 장치에서 Samba에 액세스하려면 활성화하십시오.

    ![enable samba](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_quick_setup_share/enable_samba.png){class="glboxshadow"}

2. **Quick Setup Share**를 클릭하여 공유 링크를 설정합니다.

    ![samba quick setup share](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_quick_setup_share/samba_quick_setup_share.png){class="glboxshadow"}

3. 사용자를 추가하고 **Next**를 클릭합니다. 이미 계정이 있는 경우 이 단계는 건너뜁니다.

    ![samba quick setup share, add a user](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_quick_setup_share/samba_quick_setup_share_add_user.png){class="glboxshadow"}

4. 삼각형 아이콘을 클릭하여 모든 폴더를 표시합니다. 공유할 폴더를 선택하거나 디스크 이름(disk1_part1)을 클릭하여整个 디스크를 공유합니다. 그런 다음 **Next**를 클릭합니다.

    ![samba quick setup share, add shared folder](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_quick_setup_share/samba_quick_setup_share_add_shared_folder.png){class="glboxshadow"}

5. 공유 폴더를 설정합니다.

    보안상의 이유로 **Anonymous Access**를 활성화하지 않는 것이 좋습니다.

    이전 단계에서 만든 사용자는 기본적으로 **Read-Only User**에 추가됩니다. 이 사용자가 파일을 쓰거나 삭제할 수 있도록 하려면 Read-Only User에서 제거하고 **Writable User**에 추가한 다음 **Apply**를 클릭합니다.

    ![samba quick setup share, shared folder settings](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_quick_setup_share/samba_quick_setup_share_shared_folder_settings.png){class="glboxshadow"}

6. 폴더 액세스 링크를 가져옵니다.

    페이지에 Windows 및 Unix-like OS용 링크가 표시됩니다. Unix-like 시스템에는 Android, iOS, macOS, Ubuntu 등이 포함됩니다.

    이제 이러한 링크를 통해 Samba 서비스로 공유 폴더에 액세스할 수 있습니다. 자세한 내용은 [여기](#samba-클라이언트)를 클릭하십시오.

    ![samba quick setup share, folder access link](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_quick_setup_share/samba_quick_setup_share_folder_access_link.png){class="glboxshadow"}

    **참고:** **Allow Access Samba from WAN**을 활성화하고 상위 네트워크에서 공유 폴더에 액세스하는 경우 액세스 링크의 라우터 IP(기본값 192.168.8.1)을 웹 관리 패널의 INTERNET 페이지에서 찾을 수 있는 라우터의 WAN IP로 바꾸십시오.

---

## WebDAV 설정 {#webdav-설정}

1. **Enable WebDAV**를 토글하고 **Apply**를 클릭합니다.

    * Allow Access WebDAV from WAN: 상위 장치에서 WebDAV에 액세스하려면 활성화하십시오.

    * WebDAV Protocol: **HTTP**는 암호화되지 않으므로 사용자의 책임하에 사용하십시오. **HTTPS**는 암호화되며 자체 서명된 인증서를 사용합니다.

    * WebDAV Port: 충돌이 없는 한 포트 번호를 수정할 필요가 없습니다. 권장 포트 번호 범위는 1024 - 65535입니다.

    ![enable webdav](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_quick_setup_share/enable_webdav.png){class="glboxshadow"}

2. **Quick Setup Share**를 클릭하여 공유 링크를 설정합니다.

    ![enable webdav](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_quick_setup_share/webdav_quick_setup_share.png){class="glboxshadow"}

3. 사용자를 추가하고 **Next**를 클릭합니다. 이미 계정이 있는 경우 이 단계는 건너뜁니다.

    ![webdav quick setup share, add a user](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_quick_setup_share/samba_quick_setup_share_add_user.png){class="glboxshadow"}

4. 삼각형 아이콘을 클릭하여 모든 폴더를 표시합니다. 공유할 폴더를 선택하거나 디스크 이름(disk1_part1)을 클릭하여整个 디스크를 공유합니다. 그런 다음 **Next**를 클릭합니다.

    ![webdav quick setup share, add shared folder](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_quick_setup_share/samba_quick_setup_share_add_shared_folder.png){class="glboxshadow"}

5. 공유 폴더를 설정합니다.

    보안상의 이유로 **Anonymous Access**를 활성화하지 않는 것이 좋습니다.

    이전 단계에서 만든 사용자는 기본적으로 **Read-Only User**에 추가됩니다. 이 사용자가 파일을 쓰거나 삭제할 수 있도록 하려면 Read-Only User에서 제거하고 **Writable User**에 추가한 다음 **Apply**를 클릭합니다.

    ![webdav quick setup share, shared folder settings](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_quick_setup_share/webdav_quick_setup_share_shared_folder_settings.png){class="glboxshadow"}

6. 폴더 액세스 링크를 가져옵니다.

    페이지에 Windows 및 Unix-like OS용 링크가 표시됩니다. Unix-like 시스템에는 Android, iOS, macOS, Ubuntu 등이 포함됩니다.

    이제 이러한 링크를 통해 WebDAV 서비스로 공유 폴더에 액세스할 수 있습니다. 자세한 내용은 [여기](#webdav-클라이언트)를 클릭하십시오.

    ![webdav quick setup share, folder access link](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_quick_setup_share/webdav_quick_setup_share_folder_access_link.png){class="glboxshadow"}

    **참고:** **Allow Access WebDAV from WAN**을 활성화하고 상위 네트워크에서 공유 폴더에 액세스하는 경우 액세스 링크의 라우터 IP(기본값 192.168.8.1)을 웹 관리 패널의 INTERNET 페이지에서 찾을 수 있는 라우터의 WAN IP로 바꾸십시오.

---

## DLNA 설정 {#dlna-설정}

**Enable DLNA**를 토글하고 **Apply**를 클릭합니다.

![network storage, enable dlna](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/enable_dlna.jpg){class="glboxshadow"}

스마트 TV를 라우터에 연결하면 DLNA 서버를 찾습니다.

---

## Samba 클라이언트

=== "Windows"

    Windows 11의 예시이며 Windows 10에도 적용됩니다.

    파일 탐색기를 열고 왼쪽 창에서 **This PC**를 마우스 오른쪽 버튼으로 클릭합니다. 표시되는 상황 메뉴에서 **더 많은 옵션 표시** -> **네트워크 위치 추가**를 선택합니다.

    ![windows 11 add network location](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/windows11_add_network_location.png){class="glboxshadow"}

    **사용자 지정 네트워크 위치 선택**을 클릭한 다음 **Next**를 클릭합니다.

    ![windows 11 add network location](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/windows11_add_network_location_2.png){class="glboxshadow"}

    Samba 액세스 링크를 입력합니다. 그런 다음 **Next**를 클릭합니다.

    ![windows 11 add network location](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/windows11_add_network_location_3.png){class="glboxshadow"}

    이 위치의 이름을 지정합니다. **Next**를 클릭합니다.

    ![windows 11 add network location](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/windows11_add_network_location_4.png){class="glboxshadow"}

    **Finish**를 클릭합니다.

    ![windows 11 add network location](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/windows11_add_network_location_5.png){class="glboxshadow"}

    사용자 이름과 비밀번호가 필요하면 자격 증명을 입력하라는 메시지가 표시됩니다. 그런 다음 **OK**를 클릭합니다.

    ![windows 11 add network location](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/windows11_add_network_location_6.png){class="glboxshadow"}

=== "macOS"

    Finder를 통해 Samba에 액세스할 수 있습니다.

    Finder를 열고 메뉴에서 이동 -> 서버에 연결을 클릭합니다. Samba 액세스 링크를 복사하여 붙여넣습니다.

    ![network storage, mac os finder connect to server](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/finder_connect_to_server.png){class="glboxshadow"}

    사용자 이름과 비밀번호를 묻는 메시지가 표시됩니다. 사용자 이름은 **공유 폴더 설정**을 설정할 때의 사용자 이름입니다.

    익명 액세스를 설정한 경우 아래 이미지에서 **Guest**를 선택하십시오.

    ![network storage, mac os finder connect to server username password](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/finder_username_password.png){class="glboxshadow"}

    **Continue**를 클릭하면 Finder의 사이드바에 Samba가 표시됩니다.

    ![network storage, mac os finder samba connected](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/finder_samba_connected.png){class="glboxshadow"}

=== "Android"

    Samba를 지원하는 Android 앱이 많습니다. 여기서는 [Cx File Explorer](https://play.google.com/store/apps/details?id=com.cxinventor.file.explorer&hl=en&gl=US){target="_blank"}를 예로 들겠습니다.

    홈 페이지에서 **NETWORK**를 클릭합니다.

    ![cx file explorer home page](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/cx_file_explorer_home.png){class="glboxshadow" width="400"}

    **New Location**을 클릭합니다.

    ![cx file explorer home page](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/cx_file_explorer_new_location.png){class="glboxshadow" width="400"}

    **SMB**를 클릭합니다.

    ![cx file explorer home page](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/cx_file_explorer_remote.png){class="glboxshadow" width="350"}

    **Host**, **Username**, **Password**를 입력합니다. **익명 액세스**인 경우 **Anonymous**를 확인하십시오.

    ![cx file explorer home page](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/cx_file_explorer_smb.png){class="glboxshadow" width="350"}

=== "iOS"

    iOS [Files](https://apps.apple.com/us/app/files/id1232058109){target="_blank"} 앱이 Samba를 지원하거나 다른 앱(예: [Documents](https://apps.apple.com/us/app/documents-file-reader-browser/id364901807){target="_blank"})를 사용할 수 있습니다.

    다음 섹션에서는 **Files** 앱과 **Documents** 앱을 사용하여 Samba에 연결하는 방법을 각각 설명합니다.

    - [Files](https://apps.apple.com/us/app/files/id1232058109){target="_blank"} 앱으로 Samba 서버에 연결하는 가이드.

        **Files** 앱을 엽니다. 기본적으로 설치되어 있으므로 홈 화면에서 찾을 수 있습니다. **Files**는 이제 제거 가능한 앱이므로 표시되지 않으면 App Store에서 다시 설치해야 할 수 있습니다.

        ![search files on iphone](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/ios15-iphone-12-pro-home-screen-search-files.jpg){class="glboxshadow" width=300}

        화면 하단에서 **찾아보기** 탭에 있는지 확인합니다. 오른쪽 상단의 "…" (세 개의 점) 아이콘을 탭하여 앱의 상황 메뉴를 표시합니다.

        ![ios files set up SMB](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/ios_files_smb_1.png){class="glboxshadow" width=560}

        메뉴 상단 근처의 **서버에 연결** 옵션을 탭합니다. 다음 화면에서 서버의 연결 URL을 입력합니다. URL은 [공유 링크](#shared-link)에서 찾을 수 있습니다. 계속하려면 오른쪽 상단의 **Next** 버튼을 탭합니다.

        ![ios files set up SMB](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/ios_files_smb_2.png){class="glboxshadow" width=560}

        다음 화면에서 보호된 네트워크 공유에 연결할 경우 인증 자격 증명을 입력할 수 있습니다. **등록된 사용자**를 탭하고 Samba 사용자 이름과 비밀번호로 **이름** 및 **비밀번호** 필드를 작성합니다. **익명 액세스**를 활성화한 경우 대신 "Guest"를 탭할 수 있습니다.

        ![ios files set up SMB](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/ios_files_smb_3.png){class="glboxshadow" width=560}

        오른쪽 상단의 **Next** 버튼을 눌러 연결을 완료합니다. iOS 장치가 서버에 성공적으로 연결되고 사용 가능한 공유 목록을 표시해야 합니다.

        ![ios files set up SMB](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/ios_files_smb_4.png){class="glboxshadow" width=560}

        Samba 공유는 메뉴 하단의 **Shared** 제목 아래에 표시됩니다.

        ![ios files set up SMB](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/ios_files_smb_5.png){class="glboxshadow" width=560"}

    - [Documents](https://apps.apple.com/us/app/documents-file-reader-browser/id364901807){target="_blank"} 앱으로 Samba 서버에 연결하는 가이드.

        오른쪽 하단 모서리의 더하기 버튼을 클릭합니다.

        ![documents samba](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/documents_1.png){class="glboxshadow" width="560"}

        **Add Connection**을 클릭합니다.

        ![documents samba](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/documents_2.png){class="glboxshadow" width="560"}

        **Windows SMB**를 클릭합니다.

        ![documents samba](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/documents_3.png){class="glboxshadow" width="560"}

        **Title**은 이 연결의 이름입니다. **URL**은 액세스 링크입니다. **Login**은 사용자 이름입니다. 익명 액세스인 경우 **Login**과 **Password**를 비워 두십시오.

        설정을 완료하려면 **Done** 버튼을 클릭합니다.

        ![documents samba](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/documents_4_samba.png){class="glboxshadow" width="560"}

## WebDAV 클라이언트

=== "Windows"

    WebDAV를 지원하는 소프트웨어가 많습니다. 예: [RaiDrive](https://www.raidrive.com/){target="_blank"}, [Cyberduck](https://cyberduck.io/download/){target="_blank"}, [WinSCP](https://winscp.net/eng/index.php){target="_blank"}.

    여기서는 RaiDrive를 예로 들겠습니다.

    **Add**를 클릭합니다.

    ![RaiDrive WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/raidrive_add.png){class="glboxshadow"}

    **Storage** 영역에서 **NAS** -> **WebDAV**를 클릭합니다.

    **Address** 영역에서 Address 근처의 확인란을 선택/선택 해제하여 https/http를 전환하고 주소를 입력합니다.

    **Account** 영역에서 사용자 이름과 비밀번호를 입력하거나 **Anonymous**를 확인합니다.

    마지막으로 **Connect**를 클릭하면 파일 탐색기에 X 드라이브가 추가됩니다.

    ![RaiDrive WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/raidrive_new_drive_webdav.png){class="glboxshadow"}

=== "macOS"

    WebDAV를 지원하는 앱이 많습니다. 예: [FE File Explorer](https://apps.apple.com/hk/app/fe-file-explorer/id1444382558?l=en&mt=12){target="_blank"}, [Cyberduck](https://cyberduck.io/download/){target="_blank"}.

    여기서는 FE File Explorer를 예로 들겠습니다.

    추가 버튼을 클릭합니다.

    ![FE File Explorer WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/fe_file_explorer_add.png){class="glboxshadow"}

    **WebDAV**를 선택합니다.

    ![FE File Explorer WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/fe_file_explorer_webdav.png){class="glboxshadow"}

    연결 설정을 입력합니다. 익명 액세스인 경우 **User Name**과 **Password**를 비워 두십시오. 그런 다음 **Save & Connect**를 클릭합니다.

    ![FE File Explorer WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/fe_file_explorer_webdav_connection_setting.png){class="glboxshadow"}

    *다음 보안 서버(null)에서 신뢰할 수 없는 인증서를 사용합니다. 이 서버를 신뢰하시겠습니까?*라는 경고가 표시될 수 있습니다. 이는 자체 서명된 인증서를 사용하기 때문입니다. 신뢰하십시오.

=== "Android"

    WebDAV를 지원하는 iOS 앱이 많습니다. 여기서는 [Cx File Explorer](https://play.google.com/store/apps/details?id=com.cxinventor.file.explorer&hl=en&gl=US){target="_blank"}를 예로 들겠습니다.

    참고: Cx File Explorer는 익명 액세스를 지원하지 않습니다.

    홈 페이지에서 **NETWORK**를 클릭합니다.

    ![cx file explorer home page](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/cx_file_explorer_home.png){class="glboxshadow" width="400"}

    **New Location**을 클릭합니다.

    ![cx file explorer home page](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/cx_file_explorer_new_location.png){class="glboxshadow" width="400"}

    **WebDAV**를 클릭합니다.

    ![cx file explorer home page](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/samba_client/cx_file_explorer_remote.png){class="glboxshadow" width="350"}

    **Host**, **Port**, **Username**, **Password**를 입력합니다.

    ![cx file explorer home page](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/cx_file_explorer_webdav.png){class="glboxshadow" width="350"}

=== "iOS"

    WebDAV를 지원하는 iOS 앱이 많습니다. 여기서는 [Documents](https://apps.apple.com/us/app/documents-file-reader-browser/id364901807){target="_blank"}를 예로 들겠습니다.

    오른쪽 하단 모서리의 더하기 버튼을 클릭합니다.

    ![documents WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/documents_1.png){class="glboxshadow" width="560"}

    **Add Connection**을 클릭합니다.

    ![documents WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/documents_2.png){class="glboxshadow" width="560"}

    **WebDAV Server**를 클릭합니다.

    ![documents WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/documents_3.png){class="glboxshadow" width="560"}

    **Title**은 이 연결의 이름입니다. **URL**은 액세스 링크입니다. **Login**은 사용자 이름입니다.

    설정을 완료하려면 **Done** 버튼을 클릭합니다.

    ![documents WebDAV](https://static.gl-inet.com/docs/router/en/4/tutorials/network_storage/webdav_client/documents_4_webdav.png){class="glboxshadow" width="560"}

## 모바일 앱 사용

웹 관리 패널에서는 공유 폴더만 관리할 수 있습니다. 저장 장치의 파일을 관리하려면 [모바일 앱](https://www.gl-inet.com/app/#download-app-glinet){target="_blank"}을 사용하십시오.

- **로컬 네트워크**를 통해 앱에 액세스하면 저장 장치와 용량이 표시되며 읽기/쓰기 액세스를 지원합니다.

- **클라우드**를 통해 앱에 액세스하면 저장 장치와 용량이 표시되지만 읽기/쓰기 액세스는 지원하지 않습니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 연락하세요.
