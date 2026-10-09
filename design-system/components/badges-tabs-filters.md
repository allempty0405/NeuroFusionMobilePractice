# Tabs, Filters & Choice Chips

## Global Section Navigation

동등한 상위 영역 이동에 사용합니다.

- 모아보기
- 포트폴리오
- 관심종목

Portfolio와 Watchlist의 데이터 의미는 섞지 않습니다. 선택 상태는 text contrast와 Green underline을 함께 사용합니다.

## Dimension Tabs

같은 데이터의 집계 기준을 바꿉니다.

- 자산
- 종목
- 국가
- 섹터

## Filter Tabs

목록의 대상을 좁힙니다.

- 전체, 주식, ETF, 인덱스, 원자재, 외환, 채권, 암호화폐

Navigation과 Filter를 같은 interaction으로 취급하지 않습니다.

## Choice Chip

짧은 단일 선택에 사용합니다. Currency Variant A가 이 pattern을 사용합니다.

- Selected: Primary fill + strong inverse text
- Unselected: Muted surface + body text
- Disabled: 공통 disabled token
- 44px touch target
- 긴 label이나 4개 이상 통화에서는 overflow 검증

Currency는 Asset Filter가 아닙니다. 선택된 Scope 전체 금액의 reporting currency를 변경합니다.

### Dark Mode Variant — Mobile Portfolio Allocation

**STATUS:** VALIDATED_IN_PHASE_6E_R5_PROTOTYPE

Mobile Portfolio의 `투자 비중` Lens처럼 짧은 4-way single-select에 Choice Chip을 사용할 수 있습니다.

- Touch target: 최소 `44px`
- Visual pill height: `32px`
- Radius: `--nf-radius-pill`
- Selected: `--nf-green-500` fill + `--nf-white` text
- Unselected: `--nf-zinc-600` fill + `--nf-zinc-300` text
- Selected state는 `aria-selected=true`와 시각 상태를 함께 사용
- Disabled는 기존 공통 disabled token을 사용
- 320px에서도 4개 short label이 겹치지 않는지 검수
- 긴 label / 많은 option에서는 Choice Chip을 강제하지 않음

현재 검증 사용 예:

```text
투자 비중
[자산별] [종목별] [국가별] [섹터별]
```

이 Dark Mode variant는 **Mobile Portfolio에서 검증된 Choice Chip 표현**이며 모든 Valley selected control을 green fill로 통일하는 전역 규칙이 아닙니다.

## Badge

상태나 짧은 분류에만 사용합니다. 숫자, CTA, 모든 metadata를 badge로 만들지 않습니다.
