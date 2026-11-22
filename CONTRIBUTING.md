# 기여 가이드

breachline은 아직 초기 단계입니다. 이슈와 제안은 언제든 환영합니다.

## 처음 설정

커밋 전에 비밀 값 유출과 커밋 메시지 형식을 자동으로 검사합니다.

```bash
brew install pre-commit   # 또는 pip install pre-commit
pre-commit install        # 커밋 전 검사 + 커밋 메시지 검사 훅 설치
pre-commit run --all-files   # (선택) 전체 파일 한 번 검사
```

검사 항목은 [`.pre-commit-config.yaml`](.pre-commit-config.yaml)에 있습니다.

## 커밋 메시지

영어로, [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) 형식을 따릅니다. 자세한 규칙은 [`.claude/skills/commit/SKILL.md`](.claude/skills/commit/SKILL.md)를 보세요.

```
feat(gateway): add role-based access check for device commands
```

## 새 실습 추가

1. [`labs/_template/`](labs/_template/)을 복사해 `labs/NN-이름/`을 만듭니다
2. 가이드(`README.md`)와 풀이(`SOLUTION.md`)를 나눠 씁니다
3. `verify/`에 "방어 끔=공격 성공, 켬=공격 실패"를 확인하는 테스트를 넣습니다
4. [`labs/README.md`](labs/README.md) 목록과 [`docs/reference/threat-mapping.md`](docs/reference/threat-mapping.md)에 추가합니다

## 문서

어디에 쓸지는 [docs/README.md](docs/README.md)의 "어디에 쓸지 헷갈릴 때"를 참고하세요.

## 보안 문제

취약점은 이슈 대신 [SECURITY.md](SECURITY.md)의 방법으로 알려 주세요.
