---
tags: [concept, architecture, technology]
date: 2026-04-21
sources: [raw/assets/05_SRS_v1.md, raw/assets/00_PRD_v1.md]
---

# MVP 기술 아키텍처

## 아키텍처 개요

Next.js 기반 **풀스택 모놀리스** 아키텍처. MSA 대신 단일 코드베이스로 MVP 빠른 검증에 집중.

## 기술 스택

| 영역 | 기술 | 선정 근거 |
|---|---|---|
| 프레임워크 | **Next.js 15+ (App Router)** | SSR/SSG 유연성, API Routes 내장 |
| ORM | **Prisma** | 타입 안전 DB 접근, 마이그레이션 관리 |
| 데이터베이스 | **Supabase (PostgreSQL)** | 무료 티어 충분, RLS 보안, Realtime 지원 |
| 배포 | **Vercel** | Next.js 네이티브, Edge Functions, 자동 스케일링 |
| 스타일링 | **Tailwind CSS + shadcn/ui** | 빠른 UI 구축, 일관된 디자인 시스템 |
| 인증 | **NextAuth.js / Supabase Auth** | 소셜 로그인, 이메일 인증 |

## 핵심 설계 결정

1. **단일 채널(쿠팡 파트너스) MVP 집중** → 다채널 확장은 Phase 2
2. **모바일 웹 우선** → 네이티브 앱, AI 추천, 커뮤니티 기능 배제
3. **인프라 비용 월 $50 이하** → 초과 시 Slack 알림
4. **데이터 갱신·제보 처리 48시간 SLA**

## 핵심 모듈

- [Super-Calc Engine](../entities/Super-Calc-Engine.md) — 가격 정규화·비교 엔진
- [Anti-BS Dashboard](../entities/Anti-BS-Dashboard.md) — 팩트체크 배지 시스템
- [Data Trust System](../entities/Data-Trust-System.md) — 오류 신고·처리 시스템

## 교차 참조
- [SRS 요약](../sources/05_SRS_v1.md)
- [PRD 요약](../sources/00_PRD_v1.md)
- [성분 정규화](./Data-Normalization.md)
