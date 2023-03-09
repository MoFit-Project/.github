[![CI/CD](https://github.com/MoFit-Project/Backend/actions/workflows/gradle.yml/badge.svg)](https://github.com/MoFit-Project/Backend/actions/workflows/gradle.yml)


# Mofit

### Project Tech Stack 📚
&#160;   
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=TensorFlow&logoColor=white"/> 
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat&logo=Spring Boot&logoColor=white"/> 
<img src="https://img.shields.io/badge/NGINX-009638?style=flat&logo=NGINX&logoColor=white"/>
<img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=flat&logo=Amazon AWS&logoColor=white"/> 
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=white"/>
&#160;   
<img src="https://img.shields.io/badge/Amazon RDS-527FFF?style=flat&logo=Amazon RDS&logoColor=white"/> 
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=Next.js&logoColor=white"/> 
<img src="https://img.shields.io/badge/GitHub Actions-2088FF?style=flat&logo=GitHub Actions&logoColor=white"/>
<img src="https://img.shields.io/badge/WebRTC-333333?style=flat&logo=WebRTC&logoColor=white"/> 
&#160;   
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=MySQL&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white"/>
<img src="https://img.shields.io/badge/Jira-0052CC?style=flat&logo=Jira&logoColor=white"/>
<img src="https://img.shields.io/badge/Slack-4A154B?style=flat&logo=Slack&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=GitHub&logoColor=white"/>
<img src="https://img.shields.io/badge/GameEngine-Phaser-blueviolet"/>

---

### ✨서비스 소개
```운동은 즐겁게 하자!```


&#160;   
### ✨주요 기능

- WebRTC를 통한 실시간 화상 운동 게임
- TensorFlow를 이용한 모션 체크 


&#160;   
### ✨서비스 아키텍처

![image](https://user-images.githubusercontent.com/105699532/223957920-6ec970cf-f36d-4d02-a7be-14a4aca77427.png)



&#160;   
### ✨기술적 특이점

- GitHub Actions를 이용하여, 클라이언트 및 서버를 자동 무중단 배포를 구축했습니다. Front와 Backend의 GitHub에 Actions의 workflow를 생성해서 job을 설정 후, 빌드 후 도커이미지를 도커 hub에 푸시한 후, 서버에서 docker image를 통해 docker-compose를 수행하도록 구현했습니다.

- Nginx를 이용한 reverse-proxy 구축, https 이용을 위하여 nginx를 통해 reverse-proxy로 client 서버와 api 서버, openvidu 서버가 통신가능하게 했습니다. 클라이언트 서버에서 Nginx를 통해 내부적으로 api들에 대한 분기처리를 했습니다.

- 빈번하게 호출되며, 많은 리소스를 요구하며, 클라이언트에게 전달되는 값이 동일한 랭킹같은 경우 Redis를 이용하여 캐시기능을 구현했습니다. 
  - 구현 전
  ![image](https://user-images.githubusercontent.com/105699532/223959646-939a9005-e6da-4733-9bbe-6ebab3a46fae.png)
  - 구현 후
  ![image](https://user-images.githubusercontent.com/105699532/223959903-7feca271-a128-4cb3-a584-9ba53f0f1470.png)  

- PoseNet을 이용하여, 각각의 게임 및 준비&시작 상태를 모션인식을 통해 동작하도록 했습니다.

  ![image](https://user-images.githubusercontent.com/105699532/223961203-4356d68d-dce5-49c5-9782-416a82edafd0.png)



&#160;   
---
게임 종류

- 싱글

![image](https://user-images.githubusercontent.com/105699532/223953841-6edfb611-468c-4698-9fec-6550d7abaeb2.png)

- 혼자서 하는 종합 운동 세트
- 주어진 세트를 빨리 끝내는 것을 목표로합니다.


***

- 멀티 

![image](https://user-images.githubusercontent.com/105699532/223954197-c08d9cda-4d73-498e-8b80-a179e6dc4ebb.png)

- 게임 종류에 따라 점핑 잭, 스쿼트를 상대 보다 많이 할 때 승리할 수 있습니다.


***

- 대기방

![image](https://user-images.githubusercontent.com/105699532/223955025-461ea9a2-9b28-43b3-bf89-7f47f498289c.png)

- 랭킹

![image](https://user-images.githubusercontent.com/105699532/223956798-f55ce215-5242-4443-b49b-3844c28c5e18.png)


---

### 👨‍👩‍👧 협업 툴

#### 📜 Jira
협업 및 일정, 업무 관리를 위해 Jira를 이용하였습니다. 매주 월요일 오전 회의에서 한 주동안 진행되어야 할 주 단위 계획을 짜고, 진행할 이슈들을 스프린트를 만들어 등록했습니다. 스프린트는 일주일 단위로 진행하였습니다. 세세한 일정들은 백로그를 이용해서 체크 했습니다.

#### 📜 Slack
모두가 봐야할 공지, 링크, 회의록 등을 관리했습니다. 또한 Jira와 연동하여 Jira에 등록한 스프린트의 진행사항에 대해 체크하며 진행했습니다.



### 📝ERD
![image](https://user-images.githubusercontent.com/105699532/223963125-35081bd9-4a8f-4c60-a782-d5093859c6f8.png)



---
### 팀원 소개
![image](https://user-images.githubusercontent.com/105699532/223963462-c9992e18-b026-44c1-b929-b4e01d6d7924.png)


👩‍👩‍👧‍👧 팀원 역할
---
- 안주홍

- 김현우

- 제갈인하
  - Service Architecture 구축
  - GitHub Action을 이용한 Front/Back CI/CD 구축
  - Nginx를 이용한 리다이렉트 및 reverse-proxy 구현
  - Front/Back Docker Image 빌드위한 Dockerfile 및 Docker-compose 구현
  - openvidu를 통한 WebRTC구현
  - openvidu서버 on-premise로 배포
  - Spring Boot를 사용해 백엔드 API 구현
  - Spring Boot를 이용한 JWT 인증 로그인 구현
  - Spring Boot를 이용한 Openvidu 통신 구현
  - Spring Boot를 이용한 비동기 시간 처리 구현
  
- 박진석

- 이도윤

