# ETRI-lifelog-data-project

**라이프로그 데이터를 활용한 수면의 질 추정에서의 주요 요인에 대한 연구**
----
**1. 사용한 데이터** : ETRI 라이프로그 데이터셋 (2020-2018)
- 2019-2018 수면관련 설문결과 데이터
- 2020 수면관련 설문결과 데이터
- 2019-2018 수면 측정 데이터
- 2020 수면 측정 데이터

**최종 사용 데이터** 
- last.csv : 2020년도 최종 분석 데이터
- total1819.csv : 2018,2019년도 최종 분석 데이터
----

<br/>

**2. 코드 실행 방법** 

**2.1 데이터셋 다운로드**

data라는 빈 폴더를 생성하고 그 안에 ETRI 라이프로그 데이터셋(2020-2018)를 다운로드한다.

링크 : https://nanum.etri.re.kr/share/schung1/ETRILifelogDataset2020?lang=ko_KR

데이터 파일명

- 2019-2018 수면관련 설문결과 데이터
- 2020 수면관련 설문결과 데이터
- 2019-2018 수면 측정 데이터
- 2020 수면 측정 데이터

**2.2 라이브러리 설치**

분석에 필요한 라이브러리를 설치한다.
- 기본 
```
pip install time
pip install datetime
pip install os
pip install numpy
pip install pandas
```
- 시각화
```
pip install seaborn 
pip install matplotlib
```
- 데이터 전처리 & 모델링 & 평가
```
pip install sklearn
pip install xgboost
```

**2.3 total_18,19,20.ipynb 실행**

data파일을 나오고, 업로드 된 모든 파이썬 파일을 다운로드한 후, total_18,19,20.ipynb를 실행하여 데이터 전처리를 진행하고, 기존 지표, 새로운 지표 기반의 RF 이진분류 결과를 확인한다.

**2.4 total_modeling.ipynb 실행**

다운로드한 파이썬 파일 중 total_modeling.ipynb를 실행하여 주요 지표 기반 새로운 기준으로 예측 모델링한 결과를 확인한다.

**2.5 xgb_classifier.ipynb 실행**

다운로드한 파이썬 파일 중 xgb_classifier.ipynb를 실행하여 기존 지표, 새로운 지표 기반의 XGB 이진분류 결과를 확인한다.

----

<br/>

**3. 폴더 구조**

```
|-- README.md
|-- data
|   |-- 1819_total
|   |   |-- 1.csv
|   |   |-- 10.csv
|   |   |-- 102.csv
|   |   |-- 104.csv
|   |   |-- 105.csv
|   |   |-- 106.csv
|   |   |-- 107.csv
|   |   |-- 108.csv
|   |   |-- 109.csv
|   |   |-- 11.csv
|   |   |-- 110.csv
|   |   |-- 111.csv
|   |   |-- 112.csv
|   |   |-- 113.csv
|   |   |-- 114.csv
|   |   |-- 115.csv
|   |   |-- 118.csv
|   |   |-- 119.csv
|   |   |-- 12.csv
|   |   |-- 120.csv
|   |   |-- 13.csv
|   |   |-- 14.csv
|   |   |-- 15.csv
|   |   |-- 16.csv
|   |   |-- 17.csv
|   |   |-- 18.csv
|   |   |-- 19.csv
|   |   |-- 2.csv
|   |   |-- 20.csv
|   |   |-- 21.csv
|   |   |-- 22.csv
|   |   |-- 23.csv
|   |   |-- 24.csv
|   |   |-- 25.csv
|   |   |-- 26.csv
|   |   |-- 27.csv
|   |   |-- 28.csv
|   |   |-- 29.csv
|   |   |-- 3.csv
|   |   |-- 30.csv
|   |   |-- 4.csv
|   |   |-- 5.csv
|   |   |-- 6.csv
|   |   |-- 7.csv
|   |   |-- 8.csv
|   |   `-- 9.csv
|   |-- 2020_sleep.csv
|   |-- last
|   |   |-- user01.csv
|   |   |-- user02.csv
|   |   |-- user03.csv
|   |   |-- user04.csv
|   |   |-- user05.csv
|   |   |-- user06.csv
|   |   |-- user07.csv
|   |   |-- user08.csv
|   |   |-- user09.csv
|   |   |-- user10.csv
|   |   |-- user11.csv
|   |   |-- user12.csv
|   |   |-- user21.csv
|   |   |-- user22.csv
|   |   |-- user23.csv
|   |   |-- user24.csv
|   |   |-- user25.csv
|   |   |-- user26.csv
|   |   |-- user27.csv
|   |   |-- user28.csv
|   |   |-- user29.csv
|   |   `-- user30.csv
|   |-- last.csv
|   |-- last_total_survey.csv
|   |-- total1819.csv
|   |-- total_survey_1819.csv
|   |-- user_sleep_2019_2018.csv
|   |-- user_sleep_2020.csv
|   |-- user_survey_2019_2018.csv
|   `-- user_survey_2020.csv
|-- total18,19,20.ipynb
|-- total_modeling.ipynb
`-- xgb_classifier.ipynb

```
----

<br/>

**4. 파일별 논문 해당 내용 부분**
- 파일명 (논문 해당 내용 인덱스)
    - 포함 내용
----
- total18,19,20.ipynb (2~3.2)
    - 데이터 전처리
    - 기존지표, 새로운 지표 RF 이진분류, 특성중요도
- total_modeling.ipynb (3.3)
    - 주요 지표 기반 새로운 기준으로 예측 모델링
- xgb_classifier.ipynb (3.3)
    - XGB 모델 기존 지표, 새로운 지표 이진분류
