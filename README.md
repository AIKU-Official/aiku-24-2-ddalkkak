# 딸깍 한 번 하고 나니 교수님보다 시험 문제를 잘 냄

📢 2024년 2학기 [AIKU](https://github.com/AIKU-Official) 활동으로 진행한 프로젝트입니다.   
🎉 2024년 2학기 AIKU Conference 열심히상 수상!

## 소개

시험 자료를 입력하면 이를 기반으로 객관식 문제를 생성해주는 한국어 기반 모델 만들기 (Question-Generation)

## 방법론

1. 사전에 준비된 텍스트에서 **중요 키워드 식별** (ML 방법론: 중요 키워드 식별 모델로 Gaussian NB 모델 사용)
2. 텍스트에서 중요한 키워드를 빈칸 처리함으로써 질문을 추출
3. KoBERT를 활용하여 의문문 형태의 질문으로 변환
4. 중요한 키워드의 단어 유사도를 통해 객관식 선지 생성
   
코드 작성에는 이 [깃허브](https://github.com/KristiyanVachev/Question-Generation)를 참고하였습니다. 

## 환경 설정

학습을 진행하기 위해서, [KorQuAD v1.0](https://korquad.github.io/category/1.0_KOR.html) 데이터셋, 사전 학습된 fasttext 모델을 필요로 합니다. 해당 파일은 data 폴더 내에 위치하고 있습니다.   
의문문 형태의 질문 변환 시 사전 학습된 KoBERT를 사용합니다. 모델 가중치는 [드라이브](https://drive.google.com/drive/folders/1ZiY9EFPJl7bnvLN5fbraElZ9saYH20XJ?usp=drive_link)에서 접근할 수 있습니다.


## 사용 방법

notebook 폴더 안의 ipynb 파일을 순차적으로 실행시켜주세요.

## 예시 결과

```
Question 5:
확산 모델의 기본 발상은, _____ 이미지에 노이즈를 점진적으로 추가하였다가 그 노이즈를 다시 제거해 나가면 원본 이미지를 복원할 수 있다는 것이다.

Interrogative Question 5:
확산 모델의 기본 발상은 어떤 이미지를 복원할 수 있는가?

Answer:
원본

Incorrect answers:
사본
복사본
원문
필사본
```

## 팀원

- [권보영](https://github.com/iamnotwhale): 팀장, 모델 리서치, 코드 작성 및 정리
- [강동혁](https://github.com/cucumber5252): 모델 리서치, 코드 작성, 노션 정리
- [구영서](https://github.com/andless2004): 모델 리서치, 코드 작성, 발표자료 제작
- [김민경](): 모델 리서치, 코드 작성, 발표자료 제작
