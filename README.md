## LLM을 활용한 일상대화 디스코드 챗봇<br/>[230601 ~ 231015]
_**LLM을 활용한 일상대화 디스코드 챗봇**_

## 팀원
김남주 박수영 안중보

## 배경 및 목적
- ChatGPT와 같이 웹에서 사용하는 것과 달리, 내 컴퓨터에서 내 맘대로 파인튜닝하여 실행을 하고싶었다.
- 다른 LLM들과 달리 한국어만으로 파인튜닝하여 한국어 성능이 좋은 챗봇을 만들었다.
- 주변에 친구가 없고 외로움을 느끼는 사람들에게 챗봇이 친구같이 친근하게 대답을 해주도록 한다.
- 내가 같이 대화를 하고 싶은 사람의 말투와 대화들을 학습시켜 원하는 사람과 비슷한 느낌을 줄 수 있다.

## 개념 및 설계
![image](https://github.com/zoo3323/Discord_Chatbot/assets/95582592/6e81ec92-6aa3-4580-9bc5-353d3c2b17dd)

## 사용 기술(작동 원리)
- Polyglot 모델을 활용한 챗봇
  - Koalpaca 한국어 데이터셋으로 학습된 Polyglot모델을 파인튜닝
- 디스코드에서 챗봇 사용
  - 디스코드 채팅방에 챗봇을 초대하여 대화 가능
- TTS를 활용한 음성 대화
  - 실제 사람과 대화하듯 음성으로 대화 가능

## 데이터셋

[73000여개의 20대 여성 카카오톡 질문/답변 데이터셋](https://github.com/Ludobico/KakaoChatData)을 사용
![image](https://github.com/zoo3323/Discord_Chatbot/assets/95582592/26dae378-1c4e-4911-b6cc-014bacbffc8e)
### alpaca_data
Llama 모델기반 스탠퍼드 대학교에서 제작한 Alpaca 데이터셋에 맞춰 변형하였습니다.
Llama와 크게 다른점은 없습니다.

![image](https://github.com/zoo3323/Discord_Chatbot/assets/95582592/127e3ff6-2047-474b-93ce-ad46ade047ee)


## Fine tune 방식 모델 학습 방법
### QLoRa 4bit 학습방법
QLoRA로 Polyglot-ko 5.8B 모델 학습 with 4bit
[Beomi님의 Koalpaca 코랩 예제 활용](https://github.com/Beomi/KoAlpaca#fine-tune-%EB%B0%A9%EC%8B%9D-%EB%AA%A8%EB%8D%B8-%ED%95%99%EC%8A%B5-%EB%B0%A9%EB%B2%95)<br/>
로컬에서 3070ti 8gb 사용하여 학습


## 결과물(사진)
![image](https://github.com/zoo3323/Discord_Chatbot/assets/95582592/8e35df90-b853-43e3-a6be-a87107469824)

