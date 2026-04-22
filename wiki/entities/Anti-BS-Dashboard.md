---
tags: [entity, feature, dashboard, trust, must-have]
date: 2026-04-21
sources: [raw/assets/00_PRD_v1.md, raw/assets/05_SRS_v1.md, raw/assets/06_value-proposition-sheet_V2_(Rooted).md]
---

# Anti-BS Dashboard (광고 배제 팩트체크 대시보드)

## 정의

마케팅 노이즈(제휴 커미션 콘텐츠, 스폰서 별점, 체험단 블로그)를 UI에서 **100% 제거**하고, 오직 식약처 DB 및 의학 논문에 기반한 **객관적 뱃지(결론)** 만을 제공하는 제품 상세 대시보드.

## 해결하는 Pain

| Pain ID | 내용 | AOS | DOS |
|---|---|---|---|
| **CORE-3** | 광고성 콘텐츠 범람, 신뢰 정보 부재 | **4.0** | **3.60** |
| **CORE-2** | 성분 정보 해석 불가 → 비교 불가 | 3.0 | 2.40 |
| **CJM-1** | 인지 단계 독립 정보 부재 | **4.0** | **3.60** |

- **AOS·DOS 양쪽 모두 1위** — MVP에서 가장 먼저 해결해야 하는 Pain
- [C2 박소연](./Persona-C2-Park.md), [A2 정수빈](./Persona-A2-Jung.md)의 핵심 니즈 해결

## 핵심 기능

| 기능 | 설계 |
|---|---|
| **의학 뱃지 시스템** | ✅ 식약처 인정 / ⚠️ 주의 필요 / 🚫 근거 미비 — 건강기능식품공전 기준만 호출 |
| **성분명 일상어 번역** | "콜레칼시페롤" → "몸에 잘 흡수되는 비타민 D3" |
| **가격 적정성 지표** | "이 가격대에서 시장 평균" 위치 표시 |
| **광고 원천 차단** | 리뷰/별점/블로그 홍보글 UI 미탑재. "광고 아님" 독립 선언 배지 |

## 법률 리스크 대응 (건강기능식품법)

- ✖ 잘못된 예: "치매 예방 효과"
- ✔ 정답: "기억력 개선에 도움을 줄 수 있음 (식약처 인정 원료)"
- 배지 DB는 식약처 고시 '기능성 인정 내용'만 그대로 호출하여 래핑

## JTBD 전환 트리거

> "광고인지 아닌지만 감별해 주는 직관적인 성분 판독기가 필요해요." (A2 인터뷰)
> "결론 뱃지가 있으면 좋겠어요. 제가 일일이 공부할 시간이 없거든요." (C2 인터뷰)

## 바이럴 연동

A2가 팩트체크 결과를 **SNS 공유용 비교 카드**로 1탭 생성 → C2의 첫 유입 경로 → [Q4-Q1 전환 플라이휠](../concepts/Q4-Q1-Conversion-Flywheel.md) 기동

## 교차 참조
- [Persona C2 박소연](./Persona-C2-Park.md) · [Persona A2 정수빈](./Persona-A2-Jung.md) — Primary 사용자
- [레몬 마켓과 신뢰 설계](../concepts/Lemon-Market-Trust-Design.md) — 이론적 기반
- [Data Trust System](./Data-Trust-System.md) — 데이터 정확성 보장 시스템
- [Q4-Q1 전환 플라이휠](../concepts/Q4-Q1-Conversion-Flywheel.md) — 성장 메커니즘
- [PRD 요약](../sources/00_PRD_v1.md) · [SRS 요약](../sources/05_SRS_v1.md)
- [AOS-DOS 분석](../sources/9_aos-dos-analysis.md) · [JTBD 인터뷰](../sources/10_jtbd-interview-report.md)
