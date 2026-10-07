# Feedback States

**STATUS:** VALIDATED_IN_PORTFOLIO_PROTOTYPE

## Severity Model

모든 상태를 큰 warning card로 만들지 않습니다.

```text
INLINE
→ Partial / Stale / contextual trust limitation

MODULE
→ Holdings / Allocation / Updates 등 supporting module failure

PAGE
→ Core Portfolio Summary failure
```

## 공통 상태

| 상태 | 표현 |
|---|---|
| Loading | Final geometry와 유사한 Skeleton. fake `₩0` 금지 |
| Empty | 객체는 존재하지만 내용 없음 |
| No Portfolio | Portfolio 자체 없음. Portfolio creation이 recovery |
| Partial | 정상 Complete Aggregate와 구분되는 inline trust notice |
| Stale | 최신성 한계를 inline으로 표시. Page error처럼 과장하지 않음 |
| Disconnected | source 연결 손실과 aggregate completeness 한계를 표시 |
| Disabled | 선행 조건 미충족, 실제 실행 차단 |
| Module Error | 해당 module만 대체하고 신뢰 가능한 Summary 유지 |
| Page Error | Core Summary 계산/표시 실패. Scope 등 신뢰 가능한 context는 유지 |

## Portfolio Empty

No Portfolio:
- 정상 Aggregate Summary를 `₩0`으로 표시하지 않음
- Primary recovery: `포트폴리오 추가`

Empty Portfolio / Empty Holdings:
- 총 평가금액 `₩0`
- 일일 수익 `—`
- 총 손익 `—`
- 수익률 `—`
- Individual Portfolio recovery: `종목 추가`

계산되지 않은 값을 0 또는 0%로 만들지 않습니다.

## Partial

- `일부 정보를 모두 반영하지 못했습니다`와 같은 completeness cue 필요
- Partial total을 정상 complete total처럼 읽히게 하지 않음
- 실제 포함/제외 산술 정책은 Product/Data Contract가 결정

## Stale

- 마지막 업데이트 시점은 실제 source가 있을 때만 노출
- 정확한 stale threshold/SLA를 Design System이 정의하지 않음
- 정상 화면을 유지할 수 있으면 inline hierarchy 사용

## Disconnected

- 연결이 끊긴 source가 있다는 사실을 숨기지 않음
- 나머지 source만으로 만든 값을 `전체`로 오해시키지 않음
- 계산 정책은 Design System이 정하지 않음

## Module Error

- Supporting module error가 정상 Summary를 가리지 않음
- module title/context는 유지하고 unavailable + recovery를 표시

## Zero Selection

F-02에서 0개 선택은 draft로 허용하지만 적용은 차단합니다.

- `적용하기` disabled
- `포트폴리오를 1개 이상 선택해 주세요.`
- Sheet를 닫으면 변경 discard
- 이전 적용 범위 유지

Disabled 값은 범용 component token을 재사용합니다.
