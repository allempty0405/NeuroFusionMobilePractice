# Buttons & CTA

## 유형

| 유형 | 용도 | 예 |
|---|---|---|
| Primary | 화면의 한 가지 핵심 완료 | 적용하기, 종목 추가, 저장 |
| Secondary | 핵심 행동을 보조 | 다시 시도, 필터 초기화 |
| Text | 대상 가까이 있는 경량 행동 | 수정, 전체 |
| Icon | 공간이 제한된 탐색/도구 | Back, Close, More |
| Sticky | 긴 화면에서 지속해야 할 Primary | 종목 추가 |
| Disabled | 선행 조건 미충족 | 0개 선택 상태의 적용하기 |

## 공통

- 터치 영역 최소 44×44px
- Primary CTA는 한 화면에 하나
- Button label은 행동 결과를 설명
- Loading 중 중복 실행 방지
- Sticky CTA 아래 safe area 확보
- Text Button은 icon 없이도 의미가 분명할 때 text만 사용

## Disabled

Disabled는 모든 UI에서 같은 component token을 사용합니다.

- `--nf-control-disabled-bg`
- `--nf-control-disabled-text`
- `--nf-control-disabled-icon`

Disabled는 의도적으로 낮은 대비를 허용합니다. 다만 활성 control과 상태가 구분되어야 하며, 조건을 이해하기 어려우면 인접 안내 문구를 제공합니다.

F-02:

- 0개 선택 시 `적용하기` disabled
- 버튼 위: `포트폴리오를 1개 이상 선택해 주세요.`
- 1개 이상 선택 시 즉시 활성화

## F-06 Text Action

Aggregate metric에는 전역 수정 action을 두지 않습니다. `포트폴리오별로 보기`를 펼친 뒤 각 Portfolio row의 `수정` Text Button으로 해당 Holding Snapshot 수정에 진입합니다.
