# Allocation Bar List

**STATUS:** VALIDATED_IN_PORTFOLIO_PROTOTYPE  
**SOURCE / EVIDENCE:** PHASE 6 Mobile Portfolio — F-01, F-07, F-10; rendered 320 / 360 / 390 / 430px

## Purpose

Portfolio composition을 작은 Mobile 면적에서 비교 가능한 형태로 표현합니다.

## Anatomy

1. Section title — `투자 비중`
2. Dimension Tabs
   - 자산별
   - 종목별
   - 국가별
   - 섹터별
3. Distribution rows
   - category label
   - percentage
   - horizontal proportional bar
4. Optional full-detail entry when category count exceeds preview limit

## Variants

### Dashboard Preview
- 한 번에 하나의 distribution
- 최대 5 category Concept preview
- >5이면 Detail entry

### Detail
- 동일 visual grammar로 full vertical list
- horizontal scroll 없음

## Interaction

Dimension Tabs는 navigation이 아니라 같은 데이터의 집계 기준 변경입니다.

Default:
`자산별`

## Content Rules

- percentage를 항상 text로 제공
- bar color만으로 크기나 category 의미를 전달하지 않음
- category ordering은 Product fixture/data rule을 따름
- 긴 이름은 wrap 가능

## Tokens

Component tokens:
- `--nf-allocation-bar-fill`
- `--nf-allocation-bar-track`

이 token은 기존 semantic theme token에 mapping하며 새 primitive color를 만들지 않습니다.

## Accessibility

- label + percentage가 bar 없이도 의미를 전달해야 함
- selected lens는 text + selected state로 식별
- distribution chart 자체는 decorative visual 보조이며 text data가 canonical

## Responsive Rules

- Distribution은 320–430px에서 horizontal scroll 금지
- Lens control만 필요 시 secondary horizontal control behavior를 검토할 수 있음
- 긴 label은 최대 2줄 허용 가능

## DO

- 비교 가능한 bar length + explicit percentage 사용
- Dashboard와 Detail에서 동일 grammar 사용

## DON'T

- 경쟁사 관행만으로 Donut을 기본값으로 사용
- 5개 category를 서로 다른 강한 semantic color로만 구분
- chart 때문에 `투자 비중`이 Financial Hero보다 더 강한 시각 anchor가 되게 함
