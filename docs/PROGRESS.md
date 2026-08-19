# 학습 진행 트래커 — Spring Boot + Next.js 인증/인가

강의: jhs512 (slog.gg) · 커밋 단위 학습
- 백엔드: https://github.com/jhs512/p-14181-1 (134단계)
- 풀스택: https://github.com/jhs512/p-14183-1 (79단계)
- 내 원격: https://github.com/jomin4/prgrms-spring_nextjs_auth

방식: 코드 제공 → 상세 설명 → **직접 타이핑** → 반복 (챕터 완료 시 Claude가 자동 커밋·푸시)

## ▶️ 다음 세션 시작점
**M1 하위 1-1: `RsData` 타이핑부터 시작.**
- 설정(build.gradle 의존성, DB yaml)은 세팅 완료 → 초록불(테스트 통과) 확인됨.
- 만들 파일: `back/src/main/java/com/back/global/rsData/RsData.java`
- 이후 순서: RsData → GlobalExceptionHandler → ResponseAspect → BaseEntity → Post 도메인 → PostComment → Home/InitData/설정 → 테스트
- 참고 커밋(정답): p-14181 커밋 `002` (sha 05f44f5). M1 전체 완료 시 `feat: 002`로 커밋.

## Phase 1 — 백엔드 (p-14181)

| 단계 | 커밋 | 내용 | 상태 |
|------|------|------|------|
| M0 | 001 | Spring Boot 스캐폴드 | ✅ 완료 (push됨) |
| M1 | 002 | 표준 응답 체계 + 도메인 CRUD 베이스 | ⏳ 진행중 |
| M3 | 004~ | 회원 도메인 (Member) | ⬜ |
| M4 | ~ | 인증 핵심 (Spring Security, JWT, 필터, 로그인) | ⬜ |
| M5 | ~ | 인가 (관리자 API, 권한 기반 접근제어) | ⬜ |
| M6 | ~ | 테스트 & API 문서 | ⬜ |

### M1 하위 단계 (커밋 002 분해)
| 하위 | 파일 | 개념 | 상태 |
|---|---|---|---|
| 설정 | build.gradle.kts / application*.yaml | JPA·H2·validation·springdoc 의존성, DB 프로필 | ✅ (Claude 세팅) |
| 1-1 | `global/rsData/RsData.java` | 표준 응답 래퍼 | ⬜ ⬅️ 다음 |
| 1-2 | `global/globalExceptionHandler/GlobalExceptionHandler.java` | 전역 예외 → 표준 응답 | ⬜ |
| 1-3 | `global/aspect/ResponseAspect.java` | AOP로 HTTP 상태코드 자동 반영 | ⬜ |
| 1-4 | `global/jpa/entity/BaseEntity.java` | JPA 공통 필드 + Auditing (+ @EnableJpaAuditing) | ⬜ |
| 1-5 | `domain/post/post/**` | Post entity→repository→service→dto→controller | ⬜ |
| 1-6 | `domain/post/postComment/**` | PostComment CRUD | ⬜ |
| 1-7 | Home/BaseInitData/WebMvcConfig/SpringDocConfig + 테스트 | 마무리·검증 | ⬜ |

## Phase 2 — 풀스택 / Next.js (p-14183)

_Phase 1 완료 후 시작 (M7 프론트 환경 → M8 인증 연동 → M9 게시글/댓글 UI → M10 통합)_

---
범례: ⬜ 예정 · ⏳ 진행중 · ✅ 완료
