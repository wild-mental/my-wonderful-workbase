---
tags: [prd, 기획, 건기식, 플랫폼]
date: 2026-04-21
sources: raw/assets/00_PRD_v1.md
---

# 00_PRD_v1.md

**건기식 성분·가격 비교 초자동화 플랫폼 PRD v0.1**

## 요약 (Summary)
이 문서는 건강기능식품 구매 시 소비자들이 겪는 정보 과잉, 성분 비교의 어려움, 광고의 범람을 해결하기 위해 기획된 "건기식 성분/가격 비교 초자동화 플랫폼"의 제품 요구사항 정의서(PRD)입니다. 1일 단가를 기준으로 멀티 채널(iHerb, 쿠팡, 네이버)의 실지불가를 즉시 연산해주고, 식약처 공전을 기반으로 허위 과장 광고를 막는 팩트체크 대시보드를 제공하는 것을 골자로 합니다.

## 주요 시사점 (Key Takeaways)
1. **문제 정의**: 소비자는 대리인(Agent)을 원함. 연산 소요시간(60분)과 성분 해석 불가(47.2%), 뒷광고를 핵심 고통(Pain)으로 꼽음.
2. **해결책 (Must-Have)**: 
   - [Super-Calc Engine](../entities/Super-Calc-Engine.md): 연산 시간을 5초로 압축
   - [Anti-BS Dashboard](../entities/Anti-BS-Dashboard.md): 마케팅 노이즈 100% 제거
   - Viral Engine (1-Tap 공유): 카카오톡 내장 브라우저 웹뷰로 진입 장벽 최소화
   - Data Trust System: 데이터 무결성 48시간 SLA 보장
3. **목표 및 성과 지표(KPI)**: North Star KPI를 "TTC(Time-To-Completion, 탐색-결제 완료까지의 시간) 5분 이하"로 설정.
4. **MVP 제한 사항**: 네이티브 앱, 개인화 추천, 자율 리뷰 기능은 철저히 배제(광고 침투 및 데이터 편향 우려).

## 관련 엔티티 및 개념
* **엔티티 (Entities)**: 
  * [Super-Calc Engine](../entities/Super-Calc-Engine.md): 플랫폼의 핵심 가격 산출 엔진.
  * [Anti-BS Dashboard](../entities/Anti-BS-Dashboard.md): 성분 등급 및 팩트체크를 보여주는 대시보드.
  * [타겟 페르소나 (C1, C2, A2)](../entities/Target-Personas.md): 한정훈(직구족), 박소연(입문자), 정수빈(탐색자).
* **개념 (Concepts)**: 
  * [건기식 시장 문제점](../concepts/Health-Supplement-Market-Painpoints.md): 기존 시장의 정보 비대칭성 및 광고 범람 실태.
