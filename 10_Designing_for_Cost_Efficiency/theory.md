# 10. Designing for Cost Efficiency

## 10.1 AWS 요금 모델 이해

- **온디맨드(On-Demand)**: 사용한 만큼만 비용 지불, 유연하지만 단가가 높음
- **예약(Reserved)**: 1년/3년 약정으로 할인, 장기 사용에 적합
- **스팟(Spot)**: 미사용 자원을 경매 방식으로 저렴하게 사용, 중단 가능성 있음
- **Savings Plans**: 일정 사용량 약정 시 할인

---

## 10.2 비용 효율적 설계 전략

- **Right Sizing**: 리소스 크기/타입을 실제 사용량에 맞게 조정
- **Auto Scaling**: 트래픽에 따라 자동으로 리소스 증감
- **스토리지 계층화**: S3, Glacier 등 데이터 특성에 맞는 스토리지 사용
- **비용 모니터링 및 최적화**: Cost Explorer, Budgets, Trusted Advisor 활용

---

## 참고 자료

- [AWS 요금 모델 공식 문서](https://aws.amazon.com/ko/pricing/)
- [AWS 비용 최적화 가이드](https://aws.amazon.com/ko/architecture/cost-optimization/)
