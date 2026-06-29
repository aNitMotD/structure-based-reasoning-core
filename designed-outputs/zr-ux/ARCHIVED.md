> **직접 접근 고지 / Direct Access Notice**  
> 본 문서는 저장소의 README.md 및 INTERPRETATION-GUARDRAILS.md를 먼저 확인했다는 전제 하에서만 해석되어야 합니다.  
> This document must be interpreted only on the assumption that the repository’s README.md and INTERPRETATION-GUARDRAILS.md have been reviewed first.

---

# ZR-UX Removal Decision

## English

## Status
Archived. No active development.

## Summary
ZR-UX was removed after design validation.

The goal of ZR-UX was to make ZR outputs more readable or user-friendly
through a UX or rendering layer.

## Reason for Removal
Experiments showed that any UX layer placed after ZR output
inevitably introduces semantic interpretation, even when strictly constrained.

This includes:
- restatement or paraphrasing
- perspective framing ("from a ZR-UX point of view")
- implicit responsibility attribution
- closure, guidance, or next-step signaling

These effects directly conflict with ZR’s core properties:
- non-judgment
- non-attribution
- responsibility boundary preservation
- boundary-based stopping

The issue was not insufficient constraints or wording,
but the existence of a post-analysis UX layer itself.

## Conclusion
ZR-UX was removed entirely.

Zero Reflect (ZR) is maintained as a standalone system.
ZR outputs are produced as-is, without any UX, rendering,
formatting, or post-processing layers.

Zero Reflect repository is intentionally preserved as a record
of that design decision.

---

# ZR-UX 제거 결정

## 한국어

## 상태
아카이브됨. 활성 개발 없음.

## 요약
ZR-UX는 설계 검증 이후 제거되었다.

ZR-UX의 목표는 UX 또는 렌더링 계층을 통해
ZR 출력물을 더 읽기 쉽거나 사용자 친화적으로 만드는 것이었다.

## 제거 사유
실험 결과, ZR 출력 이후에 배치되는 모든 UX 계층은
엄격하게 제약되더라도 불가피하게 의미 해석을 도입하는 것으로 확인되었다.

여기에는 다음이 포함된다:
- 재서술 또는 의역
- 관점 프레이밍("ZR-UX 관점에서")
- 암묵적 책임 귀속
- 종결, 안내, 또는 다음 단계 신호

이러한 효과는 ZR의 핵심 속성과 직접 충돌한다:
- 비판단
- 비귀속
- 책임 경계 보존
- 경계 기반 중단

문제는 제약이나 문구가 부족했던 것이 아니라,
분석 이후에 배치되는 UX 계층 자체의 존재였다.

## 결론
ZR-UX는 완전히 제거되었다.

Zero Reflect(ZR)는 독립형 시스템으로 유지된다.
ZR 출력물은 UX, 렌더링, 포매팅, 또는 후처리 계층 없이
있는 그대로 생성된다.

Zero Reflect 저장소는 해당 설계 결정을 기록하기 위해
의도적으로 보존된다.
