# 셀룰러 라우터에서 캐리어 집계 상태 확인

캐리어 집계(Carrier Aggregation)는 여러 네트워크 대역을 결합하여 셀룰러 연결에 더 큰 대역폭과 더 빠른 속도를 제공합니다.

이 기능은 SIM 캐리어 지원에 따라 달라지므로 라우터의 웹 관리 패널에서 활성화할 수 없습니다.

그러나 라우터의 웹 관리 패널에서 AT 명령을 사용하여 캐리어 집계 상태를 확인할 수 있습니다.

!!! note "지원 모델"

    - GL-E5800 (Mudi 7)
    - GL-X2000 (Spitz Plus)
    - GL-X3000 (Spitz AX)
    - GL-XE3000 (Puli AX)
    - GL-E750/GL-E750V2 (Mudi)
    - GL-X750/GL-X750V2 (Spitz)
    - GL-XE300 (Puli)
    - GL-X300B (Collie)
    - GL-AP1300LTE (Cirrus)

다음 단계에 따라 캐리어 집계 상태를 확인하세요.

1. 라우터에 SIM 카드를 삽입합니다.
2. 웹 브라우저를 열고 주소 표시줄에 `192.168.8.1`을 입력한 후 로그인합니다.
3. **INTERNET** -> **Cellular** 섹션으로 이동하여 오른쪽 상단의 세 점 아이콘을 클릭한 후 **Modem AT Command**를 클릭합니다.

    ![Modem AT Command](https://static.gl-inet.com/docs/router/en/4/tutorials/carrier_aggregation/modem-at-command.png){class="glboxshadow"}

4. 팝업 창에서 **AT+QCAINFO**를 입력한 후 **Send**를 클릭합니다.

    캐리어 집계가 활성화되어 있으면 목록에 여러 네트워크 대역이 표시됩니다.

    ![atcainfo](https://static.gl-inet.com/docs/router/en/4/tutorials/carrier_aggregation/carrier-aggregation-info.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
