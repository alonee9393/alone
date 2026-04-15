# Emotion Of Palette Music

### "Emotion_Of_Palette_Music"


"멜론" (1990 ~ 2010)년의 연도별 차트의 자료를 수집하여 가사, 감정을 분석하여 음악을 추천해주는 프로젝트.

## 개요
멜론에 인기순 아니면, 가사나 감정 같은 여러 요소로는 분석이 나와 있지 않다.
좋은 가사임에도 좋은 노래임에도 인기가 없으면 묻힐 수 밖에 없기에
묻혔던 많은 노래들이 다시 빛을 볼 수 있다면 어떨까 ?
이런 방향으로의 추천을 한다면 어떻게 추천을 해줄 수 있을까? 

## 주제 선정 이유
“음악 스트리밍 사이트” 
⇒ 멜론 연도별 차트 (1990 ~ 2010)년을 활용하여 크롤링한 자료 수집.

=> 연도별 차트 내 앨범 수록곡도 같이 소개하는 방향으로 설정하였다.

=> 이용하고 있는 사이트기에, 멜론을 선정하였다.

=> 선택한 감정으로는 “기쁨” “슬픔” “분노” “우울” “불안” “증오”이 6가지이다.

=> 왜 감정 추천을 택했는지 이유로는 노랠 들을 때, 먼저 가사와 멜로디를 보게 됩니다.  가사와 멜로디를 통해 노래에 대한 감정이나 몰입도에 영향을 받는다고 생각했습니다. 

이 감정들은 AI-HUB 데이터셋에서 공통적으로 드러나는 감정이라
분석 기반으로 적절하다고 판단했습니다.

## 감정 추천 기반 모델 사용
**KoBERT 모델**

KoBERT는 BERT를 한국어 데이터로 사전 학습한 모델로, 한국어 특유의 문맥과 의미를 효과적으로 파악

Model 학습을 위한 Data Sets 구축
 
KoBERT 모델 학습을 위한 AI HUB의 

한국어 데이터 감성 대화 말뭉치 58271개 
한국어 연속성 대화 데이터 셋 55630 개 

최종 데이터셋 총 개수 113,901개 

감정 Label : “기쁨”, “슬픔”, “분노” , “불안”, “우울” “증오” 6개의 감정.
 
모델에 넣기 위해 위의 2개의 파일을 감정 Label 6개에 맞춰 재라벨링을 진행하였다.

학습 결과, 정확도(Accuracy) 0.771로 높은 성능을 기록 (3 Epoch 학습)

### 기술스택
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)


### 화면 설계서
<img src ="https://github.com/user-attachments/assets/770e03a6-3781-4999-b10e-5765f0ad3783" width="700px">
<img src ="https://github.com/user-attachments/assets/61fa438f-d4fa-4d9d-82b5-d4a5c0c1f436" width="700px">
<img src ="https://github.com/user-attachments/assets/512fde3e-0db2-4393-aaa3-50b261440feb" width="700px">
<img src ="https://github.com/user-attachments/assets/ac975a70-4310-4587-b64b-5b24a420985f" width="700px">

### ERD
<img src ="https://github.com/user-attachments/assets/b3a3e77a-3439-4a0d-88fb-8e8de7713452" width="800px">

### 시스템 아키텍처
<img src ="https://github.com/user-attachments/assets/d62df2df-ab41-4325-b2c9-9eafedd3475b" width="600px">

### 시연영상

### 프로젝트 회고.
준비하면서 아쉬웠던 점 = 
미니 프로젝트 진행할 때마다 나던 세팅이슈가 다행히  한 번도 나지 않았지만, 처음에 생각했던 것만큼 결과를 내지 못해 항상 아쉽다는 느낌을 받는다. 후회 없이 진행해보고자 노력을 했던 것 같은데 이 노력만큼 좋은 결과를 보였어야 하는데, 아쉽단 말만 되풀이하는 것 같다.


향후 개선을 위해서 뭘 해야 할지.=
일정 상 절충하여 streamlit을 통해 구현을 했지만, 원래 하려 했던 SpringBoot로도 구현을 해보려고 합니다. 영어가사 부분을 보완할 수 있도록 모델을 확장하여 적용하고자 합니다. 다수의 감정인 경우임에도 하나의 감정만 분류되어 나오는 경우도 많았기에 이 부분도 보완할 예정입니다. 데이터 수집도 1990년대 이전 2010년 이후 데이터로 범위를 확장시키고 학습에 대한 정확도를 높일 방향의 개선점을 생각하고 있습니다.


