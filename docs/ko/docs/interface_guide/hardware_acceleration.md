# 하드웨어 가속

**참고**: 이 가이드는 펌웨어 v4.2 이전 버전에 적용됩니다. 최신 버전은 [네트워크 가속](network_acceleration.md)을 참조하세요.

---

하드웨어 가속(하드웨어 NAT, 플로우 오프로딩 또는 오프로딩이라고도 함)은 패킷 포워딩을 CPU에서 라우터의 SoC/NIC 하드웨어로 이동시켜 CPU 부하를 줄입니다. 이는 일반적으로 최대 처리량을 높이고 CPU 활용률을 낮추지만, Linux 네트워킹 스택(netfilter/iptables/nftables) 또는 SQM(Smart Queue Management)에서 사용하는 커널 대기 중복(qdisc)에 의존하는 기능에 대해 중요한 절충안이 있습니다.

하드웨어 가속이 활성화되면 다음 기능이 제대로 작동하지 않습니다: 클라이언트 속도 및 트래픽 통계, 클라이언트 속도 제한.

## 지원 모델

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
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-MT3000 (Beryl AX)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-SFT1200 (Opal)
    - GL-MT1300 (Beryl)

??? "미지원 모델"
    - GL-AXT1800 (Slate AX)
    - GL-AX1800 (Flint)
    - GL-A1300 (Slate Plus)
    - GL-E750/E750V2 (Mudi)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-AR750S (Slate)
    - GL-XE300 (Puli)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-X300B (Collie)

## 빠른 설정

웹 관리 패널 왼쪽에서 **NETWORK** -> **Hardware Acceleration**으로 이동합니다.

![Hardware Acceleration](https://static.gl-inet.com/docs/router/en/4/tutorials/hardware_acceleration/hardware_acceleration.png){class="glboxshadow"}

스위치를 토글하여 활성화하고 적용을 클릭합니다.

---

## 하드웨어 NAT vs. 소프트웨어 NAT

* 처리량(예: 멀티기가비트 광대역)을 가장 중요하게 생각하고 라우터 내 SQM 또는 클라이언트별 쉐이핑이 필요 없는 경우 → 하드웨어 NAT / 네트워크 가속을 활성화합니다. 이는 최고의 처리량과 최소의 CPU 사용량을 제공합니다.

* 낮은 대기 시간, 일관된 QoS, 클라이언트별 제한이 중요하거나 SQM(cake/fq_codel)에 의존하는 경우 → 소프트웨어 NAT를 사용합니다(하드웨어 오프로드 비활성화). SQM과 QoS는 패킷이 커널 qdisc 스택을 통과해야 합니다. 오프로드된 패킷은 이 경로를 우회하므로 쉐이핑되지 않습니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 연락하세요.
