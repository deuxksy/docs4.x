# Android 5G 핫스팟을 스캔할 수 없음

GL.iNet 라우터를 리피터로 Android 폰의 5G 핫스팟에 연결하는 것은 인터넷에 액세스하는 일반적인 방법 중 하나입니다.

그러나 Android 폰의 5G 핫스팟을 스캔할 수 없는 경우 Wi-Fi 국가 코드와 관련이 있을 수 있습니다.

일부 Android 폰은 5G 핫스팟을 기본적으로 US 채널로 설정합니다. GL.iNet 라우터를 미국에서 구매하지 않은 경우 이 문제가 발생할 수 있습니다.

아래 단계에 따라 LuCI 페이지에서 GL.iNet 라우터의 Wi-Fi 국가 코드를 변경할 수 있습니다.

## 1단계. LuCI에 로그인

GL.iNet 라우터에 로그인하고 왼쪽 사이드바에서 **SYSTEM -> Advanced Settings -> Go to LuCI**를 선택합니다. 동일한 관리자 비밀번호로 LuCI에 로그인합니다.

## 2단계. Wi-Fi 설정 편집

**Network -> Wireless**로 이동하여 5G Wi-Fi를 선택하고 편집합니다. GL-MT3000을 사용하는 경우 **Network -> MTK Wi-Fi**로 이동합니다.

![5gwifi](https://static.gl.inet.com/docs/router/en/4/tutorials/5ghotspot/5gwifi.jpg){class="glboxshadow"}

![mtkwifi](https://static.gl.inet.com/docs/router/en/4/tutorials/5ghotspot/mtkwifi.jpg){class="glboxshadow"}

## 3단계. 국가 코드로 US 선택

**Device Configuration -> Advanced Settings**에서 5GHz Wi-Fi의 국가 코드로 US(United States)를 선택합니다.

![5gus](https://static.gl.inet.com/docs/router/en/4/tutorials/5ghotspot/5gus.jpg){class="glboxshadow"}

로그아웃하기 전에 **Save & Apply**를 클릭하세요.

![saveapply](https://static.gl.inet.com/docs/router/en/4/tutorials/5ghotspot/saveapply.jpg){class="glboxshadow"}

그런 다음 Android 폰 5G 핫스팟을 다시 스캔해 보세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
