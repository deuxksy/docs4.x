# OpenVPN 서버 인증서 업데이트하는 방법

이 튜토리얼에서는 GL.iNet 라우터의 OpenVPN 서버 인증서를 업데이트하는 방법을 설명합니다.

**참고**: 이 과정은 Root CA 인증서를 업데이트해야 하며, 이로 인해 모든 기존 클라이언트 인증서(구성 파일에 포함)가 무효화됩니다. OpenVPN 클라이언트가 서버에 다시 연결하려면 모든 구성 파일을 다시 내보내야 합니다.

1. 라우터의 웹 관리 패널에 로그인한 후 **VPN** -> **OpenVPN Server**로 이동합니다.

    OpenVPN 서버가 실행 중인 경우 서비스를 중지합니다.

2. Configuration 탭에서 **Advanced Configuration**을 클릭하여 설정을 펼칩니다.

    ![advanced](https://static.gl-inet.com/docs/router/en/4/tutorials/update_ovpn_certificate/advanced.png){class="glboxshadow"}

3. **Server Root Certificate**를 찾아 텍스트 상자 안의 모든 내용을 삭제합니다.

    ![certificate](https://static.gl-inet.com/docs/router/en/4/tutorials/update_ovpn_certificate/certificate1.png){class="glboxshadow"}

    페어링된 Server Certificate와 Server Key도 자동으로 제거됩니다.

    ![certificate](https://static.gl-inet.com/docs/router/en/4/tutorials/update_ovpn_certificate/certificate2.png){class="glboxshadow"}

4. 세 상자를 모두 비워 둔고 하단의 **Apply**를 클릭합니다. 새 인증서가 자동으로 생성되어 상자에 채워집니다.

    ![apply](https://static.gl-inet.com/docs/router/en/4/tutorials/update_ovpn_certificate/apply.png){class="glboxshadow"}

5. OpenVPN 서버 인증서가 업데이트되었습니다. 하단의 **Export Client Configuration**를 클릭하여 장치 연결용 새 구성 파일을 내보냅니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
