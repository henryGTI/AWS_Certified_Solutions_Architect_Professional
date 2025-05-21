# 6. Meeting Reliability Requirements

## 6.1 신뢰성 설계 원칙 (Reliability Design Principles)

- **자동 복구(Automatically Recover from Failure)**: 장애 발생 시 자동으로 복구하는 시스템 설계
- **복구 절차 테스트(Test Recovery Procedures)**: 정기적으로 장애 복구 시나리오를 테스트
- **수평 확장(Scale Horizontally)**: 여러 인스턴스를 통해 가용성 및 확장성 확보
- **추측하지 않기(Stop Guessing Capacity)**: 실제 사용량 기반으로 리소스 할당
- **자동화된 변경 관리(Manage Change in Automation)**: 인프라 변경을 자동화하여 실수 방지

---

## 6.2 신뢰성의 기본 요구사항 (Foundational Requirements)

- **리소스 제약(Resource Constraints)**: 서비스별 한도(Quota) 및 제한 확인
- **네트워크 토폴로지(Network Topology)**: 고가용성, 확장성, 장애 격리를 위한 네트워크 설계
- **AZ(가용영역) 활용**: 여러 AZ에 리소스 분산 배치
- **중복성(Redundancy)**: 장애 발생 시 대체 가능한 리소스 확보

---

## 6.3 장애 설계 (Designing for Failure)

- **Loosely Coupled Dependencies**: 서비스 간 결합도를 낮춰 장애 전파 방지
- **Idempotency**: 동일 요청이 여러 번 처리되어도 결과가 같도록 설계
- **Graceful Degradation**: 일부 기능 장애 시 전체 서비스가 중단되지 않도록 설계

---

## 6.4 장애 감지 및 변경 관리 (Change Management)

- **CloudWatch, X-Ray**: 실시간 모니터링 및 장애 감지
- **알람 및 자동화**: 장애 발생 시 자동으로 복구 또는 알림
- **배포 자동화**: 무중단 배포, 롤백 전략

---

## 6.5 장애 관리 (Failure Management)

- **백업 및 복구**: 정기 백업, 신속한 복구 전략
- **멀티 리전 배포**: 지역 장애 대비
- **장애 복구 테스트**: 실제 장애 상황을 가정한 복구 훈련(Chaos Engineering)

---

## 참고 자료

- [AWS Well-Architected Framework - Reliability Pillar](https://docs.aws.amazon.com/ko_kr/wellarchitected/latest/reliability-pillar/welcome.html)
- [AWS 고가용성 설계](https://aws.amazon.com/ko/architecture/high-availability/)
