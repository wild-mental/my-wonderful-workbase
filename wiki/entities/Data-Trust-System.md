---
tags: [entity, system, trust, data-quality]
date: 2026-04-21
sources: [raw/assets/00_PRD_v1.md, raw/assets/05_SRS_v1.md, raw/assets/06_value-proposition-sheet_V2_(Rooted).md]
---

# Data Trust System (데이터 신뢰 시스템)

## 정의

플랫폼 데이터의 정확성과 투명성을 보장하는 시스템. 기존 비교 플랫폼의 데이터 오류 경험으로 카테고리 전체를 불신하는 E2 페르소나의 신뢰를 확보하기 위한 **필수 인프라**.

## 핵심 기능

| 기능 | 설계 |
|---|---|
| **원본 라벨 이미지** | 제품별 원본 라벨 JPEG 팝업 아코디언 메뉴 제공 |
| **데이터 출처 투명 공개** | 식약처 DB, 제조사 공개 자료 등 수집 출처·일자·버전 명시 |
| **오류 신고 체계** | 사용자 오류 신고 → **48시간 내 처리** → 결과 통보 |
| **교차 검증** | 신규 등록 제품은 "검증 중" 배지, 충분한 교차 검증 후 "검증 완료" 전환 |
| **제보자 보상** | 신고자 기여 인정 배지 |

## AOS-DOS 근거

- **EXT-2** (데이터 오류 → 카테고리 불신): AOS **4.0** / DOS **3.2** → MVP 필수
- C1(수익 엔진)의 리텐션을 유지하기 위한 SLA
- 데이터 오류율 **≤ 5%** (MVP 출시 3개월 검증 기준)

## 설계 시사점

- E2가 성분 데이터 출처를 **클릭 2회 이내**에 원본까지 추적할 수 있어야 함
- DB 확장 과정에서 신규 제품 데이터 오류율이 기존보다 높으면 충성도 하락 (커버리지 vs 정확도 트레이드오프)

## 교차 참조
- [레몬 마켓과 신뢰 설계](../concepts/Lemon-Market-Trust-Design.md)
- [성분 정규화](../concepts/Data-Normalization.md)
- [SRS 요약](../sources/05_SRS_v1.md)
- [AOS-DOS 분석](../sources/9_aos-dos-analysis.md)
