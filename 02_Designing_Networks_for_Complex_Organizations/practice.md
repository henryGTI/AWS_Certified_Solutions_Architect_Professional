# 2장 실습: Designing Networks for Complex Organizations

---

## 1. VPC 및 서브넷 생성 실습

1. **AWS 콘솔 → VPC 서비스 이동**
2. **VPC 생성**  
   - VPC 이름, IPv4 CIDR 블록(예: 10.0.0.0/16) 입력
3. **서브넷 생성**  
   - 퍼블릭/프라이빗 서브넷 각각 생성 (예: 10.0.1.0/24, 10.0.2.0/24)
4. **인터넷 게이트웨이(IGW) 연결**  
   - IGW 생성 후 VPC에 연결
   - 퍼블릭 서브넷 라우팅 테이블에 IGW 경로 추가

---

## 2. AWS Managed VPN 연결 실습

1. **VPC → VPN Connections → Create VPN Connection**
2. Customer Gateway(온프레미스 라우터 정보) 등록
3. Virtual Private Gateway(VGW) 생성 및 VPC에 연결
4. VPN 연결 생성 후, 구성 파일을 다운로드하여 온프레미스 라우터에 적용

---

## 3. Direct Connect(DX) 시나리오 이해

- 실제 실습은 어렵지만, DX 콘솔에서 가상으로 Connection 생성 과정을 체험해볼 수 있음
- DX Location, Virtual Interface(VIF) 생성, 라우팅 구성 등 확인

---

## 4. VPC 엔드포인트 생성 실습

1. **VPC → Endpoints → Create Endpoint**
2. 서비스 선택 (예: S3)
3. VPC, 서브넷, 보안그룹 선택
4. 엔드포인트 생성 후, S3에 프라이빗 네트워크로 접근 가능한지 확인

---

## 5. Transit Gateway 실습

1. **VPC → Transit Gateways → Create Transit Gateway**
2. Transit Gateway Attachment로 여러 VPC 연결
3. 라우팅 테이블 구성
4. 각 VPC에서 통신이 되는지 확인

---

## 6. Storage Gateway 실습(이론+체험)

- Storage Gateway 콘솔에서 File Gateway, Volume Gateway, Tape Gateway 생성 과정 체험
- 온프레미스 서버와 연동하는 시나리오를 이해

---

## 참고 자료

- [VPC 실습 가이드](https://docs.aws.amazon.com/ko_kr/vpc/latest/userguide/vpc-getting-started.html)
- [VPN 실습 가이드](https://docs.aws.amazon.com/ko_kr/vpn/latest/s2svpn/VPC_VPN.html)
- [VPC 엔드포인트 실습](https://docs.aws.amazon.com/ko_kr/vpc/latest/privatelink/vpc-endpoints.html)
