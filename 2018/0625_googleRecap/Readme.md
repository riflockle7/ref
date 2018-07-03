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
        

