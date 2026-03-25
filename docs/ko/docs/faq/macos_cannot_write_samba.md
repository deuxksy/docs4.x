# macOS에서 Samba 공유에 쓰기 불가

exFAT 형식의 저장 장치를 Samba 공유로 사용할 때, 일부 macOS 장치에서 공유에 파일을 쓰려고 시도하면 다음 오류 중 하나가 발생할 수 있습니다.

- "작업을 완료할 수 없습니다. 예기치 않은 오류가 발생했습니다(오류 코드 100093)."

    ![error code 100093](https://static.gl.inet.com/docs/router/en/4/tutorials/network_storage/macos_cannot_write_samba/macopyerror.jpg){class="glboxshadow"}

- "작업을 완료할 수 없습니다. 예기치 않은 오류가 발생했습니다(오류 코드 -50)."

    ![error code -50](https://static.gl.inet.com/docs/router/en/4/tutorials/network_storage/macos_cannot_write_samba/error-code-50.jpg){class="glboxshadow"}

다음 방법으로 이 문제를 해결해 보세요.

1. **Samba 공유 권한 확인​**

    Samba 공유가 쓰기 액세스로 구성되어 있는지 확인하세요. 라우터의 웹 관리 패널에 로그인하여 공유 폴더가 사용자 계정에 대해 "읽기/쓰기" 권한을 활성화했는지 확인하세요.

2. **`cp -X 파일명` 명령어를 사용하여 파일을 복사하세요.**

    Finder가 전송 중에 자동으로 확장 속성(예: 리소스 포크, 메타데이터)을 추가하는데, 이는 exFAT 저장소에 대한 Samba 처리와 충돌할 수 있습니다. **cp -X 파일명** 명령어를 사용하여 파일을 복사해 보세요.

    ![macopyfile](https://static.gl.inet.com/docs/router/en/4/tutorials/network_storage/macos_cannot_write_samba/macopyfile.png){class="glboxshadow"}

    또는 **cp -rX 폴더명** 명령어를 사용하여 폴더를 복사하세요.

    ![macopyfolder](https://static.gl.inet.com/docs/router/en/4/tutorials/network_storage/macos_cannot_write_samba/macopyfolder.png){class="glboxshadow"}

3. **Mac 재부팅**

    Apple 메뉴를 클릭하고 재부팅을 클릭하세요. 문제가 지속되면 shutdown, 모든 외부 장치 연결 해제, 30초 기다린 후 재부팅하세요.​

4. **파일 이름 변경**

    파일을 마우스 오른쪽 버튼으로 클릭하고 이름 바꾸기를 클릭하세요. 간단한 이름을 사용하고 !@# 또는 공백과 같은 특수 문자는 피하세요.​

5. **저장 장치 다시 연결**

    USB 드라이브와 같은 외부 드라이브를 사용하는 경우, 먼저 꺼낸 후 분리하고 10초 기다린 후 다시 연결하세요. 다른 USB 포트도 시도해 볼 수 있습니다.

6. **First Aid로 디스크 오류 복구**

    손상된 디스크 데이터는 쓰기 실패를 일으킬 수 있습니다. macOS 디스크 유틸리티를 사용하여 문제를 해결할 수 있습니다.

    1. Finder -> 응용 프로그램 -> 유틸리티 -> 디스크 유틸리티를 엽니다.​
    2. 왼쪽 사이드바에서 드라이브/저장 장치(로컬 또는 외부)를 선택합니다.​
    3. First Aid -> 실행을 클릭합니다. 프로세스가 완료될 때까지 기다리세요.

7. **파일 시스템 조정 또는 드라이브 포맷​

    exFAT 형식의 드라이브를 사용하는 경우 macOS에서 Samba와 호환성 문제가 발생할 수 있습니다. 다음 방법을 시도해 보세요.​

    - **FAT32로 포맷** (외부 드라이브, 크로스 플랫폼 호환성)

        1. 드라이브의 데이터를 먼저 백업하세요(포맷하면 모든 파일이 삭제됩니다).​
        2. 디스크 유틸리티를 열고 드라이브를 선택한 다음 지웁니다.​
        3. 형식으로 "MS-DOS(FAT)"(FAT32)를 선택하고 지우기를 클릭하세요.​

    - **ext4로 포맷**

        !!! Note

            ext4는 주로 Linux 시스템에서 지원됩니다. ext4로 포맷한 후 저장 장치는 Windows 운영 체제와 호환되지 않을 수 있으며, Windows 장치에서 드라이브를 인식하거나 쓰지 못하는 등의 문제가 발생할 수 있습니다.​

        1. 포맷하면 데이터가 삭제되므로 드라이브의 모든 데이터를 백업하세요.​
        2. 디스크 유틸리티 또는 Linux 시스템과 같은 도구를 사용하여 드라이브를 ext4로 포맷하세요.

8. **macOS 업데이트 및 캐시 지우기​

    오래된 소프트웨어나 손상된 캐시는 충돌을 일으킬 수 있습니다. 시스템 설정 -> 일반 -> 소프트웨어 업데이트로 이동하여 최신 버전을 설치하고 시스템 캐시를 지우세요.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}을 통해 연락하세요.
