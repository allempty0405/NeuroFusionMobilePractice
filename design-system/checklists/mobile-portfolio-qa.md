# Mobile Portfolio Design QA

## Theme

- [ ] Light/Dark가 같은 semantic token 이름을 사용한다.
- [ ] App explicit theme가 OS automatic보다 우선한다.
- [ ] Page, raised, muted, input surface가 Dark에서 구분된다.
- [ ] Green accent를 CTA와 selected state에 집중한다.

## Typography & Number

- [ ] 총 평가금액 또는 현재가가 단일 Hero anchor다.
- [ ] 금융 숫자에 tabular figures를 사용한다.
- [ ] 금액을 축약하거나 ellipsis 처리하지 않는다.
- [ ] Metadata를 과도하게 bold 처리하지 않는다.
- [ ] 360px와 430px에서 긴 금액을 확인한다.

## Components

- [ ] 반복 Holding/Portfolio를 Card로 만들지 않는다.
- [ ] Touch target이 44×44px 이상이다.
- [ ] Bottom Sheet에 scrim, handle, scroll, safe area가 있다.
- [ ] Disabled control은 공통 token을 사용하고 실제 click·keyboard·submit 입력을 차단한다.
- [ ] Icon에 text glyph를 사용하지 않는다.
- [ ] Sticky CTA가 마지막 콘텐츠를 가리지 않는다.

## Product Locks

- [ ] Portfolio와 Watchlist가 구분된다.
- [ ] Scope 변경이 Portfolio navigation처럼 동작하지 않는다.
- [ ] F-02에서 0개 선택 시 Apply가 disabled다.
- [ ] F-03 금액을 축약하지 않는다.
- [ ] F-05 기본 sort는 가나다다.
- [ ] F-06 breakdown은 inline이고 Chevron이 없다.
- [ ] F-06 수정은 Portfolio row의 Text Button이며 최초 hit area는 44×44px이다.
- [ ] 거래 History와 현금성 자산을 Core에 넣지 않는다.
- [ ] Back이 실제 entry history를 따른다.

## Currency

- [ ] KRW가 항상 첫 번째다.
- [ ] Scope에 없는 통화를 노출하지 않는다.
- [ ] Currency를 Asset Filter처럼 표현하지 않는다.
- [ ] F-01 Variant A/B의 underlying behavior가 동일하다.
- [ ] F-06 secondary currency의 위계가 낮다.

## State

- [ ] No Portfolio와 Empty Portfolio가 구분된다.
- [ ] 계산되지 않은 값은 0 대신 em dash다.
- [ ] Gain/Loss/Flat을 색상만으로 전달하지 않는다.


## Visual Review Hold

- [ ] F-06 Text Button 44px hit area가 hierarchy와 density를 해치지 않는지 시안으로 확인한다.
- [ ] F-03 비축약 금액이 360px에서 overflow하지 않는지 시안으로 확인한다.
