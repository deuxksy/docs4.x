# 네트워크 가속

네트워크 가속은 CPU 부하를 줄이고 트래픽 패킷 포워딩을 빠르게 하지만 일부 기능과 충돌할 수 있습니다.

네트워크 가속이 활성화되면 다음 기능이 제대로 작동하지 않습니다: 클라이언트 속도 및 트래픽 통계, 클라이언트 속도 제한.

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

## 설정

웹 관리 패널 왼쪽에서 **NETWORK** -> **Network Acceleration**으로 이동합니다.

![Network Acceleration](https://static.gl-inet.com/docs/router/en/4/tutorials/network_acceleration/network_acceleration.png){class="glboxshadow"}

세 가지 모드가 있습니다.

- **자동**

    자동 모드는 실제 사용에 따라 두 가지 가속 모드 간에 자동으로 전환됩니다.

- **하드웨어 가속**

    하드웨어 가속은 <u>이더넷</u> 및 <u>리피터</u>에서 작동합니다.

    하드웨어 가속은 고주파수 네트워크 작업(예: NAT, 패킷 포워딩, 체크섬 확인)을 NPU 또는 HWNAT 칩과 같은 전용 하드웨어로 오프로드합니다. 특히 이더넷(유선 WAN/LAN) 및 리피터 연결에서 작동하며 고정 경로와 간단한 규칙이 있는 이러한 시나리오에서 뛰어나 높은 처리량, 낮은 대기 시간 및 최소의 CPU 부하로 와이어 스피드 데이터 전송을 제공합니다.

- **소프트웨어 가속**

    소프트웨어 가속은 <u>셀룰러</u>에서 작동합니다.

    소프트웨어 가속은 최적화된 커널 또는 드라이버(예: SWNAT)와 결합된 라우터의 일반 CPU에 의존합니다. 셀룰러(4G/5G) 액세스에서 작동하며 일반적으로 하드웨어 가속을 사용할 수 없는 기본 시나리오로 강력한 호환성과 복잡한 프로토콜 지원을 제공합니다. 유연하지만 고대역폭 부하, 특히 DPI, QoS 또는 포트 포워딩과 같은 고급 기능을 실행할 때 CPU 병목에 도달할 수 있습니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 연락하세요.
