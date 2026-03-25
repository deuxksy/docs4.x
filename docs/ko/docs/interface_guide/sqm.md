# SQM (Smart Queue Management)

SQM(Smart Queue Management)은 라우터의 네트워크 트래픽을 지능적으로 관리하여 대기 시간과 "버퍼블로트"를 최소화하고 더 원활한 게임 및 음성 통화를 보장합니다.

**참고**:

1. 이 기능은 현재 **GL-MT5000 (Brume 3)**에서만 사용할 수 있습니다.

2. 이 기능은 라우터가 게이트웨이로 작동할 때 통과하는 트래픽(로컬 클라이언트 트래픽 및 VPN 클라이언트 트래픽 포함)에 영향을 주지만 라우터가 VPN 서버로 작동할 때 인바운드 트래픽에는 영향을 주지 않습니다.

3. SQM은 리소스 집약적이므로 저대역폭 또는 혼잡한 네트워크에서 가장 잘 작동합니다. 고속 연결에서 활성화하면 최대 처리량이 줄어들 수 있습니다.

---

웹 관리 패널 왼쪽에서 **FLOW CONTROL** > **SQM**로 이동합니다.

트래픽 스케줄링을 위해 최대 업로드 및 다운로드 속도를 먼저 설정합니다(입력 범위: 1 - 10000). 실제 인터넷 대역폭과 일치시키는 것이 가장 좋습니다.

![sqm](https://static.gl.inet.com/docs/router/en/4/interface_guide/sqm/sqm.png){class="glboxshadow"}

큐 규칙에 대해 두 가지 옵션을 사용할 수 있습니다.

- **cake**: 우수한 전반 대기 시간 제어로 스마트하고 자동적인 트래픽 쉐이핑(권장).

- **fq_codel**: 기본 대기 시간 감소로 간단하고 효율적인 공평 큐.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
