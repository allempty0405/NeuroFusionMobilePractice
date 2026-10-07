# Financial Summary Group

**STATUS:** VALIDATED_IN_PORTFOLIO_PROTOTYPE  
**SOURCE / EVIDENCE:** PHASE 6 Mobile Portfolio — F-01, F-07, F-08; rendered 320 / 360 / 390 / 430px

## Purpose

현재 Portfolio context의 핵심 금융 상태를 동일한 visual grammar로 표현합니다.

## Anatomy

1. Section title — `투자 현황`
2. Optional reporting currency control
3. Primary Hero — `총 평가금액`
4. Secondary metric — `일일 수익` + optional `일일 수익률`
5. Secondary metric — `총 손익` + optional `총 수익률`

## Variants

- Aggregate Summary — F-01
- All Portfolios Summary — F-07
- Individual Portfolio Summary — F-08
- Empty Holdings — Hero `₩0`, return values `—`
- Loading — final geometry skeleton
- Partial / Stale / Disconnected — State notice is adjacent but not part of numeric calculation

## Content Rules

- `총 평가금액` is the strongest financial anchor.
- `총 손익` = amount, `총 수익률` = percentage.
- Do not use `총 수익` ambiguously for both amount and percentage.
- Missing value is `—`, not 0.
- Core amount is not abbreviated or ellipsized.
- Reporting currency changes presentation basis, not Holdings membership.

## Tokens

Use:
- `--nf-text-title`
- `--nf-text-muted`
- `--nf-financial-gain`
- `--nf-financial-loss`
- `--nf-financial-flat`
- typography `text-financial-hero`
- tabular figures

## Accessibility

- Positive/negative uses sign + color.
- Metric accessible name includes label + value + semantic direction where applicable.
- Currency control minimum target 44×44px equivalent.

## Responsive Rules

- 360–430px: default Hero 28/36.
- 320px stress: Hero may step to 24/32 before any number abbreviation.
- Secondary metrics may stack vertically if needed.
- Horizontal scroll is prohibited.

## DO

- Keep one Hero anchor.
- Preserve full financial value.
- Keep state semantics near affected Summary.

## DON'T

- Add a decorative performance chart to this group.
- Use green for neutral positive-looking decoration.
- Show Partial/Disconnected aggregate as complete without a cue.

## Known Limitations

Production FX formula, aggregate formula and freshness SLA are outside this component contract.
