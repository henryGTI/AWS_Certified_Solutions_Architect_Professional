# 5장 실습: Determining Security Requirements and Controls

---

## 1. IAM 최소 권한 실습

1. **IAM → Users → 사용자 생성**
2. **정책 연결**: 필요한 권한만 부여 (예: S3 ReadOnly)
3. **MFA 활성화**: Security credentials → MFA 활성화

---

## 2. 네트워크 보안 실습

1. **VPC → Security Groups**  
   - 인바운드/아웃바운드 규칙 설정 (예: 80, 443 포트만 허용)
2. **NACL(Network ACL)**  
   - 서브넷 단위로 접근 제어 규칙 추가

---

## 3. 데이터 암호화 실습

1. **S3 버킷 생성 시 암호화 활성화**
   - Default encryption: SSE-S3 또는 SSE-KMS 선택
2. **EBS 볼륨 생성 시 암호화 활성화**
3. **RDS 인스턴스 생성 시 암호화 옵션 선택**

---

## 4. KMS 키 생성 및 사용 실습

1. **KMS → Customer managed keys → Create key**
2. 키 별칭, 설명, 관리자/사용자 지정
3. S3, EBS 등 리소스 암호화에 해당 KMS 키 사용

---

## 5. CloudTrail 및 CloudWatch Logs 실습

1. **CloudTrail → Trail 생성**
   - 모든 리전, 모든 S3 버킷에 대한 이벤트 기록
2. **CloudWatch Logs → 로그 그룹 생성**
   - EC2, Lambda 등에서 로그 전송 및 모니터링

---

## 6. GuardDuty, Inspector 실습

1. **GuardDuty 활성화**: 위협 탐지 및 경고 확인
2. **Inspector 활성화**: EC2 인스턴스 취약점 평가

---

## 7. 사고 대응 시나리오 체험

1. **IAM 사용자 비정상 접근 감지**: CloudTrail에서 이벤트 확인
2. **비정상 리소스 생성/삭제 탐지**: 알람 설정 및 대응

---

## 참고 자료

- [IAM 실습 가이드](https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/getting-started_create-admin-group.html)
- [KMS 실습 가이드](https://docs.aws.amazon.com/ko_kr/kms/latest/developerguide/create-keys.html)
- [CloudTrail 실습 가이드](https://docs.aws.amazon.com/ko_kr/awscloudtrail/latest/userguide/cloudtrail-create-and-update-a-trail.html)
