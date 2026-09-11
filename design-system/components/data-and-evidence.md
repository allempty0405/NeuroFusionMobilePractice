# Financial Data Display

## Mobile Portfolio 기본 필드

UX Specification이 요구하는 화면에서 다음 값을 표시할 수 있습니다.

- 총 평가금액
- 일일 수익
- 총 수익
- 보유 수량
- 평균단가
- 현재가
- Portfolio별 Holding Snapshot

이는 Event Triage의 개인정보·실제 보유값 제한과 별개입니다.

## 숫자 규칙

- 통화 기호와 부호 유지
- 금액 축약 금지
- 핵심 값 ellipsis 금지
- tabular figures 사용
- 손익은 색상과 `+`/`−`, 금액/비율을 함께 표시
- 계산되지 않은 값은 `—`; 0이나 0%로 대체하지 않음

## Reporting Currency

- KRW는 항상 포함하고 첫 번째
- Scope에 존재하는 통화만 노출
- Currency 선택은 Asset Filter가 아님
- Aggregate 화면 전체 값을 선택한 currency로 표시
- F-06 해외 종목 Hero는 Local Currency + 낮은 위계의 KRW equivalent 허용
- 하위 financial metric group은 하나의 reporting currency로 통일

## Classification

분류 metadata가 없으면 `분류 정보 없음`으로 표시합니다. 임의 추정하지 않습니다.
