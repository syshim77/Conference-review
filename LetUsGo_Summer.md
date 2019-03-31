## Let Us Go Conference Summer(2018.07.21)

1. Xcode에서 디버깅하기
  - 디버깅이란?
    * 버그(오류)를 잡기 위한 것
  - Breakpoint
    * breakpoint를 걸어두면 한줄씩 진행되다가 그 부분에서 멈추게 됨
    * 라인에 숫자표시를 하면 어떤 라인에서 오류가 발생했는지 확인 가능
    * 디버깅에 있는 버튼들의 의미(왼->오 순서)
      + 숨길 수 있는 버튼, breakpoint disable할 수 있는 버튼, 다음 breakpoint까지 진행하는 버튼, 다음 줄로 이동하는 버튼, 함수가 있다면 함수 안으로 들어가는 버튼, 함수에서 빠져나오는 버튼
    * breakpoint navigator
      + 현재 걸려있는 모든 breakpoint가 나타남
    * general breakpoint
      + 미리 만들어둔 Breakpoint
      + throw가 발생했을 때, 충돌이 일어났을 때, 어떤 메서드에 글을 입력하여 사용하고 싶을 때
  - lldb
    * Xcode에 기본적으로 내장되어있는 디버거
    * gdb보다 많은 유용한 기능 보유
    * 기본적인 gdb 스타일의 명령어를 대부분 사용 가능
    * lldb command
      + pr, p(print): value 출력할 때(주소값)
      + e(expr): 프로그램 직접 값을 수정 가능(값 변환할 때)
      + po(print object): 들어있는 값만 정확하게 나타남
      + e: 인자를 받아들임
      + p == e --
    * 변수 선언
      + e let $a = 2
      + p $a * 19
    * closure
      + fr v $0
  - Symbolicate
    * dSYMS
      + crash log를 알 수 있는 말로 바꿀 수 있도록 하는 파일
    * 아카이브 하는 곳에 두번째에 crash
  - ETC
    * view hierarchy
      + 버튼을 누르면 계층 구조를 볼 수 있게 되어있음
      + hidden, constants, wire frame or view
    * DEBUG
      + debug나 release할 때만 사용하고 싶은 경우 정의 가능
      + build setting -> -D DEBUG 라고 쓰여있고 코드에서는 #if DEBUG #endif로 사용 가능  

2. 코드 응집도
  - advantages
    * easy to read, follow, understand, find, maintenance
  - 흔히 놓치는 케이스들 코드 응집도를 높여서 코딩하는 법
    * case1: data + logic + ui
    * case2: data setter
      + 변수에 중복 코드 내용 적어두고 함수에서는 변수 바뀌는 부분만 적음
    * case3: overrides
      + closure 사용
    * case4: selector
      + wrapper 사용
    * case5: delegate
      + wrapper 사용
  - RxSwift 사용하여 응집도를 높일 수 있음  

3. observable operator 적재적소 사용하기
  - FlatMap
    * FlatMapFirst, FlatMapLatest
  - side effect
    * 안되는 곳: map, FlatMap
      + WithLatestFrom으로 side effect 해소
  - window
  - scan
  - switch  

4. iOS TDD 실무에 적용하기
  - 실패하는 테스트
  - 가장 빨리 성공하게
  - 리팩토링
    * 중복을 제거하고(상수중복. 의미중복)
    * 의미를 드러낸다(명확하게 한다)  

5. Texture Reactive wrapper 만들고 응용하기  

6. 미리보는 Marzipan
  - sneak peek
  - AppKit과 UIKit이 동시에 돌아갈 수 있게 됨
  - marzipanify
  - ios 앱을 macOS에서 실행시켜보기
