# 🔎 RFM Analysis for customer segmentation 📦
> RFM Analysis for customer segmentation based on transaction data

</br>

포스코 AI/Big Data 아카데미에서 진행한 프로젝트입니다.

회원제 유통 매장의 매출 증대를 위한 데이터 분석 프로젝트입니다.

RFM(최근 방문일, 방문 빈도, 소비 규모)를 이용하여 고객 세분화를 진행하고 연관 규칙 및 word2vec을 이용하여 연관 제품 추천 서비스를 제공합니다.

</br>

### 👪 1 ) RFM을 이용한 고객 세분화
```jsx
" 6개월동안 3일에 한 번 씩 방문해서 매번 2만원 이상씩 소비한 당신은 충성 고객 ! "

행복 그린 매장에 방문하는 고객들의 최근 방문일(Recency), 방문 빈도(Frequency), 소비 규모(Monetary)를 탐색하여 다음 두 목표를 달성한다.

1. 새로운 등급 체계를 만든다.
	기존의 등급 분류가 고객 가치를 제대로 반영하지 못하고 있음을 밝히고,
  새로운 등급 기준을 마련하여 고객의 충성도에 따라 적절한 혜택을 제공할 수 있도록 한다.

2. 패턴에 따라 고객을 분류한다.
	RFM 점수를 이용하여 <자주 방문하지만 큰 금액을 쓰지 않는 고객군>, <충성 고객이었으나 이탈한 고객군>, <관심을 갖기 시작한 신규 고객군> 등으로 고객을 분류하고,
	고객들의 행동 패턴에 따라 충성 전환 정책 / 이탈 방지 정책을 수립한다.
```

</br>

#### Note
* RFM 분석을 위한 class를 만들었습니다. 기능은 아래와 같습니다.
  > R,F,M을 가중합 하는 방법은 다양합니다. 해당 분석에서는 매출 기여도를 고려하여 가중치를 계산하였습니다.
  1. 고객별 Recency, Frequency, Monetary를 계산합니다.
  2. 각 class별 매출 기여도를 계산합니다.
  3. 매출 기여도를 기반으로 R,F,M별 가중치를 계산합니다.
  4. R,F,M의 가중합을 이용하여 등급을 분류합니다.
  5. R,F,M 각각을 고려하여 K-means clustering을 실시합니다.

</br>

#### Reference
* RFM에서등급 부여 방법에관한 연구(류귀열, 문영수/2013)

</br>

### 🛒 **2 ) 제품 추천 서비스**
```jsx
" 50대 여성들이 생콩가루와 두부를 많이 사는 이유는 무엇일까? "
연관 규칙을 통해 50대 여성이 생콩가루와 두부를 함께 자주 사고 있음을 파악하고, < 된장찌개를 위한 재료만 모았어요. > 와 같은 묶음 상품 판매 전략에 이용한다.

" 김과 돈까스 소스, 과자를 같이 산 당신 ! 혹시 소풍을 계획하고 있지 않나요? "
word2vec을 통해 함께 자주 담기는 식품을 파악하고, 묶음 상품과 프로모션 전략에 이용한다.

" 우유와 요구르트는 가까운 위치에 진열하자. "
word2vec을 통해 함께 자주 담기는 식품을 파악하고 매장 진열에 반영한다.
```
</br>

### 🙋🏻‍♀️ 역할

- 고객 분류 방법과 관련된 논문 탐색 및 구현
- 고객 등급 재분류를 위한 새로운 모델 탐색 및 구현
- 연관 분석/word2vec을 이용한 상품 추천 서비스 구현

</br>

### 🔑 사용 기술 관련 키워드

- K-means Clustering
- Association rule
- item2Vec
- Decision Tree

</br>

### 💻 개발 환경

- 사용 언어 : Python3
- 개발 환경 : Jupyter Notebook, Colab Pro, Linux
- 진행 기간 : 2020.02.19 ~ 2020.05.06
    - 해당 프로젝트는 코로나로 인하여 2월 24일부터 중단 되었다가 4월 28일부터 온라인으로 재개되었습니다.

</br>

 ### 🔍 더 자세한 설명 보러가기

분석을 하며 만났던 문제와 생각을 자세히 담았습니다. [고객 평가 지표, RFM 분석하기](https://www.notion.so/RFM-f1cd6f2358554772aff723a085832708)
