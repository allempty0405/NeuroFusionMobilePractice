# Components

Mobile Portfolio에서 반복되는 범용 component와 상태를 정리합니다.

| 파일 | 내용 |
|---|---|
| `buttons-and-cta.md` | Primary/Secondary/Text/Disabled/Sticky CTA |
| `cards-and-surfaces.md` | Page, Hero, grouped surface, divider |
| `badges-tabs-filters.md` | Navigation Tabs, Dimension Tabs, Filter, Choice Chip |
| `selection-controls.md` | Checkbox, Radio, zero-selection |
| `bottom-sheet.md` | Sheet, scrim, internal scroll, sticky action |
| `list-rows.md` | Portfolio/Holding/Breakdown/Search rows |
| `financial-summary.md` | Total valuation + daily/cumulative financial summary group |
| `allocation-bar-list.md` | Mobile allocation lens + horizontal percentage distribution |
| `update-row.md` | Portfolio-scoped 뉴스/공시/일정/이벤트/분석 row |
| `data-and-evidence.md` | 금융값, reporting currency, metadata |
| `feedback-states.md` | Loading, Empty, Partial, Stale, Disconnected, Module/Page Error |

Component는 정보 위계를 보조합니다. 기능이 많아 보이게 하기 위해 Card, Badge, Chip을 늘리지 않습니다. Event Triage 전용 component는 해당 pattern 문서에 한정합니다.

`FormField`는 PHASE 6 Portfolio Prototype에서 반복 사용했지만 Portfolio 추가/종목 추가의 Production field contract가 아직 완전하지 않으므로 현재 generic DS component로 승격하지 않습니다.
