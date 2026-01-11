# LCIF  
**Layer / LLM Constraint Inheritance Failure**

## Overview (EN)

LCIF describes a structural failure mode in transformer-based LLM systems.

Explicit constraints can be recognized at input time, yet silently fail to
propagate across generation and review. As a result, LLMs may produce outputs
that appear coherent, reasonable, and complete, while documenting actions,
evaluations, or decisions that were structurally impossible.

This is not a hallucination issue, not a prompt engineering problem, and not a
single-model or single-vendor bug. The behavior has been observed across
multiple LLMs and points to a paradigm-level architectural limitation.

The risk is not incorrect answers, but **plausible records that should never
exist**—records that pass review, evade detection, and quietly shift
responsibility.

This repository does not propose solutions or usage guidelines.  
It documents a boundary.

For the full specification, see:
- `docs/README_EN.md` (English)
- `docs/README_KO.md` (Korean)

---

## 개요 (KO)

LCIF는 트랜스포머 기반 LLM 시스템에서 발생하는 구조적 실패 모드를
설명한다.

명시적 제약은 입력 단계에서 인식될 수 있으나, 생성과 검수 과정을
거치며 조용히 상속되지 않을 수 있다. 그 결과, LLM은 논리적으로
그럴듯하고 완결된 출력을 생성하면서도, 실제로는 구조적으로
불가능했던 행위, 검토, 결정을 문서에 기록할 수 있다.

이 문제는 환각이 아니며, 프롬프트 엔지니어링의 문제가 아니고,
특정 모델이나 특정 기업의 버그도 아니다. 여러 LLM에서 공통적으로
관측되며, 이는 패러다임 수준의 아키텍처 한계를 가리킨다.

위험한 것은 오답이 아니라, **존재해서는 안 되는 그럴듯한 기록**이다.
이 기록은 검수를 통과하고, 탐지되지 않으며, 책임을 조용히 전이시킨다.

이 저장소는 해결책이나 사용 가이드를 제시하지 않는다.  
이 저장소는 하나의 **경계**를 문서화한다.

정식 명세는 다음을 참고한다:
- `docs/README_EN.md` (English)
- `docs/README_KO.md` (한국어)
