# HairBe - 맞춤형 헤어추천, 가상헤어체험
![캡처](https://github.com/sebin1213/HairBe/assets/73850629/e5f16402-0ab2-4a94-b2dc-c6fcd0111022)

## 💜서비스 소개
"야, 나 앞머리 있는게 나아, 없는게 나아??" </br>
"아... 스타일 좀 바꾸고 싶은데, 머리 어떻게 하지???"

여러분, 머리는 바꾸고 싶은데, 나한테 잘 어울릴지는 모르겠고... 직접 해보기에는 망설인 경험이 있으신가요? </br>
나에게 어울리는 스타일을 정교하게 추천받고, AI를 사용해 자연스럽게 헤어를 바꿔볼 수 있는 서비스 '헤어비'를 체험해보세요!

- 서비스 예시
  
<img src="https://github.com/sebin1213/HairBe/assets/73850629/f7dccf24-4074-4841-9a86-20d0fb7d1cef" style="width: 500px;">

</br>

## 🔗성과
- Google Play Store 뷰티분야 인기차트 6위 & 누적 사용자 10만+
- SW 마에스트로 우수 프로젝트상 수상( 상위 14% )

</br>

## 🔗서비스 링크
<a href="https://apps.apple.com/kr/app/%ED%97%A4%EC%96%B4%EB%B9%84-%EC%96%BC%EA%B5%B4%ED%98%95-%EB%B6%84%EC%84%9D%EA%B3%BC-%EA%B0%80%EC%83%81%ED%97%A4%EC%96%B4-%EC%B2%B4%ED%97%98/id6452395655">
<img src="https://postfiles.pstatic.net/MjAyMTAyMTNfMTkg/MDAxNjEzMjE2Mjk2Mzg2.-nTH-GRi0FsGzIHZr9U94a3Oe0aW7tOVLO-zPEAZeQcg.ezakZSuLPYU8UFK1R1iZmNLKkGKQhT76PN_5CEs5Hbcg.PNG.kyk0095/%EC%95%B1%EC%8A%A4%ED%86%A0%EC%96%B4-02.png?type=w773" style="width: 300px;">
</a>
<a href="https://play.google.com/store/apps/details?id=com.atowner.hairbe">
<img src="https://postfiles.pstatic.net/MjAyMTAyMTNfMjQ2/MDAxNjEzMjE2MjQ0NzE1.x4HjXVnSDjfnfusoSZMJGch4bw9vuv9CPQFhyvb-4Nwg.1jFT1DFlpIzodiM7teXJceUsgSAibXMQUxBi7iDr2HEg.PNG.kyk0095/%EA%B5%AC%EA%B8%80%ED%94%8C%EB%A0%88%EC%9D%B4.png?type=w773" style="width: 300px;">
</a>

</br>
</br>

## 서비스 주요기능
### - AI 헤어스타일 체험
![image](https://github.com/sebin1213/HairBe/assets/73850629/f2dedc1b-57bf-48df-af2d-f68aa06ad913)
![image](https://github.com/sebin1213/HairBe/assets/73850629/665a0202-b831-4db1-b868-7b8a565a6f42)


### - 얼굴형 분석 기반 헤어스타일 추천
<img src="https://github.com/sebin1213/HairBe/assets/73850629/776c17af-26c3-4852-b2e9-2edf620aeb56"  style="width: 100%;">
<img src="https://github.com/sebin1213/HairBe/assets/73850629/8c5bd21a-4b42-4e06-bf2a-3d98278ce17b"  style="width: 100%;">

</br>
<details>
<summary>얼굴형 분석 기능 구현과정</summary>
  
### 1 - 얼굴형 분석을 통한 헤어스타일 추천

#### - XGBoost 를 이용한 얼굴형 분류 기능 

  ![image](https://github.com/sebin1213/HairBe/assets/73850629/0403cb2e-43df-4f9c-9465-cf8e42e21671)
- 기존의 얼굴형 분류기준이 전문가들과 인터뷰한 결과 적합하지 않다는 결론
- 전문가들과 함께 얼굴형 분류 방식 구축, 5 개의 얼굴 형태로부터 헤어에 영향을 주는 21 가지 얼굴형 구축

![image](https://github.com/sebin1213/HairBe/assets/73850629/437b04b3-d5e8-472a-ae1b-f7ac2e0731ec)


#### - 데이터 셋 구축
새로운 분류기준을 마련했기에 기존 데이터셋을 사용할 수 없는 문제 발생.
상업적으로 사용이 가능한 이미지 ( Kaggle(niten19/face-shape-dataset), github(a312863063/seeprettyface, CelebV-HQ/CelebV-HQ) 등 )를 이용하여 새로운 데이터 셋 구축, 이미지 증강 기술을 활용하여 구축한 데이터 셋의 품질 향상

#### - 얼굴형 분석(구체적 내용은 제거했습니다.)
광대와 턱 특징을 분리하고 얼굴의 측면 비율을 독립적으로 분석하는 방법을 통해 모델링을 진행 기존 모델과 달리 얼굴 비율, 광대 및 턱 특징을 동시에 평가하는 것이 아닌, 우리의 얼굴 분류 기준에 알맞은 모델을 구성하기 위해 긴 형태와 계란 형태와 같은 유사한 기하학적 특징을 가진 얼굴 형태를 구별하는 것에 초점을 맞춰 학습 진행 턱의 기하학적 모형을 dlib 모델을 활용한 랜드마크 추출과 함께 정규화 된 거리, 비율 및 각도를 계산하여 얼굴형 분류 모델 개발

![image](https://github.com/sebin1213/HairBe/assets/73850629/a2553df0-c8bf-4646-a883-0f494ce886f3)


</details>

</br>

## ✨서비스 목적
<details>
<summary>보기</summary>

<img src="https://github.com/sebin1213/HairBe/assets/73850629/57aac208-8067-49e3-9793-de4fd181973c" style="width: 40%; float: right;">
<img src="https://github.com/sebin1213/HairBe/assets/73850629/a656f90f-0cfa-48c3-93bf-2f433fe8ca68" style="width: 40%; float: right;">

### 문제인식

- 현재 뷰티시장은 퍼스널 컬러를 시작으로 **맞춤형 스타일에 대한 관심이 커지는 추세**입니다. 특히 현재 시장에 나와있는 전문가를 통한 **퍼스널 헤어 진단 서비스는 최소 20만원 상당의 금액을 요구**하며 그 **수요 또한 매우 높기에 티켓팅 형식**으로 이루어짐.
-	새로운 스타일로의 시도는 리스크가 존재함. **“어울리지 않을까봐(70.2%)”** 가 가장 대표적인 이유.
 (2023.05.21.~2023.05.24, 120명을 대상으로 진행한 설문조사에서) 70.2%가 어울리지 않을 때의 리스크 때문에 새로운 스타일을 시도하지 못하고 있으며, 81%가 자신에게 어울리는 스타일에 대해 알기 어렵다고 답했음.
-	시도하지 않고 **본인에게 어울리는 스타일을 찾는 과정은 매우 어려움.**
 전문가의 의견에 따르면, “스타일이 어울리는 정도를 결정하는 요소는 셀 수 없이 많고” (퍼스널 컬러 진단 기업 ‘톤앤핏’ 대표 김혜인), “작은 변화에도 큰 차이가 발생하는 얼굴만으로 개인이 이를 판단하기는 어렵다” (스타일 컨설팅 기업 ‘스타일 하우’ 대표 김송하)고 함. 즉, 스스로에게 어울리는 스타일이 어떤 것인지 판단하는 과정에서 전문적인 지식을 요함.

### 기획 의도(문제해결)
-	본인에게 어울리는 헤어를 추천 받을 수 있는 앱 내 컨설팅 서비스
앱 서비스에서 얼굴형 분석, 퍼스널 컬러 검사를 통해 본인에게 어울리는 헤어스타일을 추천 받을 수 있도록 함.
-	헤어비 가상헤어체험
AI 생성 기술을 통해 다양한 헤어 스타일을 미리 체험해 볼 수 있도록 하여, 사용자가 특정 스타일에 대한 궁금증을 사진 퀄리티의 헤어 변경을 통해 해소할 수 있음. 또한 디자이너와 헤어 상담 중 어울리는 스타일을 찾을 때 실시간으로 특정 스타일을 자신의 얼굴에 적용해볼 수 있게 해 상담의 질을 높임.


</details>

</br>


## 💡가설검증
<details>
<summary>보기</summary>

💡 `가설: 헤어추전과 AI가상헤어체험기능을 통해 높은 수요의 퍼스널 헤어시장을 변화시킬 수 있을 것이다.`

- 전문진을 통한 로직 분석 및 도메인 지식 학습 그리고 빠른 배포를 통해  가설을 검증했습니다.

![image](https://github.com/sebin1213/HairBe/assets/73850629/2af0a44a-8f3f-4a2b-a507-4b4e24a777f5)


- 전문진을 기반으로 한 도메인지식 학습, 로직 검증
- 빠른 서비스 출시를 통한 가설 검증
- 퍼스널 헤어 추천 기능 출시 후 862명의 사용자 유치


</details>

---

## 개발

### 기술 스택
Java, Spring Boot, JPA, Python, FastAPI
MySQL, RabbitMQ, Redis, Diffusion AI, AWS, Docker, Github Action 

### 담당 업무
**Back-end** ( 팀원 구성 : **Back-end 1**, AI 1, Front-end 1 )

### 주요 개발
- 비용 절감 클라우드 아키텍처 설계
  - GPU서버로 인한 고비용 문제를 CloudWatch Event, Spot 인스턴스, lambda를 활용한 아키텍처 재설계를 통해 클라우드 비용 65% 절감 (관련 내용 : [GPU서버비용 절감하기-1](https://velog.io/@hope1213/GPU%EC%84%9C%EB%B2%84%EB%A5%BC-Spot-Instance-%ED%99%9C%EC%9A%A9%ED%95%B4-%EC%A0%80%EB%A0%B4%ED%95%98%EA%B2%8C-%EC%82%AC%EC%9A%A9%ED%95%B4%EB%B3%B4%EC%9E%90-1), [GPU서버비용 절감하기-2](https://velog.io/@hope1213/AWS%EC%97%90%EC%84%9C-GPU%EC%84%9C%EB%B2%84%EB%A5%BC-%EC%A0%80%EB%A0%B4%ED%95%98%EA%B2%8C-%EC%82%AC%EC%9A%A9%ED%95%B4%EB%B3%B4%EC%9E%90-2))
  - 데이터 유실을 해결을 위한 RabbitMQ 메세지 대기열 시스템 구축 (관련 내용 : [RabbitMQ 적용기](https://velog.io/@hope1213/%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%9C%A0%EC%8B%A4-%EB%B0%A9%EC%A7%80%EB%A5%BC-%EC%9C%84%ED%95%9C-RabbitMQ-%EC%A0%81%EC%9A%A9))
 
- API 성능 개선
  - EHCache를 활용한 쿼리 캐싱을 통해 API 성능 (34 TPS → 71 TPS)로 개선 (관련 내용 : [Ehcache를 활용한 API 성능개선](https://velog.io/@hope1213/Ehcache%EB%A5%BC-%ED%99%9C%EC%9A%A9%ED%95%9C-API-%EC%84%B1%EB%8A%A5%EA%B0%9C%EC%84%A0))
  - 서버의 리소스 낭비를 방지하기위해 Redis를 활용하여 API 중복요청 방지 구현 (관련 내용 : [Redis API 중복요청 방지](https://velog.io/@hope1213/Redis%EB%A5%BC-%ED%86%B5%ED%95%9C-API-%EC%A4%91%EB%B3%B5%EC%9A%94%EC%B2%AD-%EB%B0%A9%EC%A7%80))
  - Pre-signed URL을 도입하여 이미지 업로드 시 발생하는 서버의 빈번한 파일 I/O 작업과 네트워크 지연에 따른 속도 저하를 감소
 
- 기능 개발
  - JPA, QueryDSL을 활용한 Restfu API 개발
  - 비동기 & Non-blocking 방식을 도입하여 처리 성능 개선
  - AOP와 Exception Handler를 이용한 로깅
- CI/CD Workflow 구축
  - AWS & Docker & Github Actions & codeDeploy를 이용한 CI/CD 무중단 배포 자동화 구축
 
- WEB 개발 (얼굴형 보고서 공유 페이지, 프로젝트 홈페이지)  

## 아키텍처

![image](https://github.com/sebin1213/HairBe/assets/73850629/191d7566-b655-4150-9054-7463042c7500)

