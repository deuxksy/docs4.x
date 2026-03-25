# GL.iNet 라우터에서 USB 모뎀이 제대로 작동하지 않음

일부 GL.iNet 라우터에는 USB 포트가 있어 사용자가 USB 모뎀을 USB 포트에 연결하여 인터넷 액세스를 구성할 수 있으며, 다른 인터넷 액세스와 결합하여 Multi-WAN 시나리오를 실현할 수도 있습니다.

그러나 일부 USB 모뎀(ZTE F50 Mobile Wi-Fi Hotspot 등)이 라우터에서 정상적으로 사용되지 않아 네트워크가 자주 끊기는 문제가 발생할 수 있습니다.

이는 라우터의 USB 포트(일반적으로 USB 3.0)와 2.4GHz Wi-Fi 간의 호환성 문제로 인해 USB 모뎀이 계속 연결이 끊기고 정상적으로 인터넷에 액세스할 수 없는 경우가 있습니다.

이 문제를 해결하려면 USB 포트 사양을 USB 3.0에서 USB 2.0으로 전환할 수 있습니다.

GL.iNet 라우터의 관리 패널에 접속하여 **SYSTEM -> Overview -> External Storage**로 이동하세요.

USB 프로토콜 스위치 옵션이 표시됩니다.

![External Storage 1](https://static.gl.inet.com/docs/router/en/4/faq/usb_modem_not_working_properly/external_storage_1.png){class="glboxshadow"}

USB 2.0으로 전환하면 아래와 같은 프롬프트가 표시됩니다. 계속하려면 Switch를 클릭하세요.

![External Storage 2](https://static.gl.inet.com/docs/router/en/4/faq/usb_modem_not_working_properly/external_storage_2.png){class="glboxshadow"}

USB 프로토콜이 USB 2.0로 표시되면 성공적으로 전환된 것입니다.

![External Storage 3](https://static.gl.inet.com/docs/router/en/4/faq/usb_modem_not_working_properly/external_storage_3.png){class="glboxshadow"}

그 후 인터넷 연결이 개선되었는지 확인하세요.

---

관련 문서

- [호환 가능한 모뎀](https://docs.gl-inet.com/router/en/4/interface_guide/internet_cellular/#compatible-modems)

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
