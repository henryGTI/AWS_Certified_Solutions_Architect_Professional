# 1장 실습: Authentication and Access Control

## 1. IAM 사용자 생성

1. AWS 콘솔 → IAM → Users → Add users
2. 사용자 이름 입력, 프로그래밍/콘솔 접근 선택
3. 권한 부여(기존 그룹, 직접 정책 연결 등)
4. 태그 입력(선택)
5. 생성 완료 후 Access Key/Secret Key 저장

---

## 2. IAM 그룹 및 역할 생성

- 그룹 생성: 여러 사용자에게 동일 권한 부여
- 역할 생성: EC2, Lambda 등 서비스에 권한 위임

---

## 3. 정책 작성 및 연결

- AWS 관리형 정책 사용 또는 직접 정책(JSON) 작성
- 예시: S3 ReadOnly, EC2 FullAccess 등

---

## 4. MFA 활성화

1. 사용자 선택 → Security credentials → MFA 활성화
2. 가상 MFA 앱(구글 OTP 등)으로 QR코드 스캔
3. 2회 인증코드 입력 후 활성화

---

## 5. S3 버킷 접근 제어 실습

- 특정 사용자/그룹만 S3 버킷 접근 가능하도록 정책 연결
- 리소스 기반 정책(Resource-based Policy) 실습

---

## 6. Cross-Account Access 실습

- 계정 A에서 역할 생성(신뢰할 계정 B 지정)
- 계정 B에서 역할 Assume Role로 접근

---

## 참고 자료

- [IAM 실습 가이드](https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/getting-started_create-admin-group.html)
