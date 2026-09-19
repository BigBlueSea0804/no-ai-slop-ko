# No AI Slop Korean

한국어 글에서 상투적인 AI 문체와 번역투를 줄이면서 작성자의 말투, 높임말 수준과 구체적인 정보를 보존하는 글쓰기 스킬입니다.

이 프로젝트는 Peter Yang의 [No AI Slop](https://github.com/petergyang/no-ai-slop)을 바탕으로 한국어 글쓰기 특성에 맞게 수정한 버전입니다.

## 해결하려는 문제

한국어 AI 글에는 다음과 같은 표현이 반복되는 경우가 많습니다.

- "단순히 A가 아니라 B입니다"
- "A를 넘어 새로운 경험을 제공합니다"
- "이는 중요한 의미를 지닙니다"
- "사용자가 효율적으로 작업할 수 있도록 지원합니다"
- `혁신적인`, `획기적인`, `게임 체인저` 같은 근거 없는 과장
- 모든 문장이 `~합니다`로 끝나는 기계적인 리듬
- 본문을 그대로 반복하는 결론

No AI Slop Korean은 이런 패턴을 고치되 글쓴이의 유머, 직설적인 표현, 개인적인 여담과 말투는 가능한 한 유지합니다.

## 설치

ChatGPT, Claude Code, Codex 또는 스킬 설치를 지원하는 에이전트에 다음과 같이 요청할 수 있습니다.

```text
https://github.com/BigBlueSea0804/no-ai-slop-ko 에서
/no-ai-slop-ko 스킬을 전역으로 설치해 주세요.
```

`npx`를 사용할 수도 있습니다.

```sh
npx skills add BigBlueSea0804/no-ai-slop-ko --skill no-ai-slop-ko --global --yes
```

## 사용법

### 글 편집

```text
/no-ai-slop-ko

다음 글에서 상투적인 AI 표현과 번역투를 제거하되,
제 말투와 존댓말 수준은 유지해 주세요.

[초안]
```

기본 결과에는 수정한 전체 글과 짧은 **수정한 내용**이 포함됩니다.

### 패턴만 검사

```text
/no-ai-slop-ko

다음 글에서 AI처럼 보이는 문체 패턴만 찾아주세요.
글을 다시 쓰거나 AI 작성 확률을 제시하지 마세요.

[검사할 글]
```

검사 모드는 발견한 패턴의 이름, 원문, 이유와 수정 방향을 제시합니다. AI가 작성했는지는 추측하지 않습니다.

### 편집 강도 지정

```text
/no-ai-slop-ko 최소한으로만 수정해 주세요. [초안]
```

```text
/no-ai-slop-ko 문단 구조까지 적극적으로 다듬어 주세요. [초안]
```

## 주요 검사 항목

1. 상투적인 도입
2. `A가 아니라 B`, `A를 넘어 B` 형태의 과장
3. `보여줍니다`, `시사합니다`, `방증합니다` 형태의 근거 없는 해설
4. 번역투와 우회적인 표현
5. 명사화와 공문서체
6. 기계적인 종결어미 반복
7. 습관적인 삼단 나열과 동의어 순환
8. 중요성을 강요하는 표현
9. 요약형 결론과 가짜 통찰형 마지막 문장
10. 장식적인 이모지, 굵은 글씨와 지나친 소제목

## 파일 구조

- [`SKILL.md`](skills/no-ai-slop-ko/SKILL.md): 작업 모드, 편집 원칙과 실행 절차
- [`korean-patterns.md`](skills/no-ai-slop-ko/references/korean-patterns.md): 한국어 문체 패턴과 예시
- [`eval.md`](skills/no-ai-slop-ko/eval.md): 결과 자체 검수 기준
- [`plugin.json`](.codex-plugin/plugin.json): ChatGPT 및 Codex 플러그인 정보
- [`build_plugin.py`](scripts/build_plugin.py): 플러그인 패키지 생성과 검증

## 개인정보

이 프로젝트는 외부 서버를 실행하지 않는 skills-only 플러그인입니다. 입력한 글은 사용하는 ChatGPT, Codex 또는 다른 에이전트의 정책에 따라 처리됩니다.

## 라이선스와 원작

MIT License. 원작의 저작권 고지와 라이선스는 [`LICENSE`](LICENSE)에 유지되어 있습니다.
