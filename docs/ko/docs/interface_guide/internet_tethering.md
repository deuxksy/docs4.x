# USB 테더링을 통해 인터넷에 연결

USB 케이블을 사용하여 스마트폰에서 라우터로 네트워크를 공유하는 것을 테더링이라고 합니다. 호스트리스 모뎀도 모뎀 설정 중에 테더링으로 작동합니다.

**참고**: 일부 통신사에서 테더링을 제한하거나 별도로 요금을 부과할 수 있습니다. 통신사에 확인하시기 바랍니다.

## 설정

=== "iPhone"

    1. USB 케이블을 사용하여 iPhone을 라우터의 USB 포트에 연결합니다. 기기를 신뢰할지 물어보는 시스템 대화 상자가 나타면 **신뢰**를 탭하여 진행합니다.

        ![ios trust device](https://static.gl.inet.com/docs/router/en/3/setup/share/internet/tethering/iphone_trust_this_computer.png){class="glboxshadow"}

    2. iPhone **설정** -> **개인 핫스팟**으로 이동합니다. **다른 사람의 참여 허용**을 활성화합니다.

        ![ios allow others to join](https://static.gl.inet.com/docs/router/en/3/setup/share/internet/tethering/iphone_hotspot_allow_others_to_join.png){class="glboxshadow" width=400}

    3. 컴퓨터나 다른 전화를 라우터에 연결한 다음 라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Tethering** 섹션으로 이동하여 **Connect**를 클릭합니다.

        ![ios connect](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/ios_connect.png){class="glboxshadow"}

        TTL, HL, MTU와 같은 고급 설정을 지정해야 하는 경우 **Advanced**를 클릭하여 사용자 정의한 다음 **Connect**를 클릭합니다.

        ![ios advanced](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/ios_advanced.png){class="glboxshadow"}

        연결을 시작합니다.

        ![ios connecting](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/ios_connecting.png){class="glboxshadow"}

    4. 연결되면 개인 핫스팟 상태(연결된 기기 수 등)가 화면 상단의 상태 표시줄에 나타납니다.

        ![personal hotspot status](https://static.gl.inet.com/docs/router/en/3/setup/share/internet/tethering/iphone_hotspot_1_connection.png){class="glboxshadow" width=400}

        웹 관리 패널에도 테더링 연결 상태가 표시됩니다.

        ![ios tethering connected](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/ios_connected.png){class="glboxshadow"}

=== "Android"

    1. USB 케이블을 사용하여 Android 전화를 라우터의 USB 포트에 연결합니다. USB 사용 환경설정을 묻는 시스템 대화 상자가 나타날 수 있습니다. **USB 테더링** 또는 **파일 전송**을 선택합니다.

        ![android usb purpose](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/android_usb_preference.png){class="glboxshadow" width=400}

    2. 전화의 **설정** -> **네트워크 및 인터넷** -> **개인 핫스팟**으로 이동합니다. **개인 핫스팟** 또는 **USB 테더링**을 활성화합니다.

        (USB 테더링을 활성화하는 단계는 브랜드마다 다릅니다. 정확한 위치는 장치의 설정을 확인하고 필요한 경우 제조업체의 지원을 문의하세요.)

        ![android personal hotspot](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/android_personal_hotspot.png){class="glboxshadow"}

    3. 컴퓨터나 다른 전화를 라우터에 연결한 다음 라우터의 웹 관리 패널에 로그인하고 **INTERNET** -> **Tethering** 섹션으로 이동하여 **Connect**를 클릭합니다.

        ![android connect](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/android_connect.png){class="glboxshadow"}

        TTL, HL, MTU와 같은 고급 설정을 지정해야 하는 경우 **Advanced**를 클릭하여 사용자 정의한 다음 **Connect**를 클릭합니다.

        ![android advanced](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/android_advanced.png){class="glboxshadow"}

        연결을 시작합니다.

        ![android connecting](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/android_connecting.png){class="glboxshadow"}

    4. 연결되면 개인 핫스팟 상태(연결된 기기 수 등)가 화면 상단의 상태 표시줄에 나타납니다.

        웹 관리 패널에도 테더링 연결 상태가 표시됩니다.

        ![android connected](https://static.gl.inet.com/docs/router/en/4/tutorials/internet_tethering/android_connected.png){class="glboxshadow"}

    Android 공식 문서는 [Android에서 핫스팟 또는 테더링으로 모바일 연결 공유](https://support.google.com/android/answer/9059108?hl=en#zippy=%2Ctether-by-usb-cable){target="_blank"}를 참조하세요.

## 경고

인터넷 액세스를 사용할 수 없는 경우 해당 경고가 표시됩니다.

**"인터페이스는 연결되었지만 인터넷에 액세스할 수 없습니다."**

해결 방법:

1. 스마트폰에 인터넷 액세스가 있는지 확인하세요.

2. [Multi-WAN](multi-wan.md) 페이지로 이동하여 인터넷 액세스 가능 여부를 확인하세요.

## 문제 해결

연결에 실패한 경우 다음 문제 해결 단계를 시도해 보세요:

- 라우터용 정식 전원 공급기를 사용하세요.
- USB 케이블을 뽑았다가 다시 꽂으세요.
- 다른 USB 케이블을 사용하세요. 데이터 전송을 지원하는지 확인하세요(충전 전용 아님).
- "USB 테더링"을 몇 번 껐다 켜세요(Android 전화용).
- "다른 사람의 참여 허용"을 몇 번 껐다 켜세요(iPhone용).
- 스마트폰을 재시작하고 다시 시도하세요.

---

관련 문서

- [인터넷 페이지](internet.md)
- [각 인터넷 액세스 방법의 우선 순위를 설정하는 방법](multi-wan.md)
- [여러 인터넷 액세스 방법을 동시에 사용할 때 로드 밸런스를 설정하는 방법](multi-wan.md)

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
