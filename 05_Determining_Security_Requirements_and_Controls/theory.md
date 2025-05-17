# 5. Determining Security Requirements and Controls

## 5.1 보안 요구사항 및 제어의 중요성

- 클라우드 환경에서는 데이터, 네트워크, 인프라, 접근 권한 등 다양한 보안 위협에 노출될 수 있음
- AWS는 보안의 책임 공유 모델(Shared Responsibility Model)을 적용  
  - AWS: 인프라 보안 책임  
  - 고객: 데이터, 접근, 애플리케이션 보안 책임

---

## 5.2 IAM을 통한 신원 및 접근 관리

- **IAM Users, Groups, Roles**: 최소 권한 원칙 적용
- **정책(Policy)**: 리소스별 세밀한 권한 제어
- **MFA**: 중요 계정에 다중 인증 적용

---

## 5.3 인프라 보호

- **네트워크 보안**: VPC, 서브넷, 보안그룹, NACL로 접근 제어
- **AWS WAF, Shield**: 웹 애플리케이션 방어, DDoS 방어
- **Vulnerability Assessment**: Inspector, GuardDuty 등으로 취약점 탐지

---

## 5.4 데이터 보호

- **암호화**: S3, EBS, RDS 등 저장 데이터(At Rest) 및 전송 데이터(In Transit) 암호화
- **AWS KMS, CloudHSM**: 키 관리 및 하드웨어 보안 모듈
- **데이터 분류 및 접근 제한**: 민감 데이터 식별 및 접근 제어

---

## 5.5 로그 및 모니터링

- **CloudTrail**: API 호출 기록 및 감시
- **CloudWatch Logs**: 시스템/애플리케이션 로그 수집
- **Config**: 리소스 변경 추적

---

## 5.6 사고 대응 및 복구

- **Incident Response**: 보안 사고 발생 시 신속한 탐지, 분석, 대응
- **백업 및 복구**: 정기 백업, DR(Disaster Recovery) 전략 수립

---

## 참고 자료

- [AWS 보안 모범 사례](https://docs.aws.amazon.com/ko_kr/securityhub/latest/userguide/securityhub-standards-fsbp.html)
- [AWS KMS 공식 문서](https://docs.aws.amazon.com/ko_kr/kms/latest/developerguide/overview.html)
- [AWS Incident Response](https://aws.amazon.com/ko/security/incident-response/)
