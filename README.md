# Real Estate Frameworks

한국 부동산 의사결정을 위한 메타 라우터 + 프레임워크 컬렉션.

학계 이론(Hedonic, DiPasquale-Wheaton, Alonso-Muth-Mills), 투자 분석(Cap Rate/DCF, Harrison 18.6년 사이클, Highest & Best Use), 한국 제도 프레임워크(재건축 사업성, 청약 가점제, 갭투자 구조)를 하나의 라우팅 레이어 아래에 묶는다.

## 설계 원칙

1. **영어권 이론을 한국 시장 맥락으로 번역** — 이론 복붙 금지. 전세 제도, 청약 규제, 재건축 절차 등 한국 특수 요인이 반영돼야 함.
2. **리테일 투자자 직감과 학계 실증 사이의 다리** — "불패 신화" vs "일본화 논리" 같은 서사가 아니라 데이터와 제도로 판단.
3. **의사결정 보조 도구** — 정답 자판기가 아니라 사고 프레임 제공.

## 구조

```
real-estate-frameworks/
├── SKILL.md               # 메타 라우터 — 상황 → 프레임워크 선택
├── hedonic-pricing/       # 속성별 가격 분해
├── dipasquale-wheaton/    # 4분면 모델 (임대·자산·건설·재고)
├── alonso-muth-mills/     # 도심 접근성 vs 가격
├── cap-rate-dcf/          # 수익형 가치 평가
├── harrison-cycle/        # 18.6년 부동산 사이클
├── highest-best-use/      # 최유효이용 원칙
├── redevelopment-feasibility/  # 재건축 사업성 (비례율·분담금)
├── subscription-points/   # 청약 가점제 전략
└── gap-investment/        # 전세 레버리지 구조
```

## 사용

```
/real-estate <상황 설명>
```

메타 라우터가 문제를 분류하고, 관련 프레임워크(들)를 호출하여 분석을 합성한다.

## 면책

이 레포는 의사결정 보조 도구이며 투자 자문이 아니다. 실제 거래 전 전문가 검토를 거칠 것.
