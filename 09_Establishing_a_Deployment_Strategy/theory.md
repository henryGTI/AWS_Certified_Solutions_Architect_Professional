# 9. Establishing a Deployment Strategy

## 9.1 배포 전략 개요

- **배포 전략**: 새로운 코드, 인프라, 설정을 안전하게 운영 환경에 적용하는 방법
- **무중단 배포(Blue/Green, Canary, Rolling 등)**: 서비스 중단 없이 점진적으로 배포

---

## 9.2 AWS 배포 서비스

- **AWS CodeDeploy**: EC2, Lambda, ECS 등 다양한 환경에 자동 배포
- **AWS Elastic Beanstalk**: 애플리케이션 배포 및 관리 자동화
- **AWS CloudFormation**: 인프라를 코드로 관리(IaC)
- **AWS OpsWorks, App Runner, Copilot, Proton**: 다양한 배포/운영 자동화 도구

---

## 9.3 IaC(Infrastructure as Code)와 배포 자동화

- **CloudFormation, CDK**: 인프라를 코드로 정의, 버전 관리, 자동화
- **StackSets**: 여러 계정/리전에 동시에 배포

---

## 9.4 배포 모니터링 및 롤백

- **배포 상태 모니터링**: CodeDeploy, CloudWatch 등으로 배포 성공/실패 감시
- **자동 롤백**: 배포 실패 시 자동으로 이전 상태로 복구

---

## 참고 자료

- [AWS 배포 전략 공식 문서](https://aws.amazon.com/ko/devops/deploy/)
- [AWS CodeDeploy 공식 문서](https://docs.aws.amazon.com/ko_kr/codedeploy/latest/userguide/welcome.html)
- [AWS CloudFormation 공식 문서](https://docs.aws.amazon.com/ko_kr/AWSCloudFormation/latest/UserGuide/Welcome.html)
