# 듀얼 이더넷 WAN

듀얼 이더넷 WAN 기능은 기본 LAN1을 두 번째 WAN 포트로 전환하여 듀얼 이더넷 액세스를 제공하며, 안정적인 백업 연결을 제공하고 (호환되는 경우) 대역폭 집계를 지원하여 높은 수요의 사용에 대응합니다. 또한 추가 하드웨어 없이 두 개의 별도 네트워크(예: 업무 및 개인)에 동시에 연결할 수 있어 유연성을 향상시킵니다.

## 지원 모델

??? "지원 모델"
    - ※GL-E5800 (Mudi 7)
    - GL-MT3600BE (Beryl 7)
    - GL-MT5000 (Brume 3)
    - GL-BE6500 (Flint 3e)
    - GL-BE9300 (Flint 3)
    - GL-BE3600 (Slate 7)
    - GL-X2000 (Spitz Plus)
    - GL-MT6000 (Flint2)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)

    **참고**: GL-E5800 (Mudi 7)은 하나의 이더넷 포트(기본 LAN, WAN으로 전환 가능)와 **OTG 지원 USB-C 포트** 하나로 구성되어 있습니다. 듀얼 이더넷 WAN을 위해 두 번째 이더넷 포트를 추가하려면 별도 판매되는 USB-C-이더넷 어댑터를 USB-C 포트에 연결하세요.

??? "미지원 모델"
    - GL-B3000 (Marble)
    - GL-AX1800 (Flint)
    - GL-MT2500/GL-MT2500A (Brume 2)
    - GL-MT3000 (Beryl AX)
    - GL-AXT1800 (Slate AX)
    - GL-SFT1200 (Opal)
    - GL-A1300 (Slate Plus)
    - GL-MT1300 (Beryl)
    - GL-E750/E750V2 (Mudi)
    - GL-AR750S (Slate)
    - GL-XE300 (Puli)
    - GL-X750 (Spitz)
    - GL-MT300N-V2 (Mango)
    - GL-AR300M Series (Shadow)
    - GL-B1300 (Convexa-B)
    - GL-X300B (Collie)

## 설정

1. 라우터의 웹 관리 패널에 로그인합니다.

2. **NETWORK** -> **Port Management** -> **LAN** 탭으로 이동하여 포트 속성을 WAN으로 전환하고 **Apply** 를 클릭합니다.

    ![dual ethernet wan 1](https://static.gl-inet.com/docs/router/en/4/tutorials/dual-ethernet_wan/dual_ethernet_1.png){class="glboxshadow"}

3. 팝업 창에서 **Apply** 를 클릭합니다.

    ![dual ethernet wan 2](https://static.gl-inet.com/docs/router/en/4/tutorials/dual-ethernet_wan/dual_ethernet_2.png){class="glboxshadow"}

4. 듀얼 이더넷 WAN을 활성화한 후 [여기](../interface_guide/multi-wan.md)에서 멀티-WAN 기능을 구성할 수 있습니다.

---

궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하시거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용해 주세요.
