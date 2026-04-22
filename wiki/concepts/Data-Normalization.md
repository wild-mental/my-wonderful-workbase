---
tags: [concept, technology, data-engineering, moat]
date: 2026-04-21
sources: [raw/assets/5_problem-definition.md, raw/assets/6_TAM-SAM-SOM+MarketSegment.md, raw/assets/4_ksf-report.md]
---

# 성분 정규화 (Data Normalization)

## 정의

비표준으로 표기된 건기식 성분 정보(이름, 단위, 기준)를 **통일된 형식**으로 변환하는 데이터 엔지니어링 작업. 동일 성분이 "콜레칼시페롤", "비타민D3", "1,000IU", "25mcg", "25μg" 등 제각각으로 표기되는 문제를 해결.

## 왜 핵심 경쟁력인가

- [KSF #1](../sources/4_ksf-report.md): "제조원 기반 제품 클러스터링 및 데이터 표준화 역량"
- [KSF #4](../sources/4_ksf-report.md): "공급자 마케팅 용어를 표준 데이터로 환언(Translating)하는 기술력"
- 비표준 표기 정규화는 **시간 집약적 작업**으로 후발 복제가 어려운 **기술적 해자(Moat)**

## 정규화 대상

| 변환 대상 | 예시 |
|---|---|
| 성분명 통일 | 콜레칼시페롤 = 비타민D3 = Cholecalciferol |
| 단위 통일 | 1,000 IU = 25 mcg = 25 μg |
| 1일 복용 기준 통일 | 1캡슐/2캡슐/1포 → 1일 섭취 기준량 |
| 채널 간 가격 통일 | USD + 환율 + 배송비 → ₩ 최종 단가 |
| 용량 통일 | 60정/120정/240정 → 1일 단가 |

## 핵심 제약 조건

- **정확도 95% 이상** 필수 — 미달 시 오히려 신뢰 손상 ([E2 페르소나](../entities/Persona-C1-Han.md) 이탈 직결)
- 1년 차 1,000개 제품 DB 구축 목표 — AI 크롤링 + 수동 검증 속도 미검증 → **PoC 최우선**

## 교차 참조
- [Super-Calc Engine](../entities/Super-Calc-Engine.md) — 정규화 결과를 활용하는 핵심 기능
- [문제 정의서](../sources/5_problem-definition.md)
- [KSF 보고서](../sources/4_ksf-report.md)
- [Value Proposition Sheet](../sources/06_value-proposition-sheet.md)
