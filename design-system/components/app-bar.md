# App Bar

> Material Design 3 Top App Bar의 “현재 화면의 title / navigation / action” 원칙을 Valley Mobile과 Bottom Sheet Header에 맞게 적용합니다.
>
> Reference:
> - https://m3.material.io/components/app-bars/guidelines
> - https://github.com/material-components/material-components-web/tree/master/packages/mdc-top-app-bar

## Role

App Bar는 현재 context의:

- Navigation
- Title
- Immediate action

을 한 줄에서 설명합니다.

Portfolio Prototype에서는 두 범주를 구분합니다.

1. Page Detail Header
2. Bottom Sheet Header

두 유형이 모든 시각 값을 완전히 공유할 필요는 없지만, icon target / title hierarchy / trailing action grammar는 동일 원칙을 사용합니다.

## Bottom Sheet Header

PHASE 6E R17 기준:

- Height: 56px
- Leading action target: 48 × 48px
- Trailing action target: 48 × 48px
- Title: 20px / 28px, semibold
- Horizontal structure: leading / title / trailing
- Bottom divider: subtle border

Structure:

```text
No back:
Title                                         Close

With back:
Back  Title                                   Close
```

## Header Content Rule

Header에는 한 가지 현재 title만 둡니다.

Bad:

```text
종목 추가
인식 결과 검토
```

Good:

```text
인식 결과 검토
```

Step 설명, supporting description, help copy는 Header 아래 content 영역으로 이동합니다.

## Title

- One line
- Long title: ellipsis
- Current task / screen을 직접 설명
- Internal term 또는 redundant parent label 금지

## Leading Action

사용:

- Back
- Close가 leading navigation으로 필요한 contextual state

Touch target과 visual icon 크기를 분리합니다.

권장:

- target: 48 × 48px
- visual icon: 약 20~24px

## Trailing Action

사용:

- Close
- 현재 화면에서 즉시 이해되는 icon action

Header action을 늘려 toolbar처럼 사용하지 않습니다.

## Bottom Sheet Integration

Bottom Sheet anatomy:

```text
Drag Handle
↓
App Bar
↓
Scrollable Content
↓
Optional Sticky Action
```

Drag handle은 App Bar 내부가 아니라 Sheet anatomy의 독립 영역입니다.

## Accessibility

- Back / Close는 accessible name 필수
- Icon-only action은 visible icon 의미와 accessible name이 일치
- Title은 dialog의 `aria-labelledby` target으로 사용 가능
- focus-visible 상태 제공

## Valley Adaptation

M3 visual pixel-copy가 목적이 아닙니다.

유지:

- Valley dark surface
- Valley typography token
- Valley icon assets
- current spacing / semantic colors

차용:

- clear title hierarchy
- leading/trailing action structure
- compact app-bar behavior
- consistent touch targets
