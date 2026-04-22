---
tags: [entity, feature, engine, pricing, must-have]
date: 2026-04-21
sources: [raw/assets/00_PRD_v1.md, raw/assets/05_SRS_v1.md, raw/assets/06_value-proposition-sheet_V2_(Rooted).md]
---

# Super-Calc Engine (초자동화 단가 산출 엔진)

## 정의

다양한 채널(iHerb, 쿠팡, 네이버 등)에 흩어진 건강기능식품 데이터를 수집하여 **1일 복용량 기준 원화(₩) 최종 단가**로 정규화·정렬해 주는 자동화 파이프라인. 실시간 환율, 배송비, 관세, 할인코드를 모두 반영한 '실지불가'를 제공.

## 해결하는 Pain

| Pain ID | 내용 | AOS | DOS |
|---|---|---|---|
| **CORE-1** | 채널 간 단가 비교 수동 작업 과부하 | 3.0 | **2.70** |

- [C1 한정훈](./Persona-C1-Han.md)이 iHerb·쿠팡·네이버 탭 8개를 열고 엑셀로 40~60분 수동 계산하던 작업을 **5초**로 압축
- SOM 수익 모델의 핵심 축 — 1년 차 매출의 **55%**를 직접 창출

## 핵심 연산 공식

```
1일 단가 = (제품 가격 × 환율 + 배송비 + 관세 - 할인) ÷ (총 정수 ÷ 1일 복용 정수)
```

## 기술적 전제 조건

- [성분 정규화(Data Normalization)](../concepts/Data-Normalization.md) 역량이 반드시 선행
- 비표준 규격(60정/120정/240정, 1캡슐/2캡슐) 자동 파싱
- 공식 Affiliate API(쿠팡 파트너스, iHerb Affiliate) 기반 합법적 데이터 수집
- 정규화 정확도 **95% 이상** 필수 (미달 시 E2 페르소나 이탈 직결)

## MVP 구현 범위 (Phase 1)

| 항목 | MVP 범위 |
|---|---|
| 채널 | 쿠팡 파트너스 (단일 채널) |
| 제품 DB | 상위 300개 → 연말 1,000개 |
| 환율 | 실시간 반영 (iHerb는 Phase 2) |
| 리스크 | 크롤링 봇 차단 → 공식 API 파싱으로 대응 |

## JTBD 전환 트리거

> "엑셀에 달러치고 나눗셈 하다보면 현타옵니다." (C1 인터뷰)
> "바로 씁니다. 근데 조건이 있어요. 실시간 할인코드 적용된 최종가여야 합니다." (C1 인터뷰)

## 교차 참조
- [Persona C1 한정훈](./Persona-C1-Han.md) — 이 기능의 Primary 사용자
- [Data Trust System](./Data-Trust-System.md) — 데이터 정확도 보장 시스템
- [성분 정규화](../concepts/Data-Normalization.md) — 기술적 전제 조건
- [에셋 라이트 모델](../concepts/Asset-Light-Model.md) — 제휴 수수료 수익 구조
- [PRD 요약](../sources/00_PRD_v1.md) · [SRS 요약](../sources/05_SRS_v1.md) · [AOS-DOS 분석](../sources/9_aos-dos-analysis.md)
- [JTBD 인터뷰](../sources/10_jtbd-interview-report.md)
