# Dropdown Menu

## Role

단일 값 선택이 현재 화면 안에서 짧게 끝나는 경우 사용하는 generic select component입니다.

PHASE 6E R17부터 기존 Reporting Currency control의 visual grammar를 Dropdown의 기준으로 사용합니다.

대표 사용:

- Reporting Currency
- OCR 종목 매칭
- OCR 통화
- Full Holdings 정렬

Portfolio Scope처럼 다중 선택 / 긴 context가 필요한 경우 Dropdown이 아니라 Bottom Sheet를 사용합니다.

## Anatomy

```text
Dropdown
├─ Trigger
│  ├─ Selected value
│  └─ Chevron Down
└─ Menu
   ├─ Option
   ├─ Option
   └─ Selected Option + Check
```

## Trigger

Class grammar:

- `.currency-select`
- `.currency-select-trigger`

Generic Dropdown도 이 grammar를 재사용합니다.

Rule:

- Minimum height: 44px
- Selected/current value를 직접 표시
- Chevron Down
- `aria-haspopup="listbox"`
- `aria-expanded`
- Disabled state는 native `disabled` 사용

## Menu

Class grammar:

- `.currency-menu`

Rule:

- Elevated dark surface
- Border + floating shadow
- Option minimum height: 44px
- Long list: max-height + internal scroll
- Current option: `aria-selected="true"`
- Current option에는 check icon 제공
- selected 의미를 color alone으로 전달하지 않음

## Option

Class grammar:

- `.currency-option`

Content:

```text
Label                                      Check
```

OCR Asset example:

```text
Apple · AAPL                               ✓
Microsoft · MSFT
NVIDIA · NVDA
```

## Interaction

Trigger:

- Click / Enter / Space → menu open

Menu:

- Arrow Down / Arrow Up → option 이동
- Home / End → first / last
- Enter / Space → 선택
- Escape → close
- outside click → close

Close 후 focus는 trigger로 복원합니다.

## OCR Review

Browser native `<select>`를 Product UI로 사용하지 않습니다.

R17:

- `assetId` → generic Dropdown
- `currency` → generic Dropdown

중복 Holding 등 선택 불가 상태에서는 Dropdown trigger도 disabled 처리합니다.

## Full Holdings Sort

Full Holdings의 정렬도 동일 Dropdown grammar를 사용합니다.

Options:

- 평가수익률 높은 순
- 평가수익률 낮은 순
- 평가금액 높은 순
- 평가금액 낮은 순
- 1일 등락률 높은 순
- 1일 등락률 낮은 순
- 가나다 순

## Currency Dropdown

Reporting Currency는 같은 Trigger / Menu / Option grammar를 유지합니다.

Financial meaning과 접근성 label이 visible value와 항상 일치해야 합니다.

## Do / Don't

### Do

- 짧은 single-select에 사용
- trigger에서 current selection 표시
- selected check 제공
- keyboard / focus restore 지원

### Don't

- Multi-select Portfolio Scope에 Dropdown 사용
- native select와 custom menu를 화면마다 혼용
- color만으로 selected state 표시
- menu가 viewport 밖으로 잘리게 배치
