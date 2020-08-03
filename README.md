# RFM Analysis for customer segmentation
> RFM Analysis for customer segmentation based on transaction data

### RFM이란?
* 최근 방문일(Recency), 방문 빈도(Frequency), 소비 규모(Monetray)를 고려하여 고객의 가치를 판단/분석하는 방법입니다.

### Note
* 회원제 유통 매장의 transaction data를 기반으로 RFM 분석을 실시합니다.
* RFM 분석을 위한 class를 만들었습니다. 기능은 아래와 같습니다.

  > R,F,M을 가중합 하는 방법은 다양합니다. 해당 분석에서는 매출 기여도를 고려하여 가중치를 계산하였습니다.
  1. 고객별 Recency, Frequency, Monetary를 계산합니다.
  2. 각 class별 매출 기여도를 계산합니다.
  3. 매출 기여도를 기반으로 R,F,M별 가중치를 계산합니다.
  4. R,F,M의 가중합을 이용하여 등급을 분류합니다.
  5. R,F,M 각각을 고려하여 K-means clustering을 실시합니다.
  
  
 ### Reference
 * RFM에서등급 부여 방법에관한 연구(류귀열, 문영수/2013)
