# Source & Boundary

## Source

이 시스템은 두 종류의 Visual Evidence를 사용합니다.

| Source | 용도 | 한계 |
|---|---|---|
| Valley AI Web 개발자도구 CSS | Primitive, semantic naming, Web Light 값 | Mobile Dark 구조와 동일하다고 가정하지 않음 |
| Valley AI Mobile 실기기 Screenshot | Mobile hierarchy, density, Light/Dark surface, component geometry | Screenshot만으로 제품 요구사항을 만들지 않음 |

실기기 기준은 Galaxy S25 Ultra, FHD+ 2340×1080, 기본 글자 크기, 기본 화면 크기입니다. Dark JPG는 구조 검증에 사용하고, 색상값은 PNG와 Web token을 함께 대조합니다.

## 범위

현재 Primary 범위는 **Mobile Portfolio**입니다.

포함:

- Light/Dark theme semantic variables
- Mobile typography와 financial number hierarchy
- spacing, radius, divider, scrim
- Tabs, Choice Chip, Checkbox/Radio
- Button, Sticky CTA, Bottom Sheet
- Portfolio/Holding List Row
- Portfolio empty/disabled state
- Currency selector와 reporting currency 표현

별도 Pattern:

- `patterns/portfolio-aware-event-triage.md`는 Event Triage Workstream 전용입니다.
- Event Triage의 실제 보유값 제한, Outcome, Evidence, Web handoff 규칙은 Mobile Portfolio 전역에 적용하지 않습니다.

제외:

- Valley AI 전체 제품의 공식 디자인 시스템
- 실제 데이터 계약과 계산 로직
- 거래 History와 transaction accounting
- 현금성 자산
- 매수·매도·보유 추천 표현

## 변경 원칙

1. Web Light 값은 삭제하지 않고 `[data-theme="light"]`에 보존합니다.
2. Mobile Screenshot에서 확인한 Dark 값은 `[data-theme="dark"]`에 분리합니다.
3. Screenshot 추정값은 `reference`이며 Production 적용 전 contrast와 실기기 QA를 수행합니다.
4. 새 token이나 component는 사용 상황과 금지 상황을 함께 기록합니다.
