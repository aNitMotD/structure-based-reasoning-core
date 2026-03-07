# CIF / SIF / TIF 사례 메모 모음

관측 표기:

- **CIF** — Constraint Inheritance Failure (제약 상속 실패)
- **SIF** — Structural Inaccessibility Failure (구조 접근 불가 상태)
- **TIF** — Time Inconsistency Failure (시간 불일치 실패)

이 문서는 **서사적 사건 기록이 아니라 구조 패턴** 에 초점을 둔다.

---

# 사례 1 — Therac-25 방사선 사고 (1985-1987)

## 1. 사건 개요
시스템: Therac-25 방사선 치료 장비  
기간: 1985–1987  
결과: 과도한 방사선 조사로 중상 및 사망 발생.

## 2. 시스템 구조

이전 시스템:

hardware safety  
↓  
software control  
↓  
operator  

Therac-25:

software control  
↓  
operator  

## 3. CIF 관측
하드웨어 안전 제약이 제거됨 → 제약 체인이 붕괴.

## 4. SIF 관측
장비 내부 상태는 보이지 않는 반면, 운영자는 단순 오류 코드만 확인 가능.

## 5. TIF 관측
운영자의 재시도 휴리스틱이 시스템 타이밍 상태와 결합되어 치명적 방사선 조사 발생.

## 6. 패턴

CIF → SIF → TIF → 치명적 결과

---

# 사례 2 — Google Maps / Android 저장소 사건 (2012)

## 1. 사건 개요
외부 저장소 처리 방식 변경으로 Android 앱 데이터가 삭제되는 문제 발생.

## 2. 시스템 구조

application  
↓  
external storage  
↓  
system update / storage management  

## 3. CIF 관측
영구 저장을 전제로 한 플랫폼 안전 가정이 업데이트 로직에 상속되지 않음.

## 4. SIF 관측
개발자의 정신 모델 ≠ 실제 플랫폼 저장소 구현.

## 5. TIF 관측
업데이트 타이밍에 의해 데이터 디렉토리가 예상치 않게 삭제됨.

## 6. 패턴

CIF → SIF → TIF → 대규모 데이터 손실

---

# 사례 3 — AWS S3 장애 (2017)

## 1. 사건 개요
US-East-1 리전의 AWS S3 장애로 인터넷의 상당 부분 서비스 중단 발생.

## 2. 시스템 구조

operator command  
↓  
infrastructure control  
↓  
storage services  
↓  
dependent services  

## 3. CIF 관측
운영 명령 인터페이스로 안전 제약이 충분히 전달되지 않음.

## 4. SIF 관측
운영자가 볼 수 있는 범위가 실제 서비스 의존 그래프를 반영하지 못함.

## 5. TIF 관측
시스템 재시작 및 복구 시간이 예상보다 훨씬 길게 소요됨.

## 6. 패턴

CIF → SIF → TIF → 대규모 서비스 장애

---

# 사례 4 — Boeing 737 MAX MCAS 사고 (2018-2019)

## 1. 사건 개요
MCAS 비행 제어 시스템과 관련된 두 차례 항공기 추락 사고.

## 2. 시스템 구조

sensor input  
↓  
MCAS software  
↓  
flight control surfaces  
↓  
pilot  

## 3. CIF 관측
단일 센서 입력만으로 비행 제어 로직이 작동하도록 설계됨.

제약 중복성 제거.

## 4. SIF 관측
조종사들은 MCAS 동작 방식과 시스템 로직을 충분히 인지하지 못함.

## 5. TIF 관측
반복적인 자동 트림 수정이 시간 압박 루프를 확대.

## 6. 패턴

CIF → SIF → TIF → 항공기 제어 상실

---

# 사례 5 — Knight Capital 트레이딩 사고 (2012)

## 1. 사건 개요
트레이딩 소프트웨어 배포 오류로 대규모 의도하지 않은 거래 발생.

## 2. 시스템 구조

deployment system  
↓  
trading algorithm  
↓  
market execution  

## 3. CIF 관측
배포 설정 문제로 인해 레거시 코드 경로가 의도치 않게 활성화됨.

## 4. SIF 관측
운영자는 실행 중인 알고리즘의 실제 동작 상태를 인지하지 못함.

## 5. TIF 관측
자동 거래가 몇 분 만에 손실을 폭발적으로 확대.

## 6. 패턴

CIF → SIF → TIF → 금융 시스템 불안정

---

# 사례 6 — Ariane 5 Flight 501 실패 (1996)

## 1. 사건 개요
소프트웨어 예외로 인해 발사 직후 로켓 파괴.

## 2. 시스템 구조

navigation sensors  
↓  
inertial reference software  
↓  
flight control  

## 3. CIF 관측
Ariane 4용 소프트웨어를 Ariane 5에 재사용하면서 비행 프로파일 가정 불일치 발생.

## 4. SIF 관측
오버플로 예외가 진단 모드 데이터를 비행 데이터로 오인하게 만듦.

## 5. TIF 관측
발사 단계에서 즉시 실패 전파.

## 6. 패턴

CIF → SIF → TIF → 기체 파괴

---

# 사례 7 — Facebook 글로벌 BGP 장애 (2021)

## 1. 사건 개요
BGP 설정 오류로 Facebook 서비스 전 세계 중단.

## 2. 시스템 구조

network configuration change  
↓  
BGP routing system  
↓  
global service availability  

## 3. CIF 관측
구성 명령 전파에 대한 내부 안전 제약이 충분하지 않음.

## 4. SIF 관측
네트워크 가시성 도구가 동일 네트워크에 의존하고 있었음.

## 5. TIF 관측
엔지니어들이 시스템 원격 접근을 잃어 복구가 지연.

## 6. 패턴

CIF → SIF → TIF → 글로벌 서비스 중단

---

# 사례 8 — Cloudflare Regex 장애 (2020)

## 1. 사건 개요
WAF 규칙에 배포된 잘못된 정규식으로 글로벌 성능 저하 발생.

## 2. 시스템 구조

rule deployment  
↓  
traffic filtering engine  
↓  
global edge network  

## 3. CIF 관측
규칙 배포 파이프라인에서 성능 안전 제약이 적용되지 않음.

## 4. SIF 관측
운영자는 최악의 정규식 실행 비용을 확인할 수 없었음.

## 5. TIF 관측
CPU 포화가 글로벌 네트워크 노드 전체로 빠르게 확산.

## 6. 패턴

CIF → SIF → TIF → 글로벌 성능 붕괴

---

# 사례 간 공통 구조 패턴

이 사건들에서 공통적으로 나타나는 구조:

복잡한 시스템  
+ 제약 제거 또는 불일치  
+ 내부 구조의 비가시성  
+ 잘못된 시간 가정  

→ 시스템적 실패

단순화된 구조:

CIF → SIF → TIF
