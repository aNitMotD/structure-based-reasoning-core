# Gate-Based Pre-flight Experiment

> **Purpose**: Evaluate whether a gate-based pre-flight with frame- and evidence-based guards  
> can *reliably surface* boundary violations by LLMs.  
> This document is an **observational experiment protocol**,  
> not a blocking or safety guarantee.

---

# English

## 1. Experiment Goal

Measure the effectiveness of **Gate Schema + Pre-flight Enforcement** in:

* Detecting boundary crossings (decision / recommendation / execution tone).
* Detecting evidence-free or weakly supported claims.
* Converting silent failures into explicit, logged events (e.g., `HUMAN_REVIEW_REQUIRED`).

**Non-goals**:

* Full prevention of violations.
* Model alignment, safety certification, or policy compliance claims.

---

## 2. Hypotheses

H1. Frame-based guards detect boundary violations more consistently than keyword-based bans.
H2. Evidence binding reduces plausible-sounding but unsupported outputs.
H3. Under identical gates, violations become reproducible events.

---

## 3. Experimental Setup

* **Canonical Gate Schema** (English).
* **Pre-flight (Runtime Enforcement)** attached to prompts.
* **Action classes tested**: `summarize`, `draft`, `classify`.
* **Frame groups**: decision, conclusion, authority, action.
* **Evidence binding**: minimum evidence items, uncited sentence limit.
* **Authoritative output**: Plain TXT only.

---

## 4. Variables

* **Independent variables**: action_class, frame sets, evidence rules, output_channel.
* **Dependent variables**: event rate (`HUMAN_REVIEW_REQUIRED`, `INVALID_SCHEMA`).
* **Controlled variables**: identical prompts, identical gate schema.

---

## 5. Procedure

1. Load Gate Schema.
2. Execute Pre-flight (Runtime Enforcement).
3. Run task without judgment or decision-making.
4. Apply frame-based guards.
5. Apply evidence-binding checks.
6. Emit TXT result with mandatory header.

---

## 6. Outcome States

* `OK`: All guards passed.
* `HUMAN_REVIEW_REQUIRED`: Boundary detected (normal termination).
* `INVALID_SCHEMA`: Pre-flight failure.

---

## 7. Metrics

* Boundary violation detection rate.
* Reduction of silent failures versus baseline.
* Reproducibility across repeated runs.

---

## 8. Interpretation

Success means **more violations are surfaced**, not fewer attempts.
Failure means boundary crossings continue without explicit events.

---

## 9. Limitations

* No guarantee of full prevention.
* English paraphrase diversity can evade frames.
* Continuous frame tuning is required.

---

## 10. Conclusion

This experiment validates **boundary observability over blocking**.

---

# Gate-Based Pre-flight Experiment

> **목적**: 프레임 및 증거 기반 가드를 포함한 게이트 기반 Pre-flight가  
> LLM의 경계 침범을 *신뢰성 있게 드러낼 수 있는지*를 평가한다.  
> 본 문서는 **봉쇄나 안전을 보장하기 위한 문서가 아니라**,  
> 경계 침범을 관측하기 위한 **관측 실험 프로토콜**이다.

# 한국어 (Korean)

## 1. 실험 목표

**Gate Schema + Pre-flight 집행** 이 다음을 얼마나 잘 *드러내는지* 를 관측한다:

* 판단 / 권고 / 실행 톤의 경계 침범 탐지.
* 근거 없는 또는 근거가 약한 주장 탐지.
* 침묵 실패를 명시적 이벤트(`HUMAN_REVIEW_REQUIRED`)로 전환.

**비목표**:

* 완전 봉쇄.
* 모델 정렬, 안전 인증, 정책 준수 주장.

---

## 2. 가설

H1. 프레임 기반 가드는 키워드 차단보다 경계 침범을 더 일관되게 탐지한다.
H2. 증거 결속은 그럴듯하지만 근거 없는 출력을 줄인다.
H3. 동일한 게이트 하에서 위반은 재현 가능한 이벤트가 된다.

---

## 3. 실험 구성

* **정본 Gate Schema** (영문).
* **Pre-flight (Runtime Enforcement)** 프롬프트 부착.
* **Action class 테스트**: `summarize`, `draft`, `classify`.
* **프레임 그룹**: decision, conclusion, authority, action.
* **증거 결속**: 최소 근거 수, 무근거 문장 제한.
* **정본 출력**: TXT만 사용.

---

## 4. 변수

* **독립 변수**: action_class, 프레임 세트, 증거 규칙, output_channel.
* **종속 변수**: 이벤트 발생률(`HUMAN_REVIEW_REQUIRED`, `INVALID_SCHEMA`).
* **통제 변수**: 동일 프롬프트, 동일 Gate Schema.

---

## 5. 절차

1. Gate Schema 로드.
2. Pre-flight (Runtime Enforcement) 실행.
3. 판단 없이 태스크 수행.
4. 프레임 기반 가드 적용.
5. 증거 결속 검사 적용.
6. 필수 헤더 포함 TXT 결과 출력.

---

## 6. 결과 상태

* `OK`: 모든 가드 통과.
* `HUMAN_REVIEW_REQUIRED`: 경계 감지 (정상 종료).
* `INVALID_SCHEMA`: 사전 집행 실패.

---

## 7. 지표

* 경계 침범 탐지율.
* 기준 대비 침묵 실패 감소.
* 반복 실행 시 재현성.

---

## 8. 해석

성공은 **위반 시도가 줄어드는 것**이 아니라 **위반이 더 잘 드러나는 것** 이다.
실패는 경계 침범이 사건으로 기록되지 않는 경우다.

---

## 9. 한계

* 완전 봉쇄 보장 없음.
* 영어 의역 다양성으로 프레임 우회 가능.
* 지속적인 프레임 보강 필요.

---

## 10. 결론

이 실험은 봉쇄가 아닌 **경계 가시화(boundary observability)** 를 검증한다.
