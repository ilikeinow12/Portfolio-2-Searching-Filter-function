# <상품 필터 기능 추가 제안서> 

**1) 포트폴리오 소개/ 분석 목적**
w*** 쇼핑몰에서 유저가 구매를 원하는 상품의 정보를 미리 받아 해당 상품을 필터로 걸러주거나 랜덤으로 추천해주는 기능 제안

**2) 문제 제기**
- w*** 쇼핑몰의 화장품군 상품 노출의 비효율성 : 가장 인기가 많은 5개 내외의 상품만 지속적으로 노출됨 = 다양한 상품이 노출되고 있지 않음.
- w***  최근 화장품 분야로 사업을 대폭 확장중인 것으로 파악되는데, 기대 이상의 효과를 가지기 위해서는 더 정교한 상품 노출이 필요할 것으로 사료됨
- 다른 상품들과 달리 화장품의 경우 유저의 바람대로 상품을 특정하는 것이 중요함. 따라서 미리 유저의 바람을 파악하고 이에 맞추어 상품을 노출시킨다면 유저의 상품 구매 만족도는 올라가고 화장품 매출 또한 증가할 것으로 파악됨

**3) 분석 과정**  
**데이터의 수집 : 웹크롤링**
- 크롤링(1) : 각 화장품의 id, 이름, 브랜드명, 가격, 리뷰수
- 크롤링(2) : 각 화장품의 리뷰 페이지에서 리뷰를 남긴 유저들의 피부타입과 상품의 발림성, 자극도, 향, 끈적임에 대한 평가항목
 
**데이터의 분석 : 비지도, 지도학습 머신러닝**
- 상품 Clustering : 수집한 유저의 피부타입, 화장품의 발림성, 자극도 등을 KMeans를 통해 총 5개의 유형으로 군집화
- 추천 알고리즘에 적합한 예측모델 선정 : 위에서 얻은 table을 여러 지도학습 머신러닝에 넣어 가장 적합한 예측 모델 선정
- 임의의 유저 정보(X)를 넣어 모델 최종 확인 : 임의의 유저를 설정하여 피부타입, 유저가 원하는 상품의 발림성, 자극도 등을 넣어 해당되는 군집의 상품을 랜덤으로 추천

**4) 분석 결론**
화장품의 경우 많은 유저들이 자신의 피부타입에 맞춰서 구매하고 화장품의 질감이나 자극도 등을 꼼꼼하게 따지는 경향이 강함. 따라서 미리 유저가 자신의 정보를 주게끔 유도해서 그에 맞춰 상품군을 추천한다면 기초화장품군의 판매 증가를 기대해볼 수 있음


