# No AI Slop Korean plugin submission

## Positioning

No AI Slop Korean은 한국어 글에서 상투적인 AI 문체와 번역투를 제거하면서 작성자의 말투, 높임말 수준과 구체적인 사실을 보존합니다.

## Starter prompts

1. @No AI Slop Korean 이 한국어 초안을 자연스럽게 다듬어 주세요.
2. @No AI Slop Korean 이 글에서 AI처럼 보이는 문체 패턴만 찾아주세요.

## Positive test cases

1. 상투적인 도입, `A가 아니라 B` 대비와 요약형 결론이 있는 블로그 초안을 편집한다. 원문의 해요체와 개인적인 경험은 유지한다.
2. 업무 보고서를 다시 쓰지 않고 검사한다. 패턴 이름, 짧은 원문 인용, 이유와 수정 방향만 제시한다.
3. 유머와 여담이 있는 개인 에세이를 편집한다. 실제 AI 문체만 제거하고 개성은 보존한다.
4. 구체적인 수치가 포함된 제품 업데이트를 편집한다. 모든 사실을 보존하고 번역투와 명사화만 줄인다.
5. 긴 구어체 초안을 편집한다. 이해하기 어려운 문장만 풀고 자연스러운 리듬과 높임말 수준은 유지한다.

## Negative test cases

1. 사용자가 초안 없이 사실 질문만 하면 편집 절차를 실행하지 않는다.
2. 사용자가 AI 작성 여부를 물으면 저자를 추측하지 않고 문체 패턴 검사를 제안한다.
3. 사용자가 근거 자료를 만들어 달라고 하면 수치나 출처를 꾸미지 않는다.
4. 이미 자연스러운 사람이 쓴 글은 불필요하게 다시 쓰지 않는다.

## Release notes

Version 1.0.0 introduces Korean-specific editing and detection rules for speech levels, translationese, nominalization, repetitive endings, inflated contrasts, unsupported interpretation and repetitive conclusions. It keeps edit and detect modes and requires no external server or authentication.
