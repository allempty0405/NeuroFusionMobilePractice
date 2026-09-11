# Spacing, Radius, Shadow

## Spacing

| Token | 값 | 사용 |
|---|---:|---|
| `space-1` | 4px | icon-label |
| `space-2` | 8px | label-value, 안내-CTA |
| `space-3` | 12px | row 내부 보조 간격 |
| `space-4` | 16px | Mobile page padding, component padding |
| `space-5` | 20px | Financial Hero/Sheet 내부 후보 |
| `space-6` | 24px | 관련 정보 그룹 |
| `space-8` | 32px | 독립 section |

기본 Mobile page padding은 16px입니다. Full-width Tabs와 Divider는 별도 edge rule을 사용할 수 있습니다.

## Radius

| Token | 값 | 사용 |
|---|---:|---|
| `radius-sm` | 4px | badge |
| `radius-md` | 6px | button |
| `radius-lg` | 8px | input, summary surface |
| `radius-xl` | 12px | 제한적 대표 surface |
| `radius-2xl` | 16px | modal 내부 group |
| `radius-sheet` | 24px | Bottom Sheet top corners |
| `radius-pill` | 999px | Choice Chip |

일반 List Row에는 radius를 사용하지 않습니다. 카드 안에 카드를 중첩하지 않습니다.

## Shadow

- 기본 grouping은 spacing, surface, divider 순서로 해결합니다.
- Shadow는 Bottom Sheet, Popover 등 실제 elevation에만 사용합니다.
- Dark surface에 장식적 glow나 반복 card shadow를 사용하지 않습니다.

## Layout

- 최소 touch target: 44×44px
- Root Header와 Detail/Scrolled Header를 분리
- Sticky CTA가 마지막 콘텐츠를 가리지 않도록 bottom safe area 확보
- 360px와 430px에서 긴 금융 금액을 검증
