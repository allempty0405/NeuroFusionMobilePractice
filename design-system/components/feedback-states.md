# Feedback States

## 공통 상태

| 상태 | 표현 |
|---|---|
| Loading | Skeleton과 필요한 경우 text |
| Empty | 객체는 존재하지만 내용 없음 |
| No Portfolio | Portfolio 자체 없음 |
| Disabled | 선행 조건 미충족, 실행 차단 |
| Stale | 정상 화면과 구분하고 마지막 시점 제공 |
| Permission | 제한 이유와 가능한 행동 구분 |
| Error | 원인과 recovery action 제공 |

## Portfolio Empty

No Portfolio:

- Primary: `포트폴리오 추가`

Empty Portfolio:

- 총 평가금액 `₩0`
- 일일 수익 `—`
- 총 수익 `—`
- 수익률 `—`
- Sticky action: `종목 추가`

계산되지 않은 값을 0 또는 0%로 만들지 않습니다.

## Zero Selection

F-02에서 0개 선택은 draft로 허용하지만 적용은 차단합니다.

- `적용하기` disabled
- `포트폴리오를 1개 이상 선택해 주세요.`
- Sheet를 닫으면 변경 discard
- 이전 적용 Scope 유지

Disabled 값은 범용 component token을 재사용합니다.
