# 모듈 로그 가져오기

일부 GL.iNet 라우터에는 내장 3G/4G/5G 모듈이 있습니다. 네트워크 연결이 불안정한 경우 분석을 위해 모듈의 로그를 내보내야 할 수 있습니다.

셀룰러 모듈의 로그를 내보내는 단계는 다음과 같습니다.

## 1. 컴퓨터를 라우터에 연결

노트북을 라우터의 Wi-Fi에 연결하거나(SSIID와 비밀번호는 기기 하단 라벨에서 확인), 컴퓨터의 이더넷 포트를 이더넷 케이블로 라우터의 LAN 포트에 연결합니다.

## 2. 라우터에 SSH 로그인

[이 링크](https://docs.gl-inet.com/router/en/4/tutorials/ssh_log_in_to_the_router/)를 참조하세요.

## 3. 모듈 로그 가져오기

### GL-XE300/GL-X750/GL-X300B의 경우

1. 다음 명령어를 사용하여 GL.iNet 서버에서 qlog를 가져오고, qlog 파일의 SHA256이 올바른지 확인합니다.

    ```
    cd /usr/bin/ && wget https://fw.gl-inet.com/tools/quectel_tool/qlog-ar9531-sha256-75fe8b
    ```

    ```
    chmod 775 qlog-ar9531-sha256-75fe8b  && sha256sum qlog-ar9531-sha256-75fe8b
    ```

    ![Get Qlog](https://static.gl-inet.com/docs/router/en/4/tutorials/get_module_logs/ar9531_get_qlog.png){class="glboxshadow"}

2. USB 플래시 디스크를 삽입하고 df 명령어를 사용하여 마운트 경로를 확인합니다. 경로를 기억해 두세요.

    내 USB 플래시 디스크 마운트 경로는 `/tmp/mountd/disk1_part1`입니다.

    ![U Flash Drive Path](https://static.gl-inet.com/docs/router/en/4/tutorials/get_module_logs/ar9531_u_flash_drive_path.png){class="glboxshadow"}

3. 다음 명령어를 사용하여 모듈 디버그 모드를 활성화합니다.

    ```
    gl_modem AT AT+QCFG=\"dbgctl\",0
    ```

4. 다음 명령어를 사용하여 qlog를 시작합니다.

    ```
    qlog-ar9531-sha256-75fe8b -s /tmp/mountd/disk1_part1/qlogs_$(date +%Y%m%d%H%M) &
    ```

    `/tmp/mountd/disk1_part1`은 내 USB 플래시 디스크입니다. 경로를 본인의 경로로 변경해야 합니다.

5. 다음 명령어를 사용하여 모듈을 재부팅합니다.

    ```
    gl_modem AT AT+CFUN=0; sleep 1; gl_modem AT AT+CFUN=1
    ```

6. 1~3분 정도 기다린 후 다음 명령어를 사용하여 qlog를 중지합니다.

    ```
    ps  | grep qlog | grep -v grep | awk '{print $1}' | xargs kill -9
    ```

    ![Start And Stop Qlog](https://static.gl-inet.com/docs/router/en/4/tutorials/get_module_logs/ar9531_start_and_stop_qlog.png){class="glboxshadow"}

7. USB 플래시 디스크에 디렉토리가 생성되고 그 안에 몇 개의 파일이 있습니다. 이 파일들은 qlog가 수집한 데이터이며 Quectel 도구를 사용하여 디코딩해야 합니다. 이 파일들을 GL.iNet 또는 Quectel 기술 지원팀에 보내주세요.

    ![Qlogs Files](https://static.gl-inet.com/docs/router/en/4/tutorials/get_module_logs/ar9531_qlogs_files.png){class="glboxshadow"}

### GL-X3000/GL-XE3000의 경우

1. USB 플래시 디스크를 삽입하고 df 명령어를 사용하여 마운트 경로를 확인합니다. 경로를 기억해 두세요.

    내 USB 플래시 디스크 마운트 경로는 `/tmp/mountd/disk1_part1`입니다.

    ![U Flash Drive Path](https://static.gl-inet.com/docs/router/en/4/tutorials/get_module_logs/mtk7981a_u_flash_drive_path.png){class="glboxshadow"}

2. GL.iNet 서버에서 qlog를 가져오고 qlog 파일의 sha256이 올바른지 확인합니다.

    다음 명령어를 사용하여 qlog를 가져옵니다.

    ```
    cd /etc/ && wget https://fw.gl-inet.com/tools/quectel_tool/default_v15.cfg
    ```

    ```
    cd /usr/bin/ && wget https://fw.gl-inet.com/tools/quectel_tool/qlog-mtk7981a-sha256-78dda4
    ```

    ```
    chmod 775 qlog-mtk7981a-sha256-78dda4  && sha256sum qlog-mtk7981a-sha256-78dda4 && sha256sum /etc/default_v15.cfg
    ```

    ![Get Qlog](https://static.gl-inet.com/docs/router/en/4/tutorials/get_module_logs/mtk7981a_get_qlog.png){class="glboxshadow"}

3. 다음 명령어를 사용하여 qlog를 시작합니다.

    ```
    qlog-mtk7981a-sha256-78dda4 -f /etc/default_v15.cfg -s /tmp/mountd/disk1_part1/qlogs_$(date +%Y%m%d%H%M) &
    ```

4. 다음 명령어를 사용하여 모듈을 재부팅합니다.

    ```
    gl_modem -B 0001:01:00.0 SAT sp AT+CFUN=0; sleep 1; gl_modem -B 0001:01:00.0 SAT sp AT+CFUN=1
    ```

5. qlog로 패킷을 캡처한 후 다음 명령어를 사용하여 qlog를 중지합니다.

    ```
    ps  | grep qlog | grep -v grep | awk '{print $1}' | xargs kill -9
    ```

    ![Start And Stop Qlog](https://static.gl-inet.com/docs/router/en/4/tutorials/get_module_logs/mtk7981a_start_and_stop_qlog.png){class="glboxshadow"}

6. USB 플래시 디스크에 디렉토리가 생성되고 그 안에 몇 개의 파일이 있습니다. 이 파일들은 qlog가 수집한 데이터이며 Quectel 도구를 사용하여 디코딩해야 합니다. 이 파일들을 GL.iNet 또는 Quectel 기술 지원팀에 보내주세요.

    ![Qlogs Files](https://static.gl-inet.com/docs/router/en/4/tutorials/get_module_logs/mtk7981a_qlogs_files.png){class="glboxshadow"}

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 이용하세요.
