# QoS (서비스 품질)

QoS(Quality of Service)는 네트워크 혼잡 중 중요한 활동(예: 화상 통화, 게임)을 우선시켜 대역폭 할당을 최적화하여 대기 시간을 줄이고 전체 네트워크 성능을 개선합니다.

**참고**:

1. 이 기능은 현재 **GL-MT5000 (Brume 3)**에서만 사용할 수 있습니다.

2. 이 기능은 라우터가 게이트웨이로 작동할 때 통과하는 트래픽(로컬 클라이언트 트래픽 및 VPN 클라이언트 트래픽 포함)에 영향을 주지만 라우터가 VPN 서버로 작동할 때 인바운드 트래픽에는 영향을 주지 않습니다.

---

웹 관리 패널 왼쪽에서 **FLOW CONTROL** > **QoS**로 이동합니다.

트래픽 스케줄링을 위해 최대 업로드 및 다운로드 속도를 먼저 설정합니다(입력 범위: 1 - 10000). 실제 인터넷 대역폭과 일치시키는 것이 가장 좋습니다.

그런 다음 다른 애플리케이션에 대한 우선 순위를 설정하면 라우터가 그에 따라 대역폭을 할당합니다.

![qos](https://static.gl.inet.com/docs/router/en/4/interface_guide/qos/qos.png){class="glboxshadow"}

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
