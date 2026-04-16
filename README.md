# Emotion Of Palette Music
🎵 Emotion Of Palette Music

1990 ~ 2010년 멜론 연도별 차트 데이터를 기반으로
가사 감정 분석을 통해 사용자 감정에 맞는 음악을 추천하는 서비스입니다.

본 프로젝트는 개인 프로젝트로 진행하였으며,
기획부터 데이터 수집, 모델 학습, DB 설계, 서비스 구현까지 전 과정을 단독 수행하였습니다.

※ 본 저장소는 교육 과정 중 개발한 프로젝트를 포트폴리오용으로 재정리한 버전입니다.

📌 프로젝트 소개

Emotion Of Palette Music은
기존 인기순 중심 음악 추천 방식에서 벗어나,
가사의 감정 분석 결과를 기반으로 사용자 감정에 맞는 음악을 추천하기 위해 기획한 프로젝트입니다.

숨겨진 좋은 음악들이 단순 인기 지표에 의해 묻히지 않고,
감정이라는 새로운 기준으로 재발견될 수 있도록 하는 것을 목표로 하였습니다.

🎯 주제 선정 이유

기존 음악 스트리밍 플랫폼은 인기순, 장르, 아티스트 중심 추천이 주를 이루고 있으며
가사나 감정 기반 분석은 상대적으로 부족하다고 느꼈습니다.

이에 따라 다음과 같은 문제를 해결하고자 하였습니다.

인기 중심 추천 구조로 인해 숨겨진 음악 노출 부족
감정 기반 음악 탐색 기능 부재
가사와 감정을 연결한 추천 시스템 부족
😊 감정 분류 기준

AI Hub 데이터셋을 기반으로 다음 6가지 감정을 정의하였습니다.

기쁨
슬픔
분노
우울
불안
증오
🧠 모델 및 데이터셋
KoBERT 기반 감정 분석 모델

KoBERT는 한국어 문맥 이해에 최적화된 사전학습 모델로,
한국어 가사의 감정 분류에 적합하다고 판단하여 사용하였습니다.

데이터셋 구성
AI Hub 한국어 감성 대화 말뭉치: 58,271건
AI Hub 한국어 연속성 대화 데이터: 55,630건

총 113,901건 데이터 사용

감정 Label 6종으로 재정의하여 재라벨링 후 학습 진행

모델 학습 결과
Accuracy: 0.771
Epoch: 3

🧩 주요 구현 내용
멜론 연도별 차트 및 앨범 수록곡 데이터 크롤링
가사 데이터 전처리 및 정제
감정 Label 재분류 및 학습 데이터셋 구성
KoBERT 기반 감정 분류 모델 학습
Streamlit 기반 음악 추천 서비스 구현

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


