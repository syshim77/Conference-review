# Let Us Go! 2019 Spring

1. 스토리보드 없이 UI 만들기
  - 용어
    + XIB: NIB이 xml 기반으로 바뀐 것
  - 코드 vs 인터페이스 빌더
    + 왜 인터페이스 빌더를 선택하지 말아야하는가?
      * 머지 컨플릭트 문제
      * 재사용 문제
      * 발견 가능성 저하
    + 왜 코드를 선택해야하는가?
      * 머지 컨플릭트 쉽게 해결
      * 인터페이스 빌더로 추가할 수 없는 것이 있음
      * 모든 설정을 한 눈에 볼 수 있음
      * 내가 지금 무엇을 하고 있는지 보다 정확히 알 수 있음
    + 왜 코드를 선택하지 말아야 하는가?
      * 이런 상황은 없음
  - 오토레이아웃 팁과 도구
    + 스냅킷
    + UIStackView(+ UIScrollView), UILayoutGuide
    + Named Views
    + Xcode Visual Debugger, Reveal, wtfautolayout.com
2. try! Swift 2019 후기
  - Day 1,2: 세션
    + 일반 세션 + 라이트닝 토크
  - Day 3: 워크샵
  - 좋았던 점
    + 상대적으로 다양하고 깊은 주제들의 세션
    + 해외를 다녀오는 여행으로도 만족도 높음
    + 그곳의 한국인 전부가 iOS 개발자이므로 인맥 교류 활발
  - 아쉬운 점
    + 언어만 된다면 다양한 국적의 사람들과 교류 가능
    + 귀국 후 시간이 부족해서 내 것으로 만드는 시간이 모자람
3. TEXTURE
  - iOS framework built on top of UIKit
  - storyboard or xib(nib) 등 없이 코드로 UI를 그리는 프레임워크
    + 빠르고 좋음
  - 장점
    + 코드
    + 재사용이 용이(모듈화)
    + 반응, 랜더링 빠름(내부적으로 설계 잘되어있음, thread 안전성)
    + 협업에 용이
    + 다른 코드로 그리는 도구들에 비해 가독성이 좋음(FlexBox)
    + AppCode & Xcode 동시에 사용 가능
  - 단점
    + 러닝커브 조금 있음
    + 자료가 적음
    + 문서나 예제에 Object-C가 많음
4. RxFlow 시작하기
  - navigation framework(화면이동 프레임워크)
  - based on coordinator pattern
    + navigation flow, model mutation
    + ViewController를 고립되게해서 재사용 가능하게 함
  - 6가지 키워드
    + Flow, Step, Stepper. Presentable, Flowable, Coordinator
5. iOS 환경에서 SOLID 연습하기
  - Why?
    + 결합도는 낮게, 응집도는 높게
  - SOLID란?
    + SRP(단일 책임 원칙), OCP(개방 폐쇄 원칙), LSP(리스코프 치환 원칙), DIP(의존관계 역전 원칙), ISP(인터페이스 분리 원칙)
    + 객체 지향 설계
      * 최대한 인스턴스 등을 공개하지 않고 객체로 만들어서 객체에 접근하도록 설계
    + ViewController의 역할을 나눌 수 있음
6. 상속에서 프로토콜로
  - 상속에서 프로토콜로
    + Protocol Extension
    + Associated Objects
  - 프로토콜 활용
  - 기능별로 잘 분리
7. A Framework Driven Development
  - 기존 개발 방법
    + 파일 단위로 레이어를 분리
    + 소스 코드의 집중화
    + 라이브러리를 직접 관리
    + 오픈소스, 외부 SDK 직접 사용
    + 빌드 속도가 비교적 빠름(Object-C)
    + 의존성 관리도구를 지원하지 않는 Xcode
    + 소규모 프로젝트가 대부분
    + 코드, 파일 개수가 많아질수록 느려짐(Swift)
    + 응집도 감소, 결합도 증가, 부수효과 증가
    + 관리 비용 높음(관리지점 늘어남)
  - 프레임워크 주도 개발
    + 프레임워크로 레이어를 나누어 개발
    + 외부에 코드를 노출 여부를 결정 가능(public, open vs internal)
    + 다른 프레임워크와 격리화
    + 응집도 증가, 결합도 감소, 부수효과 감소
    + 각 프레임워크에서 빠르고 많은 테스트 수행
    + 메인 프로젝트의 빌드 속도가 비교적 빨라짐(프레임워크 빌드 후 메인 프로젝트 빌드)
    + 협업 시 충돌이 덜 발생함
    + but 프레임워크를 만들어야함
    + 기존 코드의 커플링을 제거하면서 리팩토링 해야함
    + 수많은 프레임워크가 생길 수 있음
  - 프로젝트 재구성
  - 프로젝트 리팩토링(Network)
8. Immutable Data
  - What & Why?
    + let: immutable, var: mutable
    + predictability, coverage(testability), race condition(thread safe), variations, unfamiliar, memory wasting, low performance
    + maintainable, performance decrease
  - How?
    + Data 안에 feature
      * copy(copy on write), extension, setter/getter, lens, lensable
    + feature 안에 Data
      * function, functor, monad
