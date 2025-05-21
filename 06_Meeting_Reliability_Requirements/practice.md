# 6장 실습: Meeting Reliability Requirements

---

## 1. Auto Scaling 그룹 및 ELB 실습

1. **EC2 → Auto Scaling Groups → Create Auto Scaling group**
   - 최소/최대/원하는 인스턴스 수 설정
   - 여러 AZ에 인스턴스 분산
2. **ELB(Elastic Load Balancer) 생성**
   - Auto Scaling 그룹과 연동하여 트래픽 분산

---

## 2. 장애 복구 시나리오 테스트

1. **Auto Scaling 그룹 내 인스턴스 강제 종료**
   - 자동으로 새로운 인스턴스가 생성되는지 확인
2. **ELB 헬스 체크 실패 시 인스턴스 교체 확인**

---

## 3. CloudWatch 알람 및 자동화 실습

1. **CloudWatch → Alarms → Create Alarm**
   - EC2, RDS 등 리소스의 CPU, 네트워크 등 모니터링
   - 임계치 초과 시 알람 및 자동 복구(Auto Recovery) 설정

---

## 4. 백업 및 복구 실습

1. **RDS → 백업 스냅샷 생성 및 복원**
2. **EC2 → AMI 생성 및 복원**
3. **S3 → 버전 관리 및 수명주기 정책 설정**

---

## 5. 멀티 AZ, 멀티 리전 배포 실습

1. **RDS → Multi-AZ 배포 옵션 활성화**
2. **S3 Cross-Region Replication 설정**
3. **Route 53 → Health Check 및 Failover Routing Policy 설정**

---

## 6. 장애 복구 훈련(Chaos Engineering) 체험

- 실제로 인스턴스/서비스를 강제로 중단시켜 복구 절차를 점검
- AWS Fault Injection Simulator(유료) 또는 수동 테스트

---

## 참고 자료

- [Auto Scaling 실습](https://docs.aws.amazon.com/ko_kr/autoscaling/ec2/userguide/GettingStartedTutorial.html)
- [CloudWatch 알람 실습](https://docs.aws.amazon.com/ko_kr/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html)
- [RDS Multi-AZ 실습](https://docs.aws.amazon.com/ko_kr/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html)
