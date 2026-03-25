# 이더넷-USB 어댑터를 통한 듀얼 유선 이더넷 WAN 구성

단일 WAN 포트 라우터에서 이더넷-USB-A 어댑터를 통해 듀얼 유선 이더넷 WAN 액세스를 구성할 수 있습니다.

GL.iNet 라우터는 일반적인 이더넷-USB-A 어댑터를 지원하여, ISP 라우터의 유선 이더넷 연결을 라우터의 USB 포트를 통해 USB 연결로 변환할 수 있습니다. 이를 통해 WAN 포트와 함께 추가 유선 이더넷 연결을 제공합니다.

## 토폴로지

![Topology](https://static.gl-inet.com/docs/router/en/4/tutorials/multiwan_wire/adaptor.png){class="glboxshadow"}

## 설정 단계

1. 이더넷-USB-A 어댑터를 GL.iNet 라우터의 USB 포트에 연결하고, 다른 쪽 끝을 ISP 라우터에 연결합니다.

2. USB 드라이버를 설치합니다.

    라우터의 웹 관리 패널에 로그인하고 **Application** -> **Plug-ins**로 이동한 다음 어댑터용 USB 네트워크 드라이버를 설치합니다.

    예를 들어 Realtek 어댑터를 사용하는 경우 **kmod-usb-net-rtl8152** 드라이버를 설치하세요.

    ![plugins](https://static.gl-inet.com/docs/router/en/4/tutorials/multiwan_wire/plugins_usb.png){class="glboxshadow"}

    설치가 완료될 때까지 기다립니다.

    ![installation suceeded](https://static.gl-inet.com/docs/router/en/4/tutorials/multiwan_wire/suceeded.png){class="glboxshadow"}

3. USB 테더링으로 연결합니다.

    드라이버 설치가 완료되면 **INTERNET** -> **Tethering** 섹션으로 이동합니다.

    USB 연결이 감지되어 ISP 라우터에 연결할 수 있습니다.

    ![detected](https://static.gl-inet.com/docs/router/en/4/tutorials/multiwan_wire/detected.png){class="glboxshadow"}

    **Connect**를 클릭하고 잠시 기다립니다. 녹색 점이 켜지고 IP 주소와 같은 정보가 페이지에 표시되면 USB 테더링 연결이 성공한 것입니다.

    ![tether](https://static.gl-inet.com/docs/router/en/4/tutorials/multiwan_wire/tether.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
