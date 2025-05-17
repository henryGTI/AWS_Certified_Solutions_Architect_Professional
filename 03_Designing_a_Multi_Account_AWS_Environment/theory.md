# 3. Designing a Multi-Account AWS Environment for Complex Organizations

## 3.1 멀티 계정 환경의 필요성

- 대규모 조직에서는 보안, 비용, 리소스 분리, 거버넌스 강화를 위해 여러 AWS 계정을 운영하는 것이 일반적입니다.
- 계정별로 프로젝트, 부서, 환경(개발/운영/테스트) 등을 분리하여 관리할 수 있습니다.

---

## 3.2 리소스 및 결제 분리 전략

### Elements of Structure
- **Organization**: AWS Organizations를 통해 계정들을 중앙에서 관리
- **OU(Organizational Unit)**: 계정들을 논리적으로 그룹화
- **Account**: 실제 AWS 리소스가 배치되는 단위
- **VPC/Subnet**: 네트워크 분리

### Resource Isolation
- 각 계정은 독립적으로 리소스를 소유하므로, 보안 및 장애 격리가 용이

### Billing Isolation
- 계정별로 비용을 분리하여 청구 가능
- Consolidated Billing(통합 결제)로 전체 비용을 한 번에 관리할 수도 있음

---

## 3.3 AWS Organizations 소개

- 여러 AWS 계정을 중앙에서 생성, 관리, 정책 적용, 결제 통합이 가능한 서비스
- **Service Control Policies(SCPs)**: 계정/OU 단위로 권한 제한 정책 적용 가능
- **Tag Policies, Backup Policies** 등 다양한 거버넌스 정책 제공

---

## 3.4 Control Tower

- 멀티 계정 환경을 자동화/표준화하여 손쉽게 구축할 수 있는 서비스
- 계정 생성, OU 구성, 기본 보안/감사/네트워크 환경 자동 설정

---

## 3.5 결제 전략

- **One Bill or Multiple Bills**: 통합 결제(Consolidated Billing) vs. 개별 결제
- **Billing Alerts**: 비용 초과 시 알림 설정

---

## 3.6 멀티 계정 환경 설계 시 고려사항

- 계정/OU 구조 설계
- 보안 및 권한 위임(Delegated Admin)
- 리소스 공유(AWS Resource Access Manager)
- 거버넌스 및 정책 적용(SCP, Tag Policy 등)

---

## 참고 자료

- [AWS Organizations 공식 문서](https://docs.aws.amazon.com/ko_kr/organizations/latest/userguide/orgs_introduction.html)
- [AWS Control Tower 공식 문서](https://docs.aws.amazon.com/ko_kr/controltower/latest/userguide/what-is-control-tower.html)
