# 8. Meeting Performance Objectives

## 8.1 성능 설계 원칙

- **최신 기술 활용**: 최신 인스턴스, 스토리지, 네트워크 등 사용
- **글로벌 배포**: 여러 리전에 서비스 배포로 지연 최소화
- **서버리스 아키텍처**: Lambda, API Gateway 등 활용
- **실험과 최적화**: 다양한 인스턴스/서비스 조합 실험

---

## 8.2 성능 아키텍처링

- **적합한 인스턴스/스토리지/DB/네트워크 선택**
- **Auto Scaling**: 트래픽에 따라 자동 확장/축소
- **Elastic Load Balancer**: 트래픽 분산
- **CloudFront**: CDN을 통한 정적/동적 콘텐츠 가속

---

## 8.3 모니터링 및 튜닝

- **CloudWatch, X-Ray**: 성능 모니터링 및 병목 탐지
- **지표 기반 튜닝**: CPU, 메모리, 네트워크, 디스크 등 모니터링 후 리소스 조정

---

## 참고 자료

- [AWS 성능 최적화 공식 문서](https://aws.amazon.com/ko/architecture/performance-optimization/)
- [AWS Well-Architected Framework - Performance Efficiency Pillar](https://docs.aws.amazon.com/ko_kr/wellarchitected/latest/performance-efficiency-pillar/welcome.html)
