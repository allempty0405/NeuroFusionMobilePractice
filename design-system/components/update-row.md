# Portfolio Update Row

**STATUS:** VALIDATED_IN_PORTFOLIO_PROTOTYPE  
**SOURCE / EVIDENCE:** PHASE 6 Mobile Portfolio — F-01, F-05, F-07

## Purpose

현재 Portfolio context에 관련된 정보 업데이트를 compact row로 표시합니다.

## Supported Information Families

- 뉴스
- 공시
- 일정
- 주요 이벤트
- 분석

## Anatomy

1. Type text/badge
2. Asset identity
3. Title — list에서 최대 2줄
4. Source
5. Timestamp 또는 event datetime

## Variants

### Preview
- 최대 3 items in current Mobile Portfolio Concept
- Full Updates entry 제공

### Full List
- 같은 semantic object 사용
- type filter와 함께 사용 가능

### Schedule
과거 content timestamp와 다르게 future event임을 명시합니다.

```text
[일정] 삼성전자
3분기 실적발표
예정 · 10월 23일 09:00
```

## Ordering Boundary

이 component는 importance/relevance ranking을 정의하지 않습니다.

금지:
- 중요
- 추천
- AI 선정
- importance score

Current Concept ordering은 Product spec의 시간 기반 규칙을 따릅니다.

## Content Rules

- Source가 있을 때 source를 표시
- source를 추론하거나 발명하지 않음
- preview에서 title 최대 2줄
- title/source/time의 hierarchy를 분리

## Accessibility

Interactive row라면 accessible name에 type, asset, title을 포함합니다.
시간 정보는 `예정` 등 temporal meaning을 text로 제공합니다.

## Responsive

- 320–430px
- title 최대 2줄
- future datetime은 잘라서 의미를 잃지 않음
- metadata가 좁을 경우 source만 truncation하고 detail에서 회복 가능해야 함
