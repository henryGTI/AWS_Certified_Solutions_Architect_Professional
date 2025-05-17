# 1장 실습: Authentication and Access Control

## 1. IAM 사용자 생성 실습

1. **AWS 콘솔 접속** → 상단 검색창에 `IAM` 입력 후 이동
2. **Users** → **Add users** 클릭
3. **User name** 입력 (예: testuser)
4. **Access type** 선택  
   - AWS Management Console access (콘솔 로그인)
   - Programmatic access (API/CLI 접근)
5. **Permissions**  
   - 기존 그룹에 추가하거나, 직접 정책 연결
   - 예시: `AmazonS3ReadOnlyAccess` 정책 연결
6. **Tags** (선택)
7. **Review** → **Create user**
8. **Access Key/Secret Key**는 안전하게 저장

---

## 2. IAM 그룹 및 역할 생성 실습

### 그룹 생성
1. **IAM → User groups → Create group**
2. 그룹 이름 입력 (예: Developers)
3. 정책 연결 (예: `AmazonEC2FullAccess`)
4. 사용자 추가

### 역할 생성
1. **IAM → Roles → Create role**
2. 신뢰할 엔터티 선택 (예: AWS 서비스 - EC2)
3. 정책 연결 (예: `AmazonS3FullAccess`)
4. 역할 이름 입력 및 생성

---

## 3. 정책 작성 및 연결 실습

1. **IAM → Policies → Create policy**
2. **Visual editor** 또는 **JSON** 탭에서 정책 작성
3. 예시: S3 특정 버킷 ReadOnly 정책
4. 정책 이름 입력 후 생성
5. 사용자/그룹/역할에 정책 연결

---

## 4. MFA 활성화 실습

1. **IAM → Users → 사용자 선택 → Security credentials**
2. **Assigned MFA device → Manage** 클릭
3. **가상 MFA 디바이스** 선택 (예: Google Authenticator)
4. QR코드 스캔 → 앱에서 생성된 코드 2회 입력
5. MFA 활성화 완료

---

## 5. S3 버킷 접근 제어 실습

1. **S3 → 버킷 선택 → Permissions → Bucket policy**
2. 특정 사용자/그룹만 접근 가능하도록 정책 작성
3. 예시 정책:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Principal": "*",
      "Action": "s3:*",
      "Resource": "arn:aws:s3:::example-bucket/*",
      "Condition": {
        "StringNotEquals": {
          "aws:username": "testuser"
        }
      }
    }
  ]
}
```

---

## 6. Cross-Account Access 실습

### 계정 A (리소스 소유 계정)
1. **IAM → Roles → Create role**
2. 신뢰할 계정에 계정 B의 Account ID 입력
3. 필요한 정책 연결 (예: S3 FullAccess)
4. 역할 이름 입력 및 생성

### 계정 B (접근 계정)
1. **IAM → Users → 사용자 선택 → Add permissions → Add inline policy**
2. `sts:AssumeRole` 권한 부여
3. AWS CLI에서 아래 명령어로 역할 Assume
```bash
aws sts assume-role --role-arn arn:aws:iam::<AccountA_ID>:role/<RoleName> --role-session-name testsession
```

---

## 참고 자료

- [IAM 실습 가이드](https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/getting-started_create-admin-group.html)
