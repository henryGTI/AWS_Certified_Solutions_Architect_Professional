# 14. Improving Security

## 14.1 보안 취약점 평가

- **AWS Inspector, GuardDuty**: 취약점 및 위협 탐지
- **최소 권한 원칙**: IAM 정책, SCP 등으로 권한 최소화

---

## 14.2 비밀 및 자격증명 관리

- **AWS Secrets Manager, Parameter Store**: 비밀번호, API 키 등 안전하게 저장/관리
- **정기적 회전(rotate)**: 자격증명 주기적 변경

---

## 14.3 데이터 보호

- **암호화**: S3, EBS, RDS 등 저장 및 전송 데이터 암호화
- **접근 제어**: S3 버킷 정책, 보안 그룹 등

---

## 14.4 보안 이벤트 대응

- **CloudTrail, CloudWatch Logs**: 이벤트 기록 및 모니터링
- **자동화된 대응**: Lambda, SNS 등으로 자동 알림/조치

---

## 참고 자료

- [AWS 보안 모범 사례](https://docs.aws.amazon.com/ko_kr/securityhub/latest/userguide/securityhub-standards-fsbp.html)
