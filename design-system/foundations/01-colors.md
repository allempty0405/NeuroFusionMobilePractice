# Colors

## 구조

Color는 `primitive → semantic → component state` 순서로 사용합니다.

- Primitive: Zinc, Green, Red 등 원시 팔레트
- Semantic: surface, text, border, financial
- Component: selected, disabled, scrim 등 상태

## Theme

같은 역할은 Light/Dark에서 같은 semantic token 이름을 사용합니다.

| 역할 | Light reference | Dark mobile reference |
|---|---|---|
| Page | Zinc 100/50 | 약 `#18181A` |
| Raised surface | White | 약 `#27272A` |
| Muted surface | Zinc 50/100 | 약 `#3F4045` |
| Input surface | Zinc 100 | 약 `#515158` |
| Strong text | Zinc 900 | 약 `#F3F3F4` |
| Body text | Zinc 700 | 약 `#CDCDCE` |
| Muted text | Zinc 500 | 약 `#6C6D70` |
| Divider | Zinc 200 | 약 `#2D2C2F` |
| Primary | Green 500 | Green 500 |

Dark 값은 실기기 Screenshot 기반 reference입니다. JPEG 단일 픽셀값을 공식 원본값으로 취급하지 않습니다.

## Financial Color

금융 손익은 시스템 성공/오류와 분리합니다.

| Token | 용도 |
|---|---|
| `financial-gain` | 양의 손익 |
| `financial-loss` | 음의 손익 |
| `financial-flat` | 0 또는 변화 없음 |

손익에는 색상과 함께 `+`, `−`, 금액 또는 비율을 표시합니다. `financial-loss`를 form error나 system error에 사용하지 않습니다.

## State

- Primary Green: Primary CTA, selected tab, selected choice, checkbox/radio selected
- Disabled: 공통 disabled surface/text/icon token 사용
- Scrim: Bottom Sheet 뒤의 비활성 Context
- Divider: 카드 대신 정보 구획을 보조하는 낮은 대비
- Green을 section decoration이나 모든 chip에 반복하지 않음

## 금지

- Primitive color 직접 사용
- Light surface를 Dark theme에서 그대로 사용
- 색상만으로 손익·선택·상태 전달
- Gain/Loss를 Success/Error와 같은 의미로 처리
