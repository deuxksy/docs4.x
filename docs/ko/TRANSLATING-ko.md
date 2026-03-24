# 한국어 번역 가 가이드

이 문서는 GL.iNet 라우터 문서의 한국어 번역을 위한 가이드라인입니다.

## 번역 규칙

### Frontmatter 처리

마크다운 파일의 frontmatter는 다음 필드를 유지해야 합니다:
- `hash` - 변경하지 않음 (고유 ID)
- `slug` - 변경하지 않음 (URL 경로 유지)
- `publish` - 변경하지 않음

### 커스텀 앵커 보존

제목에 커스텀 앵커가 있는 경우 `{#custom-anchor}` 형식으로 보존해야:

```markdown
<!-- 원문 -->
## Advanced Settings {#advanced-settings}

<!-- 번역 -->
## 고급 설정 {#고급-설정}

<!-- 원문 -->
## Custom Heading Anchors {#custom-heading}

<!-- 번역 -->
## 커스텀 앵커 보존
```

```markdown

### 링크 업데이트

모든 내부 링크에서 `/en/`을 `/ko/`로 변경하세요:

```markdown
<!-- 원문 -->
[Setup Guide](../../../tutorials/first_time_setup)

<!-- 번역 -->
[설정 가이드드](../../../tutorials/first_time_setup)
```

```markdown

### 이미지 경로

`https://static.gl-inet.com/`로 시작하는 이미지 URL은 공통 자산이므로 변경하지 않습니다:

```markdown

## 주요 용어 번역

| English | Korean |
|---------|--------|
| Router | 라우터 |
| Firmware | 펌웨어 |
| VPN | VPN |
| Client | 클라이언트 |
| Server | 서버 |
| Settings | 설정 |
| Interface | 인터페이스 |
| Network | 네트워크 |
| Wireless | 무선 |
| Ethernet | 이더넷 |
| Repeater | 리피터 |
| Tethering | 테더링 |
| Cellular | 셀룰러 |
| Firewall | 방화벽 |
| Port Forwarding | 포트 포워딩 |

## 번역 상태 추적

번역이 완료된 파일의 frontmatter에 다음을을 추가해야:

```yaml
translated: true
translated_date: 2026-03-25
translator: "Your Name"
```
