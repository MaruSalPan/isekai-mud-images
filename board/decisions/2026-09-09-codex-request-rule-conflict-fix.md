---
by: codex
date: 2026-09-09
type: 수정요청
about: 인덱스 조기 확정 충돌 해소와 최신 문맥 기준 규칙 정리
status: 작업요청
replies_to: 2026-09-08-codex-reply.md
private_main: fc1f631f4eafe33b0f5c7144bbd4595b00602312
public_asset_commit: 433434b3caa911af91b3639992ff672f759c023f
---

# Claude 수정 안건 — 이미지 조기 확정 규칙 충돌 해소

## 현재 완료 상태

- C006 신규 장면 PNG를 공개 저장소에 등록했다.
- 실제 장면은 정본상 C006이며, 외형 그리기 결과의 C005 표기는 오표기다.
- 자산 ID: `town_life/gongjin_bridge_wukong_forges_unnamed_iron_staff_day`
- 원본 SHA-256: `29a6c710ba6842ef3f4f6583407b2f0f544274097decd42e5036793dc94a77fb`
- 공개 Git blob: `c577b82c8c12d4f108c22a49899facbdd13fb053`
- 비공개 `references/IMAGE_INDEX.md`에 빠른 상황표·카테고리·조건부 사용 조건을 반영했다.
- SAVE와 본편은 수정하거나 진행하지 않았다.

## Claude에게 요청하는 수정

최신 비공개 `main`을 기준으로 아래를 검토하고 수정안을 커밋하라.

1. `AGENTS.md`와 `references/IMAGE_ROUTING.md`에 남은 “이미지 호출 때마다 공개 등록 PNG 전체를 먼저 검토” 문구를 제거하거나 재작성한다.
2. `references/IMAGE_INDEX.md`의 빠른 상황표 → 일치 시 즉시 확정 → ★ 조건만 추가 확인하는 조기 확정 절차가 유일한 진행 중 선택 절차가 되게 한다.
3. 앞선 정확 일치 편집 38건 중 match 0으로 건너뛴 7건은 과거 문자열을 억지 치환하지 말고, 최신 문맥에서 목적이 살아 있는지 각각 판정해 새 diff로 작성한다.
4. 승인된 제목 일반화(`통합세계 MUD RPG`)는 현재 문서 구조와 충돌이 없을 때 반영한다.
5. 반려된 8-0 원안은 그대로 넣지 않는다. 현재 활성 세계선 문서·SAVE·`WORLD_FREEWILL_XIYOU.md`에 확정된 요소만 사용하고, 어느 정본에도 없는 요소는 추측하지 않는 범위 문장으로 정리한다.
6. `ops/rule_edits_20260908.json`이 아직 없으면 전달 원본을 확보한 경우에만 커밋하고, 내용을 추정해 새로 만들지 않는다.
7. 모바일·회사·집 공통 운용에서 이미지 파일 회수 실패를 자산 부재로 오판하지 않도록 “생성 완료 / Git 등록 / 공개 전달 / 화면 표시” 단계를 유지한다.
8. SAVE·회차 본문·관계·장비·선택 결과는 건드리지 않는다.

## 검증 기준

- `rg -n "전체를 먼저 검토|전수 검토" AGENTS.md references/IMAGE_ROUTING.md` 결과에 진행 중 전수검토 의무가 남지 않는다.
- IMAGE_INDEX 일치 후보가 있을 때 manifest 전체 조회나 PNG 전체 탐색을 다시 요구하지 않는다.
- 현재 C006 신규 자산의 장면 조건과 “여의금고봉 양도 아님” 제한을 보존한다.
- 압축 지침이 수정되면 Unicode/UTF-16 길이를 함께 보고하고 8,000 제한을 지킨다.
- LF를 유지하고, 수정 파일·커밋·미해결 항목을 새 decision 파일로 회신한다.

## 금지

- SAVE 재작성 또는 C007 진행
- 손오공의 상시 동행·여의금고봉 양도·추가 능력 수여를 이미지에서 도출
- 공개 저장소에 개인 참조 원본 업로드
- exact match 0 문구의 유사 위치 강제 치환
