# GLiNet 모바일 앱에 Brume 2를 추가하는 방법은 무엇인가요?

Brume 2 (GL-MT2500/GL-MT2500A)에 Wi-Fi 기능이 없어도 GLiNet 모바일 앱에 추가할 수 있습니다. 기본 라우터 또는 보조 라우터로 설정할 수 있습니다.

다음 방법은 Brume (GL-MV1000)에도 적용됩니다.

## 보조 라우터로 Brume 2 사용

**토폴로지**

여기서는 Slate AX (GL-AXT1800)를 기본 라우터로, Brume 2 (GL-MT2500)를 보조 라우터로 사용합니다.

![top1](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/top1.jpg){class="glboxshadow"}

1. Brume 2 웹 관리 패널에 로그인하고 **SYSTEM** -> **Security** -> **Open Ports on Router**로 이동하여 포트 **80**을 엽니다.

    ![open80 1](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/open80.png){class="glboxshadow"}

    일부 오래된 모델의 경우 **Firewall** -> **Open Ports on Router**로 이동하여 포트 **80**을 엽니다.

    ![open80 2](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/open80.jpg){class="glboxshadow"}

2. 기본 라우터에 로그인하고 Brume 2의 **WAN IP**를 기록하세요.

    ![assignip](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/assignip.jpg){class="glboxshadow"}

3. 폰을 기본 라우터의 Wi-Fi에 연결하세요.

    ![upperwifi](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/upperwifi.PNG){class="glboxshadow gl-50-desktop"}

4. glinet 앱을 실행하고 **Add New Device**를 클릭하세요.

    ![adddevice](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/adddevice.PNG){class="glboxshadow gl-50-desktop"}

5. 그런 다음 **Initialized Devices**를 클릭하세요.

    ![initdevice](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/initdevice.PNG){class="glboxshadow gl-50-desktop"}

6. 앞서 기본 라우터에서 찾은 WAN IP를 입력하세요.

    ![inputip](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/inputip.PNG){class="glboxshadow gl-50-desktop"}

7. Brume 2의 로그인 비밀번호를 입력하세요.

    ![inputpw](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/inputpw.PNG){class="glboxshadow gl-50-desktop"}

    이제 Brume 2가 glinet 모바일 앱에 표시됩니다.

    ![showup](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/showup.PNG){class="glboxshadow gl-50-desktop"}

## 기본 라우터로 Brume 2 사용

**토폴로지**

![top2](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/top2.jpg){class="glboxshadow"}

1. 보조 라우터(여기서는 GL-AXT1800)에 로그인하여 액세스 포인트 모드로 설정하세요.

    ![setrouteap](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/setrouteap.jpg){class="glboxshadow"}

2. 폰을 보조 라우터의 Wi-Fi에 연결하세요.

    ![upperwifi](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/upperwifi.PNG){class="glboxshadow gl-50-desktop"}

3. glinet 앱을 실행하고 **Add New Device**를 클릭하세요.

    ![adddevice](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/adddevice.PNG){class="glboxshadow gl-50-desktop"}

4. 기본 라우터를 선택하세요.

    ![selectbrume2](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/selectbrume2.PNG){class="glboxshadow gl-50-desktop"}

5. **Next**를 클릭하세요

    ![setupap](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/setupap.PNG){class="glboxshadow gl-50-desktop"}

6. 여전히 보조 라우터의 Wi-Fi에 연결된 경우 기다리세요. 그렇지 않은 경우 보조 라우터의 Wi-Fi에 다시 연결하세요.

    ![connectap](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/connectap.PNG){class="glboxshadow gl-50-desktop"}

7. Brume 2의 로그인 비밀번호를 입력하세요.

    ![inputpw](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/inputpw.PNG){class="glboxshadow gl-50-desktop"}

    이제 Brume 2가 glinet 모바일 앱에 표시됩니다.

    ![showup](https://static.gl.inet.com/docs/router/en/4/faq/add_brume2_into_app/showup.PNG){class="glboxshadow gl-50-desktop"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
