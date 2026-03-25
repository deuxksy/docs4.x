# GL.iNet 라우터에서 OpenVPN TAP-S2S 모드 활성화하는 방법

## 사용 시나리오

TAP-S2S 모드를 활성화한 후 OpenVPN 클라이언트 장치는 OpenVPN 서버 장치에 원격으로 액세스할 수 있으며, OpenVPN 서버 장치도 OpenVPN 클라이언트 장치에 원격으로 액세스할 수 있습니다. 그러나 단점은 TAP-S2S 모드를 활성화한 후 OpenVPN 클라이언트가 설정한 VPN 규칙이 적용되지 않는다는 것입니다.

## TAP-S2S vs TUN 모드

네트워크 토폴로지

![tap_s2s_topology](https://static.gl-inet.com/docs/router/en/4/tutorials/tap_s2s_vs_tun/tap_s2s_topology.png){class="glboxshadow"}

![tun_topology](https://static.gl-inet.com/docs/router/en/4/tutorials/tap_s2s_vs_tun/tun_topology.png){class="glboxshadow"}

TAP-S2S와 TUN 모드는 동일한 물리적 연결 방법을 사용하지만 논리적 연결 방법이 다릅니다. 차이점은 다음과 같습니다:

1. GL-X3000 LAN 측의 장치가 GL-MT6000의 관리 백엔드에 액세스할 때 TAP-S2S 모드는 가상 IP를 사용하지 않지만 TUN 모드는 사용합니다.
2. GL-X3000 LAN 측의 장치가 GL-X3000의 관리 백엔드에 액세스할 때 TAP-S2S 모드는 가상 IP를 사용하지만 TUN 모드는 사용하지 않습니다.
3. GL-X3000 LAN 측 장치가 GL-MT6000 LAN 측 장치의 IP 주소를 알고 있을 때 TAP-S2S 모드는 직접 원격 액세스를 허용하지만 TUN 모드는 추가 설정을 활성화하지 않으면 직접 액세스할 수 없습니다.
4. TAP-S2S 모드에서 GL-X3000은 인터넷에 액세스하기 위해 GL-MT6000를 거쳐야 하지만 TUN 모드에서 GL-X3000은 인터넷에 직접 액세스할 수 있습니다. 따라서 TAP-S2S 모드에서 GL-X3000이 설정한 VPN 규칙은 적용되지 않으며 GL-MT6000이 설정한 VPN 규칙을 따라야 합니다.

## 튜토리얼

먼저 공용 IP가 있는 라우터(GL-MT6000로 가정)를 사용하여 OpenVPN 서버를 열고 장치 모드를 **TAP-S2S**로 설정한 후 **Apply**를 클릭하고 **Export Client Configuration**를 클릭합니다.

![tutorials_select_mode](https://static.gl-inet.com/docs/router/en/4/tutorials/tap_s2s_vs_tun/tutorials_select_mode.png){class="glboxshadow"}

![tutorials_export](https://static.gl-inet.com/docs/router/en/4/tutorials/tap_s2s_vs_tun/tutorials_export.png){class="glboxshadow"}

또한 공용 IP가 있는 라우터(GL-X3000로 가정)를 사용하여 OpenVPN 클라이언트를 열고 위 단계에서 다운로드한 구성 파일을 가져온 후 **Apply**를 클릭한 후 기능을 활성화합니다.

![tutorials_select_file](https://static.gl-inet.com/docs/router/en/4/tutorials/tap_s2s_vs_tun/tutorials_select_file.png){class="glboxshadow"}

![tutorials_start](https://static.gl-inet.com/docs/router/en/4/tutorials/tap_s2s_vs_tun/tutorials_start.png){class="glboxshadow"}

이때 GL-X3000 라우터의 IP 주소가 변경됩니다. GL-MT6000 관리 대시보드에 로그인한 후 **Clients**를 열고 GL-X3000의 새 IP 주소를 찾을 수 있습니다.

![tutorials_new_IP_address](https://static.gl-inet.com/docs/router/en/4/tutorials/tap_s2s_vs_tun/tutorials_new_IP_address.png){class="glboxshadow"}

GL-MT6000의 네트워크 연결이 끊기거나 OpenVPN 서버를 끄거나 GL-X3000가 OpenVPN 클라이언트를 끄면 GL-X3000의 IP 주소가 복원됩니다.

참고 사항:

- 두 장치 모두 버전 v4.5로 업그레이드해야 합니다. 그렇지 않으면 연결할 수 없습니다.
- TAP-S2S는 전역 프록시 모드에서만 작동하며 OpenVPN과 함께 자동으로 조정됩니다.
- 이 기능을 활성화한 후 다음 기능을 사용할 수 없습니다: VPN 서버, Adguard Home, 자녀 보호, ZeroTier, Tailscale, Tor, 방화벽, Multi-WAN, LAN, DNS, 네트워크 모드, IPv6, MAC 주소, Drop-in Gateway, IGMP Snooping 등.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
