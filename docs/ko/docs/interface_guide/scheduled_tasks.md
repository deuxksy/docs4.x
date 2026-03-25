# 예약 작업

웹 관리 패널 왼쪽에서 **SYSTEM** -> **Scheduled Tasks**로 이동합니다.

예약 작업을 사용하면 LED 켜기/끄기, 라우터 다시 시작, Wi‑Fi 활성화/비활성화, TX 전력 레벨 전환과 같은 기본 작업에 대한 일일 스케줄을 설정할 수 있습니다.

**참고**: 이 기능을 사용하기 전에 [시간대](time_zone.md)에서 시간을 먼저 동기화하세요. 예약된 시간에 장치가 꺼져 있으면 작업이 실행되지 않습니다.

## LED 디스플레이 스케줄

이 기능을 사용하면 라우터 LED 조명의 켜짐/꺼짐 스케줄을 설정할 수 있습니다.

활성화하면 켜짐 및 꺼짐 시간을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![LED display schedule](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/led_display_schedule.png){class="glboxshadow gl-90-desktop"}

터치스크린이 있는 모델(예: GL-BE3600 Slate 7)의 경우 LCD 디스플레이 스케줄을 사용하여 터치스크린의 켜짐/꺼짐 스케줄을 설정할 수 있습니다.

![LCD display schedule](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/lcd_display_schedule.png){class="glboxshadow"}

## 예약된 재시작

이 기능을 사용하면 라우터를 자동으로 다시 시작하는 스케줄을 설정할 수 있습니다.

활성화하면 재시작 시간을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![Schedule Reboot](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/schedule_reboot.png){class="glboxshadow gl-90-desktop"}

## Wi-Fi 스케줄

이 기능을 사용하면 라우터에서 지원하는 Wi-Fi 주파수 대역(예: 2.4GHz, 5GHz, 6GHz, MLO Wi-Fi)을 기반으로 Wi-Fi 스케줄을 설정할 수 있습니다.

MLO Wi-Fi는 켜기/끄기 스케줄 모드만 지원하며, 다른 모든 Wi-Fi 주파수 대역은 켜기/끄기 및 TX 전력 전환의 두 가지 스케줄 모드를 지원합니다.

- **켜기/끄기**: 특정 시간에 무선 네트워크를 자동으로 활성화하거나 비활성화하여 연결 편의성과 에너지 절약의 균형을 맞춥니다(예: 수면 시간 동안 꺼서 불필요한 전력 소모를 줄임).

- **TX 전력 전환**: 특정 시간에 무선 전송 전력(신호 강도 및 커버리지 결정)을 자동으로 조정하여 성능과 에너지 효율의 균형을 맞춥니다(예: 사용량이 적을 때 전력 감소).

### MLO Wi-Fi 스케줄

| 지원되는 모델           |         |
| :----------------------- | :-----: |
| GL-E5800 (Mudi 7)        |    √    |
| GL-MT3600BE (Beryl 7)    |    √    |
| GL-BE6500 (Flint 3e)     |    √    |
| GL-BE9300 (Flint 3)      |    √    |
| GL-BE3600 (Slate 7)      |    √    |

MLO 메인 Wi-Fi와 게스트 Wi-Fi 모두에 대해 켜기/끄기 스케줄을 설정할 수 있습니다.

메인 또는 게스트 Wi-Fi 스케줄을 활성화하고, 켜짐 및 꺼짐 시간을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![MLO Wi-Fi turn on/off](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/mlo_turn_on_off.png){class="glboxshadow"}

### 6GHz Wi-Fi 스케줄

| 지원되는 모델           |         |
| :----------------------- | :-----: |
| GL-E5800 (Mudi 7)        |    √    |
| GL-BE9300 (Flint 3)      |    √    |

Wi-Fi 스케줄 모드가 **켜기/끄기**인 경우 6GHz 메인 Wi-Fi와 게스트 Wi-Fi 모두에 대해 켜기/끄기 스케줄을 설정할 수 있습니다.

메인 또는 게스트 Wi-Fi 스케줄을 활성화하고, 켜짐 및 꺼짐 시간을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![6GHz Wi-Fi turn on/off](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/6g_turn_on_off.png){class="glboxshadow"}

Wi-Fi 스케줄 모드가 **TX 전력 전환**인 경우 6GHz 메인 Wi-Fi에 대한 TX 전력 전환 스케줄을 설정할 수 있습니다. 6GHz 게스트 Wi-Fi는 이 스케줄 모드를 지원하지 않습니다.

메인 Wi-Fi 스케줄을 활성화하고, TX 전력을 전환하는 두 가지 예약 작업을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![6GHz Wi-Fi switch TX power](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/6g_switch_tx_power.png){class="glboxshadow"}

- **전환**: 특정 시간(예: 22:00)에 TX 전력을 특정 레벨(예: 낮음)로 설정합니다.
- **복원**: 다른 시간(예: 07:00)에 TX 전력을 다른 레벨(예: 최대)로 복원합니다.
- **요일**: 이러한 설정에 대한 유효 요일을 선택합니다.

### 5GHz Wi-Fi 스케줄

Wi-Fi 스케줄 모드가 **켜기/끄기**인 경우 5GHz 메인 Wi-Fi와 게스트 Wi-Fi 모두에 대해 켜기/끄기 스케줄을 설정할 수 있습니다.

메인 또는 게스트 Wi-Fi 스케줄을 활성화하고, 켜짐 및 꺼짐 시간을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![5GHz Wi-Fi turn on/off](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/5g_turn_on_off.png){class="glboxshadow"}

Wi-Fi 스케줄 모드가 **TX 전력 전환**인 경우 5GHz 메인 Wi-Fi에 대한 TX 전력 전환 스케줄을 설정할 수 있습니다. 5GHz 게스트 Wi-Fi는 이 스케줄 모드를 지원하지 않습니다.

메인 Wi-Fi 스케줄을 활성화하고, TX 전력을 전환하는 두 가지 예약 작업을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![5GHz Wi-Fi switch TX power](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/5g_switch_tx_power.png){class="glboxshadow"}

- **전환**: 특정 시간(예: 22:00)에 TX 전력을 특정 레벨(예: 낮음)로 설정합니다.
- **복원**: 다른 시간(예: 07:00)에 TX 전력을 다른 레벨(예: 최대)로 복원합니다.
- **요일**: 이러한 설정에 대한 유효 요일을 선택합니다.

### 2.4GHz Wi-Fi 스케줄

Wi-Fi 스케줄 모드가 **켜기/끄기**인 경우 2.4GHz 메인 Wi-Fi와 게스트 Wi-Fi 모두에 대해 켜기/끄기 스케줄을 설정할 수 있습니다.

메인 또는 게스트 Wi-Fi 스케줄을 활성화하고, 켜짐 및 꺼짐 시간을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![2.4GHz Wi-Fi turn on/off](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/2.4g_turn_on_off.png){class="glboxshadow"}

Wi-Fi 스케줄 모드가 **TX 전력 전환**인 경우 2.4GHz 메인 Wi-Fi에 대한 TX 전력 전환 스케줄을 설정할 수 있습니다. 2.4GHz 게스트 Wi-Fi는 이 스케줄 모드를 지원하지 않습니다.

메인 Wi-Fi 스케줄을 활성화하고, TX 전력을 전환하는 두 가지 예약 작업을 설정하고, 주간 유효 날짜를 선택한 다음 적용을 클릭하세요.

![2.4GHz Wi-Fi switch TX power](https://static.gl.inet.com/docs/router/en/4/tutorials/scheduled_tasks/2.4g_switch_tx_power.png){class="glboxshadow"}

- **전환**: 특정 시간(예: 22:00)에 TX 전력을 특정 레벨(예: 낮음)로 설정합니다.
- **복원**: 다른 시간(예: 07:00)에 TX 전력을 다른 레벨(예: 최대)로 복원합니다.
- **요일**: 이러한 설정에 대한 유효 요일을 선택합니다.

---

질문이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl.inet.com/contacts/){target="_blank"}을 통해 연락하세요.
