---
tags: [source, persona, ux-strategy]
date: 2026-04-21
sources: [raw/assets/7_persona-spectrum-map.md]
---

# 고객 페르소나 스펙트럼 맵 요약

**원본:** `raw/assets/7_persona-spectrum-map.md`

## 핵심 요약

시장 세분화 분석에서 도출된 6종 페르소나의 스펙트럼 구조 및 상호 관계, 플랫폼 접점 모델, 제품 설계 우선순위 매핑을 정의한 문서.

## 페르소나 스펙트럼

| 유형 | 페르소나 | 세그먼트 | 역할 | 추정 모수 |
|---|---|---|---|---|
| 🔵 **핵심(Core)** | [C1 한정훈](../entities/Persona-C1-Han.md) (36, 개발자) | Q1-A 가성비 최적화자 | SOM **수익 엔진** | 100~150만 명 |
| 🔵 **핵심(Core)** | [C2 박소연](../entities/Persona-C2-Park.md) (43, 인사팀 과장) | Q4-A 건강 계기 진입자 | SOM **성장 엔진** | 130~240만 명 |
| 🟢 **확장(Adjacent)** | [A2 정수빈](../entities/Persona-A2-Jung.md) (27, 뷰티 마케터) | Q4-C 트렌드 추종 | SEO·콘텐츠 트래픽 | 94~135만 명 |
| 🔴 **극단(Extreme)** | E1 나경아 (62, 은퇴 교사) | Q4-A 극단 — 디지털 약자 | 접근성 설계 기준 | 350~430만 명 |
| 🔴 **극단(Extreme)** | E2 김도현 (29, 데이터 분석가) | Q1-A 극단 — 신뢰 실패자 | 데이터 정확도 SLA 기준 | — |
| ⚫ **비활성(Non-user)** | N1 조미라 (58, 경리) | Q3 수동적 수용자 | 시장 확장 한계 | 525~800만 명 |

## 페르소나 간 연결 구조

```
[A2] → SNS 바이럴 → [C2] → Q4→Q1 전환(6~12개월) → [C1] → 카카오 공유 → [N1]
```

- **E1** → 접근성 설계가 C2·N1의 진입 허들을 낮춤
- **E2** → 데이터 정확도 기준이 C1의 신뢰 확보 전제 조건

## Phase 1 MVP 핵심 기능 (공통도 최고)
1. 제품 간 성분 비교 side-by-side + 성분명 일상어 번역
2. 채널 간 단가 자동 비교 (환율 실시간 반영)
3. 증상/목적 기반 진입 필터

## 교차 참조
- [Q4-Q1 전환 플라이휠](../concepts/Q4-Q1-Conversion-Flywheel.md)
- [TAM-SAM-SOM 분석](./6_TAM-SAM-SOM.md)
- [고객 여정 지도](./8_customer-journey-map.md)
- [AOS-DOS 분석](./9_aos-dos-analysis.md)
