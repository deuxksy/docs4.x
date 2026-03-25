# GoodCloud를 통해 LuCI 인터페이스에 접근하는 방법

GL.iNet [GoodCloud](https://www.goodcloud.xyz/){target="_blank"}는 지리적 제한을 극복하고 원격 라우터 관리를 위한 편리한 방법을 제공합니다. GoodCloud를 통해 언제 어디서나 라우터의 LuCI 인터페이스에 접근하여 라우터의 다양한 설정을 수행하고 네트워크를 쉽게 관리할 수 있습니다.

## 준비 사항

- 하드웨어 장비: 인터넷이 구성되어 있고 정상적으로 작동하는 GL.iNet 라우터.
- 네트워크 환경: 라우터가 연결된 네트워크가 안정적이고 정상적으로 인터넷에 접근할 수 있어야 합니다.
- 기기 바인딩: [GL.iNet 라우터를 GoodCloud 계정에 바인딩](../interface_guide/cloud.md/#setup-your-goodcloud-account)해야 합니다. GoodCloud 계정이 없다면 [회원가입](https://www.goodcloud.xyz/){target="_blank"}을 하세요.

## GoodCloud를 통해 LuCI 인터페이스에 접근하는 단계

### 펌웨어 버전 4.7 이상의 경우

v4.7부터 사용자는 라우터의 웹 관리 패널을 거치지 않고 GoodCloud 플랫폼에서 직접 LuCI 페이지에 접근할 수 있습니다.

1. [여기](https://www.goodcloud.xyz/){target="_blank"}에서 GoodCloud 계정에 로그인합니다.

2. 왼쪽 사이드바 -> **Devices** -> **Bound Devices**에서 접근하려는 기기의 이름을 클릭하면 Remote Web Access 아이콘이 표시됩니다.

    ![remote gui](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/remote_gui_mt6000.png){class="glboxshadow"}

    팝업 창에 포트 80이 표시됩니다. 포트를 **8080**으로 변경하고 Apply를 클릭합니다.

    ![change port](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/change_port.png){class="glboxshadow"}

3. LuCI 로그인 페이지로 리다이렉트됩니다. 관리 비밀번호를 입력하여 로그인합니다.

    ![log in luci](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/log_in_luci.png){class="glboxshadow gl-80-desktop"}

4. LuCI에 성공적으로 로그인했습니다.

    ![luci interface](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/log_in_luci_mt6000.png){class="glboxshadow"}

### 펌웨어 버전 4.6 이하의 경우

1. [여기](https://www.goodcloud.xyz/){target="_blank"}에서 GoodCloud 계정에 로그인합니다.

2. 왼쪽 사이드바 -> **Devices** -> **Bound Devices**에서 접근하려는 기기의 이름을 클릭하면 Remote Web Access 아이콘이 표시됩니다.

    ![remote gui](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/remote_gui_of_bound_device.png){class="glboxshadow"}

    팝업 창에 포트 80이 표시되면 Apply를 클릭합니다.

    ![vist web apply](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/visit_web_apply.png){class="glboxshadow"}

3. GL.iNet 관리 패널 로그인 페이지로 리다이렉트됩니다. 관리 비밀번호를 입력하여 로그인합니다.

    ![admin panel login](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/admin_panel_login.png){class="glboxshadow"}

4. 로그인 후 왼쪽 사이드바 -> SYSTEM -> Advanced Settings에서 하이퍼링크를 클릭하여 LuCI 인터페이스로 이동합니다.

    ![advanced settings](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/advanced_settings.png){class="glboxshadow"}

    LuCI 로그인 페이지로 리다이렉트됩니다. 동일한 관리 비밀번호를 입력하여 로그인합니다.

    ![log in luci](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/log_in_luci.png){class="glboxshadow gl-80-desktop"}

5. LuCI에 성공적으로 로그인했습니다.

    ![luci interface](https://static.gl-inet.com/docs/router/en/4/tutorials/access_luci_via_goodcloud/luci_interface_example.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
