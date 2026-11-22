# 문서 지도

breachline 문서는 [Diátaxis](https://diataxis.fr/) 기준으로 목적에 따라 나눕니다.

| 하고 싶은 것 | 볼 곳 | 종류 |
| --- | --- | --- |
| 처음 설치하고 첫 실습까지 해 보기 | [getting-started.md](getting-started.md) | 튜토리얼 |
| 실습 하기 | [../labs/](../labs/) | 튜토리얼 |
| 특정 작업 방법 찾기 | [how-to/](how-to/) | how-to |
| API, 메시지 형식, 설정 값 찾아보기 | [reference/](reference/) | 레퍼런스 |
| 왜 이렇게 만들었는지 이해하기 | [explanation/](explanation/) | 설명 |
| 설계 결정과 그 이유 보기 | [adr/](adr/) | 설계 기록 |

## 문서 목록

상태: ✅ 작성됨 · 📝 예정

### how-to
- 📝 `how-to/add-a-lab.md` - 새 실습 만들기
- 📝 `how-to/use-api-model.md` - 에이전트에 API 모델 연결
- 📝 `how-to/connect-raspberry-pi.md` - 라즈베리파이 설비 연결

### reference
- 📝 `reference/api.md` - 관제 API
- 📝 `reference/mqtt-topics.md` - MQTT 토픽과 메시지 형식
- 📝 `reference/devices/` - 가상 설비 매뉴얼
- 📝 `reference/configuration.md` - 환경 변수와 실습 모드 설정
- 📝 `reference/threat-mapping.md` - 실습별 MITRE ATT&CK for ICS·IEC 62443 연결

### explanation
- 📝 `explanation/architecture.md` - 전체 구조
- 📝 `explanation/threat-model.md` - 위협 모델
- 📝 `explanation/deep-dives/` - 깊이 포인트 해설 (수집 신뢰성, 실시간 화면, 명령 보안 체인, 에이전트 안전성)

### adr
- ✅ [adr/README.md](adr/README.md) - 양식

## 어디에 쓸지 헷갈릴 때

- 읽는 사람이 **따라 하면서 배우는** 글 → 튜토리얼 (`getting-started.md`, `labs/`)
- 읽는 사람이 **이미 목표가 있고 방법만** 필요한 글 → `how-to/`
- **찾아보는** 사실 정보 (표, 목록, 형식) → `reference/`
- **왜**를 설명하는 글 → `explanation/`
- 결정 하나와 그 대안·이유 → `adr/`
