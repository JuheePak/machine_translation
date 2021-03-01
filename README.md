### 🤖 Machine translation project

---

#### `[Project: 여기에 텍스트 입력] 🗨`

- elice coding academy에서 진행하는 딥러닝 프로젝트 중 **RNN 기반**의 machine translation project 진행
- Sentimental_analysis로 연습 후, machine translation project 진행 예정 
- project 계획서는 아래와 같다
- 제공 받은 데이터셋(영어-프랑스어 말뭉치)은 elice에 저작권이 있으므로 ~~업로드 불가~~

  -  [emotions_dataset for NLP from kaggle (감성 분석 데이터 셋)](https://www.kaggle.com/praveengovi/emotions-dataset-for-nlp)

- 추후 발표자료 및 코드는 업로드 예정

---

##### 1. 주제: `딥러닝을 이용한 한국어-영어 번역기 만들기`

##### 2. 배경 및 목표

##### (1) 배경

- 개인이나 소규모 팀은 한국어-영어(이하 한-영) 말뭉치 데이터를 구하기 어려워 높은 수준의 번역기를 만들수 없었다 .하지만 최근 한국지능정보사회진흥원 AiHub에 한-영 번역 말뭉치 자료가 있어 AI 기술을 활용할 수 있는 충분한 양의 데이터에 접근할 수 있게 되었다.
- 한-영 말뭉치 데이터가 너무 커 우선 영어-프랑스어(이하 영-프) 말뭉치 데이터를 활용하여 번역기를 제작하고 추후 한-영 번역기에 적용하고자 한다.

##### (2) 목표

- 여러 기계 번역 모델을 활용하여 번역기를 구현하는 것을 목표로 한다.
- 영-프 BLEU 점수 기준 30점을 목표로 한다. (2017년 ConvS2S Ensemble 모델 기준 영어-프랑스어 BLEU 점수가 41.29, Transformer 41.8) [출처](https://www.researchgate.net/figure/The-Transformer-achieves-better-BLEU-scores-than-previous-state-of-the-art-models-on_tbl1_323904682)

##### 3. 일정

- 2월 23일~ 2월 25일: 감성 분석 구현
- 2월 26일~ 2월 27일: 데이터 전처리(토큰화, 패딩, 전처리 파이프라인 구성)
- 2월 28일~ 3월 1일: EDA 및 시각화
- 3월 2일~ 3월 5일: RNN 기반 모델 구현 및 튜닝
- 3월 6일: 발표

##### 4. 데이터 수집 및 전처리

- `데이터 수집`
  - 영-프 말뭉치 데이터: elice 제공
  - 한-영 말뭉치 데이터: 한국지능정보사회진흥원 AiHub
- `전처리: 토큰화(Tokenize)`
  - 토큰화: 문장을 단어로 쪼개고, 단어를 숫자에 매칭
  - 패딩: 다양한 문장 길이를 동일한 길이로 만들기 작업

##### 5. RNN 기반 4가지 모델 구현 및 테스트

- (Simple) RNN
- Embedding
- Bidirectional LSTM
- Emcoder-Decoder

##### 6. 개발 환경

- 개발 환경: Google colab, JupyterLab
- 개발 언어: Python
- 활용 라이브러리: Tensorflow, Keras