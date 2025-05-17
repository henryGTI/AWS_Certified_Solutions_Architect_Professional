# 4. Ensuring Cost Optimization

## 4.1 비용 최적화 원칙 (Cost Optimization Principles)

- **적정 용량(Capacity) 사용**: 실제 필요한 만큼만 리소스를 할당하고, 과도한 프로비저닝을 피함
- **유휴 리소스 제거**: 사용하지 않는 EC2, EBS, Elastic IP, RDS 등은 반드시 종료/삭제
- **적합한 요금제 선택**: 온디맨드, 예약 인스턴스, Savings Plans, 스팟 인스턴스 등 다양한 요금제를 상황에 맞게 활용
- **자동화된 스케일링**: Auto Scaling, Lambda 등으로 트래픽에 따라 리소스 자동 조정

---

## 4.2 태깅을 통한 거버넌스 (Establishing Governance with Tagging)

- **Cost Allocation Tag**: 리소스별로 태그를 부여해 비용을 프로젝트, 부서, 환경별로 구분
- **Tag Policy**: AWS Organizations에서 태그 정책을 강제 적용 가능
- **비용 분석 및 보고서 작성**에 필수

---

## 4.3 모니터링 및 알림 (Monitoring with Alerts, Notifications, and Reports)

- **Billing Alerts**: 예산 초과 시 알림
- **Cost Explorer**: 비용 분석 및 시각화 도구
- **AWS Budgets**: 예산 설정 및 초과 시 알림
- **CloudWatch**: 리소스 사용량 및 비용 모니터링

---

## 4.4 비용 최적화 실천 전략

- **Right Sizing**: 인스턴스 타입/크기 조정
- **Reserved/Spot 활용**: 장기 사용은 예약, 단기/유동적 사용은 스팟 인스턴스 활용
- **Storage 최적화**: S3, EBS, Glacier 등 스토리지 계층별로 데이터 관리

---

## 참고 자료

- [AWS 비용 최적화 공식 문서](https://aws.amazon.com/ko/architecture/cost-optimization/)
- [AWS Cost Explorer](https://docs.aws.amazon.com/ko_kr/cost-management/latest/userguide/ce-what-is.html)
- [AWS Budgets](https://docs.aws.amazon.com/ko_kr/cost-management/latest/userguide/budgets-managing-costs.html)
