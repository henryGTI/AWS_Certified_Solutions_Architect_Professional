# 7장 실습: Ensuring Business Continuity

---

## 1. S3 버킷 백업 및 복원 실습

1. **S3 버킷 생성 및 데이터 업로드**
2. **버전 관리(Versioning) 활성화**
3. **수명주기(Lifecycle) 정책으로 자동 백업/아카이브 설정**
4. **삭제/수정 후 이전 버전 복원 실습**

---

## 2. RDS 스냅샷 및 복원 실습

1. **RDS 인스턴스 생성**
2. **스냅샷 수동 생성**
3. **스냅샷에서 새 인스턴스 복원**

---

## 3. Cross-Region Replication 실습

1. **S3 Cross-Region Replication 설정**
2. **RDS, DynamoDB 리전 복제 옵션 확인**

---

## 4. Route 53 장애 조치(Failover) 실습

1. **헬스 체크(Health Check) 생성**
2. **Failover Routing Policy로 장애 시 자동 전환 설정**

---

## 5. DR 시나리오 테스트

- S3, RDS, Route 53 등에서 장애 상황을 가정하고 복구 절차 실습

---

## 참고 자료

- [S3 백업 실습](https://docs.aws.amazon.com/ko_kr/AmazonS3/latest/userguide/Versioning.html)
- [RDS 스냅샷 실습](https://docs.aws.amazon.com/ko_kr/AmazonRDS/latest/UserGuide/USER_CreateSnapshot.html)
- [Route 53 장애 조치 실습](https://docs.aws.amazon.com/ko_kr/Route53/latest/DeveloperGuide/dns-failover.html)
