# Mobile Portfolio Design QA

## Source / Boundary

- [ ] Current approved Product PRD가 Historical Prototype보다 우선한다.
- [ ] Current approved DESIGN이 Historical visual implementation보다 우선한다.
- [ ] 이 Design System을 Valley 공식 Production DS라고 주장하지 않는다.

## Theme

- [ ] Light/Dark가 같은 semantic token 이름을 사용한다.
- [ ] App explicit theme가 OS automatic보다 우선한다.
- [ ] Page, raised, muted, input surface가 Dark에서 구분된다.
- [ ] Green accent를 CTA / selected / gain semantics에 제한한다.

## Information Hierarchy

- [ ] F-01 order = 선택한 포트폴리오 → 투자 현황 → 투자 비중 → 보유 종목 → 보유 종목 업데이트.
- [ ] 투자 현황과 투자 비중이 같은 Primary Summary Layer로 읽힌다.
- [ ] Holdings가 Allocation 앞에 올라오지 않는다.
- [ ] Large Performance Chart가 Core Dashboard를 차지하지 않는다.

## Typography & Number

- [ ] 총 평가금액 또는 현재가가 단일 Hero anchor다.
- [ ] 금융 숫자에 tabular figures를 사용한다.
- [ ] 핵심 금액을 축약하거나 ellipsis 처리하지 않는다.
- [ ] Missing `—`와 valid zero를 구분한다.
- [ ] Metadata를 과도하게 bold 처리하지 않는다.
- [ ] 320 / 360 / 390 / 430px에서 긴 금액을 확인한다.

## Components

- [ ] 반복 Holding/Portfolio를 Card로 만들지 않는다.
- [ ] Touch target이 44×44px 이상이다.
- [ ] Bottom Sheet에 scrim, handle, internal scroll, safe area가 있다.
- [ ] Disabled control은 실제 click/keyboard/submit 입력을 차단한다.
- [ ] Icon에 text glyph를 final asset으로 사용하지 않는다.
- [ ] Sticky CTA가 마지막 콘텐츠를 가리지 않는다.

## Scope / Navigation

- [ ] Scope 변경은 Portfolio navigation처럼 동작하지 않는다.
- [ ] Portfolio 1개 선택도 `모아보기`에 남는다.
- [ ] F-02 0개 draft selection은 가능하지만 Apply는 disabled다.
- [ ] F-02 닫기/취소는 draft를 discard한다.
- [ ] Back은 실제 entry history를 따른다.

## Allocation

- [ ] 자산별 / 종목별 / 국가별 / 섹터별 4 lens가 유지된다.
- [ ] Default는 자산별이다.
- [ ] 한 번에 하나의 distribution만 표시한다.
- [ ] Dashboard는 최대 5 category Concept preview다.
- [ ] Horizontal Bar + label + %가 color 없이도 해석 가능하다.

## Holdings

- [ ] Section label은 `보유 종목`이다.
- [ ] Dashboard Preview는 최대 4 rows다.
- [ ] Default ordering은 가나다 순이다.
- [ ] Importance ranking/AI score가 없다.
- [ ] Full Row에 종목명 / 보유 수량 / 평가금액 / 총 손익·총 수익률이 있다.
- [ ] 보유비중은 secondary다.
- [ ] 일일 등락은 default row에서 제외된다.
- [ ] 동일 Asset 중복 보유는 one Aggregate Asset identity로 보인다.
- [ ] `포트폴리오별로 보기`는 inline disclosure다.
- [ ] Portfolio breakdown row의 `수정` hit area는 44×44px 이상이다.

## Updates

- [ ] 뉴스 / 공시 / 일정 / 주요 이벤트 / 분석 5 family가 유지된다.
- [ ] Dashboard Preview는 최대 3 items다.
- [ ] `중요 / 추천 / AI 선정 / importance score`가 없다.
- [ ] 일정의 future datetime이 과거 timestamp와 구분된다.
- [ ] Full Updates / Detail에서 inherited Portfolio context가 유지된다.

## Portfolio Management

- [ ] F-07 모든 포트폴리오에 Summary / Allocation / Comparison / 포트폴리오 추가가 있다.
- [ ] F-08 Individual Portfolio에 Allocation이 없다.
- [ ] `포트폴리오 추가`와 `종목 추가`가 같은 global action level에 있지 않다.
- [ ] Buy / Sell / 거래 추가 / Transaction History가 Core에 없다.

## State

- [ ] No Portfolio와 Empty Holdings가 구분된다.
- [ ] Empty Holdings = 총 평가금액 ₩0, P/L = `—`.
- [ ] Partial과 normal complete Aggregate가 구분된다.
- [ ] Stale이 최신값처럼 보이지 않는다.
- [ ] Disconnected source가 silently complete aggregate로 보이지 않는다.
- [ ] Module Error가 valid Summary를 가리지 않는다.
- [ ] Page-critical Error에서도 trusted Scope/context는 가능한 범위에서 유지한다.

## Responsive

- [ ] 320 / 360 / 390 / 430px rendered QA를 수행한다.
- [ ] Summary horizontal scroll 없음.
- [ ] Holdings row horizontal scroll 없음.
- [ ] Portfolio comparison horizontal scroll 없음.
- [ ] Long Korean/English asset name과 large KRW/USD value를 확인한다.

## Accessibility

- [ ] Gain/Loss/Flat을 색상만으로 전달하지 않는다.
- [ ] focus-visible이 있다.
- [ ] tab/checkbox/disclosure selected state가 semantic하게 표현된다.
- [ ] interactive control hit target ≥44px.
- [ ] Screen Reader Manual Test를 실제로 하지 않았다면 PASS로 표시하지 않는다.
