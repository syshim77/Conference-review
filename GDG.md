## GDG DevFest Seoul 2017 Conference review

**MVC부터 MVVM, 단방향 데이터 흐름까지**
* Forms & Controls
  - form: screen layout(target, actual, variance등의 컨트롤을 구성)
  - control: target, actual, variance
    + actual: input
    + target: getText, 값 비교, setText, setTextColor
  - Android에서는 activity/fragment와 view의 관계와 다를바 없음(form -> activity, control -> fragment)
* Data Binding
  - MVVM의 전유물이 아님
  - forms & controls나 MVC에서도 사용 가능
  - 단방향 바인딩, 양방향 바인딩
    + 순환 참조때문에 오랫동안 양방향 바인딩을 사용하려하지 않음 -> 타임 스탬프로 변경 시점을 비교함으로서 해결
* Separated Presentation
  - Separated Presentation + Observer: MVC
* MVC
  - 고전적인 MVC에서는 view와 controller가 여러개였고 model이 중요한 역할을 함
  - PM(presentation model): 디자인에 관한 모델이 있음
    + controller가 없는 경우가 많음
    + PM과 VM의 가장 큰 차이: data binding
  - passive model
* MVP
  - form&controls과 MVP를 합치려는 IBM의 노력
  - view는 control 수준으로 다루고 view/controller 구분은 제거
  - 실제 상호 작용은 분리된 presenter 객체에 넘겨 처리
  - view가 model을 다루는 방식에 따라
    + supervising controller: view가 model에서 옵저버 패턴을 통해 가져감
    + passive view: presenter가 view의 갱신을 책임짐
  - Android에서는 activity와 부속 view 객체들을 통채로 MVP의 view로 잡음
* FLUX
  - action이라는 데이터를 보내면 dispatcher가 store에게 보내고 view가 store가 가지고 있는 데이터를 화면에 표시하는 구성
  - 단방향 아키텍쳐라고 부름
  - dispatcher: 이번트 버스, RxJava 스트림, 반응형 DB로 구성 가능

**1시간만에 만드는 음성인식 인공지능 챗봇**
* 챗봇의 원리
  - 챗봇: 채팅과 로봇의 합성어
    + 인공지능을 기반으로 사람과 대화하는 프로그램
    + 인간의 언어를 흉내내어 인간의 질문에 답하는 형식(능동적인 대화가 아님)
    + 메신저 상에서 사람처럼 행동(제한된 역할)
* 챗봇을 만들 때 알아두어야 할 것
  - 대화의 범위를 제약
  - 대화의 분위기를 파악
  - 언어적인 이해와 경험 향상(머신러닝 이용)
* 챗봇의 대화 방법
  - 대화의 의도(intent)
  - 대화의 재료(entity)
  - 대화의 분위기(context)
  - 대화의 경험을 쌓고 응용(training)
* 스케치(어떤 챗봇을 만들까?)
  - 챗봇에게 무엇을 가르칠까?
    + 장소와 역할을 정의
    + 대화에 대한 스케치
* 데이터 모으기
  - 구글링을 통한 데이터 수집
  - 데이터 가공 및 정제
* 대화하는 법 가르치기
  - entity 입력
  - 대화의 기술 가르치기
    + 기본적인 인사법(보통은 기본 내장)
    + 의도(intent) 등록
    + 분위기(context) 처리
* 똑똑하게 만들기
  - 예외 처리
    + 학습 및 훈련을 하며 재학습
  - 자체 ML 학습
* 음성 지원 및 다양한 입출력 채널
  - Google Assistant
  - Messenger
* [source code](https://github.com/javalove93/dialogflowdemo)

**React와 Django로 만드는 Progressive Web App**
* BOXture
  - web application
* PWA
  - 웹의 장점과 앱의 장점을 결합한 웹앱
  - 기존의 스펙들을 이용
  - 특성
    + progressive
    + 반응형
    + 설치 가능 & 앱과 유사
    + 항상 최신 상태 유지
* BOXture 진화시키기
  - 모바일 접근성 향상
    + app shell 캐시하기(service worker가 캐시)
    + Cache-First Strategy(최신 상태로 업데이트)
    + service worker를 브라우저에 등록하기(create-react-app에서 기본 제공)
    + 캐시할 자원 등록하기(create-react-app이 만들어줌, sw-precache)
  - 홈 화면에 추가해서 앱처럼 쓰기
* Service Worker
  - 브라우저와 서버 사이의 미들웨어
  - 브라우저 기본 캐시 vs 서비스 워커
    + first visit, cleared, purged, expired, revved
  - URL을 통해 자원을 캐시
* SW-Precache
  - 새로운 자원이 나왔을 때 최신 상태로 캐싱할 수 있도록 함(자동 버저닝)
  - 2MB가 넘는 파일은 제외하고 캐시함
* Web Push 수신의 종류
  - 포어그라운드 푸쉬: 보고있을 때
  - 백그라운드 푸쉬: 다른 페이지를 보고있을 때, 안드로이드 화면을 꺼 놨을때
* [react와 django 이야기](https://github.com/milooy/react-django-pwa-kit)

**Github와 CloudFlare를 이용한 무료 고성능 웹 어플리케이션 호스팅**
* A Brief History of Web Dev
  - HTML(HyperText Markup Language)
  - CSS(Casacading Style Sheets)
  - JavaScript: DOM을 핸들링하기 위한 목적으로 만들어진 언어
  - WAS(Web Application Server)
  - Web Application
    + SPA(Single-Page Application)
* JAM Stack
  - modern web development architecture
  - based on client-side javaScript, reusable APIs, pre-built Markup
  - Static Site Generator
    + generate HTML website as an output
    + 블로그, API 문서, 개인 및 회사 홈페이지 제작 목적으로 사용하고 운영이 쉬움
    + 컨텐츠와 스타일의 분리
    + StaticGen
  - profits
    + better performance
    + low cost
    + higher security
    + better developer experience
