# NAT 설정

이 기능은 v4.5.16부터 사용할 수 있습니다.

웹 관리 패널 왼쪽에서 **NETWORK** -> **NAT Settings**로 이동합니다.

이 페이지에서는 게임 또는 스트리밍과 같은 앱의 P2P 연결 안정성을 높이기 위해 **Full Cone NAT**을 활성화하고 VoIP/SIP 기반 전화 서비스와의 호환성 문제를 해결하기 위해 **SIP ALG**을 활성화할 수 있습니다.

![nat settings](https://static.gl-inet.com/docs/router/en/4/interface_guide/nat_settings/nat_settings.png){class="glboxshadow"}

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
    - GL-AX1800 (Flint)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-A1300 (Slate Plus)
    - GL-X300B (Collie)
    - ※GL-SFT1200 (Opal)
    - ※GL-E750/E750V2 (Mudi)

    **참고**: GL-SFT1200 (Opal) 및 GL-E750/E750V2 (Mudi)는 펌웨어 v4.7 이후에서 이 기능을 지원합니다.

??? "미지원 모델"
    - GL-MT1300 (Beryl)
    - GL-AR750 (Creta)
    - GL-AR750S (Slate)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-XE300 (Puli)
    - GL-B1300 (Convexa-B)

## Full Cone NAT

Full Cone NAT은 게임 콘솔 또는 전화와 같은 장치가 온라인으로 다른 사람(예: 멀티플레이어 게임 또는 비디오 통화)에게 연결할 때 "직접 바로가기" 역할을 합니다.

외부 장치가 라우터를 통해 로컬 장치에 직접 도달할 수 있도록 하여(여러 계층 뒤에 숨기는 대신) P2P 연결 안정성을 높이고 대기 시간을 줄이며 P2P 애플리케이션의 연결 실패를 해결합니다.

**참고**: 이 기능을 활성화하면 장치 포트가 공용 네트워크에 노출되므로 다른 NAT 유형보다 보안이 낮아질 수 있습니다.

## SIP ALG

SIP ALG(Application Layer Gateway)는 비즈니스 데스크 전화 또는 앱 기반 통화와 같은 VoIP/SIP 기반 통신 서비스를 위한 라우터 "번역기" 역할을 합니다.

NAT 트래버설 문제를 해결하기 위해 설계되었으며 통화 데이터를 조정하여 여러 NAT 계층(예: 기본 라우터와 GL.iNet 라우터가 있는 네트워크에서 일반적)을 통해 원활한 전송을 보장하여 충돌을 완화하고 통화 중단을 방지합니다.

**참고**: 호환되지 않거나 잘못 구현된 SIP ALG는 통화 품질을 저하시켜 일방향 오디오, 응답 없는 벨소울림, 통화 끊김 또는 음성 사서함으로 직접 라우팅되는 통화와 같은 문제를 초래할 수 있습니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 연락하세요.
