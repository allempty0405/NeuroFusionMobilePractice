# Mobile Portfolio Pattern

## Global IA

투자분석
- 모아보기 — Default, aggregate monitoring
- 포트폴리오 — breakdown/management
- 관심종목 — attention/tracking

Portfolio와 Watchlist는 같은 객체가 아닙니다.

## Core Screens

| ID | 역할 |
|---|---|
| F-01 | 모아보기 Dashboard |
| F-02 | Portfolio Scope Bottom Sheet |
| F-03 | 모든 포트폴리오 비교 |
| F-04 | 개별 포트폴리오 |
| F-05 | Aggregate Holdings |
| F-06 | Aggregate Holding Detail |
| F-06A | Portfolio별 Holding Snapshot 수정 |

## Visual Principles

- Dark Theme 우선
- 총 평가금액 또는 현재가를 단일 Hero anchor로 사용
- Card보다 spacing과 divider 우선
- Financial value alignment 통일
- Green accent 과다 사용 금지
- 손익은 부호와 색상을 함께 사용
- 화면별 Primary CTA는 최대 하나

## Locked Interaction

- F-02 0개 선택: Apply disabled + inline guidance
- Scope 변경은 F-04 navigation이 아님
- F-03 금액 축약 금지
- F-05 기본 sort는 가나다
- F-06 Portfolio breakdown은 Check icon 기반 inline disclosure
- F-06 수정은 각 Portfolio row의 Text Button
- Back은 실제 navigation history를 유지

## Excluded from Core

- 거래 History
- 매수/매도 입력
- Screenshot Import first batch
- 현금성 자산
- 오늘 확인
- 원금 대비 label
- 정상 화면의 15분 전/LIVE badge
