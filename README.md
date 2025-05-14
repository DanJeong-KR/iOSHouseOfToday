# 오늘의 집 클론 프로젝트
Backend, Frontend, iOS까지 총 10명이 한 팀으로 구성하여 하나의 서비스를 프론트부터 서버까지 만들어 보는 프로젝트<br>
현재 매우 빠르게 성장중인 스타트업인 버킷플레이스가 서비스하고 있는 인테리어 플랫폼 `오늘의 집`을 클론한 프로젝트  <br>
* 기간 : 2019.07.01 ~ 2019.08.24 (8주)
* 소속 : 회식First팀 (Backend 4명, Frontend 3명, iOS 3명)
* 역할 : 팀장으로써 다른 팀과의 의사소통 전반, 자체 로그인과 소셜로그인(카카오, 구글, 네이버), 커스텀 UI(CustomCatetoryTabBar), 마이페이지와 사용자 프로필 전반 담당.
* 사용기술
  * Swift5
  * 라이브러리 : SwiftLint, Kingfisher, SnapKit
  * 외부 SDK : KaKaoSDK, googleSDK, naverSDK
  * 협업 툴 : Trello, Slack, Github
  * 소스 : Dynamic AutoLayout, Callback

<br>

---

### 설계
* RestAPI 설계(Backend 팀과 함께 설계)

<a href="/assets/design_API.gif" target="_blank"><img src="/assets/design_API.gif"></a>

* 플로우 차트 - AdobeXD

<a href="/images/design/design_adobeXD.gif" target="_blank"><img src="/images/design/design_adobeXD.gif"></a>

* 명세서 작성 - Keynote

<a href="/assets/design_keynote.pdf" target="_blank"><img src="/images/design/design_keynote.gif" width=600></a>

* 데이터 모델 설계 - 마인드맵

<a href="/assets/design_mindmap.pdf" target="_blank"><img src="/assets/design_mindmap.png"></a>

<br>

---

### 스크린샷

<a href="/assets/login.gif" target="_blank"><img src="/assets/login.gif" width="250"></a>
<a href="/assets/home.gif" target="_blank"><img src="/assets/home.gif" width="250"></a>
<a href="/assets/store.gif" target="_blank"><img src="/assets/store.gif" width="250"></a>

<br>

---

### 데모영상
* iOS 부분

<a href="https://youtu.be/gRF4_6vAdzI" target="_blank"><img src="/assets/thumnail.png"></a>

* Web 부분 (클릭 시 웹페이지로 이동)

<a href="http://ohome.co.kr/community" target="_blank"><img src="/assets/demo_webpage.png"></a>

<br>

---

### 협업
* [Trello](https://trello.com/b/AZbLTdbp)

<a href="https://trello.com/b/AZbLTdbp" target="_parent"><img src="/assets/teamwork_trello.png"> </a>

* [Github](https://github.com/final-project-team01) (FDS : Backend / WPS : Frontend / iOS)

<a href="https://github.com/final-project-team01" target="_blank"><img src="/assets/teamwork_github.png"> </a>

<br>

---

<br>

### 문제해결 아카이브
* Backend와 협업할 때 초반에 API 설계와 변수 네이밍 맞추기와 같은 작업을 함께 진행하는 것이 좋다는 조언을 받음
  * iOS 앱의 설계를 빠르게 완료해야 Backend팀에게 어떤 데이터 모델이 필요하다고 설득하고 맞춰나갈 수 있다고 판단하고 iOS 앱의 설계를 빠르게 진행
  * AdobeXD로 플로우차트를 설계하고 Keynote로 명세서 작성을 작성한 후 마인드맵으로 데이터모델까지 설계한 뒤 이 자료들을 토대로 Backend 팀과 RestAPI 설계를 같이 할 수 있었고 특정 시점에 적절한 데이터를 요청하는데 매끄럽게 진행

*  iOS는 3명이 함께 작업하는데 어떻게 프로젝트를 관리해야 효율적으로 작업할 수 있는지에 대한 고민
  * 프로젝트는 Github로 관리하고 팀 내에서 프로젝트 매니저를 뽑은 후 팀원들은 프로젝트를 fork 한 후 변경된 사항을 Pull Request 하는 방식으로 진행
  * master branch는 최종 버전용으로 유지하고 프로젝트 유지는 develop branch에서 개발은 feature branch에서 진행하는 등 branch를 적극 사용해서 안전성을 고려

* Backend, Frontend 팀과의 의사소통 문제 발생. 다른 팀이 어떤 일을 하고 있는지 모르는 문제
  * Trello를 활용하여 모든 팀원이 참여하는 Board생성 및 각 팀이 하고 있는 작업목록과 그에 따라 팀 Label을 붙임으로써 팀 간 실시간 의사소통 문제를 해결할 수 있었다.
* 애플에서 기본적으로 제공하는 UI가 아닌 UI를 만들어야 하고 그 UI를 여러 화면에서 재사용해서 구현해야 하는 문제.
  * 한명이 커스텀 UI(CustomCatetoryTabBar)를 추상적으로 재사용 가능하게 만드는 것을 집중적으로 담당해서 구현함으로써 해결.
* 자체 로그인 기능 뿐만 아니라 소셜로그인(카카오톡, 네이버, 구글)기능을 구현해야 하는 문제.
  * 로그인 기능은 Token이라는 권한을 서버와 주고 받아야 하기 때문에 Backend 개발자와의 실시간 소통이 중요하므로 Backend팀에 로그인 담당을 정해달라고 요청해서 실시간 소통하며 로그인 문제 해결.
  * 서버에서 구축된 Token 시스템을 기반으로 Kakao, Google, Naver의 SDK 문서를 공부하여 소셜로그인 해결.

* iOS 팀 3명이 하나의 프로젝트를 수정하기 때문에 코드가 통일성이 부족해지는 문제
  * Swift Style Guideline을 참고하여 자체적인 Style Guideline 작성해서 코드의 통일성을 고려
  (changsic.github.io/SwiftAPIDesignGuidelines/)

* 서로 어떤 작업을 하고 있는지 잘 몰라서 생기는 의사소통 문제와 오해.
  * 하루 30분씩 코드리뷰 시간을 정해서 서로 어떤 작업을 하고 있는지를 공유하는 시간 지정.
  * Commit 메세지 규칙을 정함으로써 직관적으로 서로의 작업을 공유.(changsic.github.io/CommitMessage/)
