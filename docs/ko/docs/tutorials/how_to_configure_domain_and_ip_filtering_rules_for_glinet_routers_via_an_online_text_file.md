# 온라인 텍스트 파일을 통해 GL.iNet 라우터의 도메인 및 IP 필터링 규칙 구성

펌웨어 v4.7.0부터 VPN 기능의 "대상 도메인 또는 IP 기반 VPN 정책"과 자녀 보호 기능의 "새 규칙 집합 추가"가 온라인 텍스트 파일 링크에서 규칙을 가져오는 것을 지원합니다. 이 문서에서는 이 텍스트 파일의 형식을 설명합니다.

## URL 형식 설명

### 지원 및 미지원 URL 형식

- 텍스트 파일의 지원되는 파일 형식: .txt, .conf, .log 등
- 미지원 파일 형식: .exe, .zip, .jpg 등의 바이너리 파일

### GitHub를 사용하여 텍스트 파일 호스팅

공개 GitHub 저장소에 텍스트 파일을 호스팅하는 경우 일반 GitHub URL 대신 원시 콘텐츠 URL을 사용하세요.

예를 들어 다음 GitHub URL은 원시 콘텐츠가 아닌 웹 콘텐츠를 가리킵니다:

`https://github.com/SecOps-Institute/FacebookIPLists/blob/master/facebook_ipv4_cidr_blocks.lst`

라우터가 올바른 콘텐츠를 다운로드하도록 하려면 다음 형식의 원시 콘텐츠 URL을 사용하세요:

`https://raw.githubusercontent.com/SecOps-Institute/FacebookIPLists/master/facebook_ipv4_cidr_blocks.lst`

이렇게 하면 라우터에서 파일의 일반 텍스트 콘텐츠를 가져올 수 있습니다.

## 대상 도메인 또는 IP 기반 VPN 정책의 필터 형식

"대상 도메인 또는 IP 기반 VPN 정책" 기능은 온라인 텍스트 파일에서 다음 필터 형식을 지원합니다:

* 도메인 이름 형식: `netflix.com`과 같은 도메인 이름을 사용하여 `netflix.com`의 모든 하위 도메인을 일치시킵니다.
* 하위 도메인 형식: `www.netflix.com`과 같은 전체 하위 도메인을 지정하여 특정 하위 도메인만 일치시킵니다.
* CIDR 형식: `192.168.10.0/24`과 같은 CIDR 표기법을 사용하여 IP 주소 범위를 지정합니다.
* IPv4 주소 형식: `192.168.10.10`과 같은 개별 IPv4 주소를 지정합니다.

## 자녀 보호 새 규칙 집합 추가의 필터 형식

자녀 보호의 "새 규칙 집합 추가" 기능은 온라인 텍스트 파일에서 다음 필터 형식을 지원합니다:

* 도메인 이름 형식: `instagram.com`과 같은 도메인 이름을 사용하여 `instagram.com`의 모든 하위 도메인을 일치시킵니다.
* 하위 도메인 형식: `www.instagram.com`과 같은 전체 하위 도메인을 지정하여 특정 하위 도메인만 일치시킵니다.

온라인 텍스트 파일을 만들 때 줄당 하나의 필터를 사용하세요. 라우터는 지정된 형식에 따라 각 줄을 처리하고 VPN 또는 자녀 보호 기능에 해당 규칙을 적용합니다.

## 예시

"대상 도메인 또는 IP 기반 VPN 정책"의 경우:

```
netflix.com
www.hulu.com
192.168.10.0/24
192.168.10.10
```

"자녀 보호 새 규칙 집합 추가"의 경우:

```
instagram.com
facebook
x.com
snapchat
```

이러한 필터 형식을 따르면 라우터의 VPN 및 자녀 보호 기능을 구성하기 위한 온라인 텍스트 파일을 쉽게 만들고 유지 관리할 수 있습니다.

---

여전히 궁금한 점이 있으신가요? [커뮤니티 포럼](https://forum.gl-inet.com){target="_blank"}을 방문하거나 [문의하기](https://www.gl-inet.com/contacts/){target="_blank"}를 통해 문의해 주세요.
