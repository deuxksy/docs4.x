# LAN 서브넷 충돌을 해결하는 방법은 무엇인가요?

집 라우터에서 이더넷 케이블을 GL.iNet 라우터의 WAN 포트에 연결할 때 다음 메시지가 표시될 수 있습니다.

**"LAN subnet is in conflict with the WAN subnet. Please Change LAN Subnet to a different address."**

![conflict](https://static.gl.inet.com/docs/router/en/4/faq/what_should_i_do_with_subnet_conflict/conflict.jpg){class="glboxshadow"}

집 라우터가 GL.iNet 라우터와 동일한 LAN IP를 사용하기 때문입니다. 이를 LAN 충돌이라고 합니다.

다음 단계에 따라 LAN 서브넷을 변경하세요.

## 1. LAN 서브넷 변경

**Change LAN Subnet** 하이퍼링크를 클릭하면 **LAN** 설정 페이지로 리디렉션됩니다.

![change lan ip](https://static.gl.inet.com/docs/router/en/4/faq/what_should_i_do_with_subnet_conflict/change_lan_ip.png){class="glboxshadow"}

두 번째 점 뒤의 숫자(기본값은 **8**)를 다른 숫자로 변경하세요. 예: 192.168.10.1, 그런 다음 **Apply**를 클릭하세요.

변경 후 몇 초 기다리면 페이지가 새로고쳐지고 변경된 IP 주소 **192.168.10.1**로 자동 리디렉션됩니다. 서브넷 충돌 프롬프트가 사라진 것을 볼 수 있습니다.

페이지가 리디렉션되지 않으면 다음 단계로 진행하세요.

## 2. 새 LAN IP로 로그인

주소 표시줄에 변경된 LAN IP를 수동으로 입력하고 Enter를 누르세요.

![login](https://static.gl.inet.com/docs/router/en/4/faq/what_should_i_do_with_subnet_conflict/login.png){class="glboxshadow gl-90-desktop"}

관리자 비밀번호로 로그인하면 서브넷 충돌 프롬프트가 사라집니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
