# **Subprice**
<br>

![SubPrice](https://user-images.githubusercontent.com/104040502/224969433-8a07f396-5ec7-43fc-b4be-2709eb81cd1e.png)

<br>
<br>

# 🚀 **프로젝트 개요**
## 💠 프로젝트 목적
> 영상, 쇼핑, 취미, 교육을 포함한 광범위한 분야에서 구독 시장의 규모가 커졌고, 대부분의 구독형 서비스는 사용자가 결제수단을 등록하면 매월 자동으로 결제되는 시스템을 가지고 있습니다. 구독 중인 서비스들을 한눈에 확인하여 관리하고 결제 알림을 통해 불필요한 지출을 줄이기 위해 **SubPrice** 서비스를 개발하게 되었습니다.

<br>

## ✅ 프로젝트 요약
### 1. 구독 정보 조회  
### 2. 현재 구독 중인 서비스 정보 등록 및 관리, 알림 설정
### 3. 스케줄링을 통한 구독 갱신 알림 메일 발송  

<br>
<br>


# ⚙️ **사용 기술**
## 🛠️ 아키텍처
![architecture](https://user-images.githubusercontent.com/104040502/224969565-2e6b9e2d-01a7-4072-a37d-09aaa64ca6d9.png)

<br>

## 📌 기술 스택
![image](https://user-images.githubusercontent.com/91922127/207784519-491218c0-a47f-4247-bc9a-9a88b0ba0cc2.png)

### FrontEnd & BackEnd
| <center>Application</center> | <center>Description</center>
| ---------------------- | ----------------------------
| **HTML**                   | Template 구성
| **CSS**                    | 화면 스타일 적용에 사용
| **Javascript**             | 동적인 화면처리에 사용
| **Python**                 | 백앤드 작성 언어
| **Django**                 | Model, Template, View 구성
| **NGINX**                  | 정적 요청 처리, 동적 요청을 WAS로 전달
| **UWSGI**                  | 웹 서버와 WAS 사이의 커뮤니케이션 담당
| **PostgreSQL**             | Database

<br>

### Deploy
| <center>Service</center> | <center>Description</center>
| ---------------------- | ----------------------------
| **AWS EC2**                | 클라우드 환경의 배포 서버
| **Docker**                 | 배포할 웹 애플리케이션 이미지 빌드, 컨테이너 실행
| **AWS S3**                 | 정적 파일 보관 및 정적 웹사이트 호스팅
| **AWS RDS**                | 클라우드 환경의 데이터베이스 서버

<br>
<br>

# 🚥 **프로젝트 진행**
## 🌞 프로젝트 목표
1. 웹 서비스의 구조 이해 및 계획한 서비스 구현
2. 객체지향 프로그래밍에 대한 이해 및 프로젝트 설계
3. 사용한 모듈 및 라이브러리에 대해 타당한 근거를 바탕으로 한 코드 작성
4. 발생한 에러 코드에 대한 분석 및 개선 과정 필수 정리
5. 명확한 업무 분장 및 PR 시 코드 리뷰 필수 진행을 통한 효율적인 프로젝트 진행

<br>

## 💡 중점 고려사항
### HTML, CSS
  - 기본 문법 숙지 및 이를 활용한 화면 구현
### Javascript, jQuery, Ajax
  - 기초 문법을 응용한 동적 게시판 구현
### Python, Django
  - CBV, FBV의 기본적인 구조 이해 및 코드 작성
  - Django Form, View, Decorator에 대한 심화 이론 학습 및 활용
  - ORM을 응용한 쿼리 조회 및 속도 개선에 대한 고민
### AWS EC2, S3, RDS
  - 웹 서버 구조 및 각 서비스의 역할에 대한 근본적인 이해
  - 클라우드 환경에서의 배포 실습
### Celery, Redis, Docker
  - Celery, Redis를 이용한 비동기 메시지 큐 구현
  - Docker를 통한 이미지 빌드 및 Docker-Compose를 이용한 다수의 컨테이너 관리
### 코드 컨벤션 및 브랜치 전략
  - 코드 컨벤션 : [좋은 git commit 메시지를 위한 영어 사전](https://blog.ull.im/engineering/2019/03/10/logs-on-git.html) 참조
  - 브랜치 전략 : 
    - 개별 로컬 환경에서 `develop` 브랜치로부터 작업 단위로 해당 작업의 성격 및 목적에 맞는 브랜치 명으로 새로운 브랜치를 생성하여 작업을 진행 <br>
      - **작업별 브랜치 명칭 리스트** <br>
        : `feature` (기능), `bugfix` (버그 수정), `hotfix` (긴급 버그 수정), `refactor` (리팩토링), `docs` (문서), `test` (테스트), `conf` (설정)
    - 작업이 완료된 브랜치는 리모트 환경의 동일 브랜치 명으로 푸쉬하고 리모트의 `develop` 브랜치에 PR을 생성하여 코드 리뷰 후에 병합
    - 병합이 완료된 브랜치는 즉시 삭제
    
    - `develop` 와 `main` 브랜치 간 commit 수 차이가 10개 이상 벌어지면 `main` 브랜치에 PR을 생성하여 병합
### 문서 관리
  - Notion을 이용한 프로젝트 관리 : 내용 공유 및 팀 회의 내역 정리
  - Notion의 Database 기능을 활용한 칸반 보드 운영 : 개인별 담당 업무 진행 현황 관리

<br>

## ❓❕ 기술적 이슈 및 해결 과정
- Django forms를 통해 생성한 Form을 이용한 데이터 수정 시, 기존 데이터가 로드되지 않는 부분
  - instance를 객체로 지정하여 기존 데이터를 로드하는 ModelForm과는 달리, 일반 Form의 경우에는 initial에 데이터를 dictionary로 지정 
- Nested Relationships를 갖는 모델들에 대한 Form 생성
  - Form을 이용하여 여러 모델에서 필요한 필드를 모두 선언 → formset을 이용한 개선 가능
- 비동기 스케줄링 기능 구현
  - Celery, Redis, Docker를 사용하여 해결
- Docker를 이용한 컨테이너 형태로의 배포
  - 현재는 Django로 생성한 웹 애플리케이션을 2중으로 실행하는 구조 → 추후 개선이 필요

<br>
<br>


# 💭 **DB ERD**
![image](https://user-images.githubusercontent.com/91922127/207561038-2df36c61-1950-4d51-91e9-54f437fcfb28.png)
## 🏃‍♂️ User
| <center>Table</center> | <center>Description</center>
| ---------------------- | ----------------------------
| User                   | 사용자 개인 정보

<br>

## 🔎 Subscription
| <center>Table</center> | <center>Description</center>
| ---------------------- | ----------------------------
| Type                   | 결제 유형 정보
| Company                | 결제사 정보
| Billing                | 사용자의 결제 정보
| Category               | 구독형 서비스의 카테고리 정보
| Service                | 구독형 서비스 정보
| Plan                   | 구독형 서비스 내 구독 유형 정보
| Subscription           | 사용자의 구독 서비스 정보, 결제 정보, 구독 기간 정보

<br>

## 🔔 Alarm
| <center>Table</center> | <center>Description</center>
| ---------------------- | ----------------------------
| Alarm                  | 결제 예정 알림 사용 여부 및 알림 디데이 정보
| AlarmHistory           | 알림 메일 발송 내역

<br>
<br>

# 📝 **URL List**
![url](https://user-images.githubusercontent.com/104040502/224969990-51cdc6d0-92fd-454a-96d1-f001be4e292f.png)

<br>
<br>

# 💻 **제공 기능**
## 🏳‍🌈 Common
|로그인|회원가입|
|:------:|:------:|
|![01  로그인](https://user-images.githubusercontent.com/104040502/224979213-71100650-f01d-4e7a-90ea-99e14db75ce2.gif)|![02  회원가입](https://user-images.githubusercontent.com/104040502/224979272-653c4ed5-938b-4fd0-aa3d-27ffb521e9c1.gif)|


## 🏠 Main
|구독 등록|구독 수정|
|:------:|:------:|
|![03  구독 등록](https://user-images.githubusercontent.com/104040502/224979329-f14b8915-f0f3-4458-9134-55b4cab7ece3.gif)|![04  구독 수정](https://user-images.githubusercontent.com/104040502/224979368-ce1c0fba-880e-47f5-bc51-3fee79a4d0d9.gif)|


## 🧐 History & Profile
|구독 삭제|프로필 |
|:------:|:------:|
|![05  구독 삭제](https://user-images.githubusercontent.com/104040502/224979402-09e1fa19-c12e-4f7b-b0ef-80115866a79b.gif)|![05  프로필 변경](https://user-images.githubusercontent.com/104040502/224979426-04399126-3da1-4270-ad49-942bf7b5f4b8.gif)|

<br>

### **배포 링크** : 추후 추가 예정
### **시연 영상** : 추후 추가 예정
