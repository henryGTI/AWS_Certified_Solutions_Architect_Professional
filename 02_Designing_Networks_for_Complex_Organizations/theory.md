# 2. Designing Networks for Complex Organizations

## 2.1 VPN 연결 구축

- **AWS Managed VPN**: AWS에서 제공하는 관리형 VPN 서비스로, 온프레미스와 AWS VPC를 안전하게 연결.
- **AWS VPN CloudHub**: 여러 지사(브랜치)와 AWS를 연결할 때 사용.
- **Software VPN**: 오픈소스 또는 서드파티 VPN 소프트웨어를 EC2에 설치해 직접 운영.

---

## 2.2 AWS Direct Connect(DX) 소개

- **AWS Direct Connect**: 온프레미스 데이터센터와 AWS를 전용선으로 직접 연결하여, 네트워크 지연 감소 및 대역폭 증가.
- **Dedicated Connection**: 전용 물리 회선.
- **Hosted Connection/Hosted VIF**: 파트너를 통한 공유 회선.
- **DX의 장점**: 보안, 일관된 네트워크 성능, 대용량 데이터 전송에 유리.

---

## 2.3 AWS Storage Gateway 소개

- 온프레미스와 AWS 간 데이터 연동을 위한 하이브리드 스토리지 서비스.
- **File Gateway**: 파일을 S3에 저장.
- **Volume Gateway**: 블록 스토리지 형태로 사용.
- **Tape Gateway**: 백업 테이프를 클라우드로 대체.

---

## 2.4 VPC 엔드포인트 활용

- **Interface Endpoint**: 프라이빗 IP로 AWS 서비스에 접근.
- **Gateway Endpoint**: S3, DynamoDB 등 특정 서비스에 대한 프라이빗 접근.
- **GWLB Endpoint**: Gateway Load Balancer와 연동.
- 엔드포인트를 활용하면 인터넷을 거치지 않고 AWS 서비스에 안전하게 접근 가능.

---

## 2.5 AWS Transit Gateway 소개

- 여러 VPC, 온프레미스 네트워크를 중앙에서 연결·관리하는 서비스.
- **Transit Gateway**를 통해 네트워크 토폴로지 단순화, 확장성 및 관리 효율성 향상.

---

## 2.6 네트워크 설계 시 고려사항

- **Resiliency(복원력)**: 장애 발생 시 자동 복구, 이중화 설계.
- **Quotas(제한)**: VPC, 서브넷, 라우팅 등 AWS 리소스 한도.
- **AZ(가용영역) 및 Pricing(비용)**: 네트워크 구성에 따른 비용 최적화.

---

## 참고 자료

- [AWS VPC 공식 문서](https://docs.aws.amazon.com/ko_kr/vpc/latest/userguide/what-is-amazon-vpc.html)
- [AWS Direct Connect 공식 문서](https://docs.aws.amazon.com/ko_kr/directconnect/latest/UserGuide/Welcome.html)
- [AWS Transit Gateway 공식 문서](https://docs.aws.amazon.com/ko_kr/vpc/latest/tgw/what-is-transit-gateway.html)
