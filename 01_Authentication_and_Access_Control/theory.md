# 1. Authentication and Access Control (인증 및 접근 제어)

## 1.1 IAM(Identity and Access Management) 개요

### IAM이란?
- **IAM(Identity and Access Management)**는 AWS에서 사용자와 권한을 관리하는 핵심 서비스입니다.
- AWS 리소스(EC2, S3, RDS 등)에 누가, 어떤 권한으로 접근할 수 있는지 제어합니다.

### IAM의 주요 구성요소
- **User(사용자)**: AWS 리소스에 접근하는 실제 사람 또는 애플리케이션. 각 사용자마다 고유한 자격증명(Access Key, Password 등)을 가짐.
- **Group(그룹)**: 여러 사용자를 묶어서 동일한 권한을 부여. 예) 개발자 그룹, 운영자 그룹 등.
- **Role(역할)**: AWS 서비스나 외부 사용자에게 임시로 권한을 부여. 예) EC2 인스턴스에 S3 접근 권한을 주는 역할.
- **Policy(정책)**: JSON 형식의 문서로, 어떤 리소스에 어떤 작업을 허용/거부할지 정의.

### IAM의 특징
- **Root 계정**: AWS 계정 생성 시 만들어지는 최고 권한 계정. 실제 운영에서는 사용을 최소화하고, 별도의 IAM 사용자로 작업하는 것이 보안상 안전.
- **최소 권한 원칙(Least Privilege Principle)**: 꼭 필요한 권한만 부여하는 것이 보안의 기본.

---

## 1.2 인증(Authentication)과 인가(Authorization)

- **인증(Authentication)**: 사용자가 누구인지 확인하는 과정. (예: ID/PW, MFA)
- **인가(Authorization)**: 인증된 사용자가 어떤 리소스에 어떤 작업을 할 수 있는지 결정. (예: S3 읽기/쓰기 권한)

---

## 1.3 MFA(Multi-Factor Authentication)

- **MFA**는 2단계 인증으로, 비밀번호 외에 추가 인증(OTP 등)을 요구하여 보안을 강화합니다.
- 루트 계정, 관리자 계정 등 중요 계정에는 반드시 MFA를 활성화해야 합니다.

---

## 1.4 정책(Policy) 종류

- **Identity-based Policy**: 사용자, 그룹, 역할에 직접 연결하는 정책.
- **Resource-based Policy**: S3, Lambda 등 리소스에 직접 연결하는 정책. (예: S3 버킷 정책)
- **Session Policy**: 임시 세션에 부여하는 정책. (STS 사용 시)

#### 정책 예시 (S3 ReadOnly)
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::example-bucket/*"
    }
  ]
}
```

---

## 1.5 RBAC vs ABAC

- **RBAC(Role-Based Access Control)**: 역할(예: Admin, Developer)에 따라 권한을 부여.
- **ABAC(Attribute-Based Access Control)**: 태그(부서, 프로젝트 등)와 같은 속성에 따라 권한을 부여.  
  예) `Department=Finance` 태그가 있는 리소스만 접근 허용.

---

## 1.6 액세스 위임(Delegation)

- **Cross-Account Access**: 다른 AWS 계정의 리소스에 접근할 때 역할(AssumeRole) 사용.
- **Temporary Credentials**: AWS STS(Security Token Service)를 통해 임시 자격증명 발급.

---

## 1.7 AWS Directory Service

- 온프레미스 Microsoft AD와 연동하거나, AWS에서 관리형 AD를 제공.
- SSO(Single Sign-On), 사용자 인증, 그룹 관리 등 엔터프라이즈 환경에서 유용.

---

## 참고 자료

- [IAM 공식 문서](https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/introduction.html)
- [IAM Policy Generator](https://awspolicygen.s3.amazonaws.com/policygen.html)
