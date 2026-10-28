# Bottom Sheet

> PHASE 6E R17에서 Material Design 3 Bottom Sheet의 anatomy / interaction 원칙을 Valley Mobile dark UI에 맞게 적용한 범용 component입니다.
>
> Reference:
> - https://m3.material.io/components/bottom-sheets/guidelines
> - https://github.com/material-components/material-components-android/blob/master/docs/components/BottomSheet.md

## 역할

Valley Mobile에서는 현재 **Modal Bottom Sheet**를 사용합니다.

Modal Sheet는 현재 화면 위에 secondary task / selection을 일시적으로 제공하고, 완료 또는 닫기 후 원래 context로 돌아갑니다.

대표 사용:

- Portfolio Scope 선택
- Portfolio 선택
- 종목 정렬
- 종목 추가 multi-step flow

## Anatomy

1. Scrim
2. Sheet container
3. Drag handle
4. Sheet App Bar
5. Scrollable content
6. Optional sticky action area
7. Bottom safe area

Sheet Header 규칙은 `app-bar.md`를 따릅니다.

## Container

### Visual

- Surface: Valley `surface-raised` / current dark surface token
- Top corners: 28px
- Sheet 자체에 불필요한 nested card를 추가하지 않음
- Scrim으로 main content와 modal context를 분리

### Height

Material 3의 “drag / preset state” 원칙을 사용하되, 아래 값은 **Valley implementation rule**입니다.

| Context | Initial height |
|---|---:|
| Scope / Picker / Sort | 72% viewport |
| Add Holding multi-step flow | 90% viewport |

Allowed interactive range:

- Minimum: 40% viewport
- Maximum: 94% viewport

Preset snap points:

- 50%
- 72%
- 90%

Preset 값은 Product requirement가 아니라 현재 Mobile component behavior입니다.

## Drag Handle

### Visual

- Visible bar: 32 × 4px
- Neutral gray
- Pill radius

### Interaction area

- 64 × 48px
- Visual bar 크기와 touch target을 분리

### Behavior

Drag:

- 위로 drag → 높이 증가
- 아래로 drag → 높이 감소
- release → 가장 가까운 preset으로 snap

Tap / keyboard:

- Tap / Enter / Space → preset 순환
- Arrow Up → 한 단계 확장
- Arrow Down → 한 단계 축소
- Home → 최소 preset
- End → 최대 preset

Accessibility:

- Handle은 focusable control
- `role="slider"`
- `aria-valuemin`
- `aria-valuemax`
- `aria-valuenow`
- `aria-valuetext`

Drag만 유일한 조작 방법으로 사용하지 않습니다.

## Sheet App Bar

Sheet 내부 Header는 compact app-bar grammar를 사용합니다.

구조:

```text
[optional Back]  Title                           [Close]
```

금지:

- Header 안에 step eyebrow 반복
- Title 위에 `종목 추가` 같은 중복 context label
- Close / Back touch target 축소

Supporting description이 필요하면 Header가 아니라 scrollable content 시작부에 둡니다.

## Scrolling

- Content가 현재 height를 넘으면 Sheet 내부만 vertical scroll
- Header / drag handle은 content scroll과 분리
- Sticky CTA는 content를 가리지 않음
- Background page는 modal 상태에서 `inert` 또는 동등하게 interaction 차단

## Dismiss

지원:

- Close icon
- Escape
- Scrim click
- Product flow의 완료 action

닫힌 뒤에는 trigger로 focus를 복원합니다.

## Selection Draft

Selection Sheet는 적용 전 draft state를 사용할 수 있습니다.

예: Portfolio Scope

- Apply 전 변경은 draft
- Close / Escape 시 미적용 draft discard
- 0개 선택은 허용 가능
- 단, 현재 Scope contract에서는 0개일 때 `적용하기` disabled

## F-02 Portfolio Scope

- Title: `포트폴리오 선택`
- Multi-select
- `모든 포트폴리오`는 전체 선택 / 전체 해제 toggle
- 선택 count는 trigger에서 확인
- Scope 변경 후에도 `모아보기` 유지

## Add Holding Sheet

Initial height:

- 90%

Flow:

```text
종목 추가
→ 등록 방식
→ 다음 step
→ 검토 / 입력
→ 저장
```

등록 방식 선택 후 입력 UI를 같은 화면 아래에 append하지 않습니다.

## Do / Don't

### Do

- Secondary task를 current context 위에서 처리
- Drag handle과 keyboard alternative를 함께 제공
- 내부 scroll 사용
- 44~48px touch target 유지
- Header / content / action 영역을 분리

### Don't

- 모든 화면을 Sheet로 전환
- drag만으로 높이 제어
- Header 안에 subtitle / eyebrow를 계속 누적
- background page와 Sheet를 동시에 interactive하게 유지
