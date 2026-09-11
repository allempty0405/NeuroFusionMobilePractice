# Token Map

## 계층

| 계층 | 예 | 원칙 |
|---|---|---|
| Primitive | `--nf-zinc-900` | 화면에서 직접 사용하지 않음 |
| Semantic | `--nf-surface-page` | Light/Dark에서 동일한 역할명 |
| Component | `--nf-control-disabled-bg` | 특정 state에 사용 |

## Theme

- `:root, [data-theme="light"]`: Valley Web Light reference
- `[data-theme="dark"]`: Valley Mobile Dark screenshot reference
- OS theme 연동 시 `prefers-color-scheme`을 사용할 수 있으나 앱의 theme state가 있으면 명시적 `data-theme`이 우선합니다.

## 핵심 Semantic

| 목적 | Token |
|---|---|
| Page | `--nf-surface-page` |
| Raised surface | `--nf-surface-raised` |
| Muted surface | `--nf-surface-muted` |
| Input | `--nf-surface-input` |
| Strong text | `--nf-text-strong` |
| Body | `--nf-text-body` |
| Muted | `--nf-text-muted` |
| Divider | `--nf-border-subtle` |
| Gain/Loss/Flat | `--nf-financial-*` |
| Disabled | `--nf-control-disabled-*` |
| Scrim | `--nf-scrim` |

## 사용 우선순위

1. Component token
2. Semantic token
3. Primitive는 token 정의 내부에서만 사용
4. 새 token은 source와 사용 상황을 문서화
5. Event Triage 전용 token은 해당 pattern 안에 한정


## Compatibility Alias 정책

기존 Prototype 보호를 위해 이전 `surface-dashboard-*`, `surface-card*` alias를 유지합니다. 신규 Mobile Portfolio 구현은 `surface-page`, `surface-raised`, `surface-muted` semantic token을 우선 사용합니다.

다음 중 하나가 발생하면 교체·제거 검토 시점입니다.

- 신규 코드에서 legacy alias가 추가로 사용됨
- 기존 화면을 Mobile Portfolio theme 구조로 이관함
- repository 검색에서 legacy consumer가 0개가 됨
- alias가 Light/Dark 의미를 모호하게 만듦

Alias 제거는 자동으로 하지 않습니다. 사용처를 확인하고 breaking change 가능성을 사용자에게 알린 뒤 결정합니다.
