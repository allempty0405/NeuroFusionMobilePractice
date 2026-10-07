# Valley AI Mobile Portfolio Design System

이 폴더는 Valley AI Web 개발자도구 스타일과 Valley AI Mobile 실기기 스크린샷을 근거로, `NeuroFusionMobilePractice`의 **Mobile Portfolio** 화면을 설계·구현하기 위한 참고 디자인 시스템입니다.

Valley AI 공식 디자인 시스템이나 1:1 복제본이 아닙니다. Web의 primitive/token 구조는 보존하되, Mobile의 Light/Dark theme, 밀도, Bottom Sheet, List Row와 금융 데이터 표현을 별도 semantic layer로 정리합니다.

> **STATUS: REFERENCE DS / NeuroFusion Reference Design System**  
> 이 저장소의 token, component, pattern은 Valley 공식 Production Design System이라고 주장하지 않습니다.

## Source 우선순위

기존 Historical Prototype 자료는 보존하되, **현재 Mobile Portfolio Workstream**에서는 다음 우선순위를 사용합니다.

1. 승인된 Current Mobile Portfolio Product PRD (`04_MOBILE_PORTFOLIO_PRD.md`)
2. 승인된 Current Mobile Portfolio DESIGN (`05_MOBILE_PORTFOLIO_DESIGN.md`)
3. Current Web → Mobile Transformation Rules (`03_WEB_TO_MOBILE_TRANSFORMATION_RULES.md`)
4. Verified Valley Product / Web / Mobile evidence
5. 이 Reference Design System
6. Historical Prototype / Wireframe material
7. External reference / inference

다른 Workstream의 Source Priority를 이 규칙으로 자동 대체하지 않습니다. 이 우선순위는 현재 Mobile Portfolio Workstream의 정합성 문제를 해결하기 위한 범위 제한 규칙입니다.

Web CSS와 Screenshot은 visual evidence이며 새로운 Product Requirement를 만들지 않습니다. Historical Prototype이 현재 PRD/DESIGN과 충돌하면 Historical Prototype을 수정 근거로 사용하지 않습니다.

## 폴더

| 폴더 | 내용 |
|---|---|
| `foundations/` | Source 경계, Light/Dark color, typography, spacing, radius, accessibility |
| `tokens/` | Theme별 CSS variables와 token mapping |
| `components/` | Button, Surface, Tabs, Choice Chip, Selection, Bottom Sheet, List Row, 금융 Summary/Allocation/Update 상태 |
| `patterns/` | Mobile Portfolio 화면 패턴과 별도 Workstream 패턴 |
| `Icon/` | 기존 SVG icon. 원본 파일 수정 금지 |
| `checklists/` | 디자인·구현 QA |

## 핵심 원칙

- Light와 Dark는 같은 semantic token 이름에 theme별 값을 연결한다.
- Mobile Portfolio는 Dark Theme를 우선 설계하되 Light token을 삭제하지 않는다.
- Primitive를 화면에서 직접 사용하지 않고 semantic/component token을 사용한다.
- 카드보다 spacing과 낮은 divider로 그룹을 만든다.
- 금융 손익은 success/error가 아니라 gain/loss/flat token으로 표현한다.
- 색상만으로 손익이나 상태를 전달하지 않는다.
- `투자 현황 → 투자 비중 → 보유 종목 → 보유 종목 업데이트`의 Current hierarchy를 보존한다.
- Event Triage 전용 제한을 Mobile Portfolio 전역 규칙으로 사용하지 않는다.
- 실제 구현 전 `patterns/mobile-portfolio.md`, Current PRD와 Current DESIGN을 함께 확인한다.
