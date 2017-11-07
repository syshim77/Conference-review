## Let us: Go! Conference review

**iOS 앱의 접근성 향상하기**
* 접근성(손쉬운 사용)
  - ex) display zoom, classic invert, smart invert, dynamic type, bold text, reduce motion, reachability, assistive touch, voice over etc

**하이브리드 개발 장점**
* 언제든지 즉시 업데이트 가능
  - 앱 재배포할 필요없음
  - 화면 재배치 가능
* xib, storyboard 런타임 중 리소스 형태로 불러올 수 있음
  - xib를 런타임 중에 컴파일해서 쓸 수 있음

**core ML 시작하기**
* 머신러닝의 모델을 이용(학습된 모델 사용)
* 아이폰에서 빠른 속도로 사용할 수 있도록 함
* 장점
  - simple
  - performant
  - compatible
* app making 할 때 장단점
  - 장점
    + userprivacy, data cost, accessibility, server cost
  - 단점
    + 앱 용량 증가

**Keras 사용**
* Keras란?
  - 딥러닝 API(파이썬으로 구현됨)
    + Y = w*X + b 와 같은 식에서 딥러닝이 w와 b를 구해줌(Y: output, X: input)

**디자인 패턴 적용**
* 생성 패턴, 구조 패턴, 행동 패턴으로 나뉨
* 협업할 때 커뮤니케이션 도구로 사용됨
* 종류
  - 팩터리 메서드 패턴
    + 생성 패턴
    + 템플릿 메서드 페턴(리펙토링에 유리)
  - 추상 팩터리 패턴
    + 생성 패턴
  - 빌더 패턴
    + 생성 패턴
  - 어댑터 패턴
    + 구조 패턴
    + 클래스 interface(사용자가 기대하는 다른 interface로 변환)
  - 컴포지트 패턴
    + 구조 패턴
    + 객체 관계가 트리 구조, 부분-전체 계층
* 단키
  - 팩토리 메서드 패턴, 빌더 패턴, 어댑터 패턴
* 처음부터 디자인 패턴을 정하고 코딩하는 것도 좋지만 어려운 경우가 많으므로 추가 스펙에 대한 리펙토링을 통해 작용하는 것도 좋은 방법
* safe area
  - UIViewController 속성

**Interface**
* 추상 클래스 vs 인터페이스 상속 후 오버라이드
  - 추상 클래스: 연관성 있음
  - 인터페이스: 연관성 없음
    + 연관성: 관련있는 특성이나 성질
* 상속
  - 수직 상속: 선천성 성질, 유연한 설계가 어려움
  - 수평 상속: 후천성 능력, 유연한 설계 가능(구현이 결합되어있지 않음)
* 좋은 인터페이스 = 잘 사용되는 인터페이스
  - 인코더/디코더: 인터페이스 정보로만 사용(encoderable, decoderable)
  - custom: 인터페이스 정보로만 사용(equatable)
* swift에서는 protocol

**Codable(property list ~ JSON)**
* swift4에서 추가된 protocol
* codable type
  - property list encoder/decoder
  - JSON encoder/decoder

**functional reactive programming paradigm**
* programming
  - input -> programming -> output
* paradigm
  - 한 시대를 살아가는 사람들의 공통적인 견해
  - 시대가 바뀌면 바뀜
  - 시대의 변화: low memory -> mass production -> concurrency
    + low memory: optimized, data : program = 1 : 1
    + mass production: reusable
    + concurrency: performancy, responsibility
  - functional programming
    + immutable, composition, high-order function, pure function, first class citizen
  - function
    + generator: output만 존재
    + function: input, output 둘 다 존재
    + consumer: input만 존재
  - data 중심에서 function 중심으로 paradigm이 변화됨
* reactive
  - generator(observable)에서 consumer(subscriber)로 operator(data/event)를 사용하여 stream으로 이동
  - 순서대로 읽히고 순서대로 동작하도록 코딩(stream과 stream 연결)
  - rxSwift
* functional
  - side effect 없도록 programming 하는 paradigm

**Test Driven Development iOS에 적용**
* TDD
  - step 1: 테스트 함수 작성
  - step 2: 실제 코드
* test 종류
  - unit Test
  - integration test
