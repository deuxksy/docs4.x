# GL.iNet 라우터에서 특정 클라이언트 장치 차단하기

이 튜토리얼에서는 GL.iNet 라우터에서 특정 클라이언트 장치를 차단하는 방법을 안내합니다. 클라이언트 장치를 차단하면 네트워크에 대한 무단 액세스를 방지할 수 있습니다. 이를 통해 네트워크 보안을 강화하거나 가족의 인터넷 액세스를 제어할 수 있습니다.

GL.iNet 라우터는 MAC 주소(네트워크의 개별 장치에 할당된 고유한 12자리 식별자)를 기준으로 클라이언트 장치를 차단합니다. 이 방법은 MAC 주소 필터링이라고도 합니다.

GL.iNet 라우터에서 클라이언트 장치를 차단하는 방법은 두 가지가 있습니다: [라우터 관리 패널](#관리-패널을-통한-클라이언트-장치-차단) 또는 [GL.iNet 모바일 앱](#glinet-모바일-앱을-통한-클라이언트-장치-차단)을 통하는 방법입니다.

## 관리 패널을 통한 클라이언트 장치 차단

### 1. 관리 패널에 로그인하세요

웹 브라우저에서 `192.168.8.1`을 입력합니다. 비밀번호를 입력한 후 **Login**을 클릭합니다.

### 2. 클라이언트 장치 차단하기

MAC 주소 보유 여부에 따라 클라이언트 장치를 차단하는 방법은 두 가지가 있습니다:

* MAC 주소가 없는 경우: 목록에 표시되는 장치를 차단할 수 있는 [첫 번째 방법](#방법-1-mac-주소 없이-장치-차단)을 사용하세요.
* MAC 주소가 있는 경우: [두 번째 방법](#방법-2-mac-주소로-장치-차단)을 사용하세요.

#### 방법 1: MAC 주소 없이 장치 차단

1. 왼쪽 사이드바에서 **Clients**를 클릭합니다.
![클라이언트 클릭](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/click-clients.jpeg){class="glboxshadow"}

2. 장치 옆에서 스위치를 켭니다.
![스위치 토글](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/toggle-block.jpeg){class="glboxshadow"}

목록에서 차단하려는 장치가 표시되지 않으면 [차단 목록에 MAC 주소를 추가하여](#방법-2-mac-주소로-장치-차단) 차단해야 합니다.

#### 방법 2: MAC 주소로 장치 차단

이 방법을 사용하려면 장치의 MAC 주소를 가져와야 합니다. 장치 제조업체에서 제공하는 지침을 참조하세요.
장치의 MAC 주소를 가져온 후 다음 단계를 따르세요:

1. 왼쪽 사이드바에서 **Clients**를 클릭합니다.
2. 상단에서 **Blocklist**를 클릭합니다.
![차단 목록 클릭](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/click-blocklist.jpeg){class="glboxshadow"}
3. 다음 방법 중 하나를 사용하여 장치를 차단하세요:
    - MAC 주소를 개별적으로 입력하려면: 빈 필드에 입력합니다.
    - MAC 주소 목록을 가져오려면: **Import Clients**를 클릭합니다. 파일을 가져온 후 **Import**를 클릭합니다.
4. **Apply**를 클릭합니다.
![적용 클릭](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/click-apply.jpeg){class="glboxshadow"}

## GL.iNet 모바일 앱을 통한 클라이언트 장치 차단

**참고:** 시작하기 전에 장치에 GL.iNet 모바일 앱을 설치하고 설정하세요.

MAC 주소 보유 여부에 따라 클라이언트 장치를 차단하는 방법은 두 가지가 있습니다:

* MAC 주소가 없는 경우: 목록에 표시되는 장치를 차단할 수 있는 [첫 번째 방법](#모바일-1)을 사용하세요.
* MAC 주소가 있는 경우: [두 번째 방법](#모바일-2)을 사용하세요.

### 방법 1: MAC 주소 없이 장치 차단 {#mobile-1}

1. 메인 앱 화면에서 **Connected Clients** 및 **Office Clients** 아래에서 차단하려는 장치를 탭합니다.
![장치 탭](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/tap-a-device.jpeg){class="glboxshadow"}

2. **Settings**에서 **Block** 스위치를 켭니다.
![차단 토글](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/settings-toggle-block-to-on.jpeg){class="glboxshadow"}

목록에서 차단하려는 장치가 표시되지 않으면 [차단 목록에 MAC 주소를 추가하여](#모바일-2) 차단해야 합니다.

### 방법 2: MAC 주소로 장치 차단 {#mobile-2}

이 방법을 사용하려면 차단하려는 장치의 MAC 주소를 가져와야 합니다. 제조업체에서 제공하는 지침을 참조하세요.
장치의 MAC 주소를 가져온 후 다음 단계를 따르세요:

1. 메인 앱 화면에서 설정 아이콘을 탭한 후 **Access Control**을 탭합니다.
![액세스 제어 탭](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/tap-access-control.jpeg){class="glboxshadow"}

2. **Block**을 탭합니다.
![차단 탭](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/tap-block.jpeg){class="glboxshadow"}

3. 다음 방법 중 하나를 사용하여 장치를 차단하세요:
    - MAC 주소를 개별적으로 입력하려면: **Add MAC address**를 탭합니다. MAC 주소를 입력한 후 **Done**을 탭합니다.
    - MAC 주소 목록을 가져오려면: **Import Clients** > **Import Clients**를 클릭합니다. 파일을 탭합니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
