# 3장 실습: Designing a Multi-Account AWS Environment

---

## 1. AWS Organizations 생성 및 계정 추가

1. **AWS 콘솔 → AWS Organizations 서비스 이동**
2. **Create organization** 클릭 (기존에 없을 경우)
3. **Organizational Unit(OU) 생성**  
   - 예: Dev, Prod, Test 등
4. **계정 추가**  
   - OU별로 새 계정 생성 또는 기존 계정 초대

---

## 2. Service Control Policies(SCP) 적용 실습

1. **AWS Organizations → Policies → Service Control Policies**
2. **Create policy** 클릭, 정책 작성  
   - 예: S3 생성 금지 정책
   ```json
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Deny",
         "Action": "s3:CreateBucket",
         "Resource": "*"
       }
     ]
   }
   ```
3. 정책을 OU 또는 계정에 연결

---

## 3. Control Tower 체험

1. **AWS 콘솔 → Control Tower 서비스 이동**
2. **Set up landing zone** 클릭
3. 기본 OU, 계정, 네트워크, 감사 계정 등이 자동으로 생성되는 과정 체험

---

## 4. 결제 및 비용 관리 실습

1. **Billing → Cost Explorer**에서 계정별 비용 확인
2. **Billing alerts** 설정  
   - 예: 월별 10만원 초과 시 이메일 알림

---

## 5. 리소스 공유 실습 (AWS Resource Access Manager)

1. **AWS RAM → Create resource share**
2. 공유할 리소스(VPC, Subnet 등) 선택
3. 공유 대상 계정 또는 OU 지정

---

## 참고 자료

- [AWS Organizations 실습 가이드](https://docs.aws.amazon.com/ko_kr/organizations/latest/userguide/orgs_manage_policies_scps.html)
- [Control Tower 실습 가이드](https://docs.aws.amazon.com/ko_kr/controltower/latest/userguide/getting-started-with-control-tower.html)
