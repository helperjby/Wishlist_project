[![image](https://user-images.githubusercontent.com/95989232/166428931-1ee9948f-cc1c-42a2-b0a9-47dae9b8b90d.png)](https://www.kaggle.com/competitions/instacart-market-basket-analysis/overview)

## 🛒위시리스트 팀 소개
|팀원|역할|
|---|:---:|
|박산들|데이처 전처리|
|김아네스||
|장병용|EDA|
|정경환|모델링|

<br/>

## 일정표
|단계|내용|M1|M2|H1|H2|H3|H4|H5|H6|  
|:---:|:-----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|  
|1|에자일 소다 OT|☑️|☑️|◾|◾|◾|◾|◾|◾|  
|2|주제 및 계획 설정|◾|☑️|☑️|◾|◾|◾|◾|◾|  
|3|데이터 구성 및 EDA|◾|◾|☑️|☑️|☑️|◾|◾|◾|   
|4|모델 개발|◾|◾|◾|◾|☑️|☑️|☑️|◾|   
|5|최종 보고|◾|◾|◾|◾|◾|◾|◾|☑️|

<br/>

## 프로젝트 소개

Instacart는 미국과 캐나다에서 웹과 앱을 통해 식료품 배달과 픽업 서비스를 운영하는 미국 회사입니다. instacart에서 제공한 익명화 된 고객의 구매내역 데이터를 기반으로 다시 주문할 제품을 예측하는 모델을 개발합니다.

<br/>

## 목표
### 정량적 목표
- 캐글 리더보드 점수 0.40311 이상 달성
### 정성적 목표
- 제공된 데이터 분석
- 더 나은 교차 판매 및 상향 판매를 위한 제품 간의 연관성 찾기
- 타겟 마케팅을 위한 고객 세분화 수행 및 고객 행동 예측
- 고객 주문에 대한 익명 데이터를 사용하여 이전에 구매한 제품이 사용자의 다음 주문목록에 포함될지를 예측하는 최적의 모델을 개발

<br/>

## [데이터 설명](https://www.kaggle.com/competitions/instacart-market-basket-analysis/data)

- aisles: 제품의 소 분류가 총 134개 나열되어 있습니다.
- Departments: 이 파일에는 제품의 대 분류가 총 21개 나열되어 있습니다.
- orders: 이 파일에는 총 206209명의 사용자가 주문한 총 3421083개의 주문이 있습니다.
    - Order_number: 고객별 주문 횟수는 0에서 100까지입니다.
    - Order_dow(day of week): 0, 1, 2, 3, 4, 5, 6이 각각 토일월화수목금으로 매핑할 수 있습니다. 토요일과 일요일 주문이 다수를 차지합니다.
    - Order_hour_of_day: 대부분의 주문은 낮 시간에 이루어집니다.
    - Days_since_prior_order: 이전 주문 이후 경과 일수를 보면 7, 14, 21, 30이 많으므로 일주일에 한 번 주문하는 추이를 보입니다.
    - '요일'과 '시간' 사이의 히트맵을 기반으로 하면 토요일 오후와 일요일 오전이 주문이 가장 많은 시간이라고 말할 수 있습니다.
- order_products_prior: 이 파일은 주문한 제품과 장바구니에 추가된 순서에 대한 정보를 제공하며 제품이 재 주문 되었는지 여부도 알려줍니다. 이 파일에는 총 49677개의 제품이 주문된 총 3214874개의 주문 정보가 있습니다.
- order_products_train: order_products_prior파일과 마찬가지로 주문한 제품과 장바구니에 추가된 순서에 대한 정보와 제품이 재 주문 되었는지 여부를 알려줍니다. 이 파일에는 총 39123개의 제품이 주문된 총 131209개의 주문 정보가 있습니다.
- Products: 이 파일에는 총 49688개의 제품 목록과 해당 카테고리 및 부서가 포함되어 있습니다. 다른 카테고리와 다른 부서에 있는 제품의 수는 다릅니다.

<br/>

## 탐색적 데이터 분석

[링크](https://github.com/Agile-Soda-Instacart-Team/Wishlist/blob/main/EDA/EDA_wishlist.ipynb)

<br/>

## ML 모델

대용량 데이터를 처리하고 병렬화할 수 있으며 변수 중요도를 제공하는 XGBoost모델을 선정하였습니다. 성능지표는 F1 score를 사용합니다.
