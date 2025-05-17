# 4장 실습: Ensuring Cost Optimization

---

## 1. 리소스 태깅 실습

1. **EC2, S3, RDS 등 리소스 생성 시 태그 추가**
   - 예: Key=Project, Value=TestProject
   - 예: Key=Environment, Value=Dev

2. **AWS 콘솔 → Resource Groups → Tag Editor**에서 태그별 리소스 검색 및 관리

---

## 2. 비용 분석 및 예산 설정 실습

1. **AWS 콘솔 → Billing → Cost Explorer**
   - 서비스별, 계정별, 태그별 비용 분석
   - 기간별 비용 추이 그래프 확인

2. **AWS Budgets → Create budget**
   - 월별 예산(예: 10만원) 설정
   - 예산 초과 시 이메일 알림 설정

---

## 3. Billing Alerts 및 알림 설정

1. **Billing → Preferences → Billing alerts** 활성화
2. **CloudWatch → Alarms**에서 비용/사용량 기반 알람 생성

---

## 4. Right Sizing 실습

1. **EC2 → 인스턴스 → 사용률(CloudWatch Metrics) 확인**
2. CPU/메모리 사용률이 낮은 인스턴스는 더 작은 타입으로 변경
3. 필요 없는 인스턴스/볼륨/스냅샷/Elastic IP는 삭제

---

## 5. 예약 인스턴스/스팟 인스턴스 실습

1. **EC2 → Reserved Instances**에서 예약 구매 체험
2. **EC2 → Spot Requests**에서 스팟 인스턴스 생성

---

## 참고 자료

- [AWS 태그 관리 실습](https://docs.aws.amazon.com/ko_kr/general/latest/gr/aws_tagging.html)
- [비용 분석 실습](https://docs.aws.amazon.com/ko_kr/cost-management/latest/userguide/ce-using-cost-explorer.html)
- [AWS Budgets 실습](https://docs.aws.amazon.com/ko_kr/cost-management/latest/userguide/budgets-create.html)
