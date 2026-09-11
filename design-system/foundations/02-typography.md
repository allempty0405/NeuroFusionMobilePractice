# Typography

## Font Family

Web과 Mobile 모두 Pretendard Variable을 사용합니다. Mobile Portfolio의 기본 font family로 확정합니다.

```css
font-family: "Pretendard Variable", Pretendard, ui-sans-serif, system-ui, sans-serif;
```

## Font Decision

```text
MOBILE FONT FAMILY: PRETENDARD — LOCKED
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


## Font Asset Verification

사용자가 전달한 Pretendard OTF 9종을 확인했습니다.

- Thin
- ExtraLight
- Light
- Regular
- Medium
- SemiBold
- Bold
- ExtraBold
- Black

현재 semantic role에서 필요한 weight는 Regular 400, Medium 500, SemiBold 600, Bold 700입니다. 나머지 weight는 장식적 위계 확장을 위해 자동 사용하지 않습니다.

Font binary는 Wireframe 산출물에서 직접 사용하고, 실제 구현 repository에 asset을 연결할 때 경로·라이선스·bundle size를 함께 검토합니다.
