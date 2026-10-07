# List Rows

**STATUS:** VALIDATED_IN_PORTFOLIO_PROTOTYPE  
**SOURCE:** PHASE 6 Mobile Portfolio Hi-fi Prototype rendered at 320 / 360 / 390 / 430px

## 공통

- Full-width row
- Card와 shadow 사용하지 않음
- Identity는 왼쪽, financial value는 오른쪽
- 숫자는 우측 정렬과 tabular figures
- 보조 metadata는 낮은 weight/contrast
- 필요한 경우 inset divider
- 긴 이름은 지정된 영역에서만 wrap 또는 ellipsis
- 핵심 금융 금액은 ellipsis / 축약하지 않음
- 기본 Row 이해에 horizontal scroll을 요구하지 않음

## Variants

### Portfolio Comparison Row

Mobile의 `모든 포트폴리오` 비교에 사용합니다.

Primary:
- 포트폴리오 이름
- 평가금액
- 총 손익 / 총 수익률

Secondary:
- 보유 종목 수
- 일일 수익

Desktop comparison table을 축소하지 않습니다. Portfolio 이름과 평가금액을 첫 행에서 식별하고, secondary 상태는 다음 행으로 분리할 수 있습니다.

### Holding Row — Full

F-03 / F-09의 기본 구조:

```text
종목명                              평가금액
보유 수량 · 보유비중              총 손익 / 총 수익률
```

기본 Row에 넣지 않음:
- 현재가
- 평균단가
- 섹터
- 국가
- 일일 등락
- chart / sparkline

### Holding Row — Dashboard Preview

F-01 / F-08의 compact variant:

```text
종목명                              평가금액
보유 수량                          총 손익 / 총 수익률
```

`보유비중`은 Full Holdings의 secondary field이며 Dashboard Preview에서는 생략할 수 있습니다.

### Portfolio Breakdown Row

Aggregate Holding Detail의 inline disclosure 안에서 사용합니다.

- Portfolio 이름
- 보유 수량
- 평균단가
- `수정` Text Button

Row 전체를 Portfolio navigation으로 만들지 않습니다.

### Search Result Row

Asset identity, 보조명, 현재 값과 선택 control을 표시할 수 있습니다. Search/Filter 영역과 결과 목록의 divider를 구분합니다.

## Responsive

- 320 / 360 / 390 / 430px 검수
- 320px에서는 긴 종목명 최대 2줄 허용 가능
- 핵심 금액 줄바꿈·ellipsis·축약 금지
- 오른쪽 financial block은 가능한 no-wrap 유지
- 손익 금액 + 수익률이 320px에서 충돌하면 같은 오른쪽 block 내부에서 수익률을 다음 줄로 stack
- Horizontal scroll 금지

## Accessibility

- Interactive row의 hit area는 최소 44px 높이
- 손익은 색 + `+ / −` 부호를 함께 사용
- Accessible name에서 identity와 핵심 financial state를 연결
