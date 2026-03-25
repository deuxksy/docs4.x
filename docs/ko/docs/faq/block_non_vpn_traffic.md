# 모든 데이터를 VPN 통해 전송하려면 어떻게 하나요?

라우터의 모든 네트워크 트래픽을 VPN 통해 라우팅하고 VPN 실패 시 모든 인터넷 연결을 차단하려면 아래 단계에 따라 **VPN Kill Switch**를 활성화하세요.

**참고**: VPN Kill Switch를 활성화하기 전에 GL.iNet 라우터에 VPN 클라이언트를 설정하세요.

## 펌웨어 v4.7 이전

라우터의 웹 관리 패널에 로그인하여 **VPN** -> **VPN Dashboard** -> **VPN Client** 섹션으로 이동한 후 **Global Options**를 클릭하세요.

![global options 1](https://static.gl.inet.com/docs/router/en/4/faq/block_non_vpn_traffic/4.7-global-options-1.png){class="glboxshadow"}

**Block Non-VPN Traffic** (일부 펌웨어 버전에서는 Kill Switch라고 함)을 토글한 후 **Apply**를 클릭하세요.

![global options 2](https://static.gl.inet.com/docs/router/en/4/faq/block_non_vpn_traffic/4.7-global-options-2.png){class="glboxshadow gl-80-desktop"}

**참고:** Block Non-VPN Traffic / Kill Switch를 활성화하면 VPN이 비활성화되거나 연결이 끊어졌을 때 DNS 누출을 방지하기 위해 라우터에 연결된 모든 장치의 인터넷 액세스가 제한됩니다.

## 펌웨어 v4.8 이상

펌웨어 v4.8에서 VPN Kill Switch는 두 가지 모드로 분리되었습니다.

- **Tunnel Kill Switch**: 해당 VPN 터널이 활성화될 때 기본적으로 활성화됩니다.

- **Enhanced Kill Switch (정책 모드에서)**: VPN 터널 및 위 정책에서 다루지 않는 모든 트래픽이 여전히 인터넷에 액세스할 수 있도록 기본적으로 비활성화됩니다. 즉, 비-VPN 트래픽의 일반적인 인터넷 액세스를 유지합니다.

### Tunnel Kill Switch

라우터의 웹 관리 패널에서 **VPN** -> **VPN Dashboard**로 이동하세요.

라우터를 VPN 클라이언트로 설정한 경우 VPN이 활성화되면 이 VPN 터널의 Kill Switch가 기본적으로 활성화됩니다.

![global mode kill switch](https://static.gl.inet.com/docs/router/en/4/faq/block_non_vpn_traffic/4.8-global-mode-killswitch.png){class="glboxshadow"}
<small>(VPN Global Mode)</small>

![policy mode kill switch](https://static.gl.inet.com/docs/router/en/4/faq/block_non_vpn_traffic/4.8-policy-mode-killswitch.png){class="glboxshadow"}
<small>(VPN Policy Mode)</small>

터널 이름 옆의 기어 아이콘을 클릭하여 **Tunnel Options**로 들어가세요.

![tunnel options 1](https://static.gl.inet.com/docs/router/en/4/faq/block_non_vpn_traffic/4.8-global-mode-options1.png){class="glboxshadow"}

이 터널의 Kill Switch는 기본적으로 활성화됩니다.

![tunnel options 2](https://static.gl.inet.com/docs/router/en/4/faq/block_non_vpn_traffic/4.8-global-mode-options2.png){class="glboxshadow"}

### Enhanced Kill Switch

이 기능은 정책 모드에서 사용할 수 있습니다.

라우터의 웹 관리 패널에서 **VPN** -> **VPN Dashboard**로 이동하여 VPN 모드를 **Policy Mode**로 전환한 후 하단에서 **All Other Traffic**라는 섹션을 찾으세요. 이 섹션은 펌웨어 버전에 따라 약간 다를 수 있습니다.

![all other traffic](https://static.gl.inet.com/docs/router/en/4/faq/block_non_vpn_traffic/4.8-all-other-traffic.png){class="glboxshadow"}

All Other Traffic은 VPN 터널과 위 정책에서 다루지 않는 트래픽 또는 VPN 연결에서 장애 조치(Failover)된 트래픽의 일반적인 인터넷 액세스를 보장하는 기본 터널입니다. 이 터널은 기본적으로 활성화되며 Enhanced Kill Switch와 상호 배타적입니다.

**참고**: All Other Traffic을 비활성화하면 VPN을 통해서만 인터넷에 액세스할 수 있습니다. 일치하지 않는 모든 트래픽이 차단됩니다. 이 설정은 각 터널의 개별 Kill Switch를 재정의하지 않습니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
