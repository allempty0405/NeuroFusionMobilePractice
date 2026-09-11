# Cards & Surfaces

## Surface Hierarchy

| Level | Token | 사용 |
|---|---|---|
| Page | `--nf-surface-page` | 전체 배경 |
| Raised | `--nf-surface-raised` | Bottom Sheet, 필요한 summary |
| Muted | `--nf-surface-muted` | Input, grouped information |
| Selected | `--nf-surface-selected` | 선택 보조 표현 |
| Scrim | `--nf-scrim` | Sheet 뒤 context |

## Mobile Portfolio 원칙

- Holding/Portfolio 반복 목록은 Card가 아닌 full-width row
- Section은 spacing과 낮은 divider로 구분
- 대표 Financial Hero에만 제한적으로 surface 허용
- 카드 안에 카드 중첩 금지
- Shadow는 Sheet/Popover처럼 실제 elevation이 있는 경우만 사용
- 모든 정보를 chip이나 badge로 만들지 않음
- Page와 raised surface의 차이가 theme 양쪽에서 확인되어야 함

## Dense Data

Mobile 첫 화면에는 긴 표, 세부 재무표, 큰 차트와 반복 Card를 동시에 배치하지 않습니다. 숫자 비교에는 일정한 column과 tabular figures를 우선합니다.
