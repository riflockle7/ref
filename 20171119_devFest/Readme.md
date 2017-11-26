# 2017 DevFest 내용 정리

### 1. MVC부터 MVVM, 단방향 데이터 흐름까지

### 서론

Form (Activity / Fragment)  
- ScreenLayout  
- Form Logic : 컨트롤 내에 프로그래밍 / 어려운 행동을 정의  

Control (View)  
- Target
- Actual
- Variance

Data Binding (1970~80)
- MVVM의 전유물이 아님 

양방향 바인딩 
- 순환 참조의 문제, 메모리 문제 등의 문제가 있음
- 상태의 개수가 많아질수록 양방향 바인딩은 여러가지 문제가 있다.
- 현재 구글 앵귤러에서도 양방향 바인딩 포기한 상태 (React 반박 : 그 많은 상태들을 상태와 비교로 관리할 것인가?)
- 하나의 앱이 동시에 두가지 인터페이스를 가지고 있어야 함
- GUI 코드 따로 / CLI 코드 따로 -> Separated Presentation 의 시작 (Model의 대두되기 시작)


### MVC 패턴
- Separated Presentation과 Observer 패턴을 합침  
  
Model : 모델에 대한 시식 없음
View  : 보이는 영역
Controller : 입력을 받아 무엇을 할지 설정

#### 초기 MVC
1. 옵저버 패턴에 의존 (모델에 의존 / Active Model)
2. Object Changed (옵저버 패턴이어서 있는 특징)
3. Reading (Model)
- 주요 제어 흐름
- actual
- variance
4. EditTextView / EditTextControl 을 만들고 모델에 옵저버 패턴으로 다 넣음

#### Presentation Model (PM)
- Control이 무의미
- MVVM과 비슷하지만 차이점은 데이터 바인딩 방식! (MVVM은 양방향 데이터 바인딩을 사용)
- 뷰에서 입력 받음
- 어떻게 보일지 결정은 PM에게 넘기고 모델로 보냄
- 시간이 된다면 Jone Smith의 발언을 참고해보아도 좋겠다.

#### MVC 중기
1. 모델이 능동적이지 않음   
   -> 컨트롤러가 더 많은 책임을 가짐
2. View역활이 한정적일때 View가 Model을 구독할 수 없을 때 효과적임
   -> http 기반에서도 능동적으로 요구하기 어려움)
   -> View에 로직을 넣기 힘든 환경 (XML)
3. Activity / Fragment를 컨트롤러로 잡고, XML로 생성된 뷰 객체들이 제한적인 View로 가정하고 Controller가 다 챙겨주는 형태가 일반적

#### MVP



