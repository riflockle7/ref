# Google for Mobile 2018 I/O RECAP

때는 바야흐로 6월 25일!!  
오늘도 개발에 대한 열정을 감추고 Google for Mobile 2018 I/O RECAP 행사에 참여한다! (휴가는 Bonus~)  
![image](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_introduce_signification.jpeg?raw=true)
#### 그 와중에 소소한 YAPP 부심 넘치는 인증샷을 남겨본다 :)


## 0. 서론
### 0_1. Google I/O 최신 기술 총 정리
- keyPoint
  - AI의 대중화  
    - Google Photo  
      AI를 활용하여 사진을 더 예쁘게 캡쳐
    - Adaptive Battery  
      사용자의 앱 이용 방식을 학습하고 자주 사용하지 않는 앱의 전력 소모 기능들을 제한
    - ML Kit  
      모바일 개발자를 위한 머신러닝 kit
      
  - 디지털 웰빙  
    - DashBoard  
      앱 사용 성향 등을 분석
    - AppTimer  
      앱 사용 시간 등을 설정
    - WindDown  
      방해금지 모드와 비슷
      흑백화면 등으로 전환하여 사용자에게 알림
      
### 0_2. Android의 새로운 기능 소개
- keyPoint
  #### - android app bundle  
    - App의 사이즈를 최소화함 (실제 100MB의 앱의 설치율은 30% 떨어짐)  
      ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_app_bundle_rate.png?raw=true)  
    #### - 순서
      ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_app_bundle_logic.jpeg?raw=true)  
      1. App Bundle을 활용하여 동적 기능 모듈(dynamic feature modules)을 앱에 추가  
      2. 임의의 기기에 대해 앱에 필요한 모든 것 (ex>  언어, 화면 해상도, 하드웨어 아키텍처 등) 이 들어있는 App Bundle 빌드  
      3. 앱 다운로드 시점에서 사용자의 기기와 일치하는 코드와 리소스만 전달 (Dynamic Delivery / `아래 그림 참고`)  
      ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_app_bundle_dynamic_delivery.gif?raw=true)  
      
  #### - Kotlin    
      개발자의 35%가 코틀린을 사용하고 있음  
      코드가 `간결`해짐  
      `다양한 플랫폼`에서 코틀린 사용 가능  
      ![images]()  
      > Kotlin / JVM
      >   - Desktop
      >   - Android
      >   - Android of Things
      >   - Server-side  
      > Kotlin / JS
      >   - Front-end  
      >   - Server-side  
      > Kotlin / Native
      >   - Server-side
      >   - Desktop
      >   - Embedded
      >   - OS (macOS / Windows, Linux, Raspberry Pi)
      
  #### - Google Play Instant
      미니게임(실제 게임의 베타 역활), 튜토리얼보다 난이도 있는 체험, 경험 못한 레벨 체험 등을 지원  
      게임 한도 크기 : 4MB -> 10MB
      유니티, Cocos 지원  
      
  #### - Faster Development  
    - JetPack (androidx)  
      ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_faster_development_jetpack.png?raw=true)  
      - Android 앱을 만들기 위한 컴포넌트, 도구 및 지침 세트
      - `별도의` 라이브러리로서 제공
      - Android Jetpack 라이브러리는 모두 새로운 androidx.* 네임스페이스로 이동 (Android Studio 3.2 이상부터 androidx 패키지 명 대응 refactoring 가능)  
      ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_faster_development_androidx.png?raw=true)  
      - 특정 버전에 관계없이 기능을 제공하도록 빌드  
      - 이전 버전과의 호환성을 제공  
      - 기타 자세한 가이드라인은 [g.co/androidjetpack](g.co/androidjetpack) 에서 확인
      - 개인적으로 기대되는 JetPack 기능 WorkManager
        ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_faster_development_jetpack_workmanager.jpeg?raw=true)  
    - Android Studio 3.2 Canary
      - Emulator 스냅샷 지원  
      - 구동속도 개선  
            
  #### - Increasing Engagement  
    - Android Slices  
      앱 UI를 Google 어시스턴트 내에 검색 결과로 표시 가능  
      자세한 내용은 [g.co/androidjetpack](g.co/androidjetpack) 참고  
    - Actions  
      내가 자주했던 내용을 학습하여 AI를 활용한 내 action 예측 기능  
      ex> 이어폰 낄 시 -> 멜론 어플 실행

#### - 기타 QnA (http://nobase-dev.tistory.com/46?category=826656)   
> Q : RPG 게임에도 Instant App이 도움이 될까?  
> A : Yes. 사전등록, 미니게임 또는 친구추가, 길드초대 등 유저 경험을 제공할 수 있음.
>
> Q: 인디 게임도 Instant App이 도움이 될까?  
> A : Yes. 인디게임에 더 필요할 듯. 무료나 프리미엄 등 모든 게임 지원함.
> 
> Q : Kotlin 사용으로 얻을 수 있는 이득은?  
> A : boiler pate 코드가 안 생김. 약 40% 코드 줄어듬. 효율적이고 스마트하게 행복하게 일할 수 있음. 진짜임.
> 
> Q : 안드로이드 제트팩이 코틀린과 100% 호환 가능한가?  
> A : 완벽히 지원함.
> 
> Q : HTML 5 에도 Instant App 지원이 가능한가?  
> A : Instant App의 원래 취지는 네이티브 요소를 웹의 편리함으로 가져오자는 취지였음. 취지에는 안맞을 듯.  

## 1. Android P 최신 기능 소개

- keyPoint
  #### - Intelligent (머신러닝 / AI)  
  #### - Adaptive Battery  
    App Standby Buckets
    ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_p_app_bundle_bucket.jpeg?raw=true)  
      - 앱을 4가지 버전으로 관리  
        > Active : 현재 사용 중  
        > Working set : 정기적으로 사용 중  
        > Frequent : 자주 사용하지만 매일은 아님  
        > Rare : 앱이 자주 사용되지 않음  
      - Rare로 분류 시 제약이 생기며, FCM 같은 기능도 등급 조정이 가능
    Background Restrictions  
      - 순서
        1. Android Vitals에서 Bad behavior을 발견
        2. 유저에게 제한을 걸 건지 물어봄
        3. 유저가 ok 할 시, 해당 앱은 Bad behavior로 판단되어 제약이 걸림  
        > #### Vitals 에서 Bad behavior 로 판단하는 요소
        > ANR rates  
        > Crash rates  
        > Excessive wakeups  
        > Stuck Partial wake locks  

        > #### Bad behavior로 판단될 경우  
        > 알람 X / 네트워크 작업 X  
        > 백그라운드 처리 기능  
        > foreground 서비스(!!)  

  #### - App Action  
    내가 자주했던 내용을 학습하여 AI를 활용한 내 action 예측 기능  
      ex> 이어폰 낄 시 -> 멜론 어플 실행  
    사용자 행동 학습 후 여러 서비스에서 제공함.  
    사용자 니즈는 캐치할 수 있으나, 그걸 할 수 있는 앱은 알 수 없음  
    -> 앱에서 Built-in Intents를 사용해야 함. (이는 actions.xml에 정의해야함)  
    ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_p_app_bundle_built_in_intent.jpeg?raw=true)  
    참고 : [https://developers.google.com/actions/reference/built-in-intents/](https://developers.google.com/actions/reference/built-in-intents/)  
    
  #### - Slice
    앱 일부를 다른 앱, 구글 어시스턴트 등에서 사용  
    위젯의 강화판  
    템플릿 제공  
    support 라이브러리 형태로 지원  
    action와, toggle, slider 등 제공  
    SlideProvider로 생성  

  #### - 기타 
    [Notification](https://developer.android.com/preview/features?hl=ko#notifications)  
      - Messaging Style  
      - Image 지원  
        ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_p_notification_image.png?raw=true)  
      - SmartReply 기능 지원  
        ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_p_notification_smartreply.png?raw=true)  
      > 사용자가 빈번히 Notification을 dismiss할 경우 시스템에서 Blocking을 제안함(Notification Blocking). 
      > 이 경우 Notification Channel 단위로 처리되므로
      > 앱에서 Channel 관리가 필요할 것으로 보임
    [Display Cutout](https://developer.android.com/preview/features?hl=ko#cutout)  
      - Status Bar 높이를 하드코딩한 경우 문제
        (기존은 24dp로 알려져 있으나, Cutout의 경우 약 57~8dp)  
        ![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_p_app_etc_.png?raw=true)   
    [Private API](https://developer.android.com/preview/restrictions-non-sdk-interfaces)  
      아래 사항의 경우 제한 적용
      > - 비 SDK 인터페이스  
      > - 리플렉션 또는 JNI를 사용  
        

## 1. 새로운 모듈 Android App Bundle로 앱 개발하기

#### Android App Bundle
- 크기가 작은 앱으로도 우수한 사용 환경을 간편하게 제공할 수 있도록 도와주는 새로운 앱 모델
- 앱 크기를 대폭 줄이고 Dynamic Delivery를 통해 유저들이 앱을 빠르게 다운로드 할 수 있음
- 프로토콜 버퍼 형식인 android app bundle (apk는 바이너리 형식)  
- 내부에 dex 폴더가 따로 있음  
  ![images]()  
- 위의 resources.pb는 apk의 resources.arac에 해당하는 파일 (프로토콜 버퍼 형식)

#### App Bundle이 가능하게 하는 2가지 기능
#####Dynamic delivery system
- 기본 구성요소는 Split APK 매커니즘
- Android 플랫폼은 설치된 분리된 여러 APK를 하나의 앱으로 취급할 수 있음  
- 사용 예  
  ![images]()  
> Split APK의 종류  
> 1. Base APK  
>   모든 APK가 액세스할 수 있는 코드와 리소스 포함하여 앱의 기본기능 제공.  
>   앱 다운로드시 설치되는 첫 번째 APK
>
> 2. Configuration APKs  
>   각 APK에는 특정 화면 밀도, CPU 아키텍처, 언어에 대한 기본 라이브러리 및 리소스를 포함.  
>   기기가 Base APK 또는 Dynamic feature APK 다운로드시 필요한 라이브러리와 리소스만 다운로드 됨.
>
> 3. Dynamic feature APKs
>   각 APK에는 앱 설치시 필요하지 않지만 나중에 다운로드하여 설치할 수 있는 코드와 리소스가 포함되어 있음.
> ![images]()
> ![images]()
> ![images]()

#### As a Result!
App Bundle을 통해서 평균 20% 이상의 앱 용량을 절감함.
![images]()

##### App Bundle 배포
App Bundle을 만든 후 signing 하여 Google Play에 업로드  
App Bundle은 기기에 APK를 배포할 수 없음  
하나의 빌드 아티팩트에 모든 앱의 컴파일된 코드와 리소스를 포함(새로운 업로드 형태)  

순서
> 1. signing된 App Bundle을 업로드
> 2. Google Play는 앱의 APK를 만들고 서명
> 3. Dynamic Delivery를 통해 사용자에게 필요한 모든 것을 제공

##### [bundletool](https://github.com/google/bundletool)
로컬에서 테스트시 사용  
> Android App Bundle 빌드  
> APK archive 생성  
> APK 추출  
> APK 설치  
> 장치 사양 추출  

##### 기타
> Q : 사용자가 설치 후 언어 변경시 앱을 재설치해야 하나?  
> A : Split App만 설치하면 됨.  
> Q : assets 타켓팅시 불필요한 파일 포함되는데 개선 여부는?  
> A : 타켓팅을 상세히 해서 하면 됨.  
> Q : 앱 수정시 앱 번들 모두 업데이트해야 하나?  
> A : 그렇다.  
> Q : 베이스 외 모듈 배포 가능하나?  
> A : On Demand 버전은 따로 배포가 안됨.  
> Q : 앱번들을 위한 최소 버전은?  
> A : Pre L도 지원함으로 따로 최소 버전은 없음.  
> Q : 모듈화에 대해 자세한 설명이나 사례는?  
> A : 게임에서 레벨에 따라 별도 다운로드 제공.  
> Q : 앱 번들 기기 지원 관련 이슈는?  
> A : 현재는 없음.  


Publishing App Bundle


Modular App development
  

## 2. 빠르고 세련된 Android 개발 - Android Jetpack & Android Studio

#### Android 개발의 역사(?)
![images]()

#### [Layout Inspector](https://developer.android.com/studio/debug/layout-inspector?hl=ko)  
- ver 3.1 이후 **Hierarchy Viewer**를 대체  
- 런타임에 앱의 뷰 계층을 검사  
- Layout Inspector가 스냅샷을 캡처하여 .li 파일로 저장함  
- li 파일은 project name/captures 에 저장됨
  > 파일 구성  
  > - View Tree  : 레이아웃에 있는 뷰 계층  
  > - Screenshot : 각 뷰에 대한 기기 스크린샷이며 경계가 표시됨  
  > - Properties Table: 선택한 뷰의 레이아웃 속성  

#### [Profile](https://developer.android.com/studio/debug/layout-inspector?hl=ko)  
- ​[CPU](https://developer.android.com/studio/profile/cpu-profiler?hl=ko)
  ![images]()

- [Memory](https://developer.android.com/studio/profile/memory-profiler?hl=ko)
  ![images]()
  
- [Network](https://developer.android.com/studio/profile/network-profiler?hl=ko)
  ![images]()

#### Runtime
##### 1. Dalvik
- app Size의 최적화
- heap fragmentation (파편화된 메모리)
- allocation 최적화 필요

##### 2. ART
- JIT + AOT
- performance의 최적화
- heap defragmentation
- Large object heap

#### Language
##### 1. Java
- Kotlin 이전에 사용했던 언어  
- version 지원 미흡 (java8..)

##### 2. Kotlin
- Java보다 간결함
- lint check 지원
- style & [interop guide](https://android.github.io/kotlin-guides/interop.html)

#### Library & API
- AbsoluteLayout : 사용하지 말 것 (개인적으로 처음 들어봤음..)  
- LinearLayout : 간단한 경우 사용  
- FameLayout : 역시 간단히 사용  
- GridLayout : 권장하지 않음 (개인적으로 position 0 버그가 힘들었음..)  
- RelativeLayout : 사용에 대한 비용이 비쌈  
- ConstraintLayout : 권장하며 애니메이션 적용 가능한 2.0 버전 나올 예정

#### AdapterView
- ListView / GridView / Gallery => RecyclerView!!!
- LayoutManager 등을 통한 다양한 레이아웃 제공  

#### [Fragment](https://developer.android.com/reference/android/app/Fragment)
> This class was deprecated in API level 28. 
> Use the Support Library Fragment for consistent behavior across all devices and access to Lifecycle.  

-> Support Library에 있는 Fragment 사용 권장  
- android.app.Fragment
- android.support.v4.app.Fragment (권장)

#### Activity
- 가능하다면 SingleActivity 사용

#### [Architecture](https://developer.android.com/topic/libraries/architecture/)
- 기존엔 가이드가 없었음
- 현재는 AAC(Android Architecture Components) 로 가이드 제공 (필수는 아님)

#### [Life Cycle](https://developer.android.com/topic/libraries/architecture/lifecycle)
- Callback 처리 등으로 액티비티나 프래그먼트가 heavy 해짐
- AAC 에서 액티비티와 독립적으로 Life Cycle을 제공

#### [Views and Data](https://developer.android.com/topic/libraries/architecture/viewmodel)
- ViewModel이 처리
- 인스턴스만 Activity에서 관리

#### [Data](https://developer.android.com/topic/libraries/architecture/room)
- SQLITE
- Room


#### [Android Jetpack](https://developer.android.com/jetpack/)
- Android 앱을 만들기 위한 컴포넌트, 도구 및 지침 세트  
- `별도의` 라이브러리로서 제공  
- Android Jetpack 라이브러리는 모두 새로운 androidx.* 네임스페이스로 이동 (Android Studio 3.2 이상부터 androidx 패키지 명 대응 refactoring 가능)  
![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_faster_development_androidx.png?raw=true)  
- 특정 버전에 관계없이 기능을 제공하도록 빌드  
- 이전 버전과의 호환성을 제공  
- 기타 자세한 가이드라인은 [g.co/androidjetpack](g.co/androidjetpack) 에서 확인
![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_faster_development_jetpack.png?raw=true)  
- 개인적으로 기대되는 JetPack 기능 WorkManager
![images](https://github.com/ridickle7/LeeSangWoo_Reference/blob/master/1.%20ImageRef/recap/recap_faster_development_jetpack_workmanager.jpeg?raw=true)  

#### 기타
- AAR / JAR
- [D8 (Dex Compiler)](https://android-developers.googleblog.com/2017/08/next-generation-dex-compiler-now-in.html)
- R8 (Proguard replacement)
- [SQL Query](https://developer.android.com/reference/android/arch/persistence/room/Query) (@Query 애너테이션 사용)
- Kotlin Lint check 지원

