# AstroWarp

**참고**: 이 가이드에서는 AstroWarp의 새로운 버전을 소개합니다. 이 버전은 현재 **Flint 3 (GL-BE9300)**의 펌웨어 v4.8.4와 **Slate 7 (GL-BE3600)**의 펌웨어 v4.8.3에서 사용할 수 있습니다.

다른 모델의 경우 [이 링크](https://docs.astrowarp.net/){target="_blank"}를 참조하세요.

---

AstroWarp는 GL.iNet 라우터에 통합된 고급 네트워킹 기능입니다. 등록이나 로그인 없이 홈 네트워크에 원격으로 원활하게 액세스할 수 있습니다. 내장된 트래픽 난독화 기능이 있는 AmneziaWG 프로토콜을 사용하여 연결을 안정적이고 안전하게 유지하므로, 어디서든 신뢰할 수 있는 원격 액세스에 적합합니다.

사용자는 GL.iNet 라우터 관리 패널을 통해 직접 AstroWarp 네트워크를 설정할 수 있습니다. 액세스 코드를 사용하여 라우터를 페어링하면 몇 초 만에 여행용 라우터를 홈 네트워크에 안전하게 연결할 수 있습니다.

**참고:**

1. 다음 기능과 함께 AstroWarp를 사용하는 것은 권장하지 않습니다. 라우팅 충돌이 발생할 수 있습니다: GoodCloud Site to Site, ZeroTier, Tailscale, Tor
2. AstroWarp가 활성화되어 있으면 네트워크 모드를 사용할 수 없습니다.

## 빠른 설정

다음 예제에서는 **Flint 3 (GL-BE9300)**과 **Slate 7 (GL-BE3600)**을 사용하여 AstroWarp 네트워크를 설정합니다.

Flint 3은 홈 라우터 역할을 하고, Slate 7은 인터넷 액세스를 위해 네트워크 트래픽을 Flint 3으로 라우팅하는 여행용 라우터 역할을 합니다.

![topology](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/aw_topology.png){class="glboxshadow"}

**참고**: 각 GL.iNet 라우터는 AstroWarp 네트워킹을 위해 **월 10GB 무료 데이터**를 제공합니다. AstroWarp 네트워크의 기기는 인터넷 액세스를 위해 홈 라우터의 데이터를 사용합니다. 필요에 따라 AstroWarp+ 플랜으로 업그레이드하여 무제한 데이터를 사용할 수 있습니다.

1. Flint 3을 인터넷에 연결합니다.

    Flint 3의 웹 관리 패널에 로그인한 후 **INTERNET** 페이지로 이동합니다. 지원되는 인터넷 연결 방법 중 하나를 사용하여 인터넷에 연결합니다: Ethernet, Repeater, Tethering, Cellular

    아래와 같이 Flint 3 홈 라우터는 이더넷 케이블을 통해 ISP 모뎀(Hong Kong Broadband Network Ltd)에 연결되어 있습니다.

    ![home internet](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/home_internet.png){class="glboxshadow"}

2. 액세스 코드 생성

    Flint 3의 웹 관리 패널에서 **CLOUD SERVICES** -> **AstroWarp**로 이동합니다. **Use At Home**를 클릭합니다.

    ![use as home](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/use_at_home.png){class="glboxshadow"}

    **Access Code**가 생성됩니다. 나중에 사용할 수 있도록 이 코드를 복사합니다.

    ![generate access code](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/home_generate_code.png){class="glboxshadow"}

3. Slate 7을 인터넷에 연결합니다.

    Slate 7의 웹 관리 패널에 로그인한 후 **INTERNET** 페이지로 이동합니다. 지원되는 인터넷 연결 방법 중 하나를 사용하여 인터넷에 연결합니다: Ethernet, Repeater, Tethering, Cellular

    아래와 같이 Slate 7 여행용 라우터는 iPhone 15 Pro의 개인 핫스팟(심수에 위치, China Unicom Guangdong Province 네트워크 사용)에 연결되어 있습니다.

    ![travel internet](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/travel_internet.png){class="glboxshadow"}

4. 액세스 코드 입력

    Slate 7의 웹 관리 패널에서 **CLOUD SERVICES** -> **AstroWarp**로 이동합니다. **Use While Travelling**를 클릭합니다.

    ![use for travel](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/use_for_travel.png){class="glboxshadow"}

    2단계에서 얻은 액세스 코드를 입력합니다.

    ![enter access code](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/enter_access_code.png){class="glboxshadow"}

    확인이 완료될 때까지 기다립니다.

    ![verifying](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/verifying.png){class="glboxshadow"}

    그러면 Flint 3 홈 라우터에 성공적으로 연결됩니다. 이제 홈 네트워크를 통해 안전하게 인터넷을 탐색할 수 있습니다.

    ![connected travel](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/connected_travel.png){class="glboxshadow"}

    Flint 3의 웹 관리 패널에서도 아래와 같이 연결 상태가 표시됩니다.

    ![connected home](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/connected_home.png){class="glboxshadow"}

## 연결 테스트

1. 노트북이나 스마트폰을 Slate 7 여행용 라우터의 Wi-Fi에 연결합니다.

2. 브라우저를 열고 [ipcheck.ing](https://ipcheck.ing/){target="_blank"} 또는 다른 IP 주소 조회 웹사이트를 방문합니다.

    Flint 3의 공인 IP 주소가 표시되며, 이는 Slate 7이 Flint 3 홈 라우터를 통해 인터넷에 액세스하고 있음을 나타냅니다.

    ![ipcheck hk](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/ipcheck_hk.png){class="glboxshadow"}

3. Slate 7에서 AstroWarp 연결을 끊은 다음, 웹페이지를 새로고침하여 IP 조회 요청을 다시 제출합니다.

    Slate 7의 공인 IP 주소가 표시되며, 이는 Slate 7이 로컬 네트워크를 통해 인터넷에 액세스하고 있음을 나타냅니다.

    ![ipcheck sz](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/ipcheck_sz.png){class="glboxshadow"}

## 플랜 업그레이드

각 GL.iNet 라우터는 AstroWarp 네트워킹을 위해 **월 10GB 무료 데이터**를 제공합니다. AstroWarp 네트워크의 기기는 인터넷 액세스를 위해 홈 라우터의 데이터를 사용합니다.

필요에 따라 **AstroWarp+** 플랜으로 업그레이드하여 무제한 데이터를 사용할 수 있습니다.

![upgrade plan](https://static.gl-inet.com/docs/router/en/4/interface_guide/astrowarp/upgrade_plan.png){class="glboxshadow"}

---

궁금한 점이 있으시면 [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
