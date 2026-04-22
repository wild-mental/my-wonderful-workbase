---
tags: [source, aos-dos, opportunity-scoring, market-analysis]
date: 2026-04-21
sources: [raw/assets/9_aos-dos-analysis.md]
---

# AOS-DOS 통합 분석 요약

**원본:** `raw/assets/9_aos-dos-analysis.md`

## 핵심 요약

6종 페르소나의 19개 Pain/Goal을 Importance·Satisfaction·Market Relevance로 수치화하여 AOS(Attractiveness of Opportunity Score)와 DOS(Demand Opportunity Score)를 산출. MVP 기능 우선순위를 데이터 기반으로 결정하는 핵심 분석 프레임워크.

## 공식
- **AOS** = Importance × (1 − Satisfaction/5)
- **DOS** = AOS × Market Relevance

## Q1 핵심 혁신 기회 Top 8 (AOS ≥ 2.5, DOS ≥ 1.5)

| 순위 | Pain ID | Pain 내용 | AOS | DOS | Phase |
|---|---|---|---|---|---|
| 1 | CORE-3 | 광고 범람 + 독립 비교 부재 | 4.0 | 3.60 | **MVP** |
| 1 | CJM-1 | 인지단계 독립 정보 부재 | 4.0 | 3.60 | **MVP** |
| 3 | ADJ-1 | 트렌드 성분 근거 판단 불가 | 4.0 | 3.20 | Phase 2 |
| 3 | EXT-2 | 데이터 오류 → 카테고리 불신 | 4.0 | 3.20 | **MVP** |
| 5 | CORE-1 | 채널 단가 수동 비교 과부하 | 3.0 | 2.70 | **MVP** |
| 6 | CORE-2 | 성분 해석 불가 | 3.0 | 2.40 | **MVP** |
| 6 | CJM-2 | 고려단계 검증 수단 없음 | 3.0 | 2.40 | **MVP** |
| 8 | EXT-1 | 디지털 접근 장벽 | 4.0 | 2.00 | Phase 2 |

## AOS 분포
- AOS 4.0 (최고): 5개(26%) — **대체 솔루션 사실상 부재한 시장 공백**
- AOS 3.0: 3개(16%), AOS 2.4: 6개(32%)
- **74%가 Q1 혁신기회에 집중 → Unmet Need가 극도로 높은 블루오션**

## 핵심 발견
1. **AOS 최고 ≠ DOS 최고:** EXT-1은 AOS 4.0이나 DOS 2.0 → Phase 2
2. **DOS가 AOS 순위를 역전:** CORE-1(채널 단가)은 AOS 3.0이나 DOS 2.70 (SOM 수익 55% 직결)
3. **N1은 DOS -0.60:** 직접 투자 무의미 재확인

## 교차 참조
- [TAM-SAM-SOM 분석](./6_TAM-SAM-SOM.md)
- [페르소나 스펙트럼 맵](./7_persona-spectrum-map.md)
- [JTBD 인터뷰](./10_jtbd-interview-report.md)
- [건기식 시장 문제점](../concepts/Health-Supplement-Market-Painpoints.md)
