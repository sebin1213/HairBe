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

## ✨서비스 목적
<img src="https://github.com/sebin1213/HairBe/assets/73850629/57aac208-8067-49e3-9793-de4fd181973c" style="width: 40%; float: right;">
<img src="https://github.com/sebin1213/HairBe/assets/73850629/a656f90f-0cfa-48c3-93bf-2f433fe8ca68" style="width: 40%; float: right;">

- 현재 뷰티시장은 퍼스널 컬러를 시작으로 **맞춤형 스타일에 대한 관심이 커지는 추세**입니다.
- 특히 현재 시장에 나와있는 전문가를 통한 **퍼스널 헤어 진단 서비스는 최소 20만원 상당의 금액을 요구**하며 그 **수요 또한 매우 높기에 티켓팅 형식**으로 이뤄집니다.
- 하지만, 얼굴 길이, 이목구비의 생김새, 눈썹, 인중의 길이, 목길이 등 **헤어스타일이 어울리는 정도를 결정하는 요소는 수없이 많습니다.** (’톤앤핏’ 대표 /스타일컨설턴트 김혜인 2023.08.04 헤어비팀과의 인터뷰 중)
- 또한 어울리는 스타일을 찾는 건 전문가의 도움이 필요합니다. 작은 부분만 변해도 얼굴의 전체 분위기가 변하는데 **개인이 이를 판단하기는 어렵습니다**.” (’스타일하우’대표 / 스타일컨설턴트 김송하 2023.07.18 헤어비팀과의인터뷰 중)

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

