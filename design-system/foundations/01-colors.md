# Colors

## 구조

Color는 `primitive → semantic → component state` 순서로 사용합니다.

- Primitive: Zinc, Green, Red 등 원시 팔레트
- Semantic: surface, text, border, financial
- Component: selected, disabled, scrim 등 상태

## Theme

같은 역할은 Light/Dark에서 같은 semantic token 이름을 사용합니다. Web Light는 기존 CSS 값을 보존하고, Mobile Dark는 실기기 Screenshot 추출값과 가장 가까운 primitive token에 연결합니다.

| 역할 | Screenshot 근삿값 | Dark token mapping |
|---|---|---|
| Page | `#18181A` | `zinc-900` |
| Raised surface | `#27272A` | `zinc-800` |
| Muted surface | `#3F4045` | `zinc-700` |
| Input surface | `#515158` | `zinc-600` |
| Strong title | `#F3F3F4` | `zinc-100` |
| Strong text | `#E0E1E1` | `zinc-200` |
| Body text | `#CDCDCE` | `zinc-300` |
| Muted text | `#6C6D70` | `zinc-500` |
| Divider | `#2D2C2F` | `zinc-800` |
| Primary | 약 `#22C55E` | `green-500` |

Screenshot 값은 token 선택을 위한 Evidence이며 별도의 유사 HEX를 계속 늘리지 않습니다. 명확한 대응 primitive가 없는 Scrim과 selected surface는 Screenshot reference에서 확정한 고정 semantic 값을 사용합니다.

## Financial Color

금융 손익은 시스템 성공/오류와 분리합니다.

| Token | Mapping | 용도 |
|---|---|---|
| `financial-gain` | `green-500` | 양의 손익 |
| `financial-loss` | `red-400` | 음의 손익 |
| `financial-flat` | `zinc-200` | 0 또는 변화 없음 |

손익에는 색상과 함께 `+`, `−`, 금액 또는 비율을 표시합니다. `financial-loss`를 form error나 system error에 사용하지 않습니다.

## State

- Primary Green: Primary CTA, selected tab, selected choice, checkbox/radio selected
- Disabled: 공통 disabled surface/text/icon token 사용
- Disabled는 의도적으로 낮은 대비를 허용하되 활성 상태와 구분
- Scrim: Bottom Sheet 뒤의 비활성 Context
- Divider: 카드 대신 정보 구획을 보조하는 낮은 대비
- Green을 section decoration이나 모든 chip에 반복하지 않음

## 금지

- Primitive color를 component에서 직접 사용
- Light surface를 Dark theme에서 그대로 사용
- Screenshot마다 새 HEX token을 추가
- 색상만으로 손익·선택·상태 전달
- Gain/Loss를 Success/Error와 같은 의미로 처리


## Fixed Selected Color

Mobile Dark selected surface는 투명도나 `color-mix()`를 사용하지 않고 Screenshot reference와 가까운 고정값 `#1E2520`을 사용합니다. 배경과 조합되는 결과가 실행 환경마다 달라지지 않도록 합니다.
