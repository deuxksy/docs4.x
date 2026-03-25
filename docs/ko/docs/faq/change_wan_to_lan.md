# WAN을 LAN으로 변경

라우터의 WAN 포트를 LAN 포트로 변경할 수 있습니다. 이는 라우터를 리피터 모드로 사용할 때 WAN 포트가 불필요하게 되므로 특히 유용합니다. WAN 포트를 LAN 포트로 변경하면 확장된 연결을 위한 추가 LAN 포트가 생깁니다.

아래 단계에 따라 WAN을 LAN으로 변경하세요.

## 펌웨어 4.7 이상

1. WAN 포트를 연결하지 마세요.

2. 장치를 라우터에 연결하고 라우터의 웹 관리 패널에 액세스하세요.

3. 웹 관리 패널에서 **INTERNET** -> **Ethernet** 섹션으로 이동하고 우측 상단의 기어 아이콘을 클릭하세요.

	![port management](https://static.gl.inet.com/docs/router/en/4/faq/change_wan_to_lan/ethernet_gear_icon.png){class="glboxshadow"}

	**Port Management** 페이지로 이동하며 WAN 포트 상태가 WAN으로 사용 중인 것으로 표시됩니다.

	![port management](https://static.gl.inet.com/docs/router/en/4/faq/change_wan_to_lan/port_management.jpg){class="glboxshadow"}

4. **LAN**을 클릭하여 이더넷 포트 속성을 변경하고 **Apply**를 클릭하세요.

	![switch to lan apply](https://static.gl.inet.com/docs/router/en/4/faq/change_wan_to_lan/switch_to_lan_apply.jpg){class="glboxshadow"}

	팝업 경고 창에서 **Apply**를 클릭하여 확인하세요.

	![caution](https://static.gl.inet.com/docs/router/en/4/faq/change_wan_to_lan/caution.png){class="glboxshadow"}

	**참고**: 이 과정에서 Wi-Fi가 일시적으로 연결이 끊길 수 있습니다. 완료된 후 라우터에 다시 연결하세요.

5. Ethernet 섹션으로 돌아가면 WAN 포트가 이제 LAN 포트로 사용되고 있는 것으로 표시됩니다.

	![wan using as lan](https://static.gl.inet.com/docs/router/en/4/faq/change_wan_to_lan/wan_using_as_lan.png){class="glboxshadow"}

	**Port Management** 페이지에서 다시 WAN으로 전환하거나 RESET 버튼을 4초간 눌러 WAN 인터페이스를 재시작할 수 있습니다.

## 펌웨어 4.6 이전

1. WAN 포트를 연결하지 마세요.

2. 장치를 라우터에 연결하고 웹 관리 패널에 액세스하세요.

3. 웹 관리 패널에서 **INTERNET** -> **Ethernet** 섹션으로 이동합니다. WAN 포트 상태가 **Using as WAN**으로 표시됩니다. **Change to LAN**을 클릭하세요.

	![internet page](https://static.gl.inet.com/docs/router/en/4/tutorials/change_wan_to_lan/ethernet_no_cable.png){class="glboxshadow"}

4. **Apply**를 클릭하여 확인하세요.

	![caution change wan as lan](https://static.gl.inet.com/docs/router/en/4/tutorials/change_wan_to_lan/ethernet_change_to_lan_caution.png){class="glboxshadow"}

	**참고**: 이 과정에서 Wi-Fi가 일시적으로 연결이 끊길 수 있습니다. 완료된 후 라우터에 다시 연결하세요.

5. Ethernet 섹션으로 돌아가면 `Using as LAN`으로 표시됩니다.

	![using as lan](https://static.gl.inet.com/docs/router/en/4/tutorials/change_wan_to_lan/ethernet_using_as_lan.png){class="glboxshadow"}

	위 절차를 반복하여 설정을 되돌릴 수 있습니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
