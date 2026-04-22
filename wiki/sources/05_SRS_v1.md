---
tags: [source, srs, technical-requirements, architecture]
date: 2026-04-21
sources: [raw/assets/05_SRS_v1.md]
---

# SRS v1 (소프트웨어 요구사항 명세서) 요약

**원본:** `raw/assets/05_SRS_v1.md`

## 핵심 요약

Super-Calc MVP의 기술 아키텍처, 기능/비기능 요구사항, 데이터 모델, API 명세를 정의한 소프트웨어 요구사항 명세서. Next.js 기반 풀스택 모놀리스 아키텍처 채택.

## 기술 스택

| 영역 | 기술 |
|---|---|
| **프레임워크** | Next.js 15+ (App Router) |
| **ORM** | Prisma |
| **데이터베이스** | Supabase (PostgreSQL) |
| **배포** | Vercel |
| **스타일링** | Tailwind CSS + shadcn/ui |
| **인증** | NextAuth.js / Supabase Auth |

## 핵심 기능 요구사항

1. **Super-Calc Engine (FR-CALC):** 채널 통합 1일 단가 정규화 엔진
2. **Anti-BS Dashboard (FR-ANTI):** 식약처 기반 팩트체크 배지 시스템
3. **제품 검색/필터 (FR-SEARCH):** 증상·성분 기반 검색
4. **제휴 커머스 연동 (FR-AFFILIATE):** 쿠팡 파트너스 딥링크
5. **데이터 신뢰 시스템 (FR-TRUST):** 오류 신고·48h 처리 SLA

## 비기능 요구사항

| 영역 | 목표 |
|---|---|
| 성능 | 페이지 로드 < 3초, API 응답 < 500ms |
| 가용성 | 월 99.5% 이상 |
| 보안 | 최소 수집 원칙, B2B 데이터 k-anonymity ≥ 5 |
| 비용 | MVP 인프라 월 $50 이하, 초과 시 Slack 알림 |

## 핵심 설계 결정
- 단일 채널(쿠팡 파트너스) MVP 집중 → 다채널 확장은 Phase 2
- 모바일 웹 우선, 네이티브 앱/AI 추천/커뮤니티 배제
- 데이터 갱신 및 제보 처리 48시간 SLA

## 교차 참조
- [PRD 요약](./00_PRD_v1.md)
- [Super-Calc Engine](../entities/Super-Calc-Engine.md)
- [Anti-BS Dashboard](../entities/Anti-BS-Dashboard.md)
- [MVP 기술 아키텍처](../concepts/MVP-Tech-Architecture.md)
