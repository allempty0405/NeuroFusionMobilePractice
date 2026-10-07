# Mobile Portfolio Pattern

**STATUS:** VALIDATED_IN_PORTFOLIO_PROTOTYPE  
**CURRENT PRODUCT SOURCE:** approved `04_MOBILE_PORTFOLIO_PRD.md`  
**CURRENT DESIGN SOURCE:** approved `05_MOBILE_PORTFOLIO_DESIGN.md`

Historical Prototype/Wireframe rules are reference only when they conflict with current PRD/DESIGN.

## Global IA

```text
투자분석
├─ 모아보기 — Aggregate Monitoring
├─ 포트폴리오 — Breakdown / Management
└─ 관심종목 — Attention / Tracking
```

Portfolio와 Watchlist는 같은 객체가 아닙니다.

`모아보기`는 selected Portfolio set에서 파생되는 Aggregate View이며 Portfolio Entity가 아닙니다.

Scope 변경은 Individual Portfolio navigation이 아닙니다.

## F-01 Locked Information Order

```text
선택한 포트폴리오
→ 투자 현황
→ 투자 비중
→ 보유 종목
→ 보유 종목 업데이트
```

`투자 현황 + 투자 비중`은 같은 Primary Summary Layer에 속합니다.

## Current Core Screens

| ID | 역할 |
|---|---|
| F-01 | 모아보기 Dashboard |
| F-02 | 포트폴리오 선택 Bottom Sheet |
| F-03 | 전체 Aggregate 보유 종목 |
| F-04 | Aggregate Holding Detail |
| F-05 | 보유 종목 업데이트 |
| F-06 | Update Detail |
| F-07 | 모든 포트폴리오 |
| F-08 | Individual Portfolio |
| F-09 | Individual Portfolio 전체 보유 종목 — conditional |
| F-10 | 투자 비중 Detail — >5 category fixture에서 conditional |
| F-11 | 포트폴리오 추가 |
| F-12 | 종목 추가 |
| F-13 | 보유 정보 수정 |

## Summary Pattern

- 총 평가금액 = single Financial Hero
- 일일 수익 = secondary
- 총 손익 / 총 수익률 = secondary
- Missing `—` ≠ numeric zero
- Reporting currency는 Holdings filter가 아님
- Large Performance Chart는 Core Dashboard requirement가 아님

Reusable component reference:
`components/financial-summary.md`

## Allocation Pattern

- `투자 비중`은 Holdings보다 앞에 유지
- Lenses: 자산별 / 종목별 / 국가별 / 섹터별
- Default: 자산별
- one distribution at a time
- Dashboard: 최대 5 category Concept preview
- >5 → F-10 Detail
- Visualization: Horizontal Bar + label + percentage

Reusable component reference:
`components/allocation-bar-list.md`

## Holdings Pattern

### F-01 Preview
- Label = `보유 종목`
- 4 rows Concept limit
- 가나다 순
- importance ranking 없음

### F-03 Full Holdings
Core:
- 종목명
- 보유 수량
- 평가금액
- 총 손익 / 총 수익률

Secondary:
- 보유비중

Default row에서 제외:
- 일일 등락
- 현재가
- 평균단가
- chart

### Duplicate Holding

같은 Asset이 여러 selected Portfolio에 있으면:

```text
one Aggregate Asset row
→ F-04
→ `포트폴리오별로 보기` inline disclosure
→ source Portfolio rows
```

Disclosure는 page navigation이 아닙니다.

Production aggregate average-cost arithmetic은 이 Pattern이 정의하지 않습니다.

## Updates Pattern

Five families:
- 뉴스
- 공시
- 일정
- 주요 이벤트
- 분석

Dashboard Preview = 3 Concept items.

`중요 / 추천 / AI 선정 / importance score`를 만들지 않습니다.

Reusable component reference:
`components/update-row.md`

## Portfolio Management

### F-07 모든 포트폴리오
- 투자 현황
- 투자 비중
- Portfolio comparison
- 포트폴리오 추가
- scoped Updates Preview

### F-08 Individual Portfolio
- Portfolio identity
- 총 평가금액
- 일일 수익
- 총 손익
- 보유 종목 Preview
- 종목 추가

**Individual Portfolio에 Allocation을 추가하지 않습니다.**

`포트폴리오 추가`와 `종목 추가`는 다른 context의 action입니다.

## State Pattern

구분:

```text
INLINE — Partial / Stale trust context
MODULE — Holdings / Allocation / Updates unavailable
PAGE — Core Summary failure
```

No Portfolio ≠ Empty Holdings.  
Partial ≠ Stale ≠ Disconnected.  
Missing ≠ 0.

상세 규칙은 `components/feedback-states.md` 참조.

## Visual Principles

- Dark Theme 우선
- Card보다 spacing과 divider 우선
- 반복 Holding/Portfolio = full-width row
- Financial number = tabular figures
- Green accent 과다 사용 금지
- 손익 = 부호 + 색상
- 화면별 Primary CTA 최대 하나
- Core Summary / Holdings / Portfolio comparison horizontal scroll 금지

## Responsive

검증 폭:
- 320 stress
- 360
- 390
- 430

320px에서 정보 밀도를 작은 글씨로 해결하지 않습니다.
Financial Hero는 필요 시 28/36 → 24/32로만 step-down하며 금액을 축약하지 않습니다.

## Accessibility

- Minimum hit target 44×44 logical px equivalent
- color-only financial/state signal 금지
- selected state에 text/check/underline 병행
- screen-reader intended semantics 문서화
- Manual Screen Reader Test가 없으면 `NOT TESTED`

## Excluded from Core

- Buy / Sell
- 거래 추가
- Transaction History
- Production aggregate formula
- verified FX formula
- Production freshness SLA
- Production update relevance ranking

## Prototype Validation Evidence — PHASE 6

- F-01/F-02/F-03/F-04/F-05/F-07/F-08 rendered at 320 / 360 / 390 / 430px
- horizontal overflow: none in tested core screens
- Holdings Row collision: none in tested widths
- F-01 preview: Allocation 5 / Holdings 4 / Updates 3
- F-02 zero selection: Apply disabled + guidance
- Duplicate Asset fixture: one Aggregate Row → two source Portfolio rows
- Individual Portfolio: Allocation absent
- Empty Holdings: `₩0 / — / —`
- Partial/Stale/Disconnected visually distinct
- Screen Reader Manual Test: NOT TESTED
