# 학습 진행 트래커 — Spring Boot + Next.js 인증/인가

강의: jhs512 (slog.gg) · 커밋 단위 학습
- 백엔드: https://github.com/jhs512/p-14181-1 (134단계)
- 풀스택: https://github.com/jhs512/p-14183-1 (79단계)
- 내 원격: https://github.com/jomin4/prgrms-spring_nextjs_auth

방식: 코드 제공 → 상세 설명 → **직접 타이핑** → 반복 (챕터 완료 시 Claude가 자동 커밋·푸시)

## Phase 1 — 백엔드 (p-14181)

| 단계 | 커밋 | 내용 | 상태 |
|------|------|------|------|
| M0 | 001 | Spring Boot 스캐폴드 (build.gradle.kts, BackApplication, application.yaml) | ✅ 완료 |
| M1 | 002 | 표준 응답 체계 + 도메인 CRUD 베이스 (RsData, 예외처리, ResponseAspect, JPA/H2, Post·PostComment CRUD, springdoc) | ⏳ 진행중 |
| M3 | 004~ | 회원 도메인 (Member 엔티티/서비스/리포지토리) | ⬜ |
| M4 | ~ | 인증 핵심 (Spring Security, JWT, 필터, 로그인) | ⬜ |
| M5 | ~ | 인가 (관리자 API, 권한 기반 접근제어) | ⬜ |
| M6 | ~ | 테스트 & API 문서 | ⬜ |

> 커밋 002는 원 강의에서 베이스 프로젝트가 한 번에 들어오므로, 학습을 위해 논리적 하위 단계로 쪼개서 진행한다.

## Phase 2 — 풀스택 / Next.js (p-14183)

_Phase 1 완료 후 시작 (M7 프론트 환경 → M8 인증 연동 → M9 게시글/댓글 UI → M10 통합)_

---
범례: ⬜ 예정 · ⏳ 진행중 · ✅ 완료
