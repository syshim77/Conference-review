## Let'Swift Conference review

**키노트**

**What's New Swift 4**
* Multi-Line String Literals
* String
  - Substring
  - StringProtocol
* Private
  - private, fileprivate
* Smart KeyPaths
  - KeyPaths
  - KVO
* Existentials
  - class and subtype
* One-Sided Ranges
  - Pattern Matching
* Limiting @obj inference
* Codable
  - Nested, Codable, Decodable
  - Array, Dictionary
  - Change Key Names

**Swift vs Kotlin**
* Swift
  - iOS 언어
* Kotlin
  - 안드로이드 언어

**Concurrency in Swift**
* Parallelism <-> Concurrency
* Thread
  - critical section, share data, syncronization
    + race conditions, dead lock, starvations, IO waiting, rendezvous problem
* Darwin, libkern, stdatomic.h
* Foundation
  - NSThread, NSTimer, NSOperation, GCD(Grand Central Dispatch), NSLock

**Metal 기반 특별한 UI/UX 제공하기**
* GlitchLabel
  - CoreAnimation, CoreGraphic 등을 이용하여 구현
* MetalKit + MSL(Metal Shader Language)
  - 퍼포먼스 부족, 구현 힘듬, 코드 난잡 문제 해결
  - GPU에 바로 접근, 비교적 쉬운 이미지 처리, Shader 코드 분리
* Post Processing
* MSL 스펙 문서
  - 단일 텍스쳐
  - 텍스쳐 + 텍스쳐
  - View

**iOS 11 ARKit 시작하기**

**토스의 개발/배포 환경**
* 앱 쪼개기
  - 4개의 서버별로 앱 만들기
  - 관리, 유지보수하기 쉬워짐
* 제휴 SDK 관리하기
  - .xcodeproj 최대한 덜 건드리기
  - 제휴 SDK 이력 업데이트 관리 쉽게됨
* 배포 쉽게하기
  - fastlane
  - fabric beta

**Serverless vs Server-side Swift**
* Firebase, node(서버구축)
* Swift 서버 도전

**RxSwift 활용하기**

**ReactorKit으로 단방향 반응형 앱 만들기**

**비밀의 숲**
