# List Rows

## 공통

- Full-width row
- Card와 shadow 사용하지 않음
- Identity는 왼쪽, financial value는 오른쪽
- 숫자는 우측 정렬과 tabular figures
- 보조 metadata는 낮은 weight/contrast
- 필요한 경우 inset divider
- 긴 이름은 지정된 영역에서만 ellipsis

## Variants

### Portfolio Comparison Row

Portfolio 이름과 보유 종목 수, 평가금액, 총 수익, 일일 수익을 비교합니다. 금액 축약은 허용하지 않습니다.

### Holding Row

종목명, 보유 수량, 평가금액, 총 수익만 표시합니다. 현재가, 평균단가, 섹터, 국가, chart를 추가하지 않습니다.

### Portfolio Breakdown Row

F-06 expanded 상태에서 Portfolio 이름, 보유 수량, 평균단가와 `수정` Text Button을 표시합니다. Row 전체를 navigation으로 만들지 않습니다.

### Search Result Row

Asset identity, 보조명, 현재 값과 선택 control을 표시할 수 있습니다. Search/Filter 영역과 결과 목록의 divider를 구분합니다.

## Responsive

- 360~430px 확인
- 핵심 금액 줄바꿈·ellipsis 금지
- 긴 종목명/Portfolio명에만 ellipsis 허용
- F-03 긴 금액은 3열 구조와 평가금액 1행+손익 2열 구조를 시각 비교
