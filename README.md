# BDP-FINAL-24

이 프로젝트는 Hadoop 기반의 빅데이터 처리 기술을 활용하여 대용량의 데이터를 수집, 분석, 활용 할 수 있는 시스템을 개발하며 의미 있는 인사이트를 도출하는 것을 목표로 합니다.

---

## 📋 (11/22) 회의 내용: 주제 후보 및 데이터 탐색 
: 첫 회의에서는 다양한 주제를 제안하고, 이를 분석 가능한 데이터와 결합하여 구체적인 프로젝트 방향성을 설정하였습니다.

### #1 주제 후보
1. **논문 트렌드 분석**
   - **문제 정의**: 특정 학문 분야의 빠르게 변화하는 트렌드를 분석하여 최신 연구 방향과 주요 키워드를 파악.

   - **데이터 전처리**:
     - 중복 제거, 텍스트 정리, 주제 분류 (NLP 활용).

   - **분석 방법**:
     1. 키워드 시계열 분석.
     2. 주제 모델링 (LDA, BERT 등).
     3. 인용 및 협업 네트워크 시각화.

2. **TripAdvisor를 활용한 한국 여행지 추천 시스템**
   - **문제 정의**: 계절 및 사용자 리뷰 기반으로 여행지를 추천하는 사용자 맞춤형 시스템 구축.

   - **데이터 분석 방법**:
     - 불용어 제거 후 TF-IDF와 WordCount로 주요 키워드 도출.
     - Content-Based Filtering과 Collaborative Filtering을 활용한 추천 알고리즘 설계.
     - WordCloud와 지도 시각화를 통해 결과 시각화.

3. **GOTY(Game of the Year) 예측 시스템**
   - **문제 정의**: 게임 리뷰 데이터를 기반으로 GOTY 수상 가능성을 예측.

   - **데이터 분석 방법**:
     - 감정 분석 (VADER) 및 텍스트 정리.
     - 긍정 리뷰 비율 및 평균 평점을 기준으로 GOTY 가능성 도출.

4. **기상 변화와 농산물 가격 간 상관관계 분석**
   - **문제 정의**: 기상 데이터와 농산물 가격의 상관관계를 분석하여 농업 생산성에 미치는 영향을 파악.

   - **데이터 분석 방법**:
     - 기상 변수와 가격 데이터를 결합하여 Spark MLlib로 상관관계 분석.
     - 시계열 분석(LSTM, ARIMA)을 통해 가격 변동 예측 모델 구축.

5. **교통 사고 데이터 분석 및 사고 위험 지역 예측**
   - **문제 정의**: 교통사고 데이터를 분석하여 사고 위험 지역 및 시간대를 예측.

   - **데이터 분석 방법**:
     - Random Forest 및 Decision Tree를 활용하여 위험 지역 예측.
     - 교차 검증으로 모델 성능 평가.

6. **생필품 농수축산물 물가 분석 및 상품 추천**
    - **문제 정의**  
    급격한 물가 인상으로 인해 힘들어진 명지대학교 자취생의 생활비 절약을 위한 **물가 예측 및 비교 서비스**.

    - **데이터 분석 방법**:
        - **품목별 가격 비교**  
        서울시 전체 시장, 학교 주변 5개 시장, 이마트 에브리데이 데이터를 기준으로 대표 품목의 가격 비교.
        - **자치구 물가 분석**  
        품목 그룹화를 통한 자치구별 평균 물가 비교.
        - **대표 상품 물가 예측**  
        SARIMA, RNN, LSTM 모델을 활용한 시계열 분석을 통해 물가 변동 예측.

---

## 🤔 채점 기준 적용

: 회의에서 주제를 선정하기 위해 다음과 같은 **채점 기준**을 적용했습니다

1. **데이터 수집 방법 자동화**  
   - 데이터는 공공 API, 크롤링 등을 통해 자동화 가능한가?  
   - 예: TripAdvisor API, 기상청 및 농림축산식품부 데이터 포털.

2. **데이터 전처리 및 저장 방법**  
   - 데이터 전처리가 얼마나 체계적으로 이루어질 수 있는가?  
   - 빅데이터 환경(Hadoop, Hive, Spark)에서 데이터 저장 및 처리 가능성.  

3. **문제 정의**  
   - 문제 정의가 명확하고 분석 목표가 구체적인가?  

4. **데이터 분석 방법**  
   - 분석 방법이 프로젝트 목적을 달성하기에 적합한가?  
   - Spark MLlib, NLP, 추천 알고리즘 등 다양한 기술의 활용 가능성.

5. **데이터 크기와 분석 난이도**  
   - 데이터가 충분히 크고, 분석에 도전적이면서도 실현 가능한가?

6. **빅데이터 확장 가능성**  
   - 빅데이터 기술(Hadoop, Spark 등)을 활용한 확장 가능성이 높은가?

7. **개인 참여도**  
   - 각 팀원이 기여할 수 있는 작업이 충분히 분배되었는가?  
   - GitHub에 개인별 작업 기록을 남기고 팀 내에서의 역할을 명확히 정의.

8. **발표 및 질의응답**  
   - 결과를 시각화하고, 설득력 있는 발표를 준비할 수 있는 주제인가?

---

## 🚀 최종 주제 선정

### 최종 주제: **생필품 농수축산물 물가 분석 및 추천**
급격한 물가 인상으로 인해 힘들어진 명지대학교 자취생의 생활비 절약을 위한 **물가 예측 및 비교 서비스**.

---

## 🎯 프로젝트 목표
명지대학교 자취생들의 생활비 절약을 위해:
1. 주변 시장의 생필품 물가를 비교하고,
2. 학교 주변 물가 변동을 예측하여,
3. **합리적인 소비 결정을 지원**하는 서비스를 제공하는 것이 목표입니다.

---

## ➤ 데이터 설명

### 1. 서울시 생필품 농수축산물 API
- **데이터 출처**:  
  [서울시 생필품 농수축산물 API](https://data.seoul.go.kr/dataList/OA-1170/S/1/datasetView.do)
- **특징**:  
  - 매주 1회 업데이트되는 전통시장 물가 데이터.
  - 서울시 물가 모니터가 자치구별 전통시장 16개 품목의 가격을 조사하여 공개.
  - 대형마트 데이터는 제외.

---

### 2. 이마트 에브리데이 데이터
- **데이터 수집 방법**:  
  크롤링(Selenium, BeautifulSoup)을 활용.
- **출처**:
  - [네이버 쇼핑 API 활용 예제](https://robomoan.medium.com/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EB%84%A4%EC%9D%B4%EB%B2%84-%EC%87%BC%ED%95%91%EC%9D%B8%EC%82%AC%EC%9D%B4%ED%8A%B8-api-%ED%98%B8%EC%B6%9C%ED%95%98%EA%B8%B0-cd32757b89cb)
  - [쿠팡 API 활용 예제](https://dataanalytics.tistory.com/entry/Python-%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EC%BF%A0%ED%8C%A1-%ED%8C%8C%ED%8A%B8%EB%84%88%EC%8A%A4-API-%ED%99%9C%EC%9A%A9%ED%95%98%EA%B8%B0)

---

## ➤ 데이터 분석 방법

### 1. 품목별 가격 비교
- 서울시 전체 전통시장, 학교 주변 5개 시장, 이마트 에브리데이를 기준으로 대표 품목의 가격을 비교.

### 2. 자치구 물가 분석
- 품목 그룹화를 통해 자치구별 평균 물가를 비교.

### 3. 대표 상품 물가 예측
- SARIMA, RNN, LSTM 모델을 활용하여 시계열 분석을 통해 물가 변동을 예측.

---

## ➤ 모델(예측 방법)

- **SARIMA**: 계절성과 추세를 반영한 시계열 분석.  
- **RNN**: 순환 신경망을 활용한 시간의 흐름에 따른 예측.  
- **LSTM**: 장기적인 패턴을 학습하여 정밀한 예측 수행.

---

## ➤ 고려할 점

1. **서울시 데이터와 이마트 데이터의 품목 매칭**
   - 서울시 데이터 품목 이름 예시:
        - 쌀(이천쌀) 20kg 1포, 사과(부사) 1개, 배(신고) 1개, 치약 160g, 상추 100g, 라면 5개입 1봉

2. **대표 상품 선정**
   - 자취생들이 자주 구매하는 대표 품목으로 분석.  
   - 대표 품목 예시:
     - '라면 5개입 1봉’,  '바디워시 1000ml 1개’, '컵라면 1개’,  '맥주 500ml 1캔’, '비누 4개입 1개', '생수 500ml 1병’, '맛김 16팩', '우유 1L'  '즉석밥 210g 3개입’, '햄 340g’, '통조림(참치) 150g',  '치약 160g 1개', '칫솔 4입 1개', '샴푸 680ml 1통', '식용유 1.8L', '소주 360ml, 1병’, '쌀 20kg 1포' 

---

## 📚 참고 자료

- [서울시 생필품 농수축산물 API](https://data.seoul.go.kr/dataList/OA-1170/S/1/datasetView.do)
- [네이버 쇼핑 API 활용 예제](https://robomoan.medium.com/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EB%84%A4%EC%9D%B4%EB%B2%84-%EC%87%BC%ED%95%91%EC%9D%B8%EC%82%AC%EC%9D%B4%ED%8A%B8-api-%ED%98%B8%EC%B6%9C%ED%95%98%EA%B8%B0-cd32757b89cb)
- [쿠팡 API 활용 예제](https://dataanalytics.tistory.com/entry/Python-%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EC%BF%A0%ED%8C%A1-%ED%8C%8C%ED%8A%B8%EB%84%88%EC%8A%A4-API-%ED%99%9C%EC%9A%A9%ED%95%98%EA%B8%B0)