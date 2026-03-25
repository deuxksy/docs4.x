# 자녀 보호

자녀 보호는 부적절하지 않은 웹사이트를 차단하고 자녀가 기기를 사용하는 시간을 제한하여 온라인에서 자녀를 안전하게 보호하는 방법입니다. 해로운 콘텐츠 액세스를 방지하고 스크린 시간을 관리하며 자녀가 인터넷을 책임감 있게 사용하도록 돕습니다.

이 기능은 펌웨어 v4.2부터 사용할 수 있습니다.

이 동영상을 보거나 아래 단계에 따라 GL.iNet 라우터의 자녀 보호 기능에 대해 자세히 알아보세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/pOyDwQRc3io" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 로컬 버전

로컬 버전은 GL.iNet에서 제공합니다. 현재 베타 버전이며 추가 비용이 없습니다. 이 버전에서 애플리케이션별로 요청을 필터링하려면 도메인을 수동으로 입력해야 합니다.

### 지원 모델

??? "지원 모델"
    - GL-E5800 (Mudi 7)
    - GL-MT5000 (Brume 3)
    - GL-MT3600BE (Beryl 7)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-BE3600 (Slate 7)
    - GL-X2000 (Spitz Plus)
    - GL-B3000 (Marble)
    - GL-MT6000 (Flint2)
    - GL-AX1800 (Flint)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-A1300 (Slate Plus)

??? "미지원 모델"
    - GL-SFT1200 (Opal)
    - GL-MT1300 (Beryl)
    - GL-E750/E750V2 (Mudi)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-AR750S (Slate)
    - GL-XE300 (Puli)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-AP1300 (Cirrus)
    - GL-X300B (Collie)

### 설정

라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **Parental Control**로 이동합니다.

펌웨어 ver.4.8.4 이상에서는 **Flow Control** -> **Parental Control**로 이동합니다.

라우터 시간이 정확한지 확인하세요. 정확하지 않으면 **SYSTEM** -> **Time Zone**로 이동하여 먼저 동기화하세요.

![router time](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/parental_control_time.png){class="glboxshadow"}

자녀 보호를 활성화하고 **Apply**를 클릭합니다.

![parental control, enable](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/parental_control_enable.png){class="glboxshadow"}

- **Block WAN for Unmanaged Devices**: 관리되지 않는 기기가 인터넷에 액세스하는 것을 차단하는 데 사용됩니다.

그런 다음 설정 마법사를 따라 자녀 보호를 설정합니다.

참고용 두 가지 사용 사례가 있습니다. 상황에 따라 조정할 수 있습니다.

**사례 1**

**시나리오**: 프로필의 기기는 평일 오전 8시부터 11시까지 공부할 목적으로, 주말 저녁 6시부터 8시까지 게임 목적으로만 인터넷에 액세스할 수 있습니다. 그 외 시간에는 인터넷 액세스가 기본적으로 차단됩니다.

다음 단계를 따르세요.

1. 프로필을 만들고 이름을 지정합니다.

    ![create a profile](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/guide/guide_create_profile_1.png){class="glboxshadow"}

2. 관리할 기기를 선택합니다. 라우터에 연결되지 않은 경우 MAC 주소를 입력하여 수동으로 추가합니다.

    ![select devices](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/guide/guide_create_profile_2.png){class="glboxshadow"}

3. 액세스 제한을 설정합니다.

    두 가지 기본 규칙 세트가 있습니다: **인터넷 액세스 차단** 및 **제한 없음**. 나중에 사용할 **학습** 및 **놀이**라는 두 개의 규칙 세트를 더 만듭니다.

    **Add a New Ruleset**을 클릭합니다.

    ![add new ruleset](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/guide/guide_create_profile_3.png){class="glboxshadow"}

4. 규칙 세트 이름(예: 학습), 색상 및 차단할 사이트 목록을 지정합니다. 그런 다음 **Apply**를 클릭합니다.

    ![create a ruleset 1](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/guide/guide_create_ruleset_4.png){class="glboxshadow"}

    **참고**: 차단 목록에 입력된 도메인 이름에는 하위 도메인이 포함됩니다. 예를 들어 "example.com"을 입력하면 "subdomain.example.com"과 같은 하위 도메인도 포함됩니다.

    마찬가지로 놀이라는 다른 규칙 세트를 만듭니다. 색상, 차단할 사이트를 지정하고 **Apply**를 클릭합니다.

    ![create a ruleset 2](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/guide/guide_create_ruleset_5.png){class="glboxshadow"}

5. 적용되면 총 4개의 규칙 세트가 표시됩니다.

    **기본 규칙 세트**로 **인터넷 액세스 차단**을 선택하고 **Finish**를 클릭합니다.

    ![create a profile guide](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/guide/guide_create_profile_6.png){class="glboxshadow"}

6. 그 다음 일정 설정으로 이동합니다. **Go to Set**을 클릭합니다.

    ![set schedule](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/guide/guide_schedule_7.png){class="glboxshadow"}

7. 일정에 **학습** 규칙 세트를 추가합니다. **실행 시간**을 평일 오전 8시부터 11시까지로 설정합니다. **Apply**를 클릭합니다.

    ![set schedule](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/guide/guide_schedule_8.png){class="glboxshadow"}

8. 새로 만든 프로필의 편집 페이지로 이동합니다.

    ![modify profile](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/modify_profile.png){class="glboxshadow"}

    일정이 생성된 것을 볼 수 있습니다. 오른쪽 상단의 **Add Schedule**을 클릭합니다.

    ![add schedule](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/add_schedule.png){class="glboxshadow"}

9. 일정에 다른 규칙 세트 **놀이**를 추가합니다. **실행 시간**을 주말 저녁 6시부터 8시까지로 설정합니다. **Apply**를 클릭합니다.

    ![add schedule](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/create_schedule_2.png){class="glboxshadow"}

10. 그러면 **놀이** 규칙 세트도 일정에 추가된 것을 볼 수 있습니다.

    ![schedules](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/schedules_2.png){class="glboxshadow"}

    **참고**: 빨간 점선은 현재 시간을 나타냅니다.

    일정의 특정 부분을 클릭하여 일정 규칙 세트를 수정할 수도 있습니다.

    ![edit schedule](https://static.inet.com/docs/router/en/4/interface_guide/parental_control/schedule_edit.jpg){class="glboxshadow"}

11. 상단의 **Parental Control**을 클릭하여 자녀 보호 페이지로 돌아갑니다.

    ![back to parental control page](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/back_to_parental_control_page.png){class="glboxshadow"}

    최종 구성을 볼 수 있습니다. 기존 프로필과 규칙 세트를 수정하거나 새로 추가할 수 있습니다.

    ![final configuration](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/final_configuration.png){class="glboxshadow"}

**사례 2**

**시나리오**: 프로필의 기기는 주말 저녁 6시부터 8시까지 게임과 짧은 동영상을 재생할 수 있으며, 다른 모든 시간(밤 9시부터 다음 날 아침 7시까지 포함)에는 인터넷 액세스가 기본적으로 차단됩니다.

동영상 자습서를 참조하세요.

<iframe width="560" height="315" src="https://www.youtube.com/embed/5-EOWZ3WkeE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### 문제 해결

구성한 설정이 적용되지 않는 경우 다음 가능한 이유를 확인하세요.

1. DNS 캐시.

    브라우저와 운영 체제는 DNS 캐시를 유지 관리하므로 변경 사항이 적용되는 데 시간이 걸릴 수 있습니다. 즉시 변경 사항을 적용하려면 캐시를 지우세요.

      * [데스크톱 Chrome에서 캐시 지우기](https://support.google.com/accounts/answer/32050){target="_blank"}

      * [데스크톱 Edge에서 캐시 지우기](https://www.microsoft.com/en-us/edge/learning-center/how-to-manage-and-clear-your-cache-and-cookies?form=MA13I2){target="_blank"}

2. 프로필 일정이 아직 시작되지 않았습니다.

3. 입력한 도메인 이름이 올바르지 않을 수 있습니다.

    웹사이트의 도메인은 공개되어 있지만 앱이 사용하는 API 도메인은 공개되지 않는 경우가 많습니다. 이를 해결하려면 Wireshark와 같은 도구를 사용하여 패킷을 캡처하거나 관련 도메인을 검색하세요.

    예를 들어 "www.google.com"을 차단하려면 "www.google.com"보다 "google.com"을 사용하는 것이 더 효과적입니다.

4. 대상 기기가 연결할 때마다 무작위 MAC 주소를 사용하여 규칙이 적용되지 않습니다.

## Bark 버전

[Bark](https://www.bark.us/){target="_blank"} 버전은 Bark가 자체 플랫폼에서 제공하고 관리하며 원클릭으로 애플리케이션과 웹사이트를 필터링하고 요청 기록을 모니터링할 수 있는 옵션을 제공합니다.

24개 이상의 인기 앱 및 소셜 미디어 플랫폼에 대한 모니터링 기능을 제공하며 이는 로컬 자녀 보호 기능의 프리셋 목록에 포함되어 있습니다.

로깅 기능을 통해 어떤� 클라이언트가 어떤� 웹사이트에 언제 액세스했는지 기록합니다. 이를 통해 부모가 로그를 쉽� 확인하고 블랙리스트에 없는 웹사이트를 식별하여 관리 범위에 빠르게 추가할 수 있습니다.

Bark 자녀 보호 기능은 펌웨어 v4.5부터 사용할 수 있으며 선택된 GL.iNet 라우터에서만 지원됩니다.

**참고**:

1. Bark 서비스는 **미국, 호주, 남아프리카 공화국**에서만 사용할 수 있습니다. 자세한 내용은 [여기](https://support.bark.us/hc/en-us/articles/360049965072-International-availability){target="_blank"}를 클릭하세요.

2. Bark 서비스는 일반적으로 유료 구독이 필요합니다. 하지만 Bark와의 파트너십으로 인해 GL.iNet은 선택된 라우터 모델에서 Bark Home 플�을 무료로 제공하므로 추가 비용 없이 고급 모니터링과 알림을 받을 수 있습니다.

3. 두 자녀 보호 버전은 동시에 활성화할 수 없습니다. 버전을 전환하면 다른 버전이 자동으로 비활성화됩니다.

### 지원 모델

??? "지원 모델"
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-B3000 (Marble)
    - GL-MT6000 (Flint2)

??? "미지원 모델"
    - GL-E5800 (Mudi 7)
    - GL-MT5000 (Brume 3)
    - GL-MT3600BE (Beryl 7)
    - GL-BE3600 (Slate 7)
    - GL-X2000 (Spitz Plus)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-AX1800 (Flint)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-A1300 (Slate Plus)
    - GL-SFT1200 (Opal)
    - GL-MT1300 (Beryl)
    - GL-E750/E750V2 (Mudi)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-AR750S (Slate)
    - GL-XE300 (Puli)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-AP1300 (Cirrus)
    - GL-X300B (Collie)

### 설정

라우터의 웹 관리 패널에 로그인하고 **APPLICATIONS** -> **Parental Control**로 이동합니다.

Bark 버전을 선택하고 스위치를 토글한 다음 **Apply**를 클릭합니다.

![switch_versions](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/switch_versions.png){class="glboxshadow"}

![bark_enable](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/bark_enable.png){class="glboxshadow"}

**참고:** Bark 서비스는 특정 국가에서 사용할 수 없을 수 있습니다. GL.iNet은 이 서비스의 제공자가 아니므로 Bark 사용에 문제가 있는 경우 [Bark 기술 지원](https://www.bark.us/contact-us/?ref=glinet&home=glinet)에 직접 문의해 주세요.

Bark 서비스는 활성화되어 있지만 이 기기는 아직 계정과 페어링되지 않았습니다. [기기 페어링 링크](https://www.bark.us/app/signup/?ref=glinet&home=glinet)를 사용하여 이 기기를 Bark 계정에 페어링하세요.

![bark_pairing_link](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/bark_pairing.png){class="glboxshadow"}

페어링되면 페이지가 다음과 같이 표시됩니다.

![bark_paired](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/bark_paired.png){class="glboxshadow"}

이제 기기가 Bark Cloud 서비스에 연결되었고 계정과 페어링되었습니다. [Bark](https://www.bark.us/app/children/?ref=glinet&home=glinet)로 이동하여 로그인하고 네트워크 제어용 프로필을 만드세요.

![bark_set_up](https://static.gl.inet.com/docs/router/en/4/interface_guide/parental_control/bark_setup.png){class="glboxshadow gl-90-desktop"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
