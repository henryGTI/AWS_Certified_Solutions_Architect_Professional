# 7. Ensuring Business Continuity

## 7.1 비즈니스 연속성(BC)와 고가용성(HA)

- **비즈니스 연속성(BC)**: 장애, 재해, 사고 발생 시에도 핵심 비즈니스가 지속될 수 있도록 하는 전략
- **고가용성(HA)**: 시스템이 항상 동작하도록 설계

---

## 7.2 DR(Disaster Recovery) 전략

- **백업 및 복원(Backup & Restore)**: 정기적으로 데이터를 백업, 필요 시 복원
- **파일럿 라이트(Pilot Light)**: 최소한의 핵심 시스템만 상시 운영, 장애 시 전체 시스템 신속 복구
- **웜 스탠바이(Warm Standby)**: 축소된 규모의 시스템을 상시 운영, 장애 시 확장
- **액티브-액티브(Active-Active)**: 두 개 이상의 시스템이 동시에 운영, 장애 시 자동 전환

---

## 7.3 AWS에서의 DR 옵션

- **S3, Glacier**: 백업 데이터 저장
- **RDS, DynamoDB**: 스냅샷, 멀티 AZ, 리전 복제
- **Route 53**: 헬스 체크 및 장애 조치(Failover)
- **CloudEndure, AWS Backup**: 자동화된 백업/복구

---

## 7.4 DR 테스트 및 모니터링

- 정기적으로 DR 시나리오 테스트
- 장애 감지 및 알림 설정

---

## 참고 자료

- [AWS DR 전략](https://aws.amazon.com/ko/backup-recovery/disaster-recovery/)
- [AWS Well-Architected Framework - BC/DR](https://docs.aws.amazon.com/ko_kr/wellarchitected/latest/reliability-pillar/disaster-recovery.html)
