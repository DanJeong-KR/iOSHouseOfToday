# 오늘의 집 클론 프로젝트
패스트캠퍼스에서 진행하는 팀 프로젝트 <br>
Backend, Frontend, iOS까지 총 10명이 한 팀으로 구성하여 하나의 서비스를 프론트부터 서버까지 만들어 보는 프로젝트<br>
현재 매우 빠르게 성장중인 스타트업인 버킷플레이스가 서비스하고 있는 인테리어 플랫폼 `오늘의 집`을 클론한 프로젝트  <br>
* 기간 : 2019.07 ~ 현재
* 소속 : 회식First팀 내 iOS개발 팀
* 역할 : iOS팀 팀장으로써 다른 팀과의 의사소통 전반, 자체 로그인과 소셜로그인(카카오, 구글, 네이버), 커스텀 UI(CustomCatetoryTabBar), 마이페이지와 사용자 프로필 전반 담당
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
  * Backend 개발자와 협의해서 프로젝트를 시작하기 전에 REST API를 함께 설계해서 프로젝트를 매끄럽게 진행할 수 있었다.
* Github로 프로젝트 관리를 어떻게 효율적으로 할 수 있을지 고민.
  * master 프로젝트를 생성하고 팀원이 fork 하는 방식으로 해결.
* Backend, Frontend 팀과의 의사소통 문제 발생. 다른 팀이 어떤 일을 하고 있는지 모르는 문제
  * Trello를 활용하여 모든 팀원이 참여하는 Board생성 및 각 팀이 하고 있는 작업목록과 그에 따라 팀 Label을 붙임으로써 팀 간 실시간 의사소통 문제를 해결할 수 있었다.
* 애플에서 기본적으로 제공하는 UI가 아닌 UI를 만들어야 하고 그 UI를 여러 화면에서 재사용해서 구현해야 하는 문제.
  * 한명이 커스텀 UI(CustomCatetoryTabBar)를 추상적으로 재사용 가능하게 만드는 것을 집중적으로 담당해서 구현함으로써 해결.
* 자체 로그인 기능 뿐만 아니라 소셜로그인(카카오톡, 네이버, 구글)기능을 구현해야 하는 문제.
  * 로그인 기능은 Token이라는 권한을 서버와 주고 받아야 하기 때문에 Backend 개발자와의 실시간 소통이 중요하므로 Backend팀에 로그인 담당을 정해달라고 요청해서 실시간 소통하며 로그인 문제 해결.
  * 서버에서 구축된 Token 시스템을 기반으로 Kakao, Google, Naver의 SDK 문서를 공부하여 소셜로그인 해결.
* 3명이 하나의 프로젝트를 수정하고 작성하기 때문에 코드가 통일성이 부족하고 지저분해 지고 git으로 commit 할 때 직관적으로 이해하기 힘든 문제 발생
  * 변수 네이밍 작성 규칙과 Commit 메세지 작성 규칙을 작성함으로써 코드를 조금 더 통일성 있고 깔끔하게 작성할 수 있게 되었다.
