# Typography

## Font Family

Web CSS에서 확인된 Pretendard Variable을 우선 reference로 사용합니다. Mobile 앱의 실제 font family는 별도 코드 확인 전까지 provisional입니다.

```css
font-family: "Pretendard Variable", Pretendard, ui-sans-serif, system-ui, sans-serif;
```

## Base Scale

| Token | 크기/행간 |
|---|---:|
| `text-xs` | 12/16px |
| `text-sm` | 14/20px |
| `text-base` | 16/24px |
| `text-lg` | 18/28px |
| `text-xl` | 20/28px |
| `text-2xl` | 24/32px |
| `text-financial-hero` | 28/36px |

10px는 비핵심 annotation 외에는 사용하지 않습니다.

## Semantic Roles

| 역할 | Style | 사용 |
|---|---|---|
| Screen Title | 24/32, 700 | Root 화면 제목 |
| Detail Title | 20/28, 600 | Portfolio/종목 상세 |
| Section Title | 18/28, 600 | 독립 section |
| Row Title | 16/24, 500 | 종목명, Portfolio명 |
| Body | 14/20, 400 | 설명 |
| Metadata | 12/16, 400 | ticker, 종목 수 |
| Metric Value | 16/24, 500 | 평가금액, 손익 |
| Financial Hero | 28/36, 600 | 총 평가금액, 현재가 |
| Button Label | 16/24, 600 | Primary CTA |

## Financial Number

- Tabular figures 적용
- 통화 기호와 부호 유지
- 핵심 금액 ellipsis 금지
- Mobile Portfolio 금액 축약 금지
- Secondary currency는 Primary보다 크기·명도를 낮춤
- 작은 metadata를 일괄 bold 처리하지 않음
