# Bottom Sheet

## 구조

1. Scrim
2. Sheet surface
3. Drag handle
4. Title
5. Optional search/filter
6. Scrollable content
7. Optional sticky CTA
8. Bottom safe area

## Visual

- Dark/Light theme의 `surface-raised` 사용
- Top corner: `radius-sheet`
- Scrim: `--nf-scrim`
- 내부 horizontal padding: 16~20px
- 강한 shadow보다 surface와 scrim으로 elevation 표현

## Behavior

- 콘텐츠 기준 높이, 최대 약 72% viewport
- 긴 목록은 Sheet 내부에서만 scroll
- 닫으면 미적용 draft discard
- Sticky CTA가 목록을 가리지 않도록 bottom padding 확보

## F-02 Portfolio Scope

- 사용자-facing title: `포트폴리오 선택`
- 보조 설명 없음
- Multi-select
- 최소 1개 필수
- 0개면 `적용하기` disabled + inline guidance
- 1개만 선택해도 F-01에 머무름
- Scope 변경을 Portfolio navigation으로 처리하지 않음
