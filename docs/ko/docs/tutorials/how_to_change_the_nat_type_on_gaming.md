# 게임에서 NAT 유형 변경하기

대부분의 게임 제조업체는 더 나은 NAT 유형을 얻기 위해 라우터에서 UPnP를 켜라고 요청하지만, 연구에 따르면 UPnP는 안전하지 않은 프로토콜입니다.

DMZ 또는 포트 포워딩 기능을 통해 더 안전한 방식으로 동일한 목적을 달성할 수 있습니다.

## 게임 IP 확인

클라이언트 목록으로 이동하여 게임에 할당된 IP를 확인하세요. 다음 설정에서 이 IP 주소를 사용해야 합니다.

![gameip](https://static.gl-inet.com/docs/router/en/4/tutorials/gamling/gameip.png){class="glboxshadow"}

## 방법 1: DMZ

사이드바의 **Network > Port Forwarding**으로 이동하여 게임 IP로 DMZ를 활성화합니다.

![dmz](https://static.gl-inet.com/docs/router/en/4/tutorials/gamling/dmzgame.png){class="glboxshadow"}

## 방법 2: 포트 포워딩

사이드바의 **Network > Port Forwarding**으로 이동하여 게임 IP로 필요한 포트를 추가합니다.

![inputport](https://static.gl-inet.com/docs/router/en/4/tutorials/gamling/inputport.png){class="glboxshadow"}

예시: PS5 포트

UDP 3074, 3478-3479

TCP 1935, 3478-3480


![ps5port](https://static.gl-inet.com/docs/router/en/4/tutorials/gamling/ps5port.png){class="glboxshadow"}

Xbox 포트

UDP 88, 3074

TCP 3074

일부 게임에서는 다른 포트를 포워딩해야 할 수 있으므로 자세한 내용은 이 웹사이트를 참조하세요.

[다양한 게임의 포트 포워딩](https://portforward.com/games/)

## Full Cone NAT

**Network > NAT Settings**에서 Full Cone NAT를 활성화하여 대기 시간을 개선할 수 있습니다.

![conenat](https://static.gl-inet.com/docs/router/en/4/tutorials/gamling/conenat.png){class="glboxshadow"}

* 이 기능은 펌웨어 4.5 이상에서 사용할 수 있습니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
