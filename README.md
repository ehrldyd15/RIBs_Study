# RIBs를 이용하고 토이프로젝트를 완성시켜보자!!

## _1. RIBs가 나온 배경._

### MVC 아키텍처

![MVC](https://user-images.githubusercontent.com/46097621/166392396-2c5a4e50-1b46-4720-a1c1-f1a0ddf89126.png)

- MVC를 사용할 때 새로운 기능이 늘어나며 앱의 복잡성 증가
- 모듈이 증가할수록, 테스트 하기 점점 어려워지는 현상
- 수 년 동안 MVC패턴 사용 -> 관리하기가 힘든 scale (하나의 ViewController파일에 300줄 -> 3000줄)
- massive view controllers (비즈니스 로직, 데이터 변경, 데이터 검증, 네트워크 로직, 라우팅 로직)
- 테스트가 어려운 구조 (if-else문으로 테스트)

### VIPER 아키텍처

![VIPER](https://user-images.githubusercontent.com/46097621/166393044-cdc64cd2-271c-47db-8c6a-8a6020d237f4.png)

- View
- Interactor: 비즈니스 로직포함, API나 DB로 Data르 받아서 Entity(모델) 생성
- Presenter: View에서 유저 액션을 받고, Interactor에 data를 요창하여 View에 그려주는것을 다시요청
- Entity: Interactor에 의해 만들어지는 모델
- Router: 화면전환 로직

### VIPER의 장점 (MVC에 비해 더욱 추상적)

- Router
- Interactor는 단순히 데이터의 manipulation or verification만 관여 (api 호출)
- Presenter는 business 로직을 가지고 presentation 로직을 포함
- Presenter, Interactor들은 가볍게 유닛 테스트가 가능

### RIBs 탄생 배경 (VIPER 단점 보완)

- “제대로 된 모듈화가 목적”이지만 VIPER는 그러지 않는 점이 존재
- View 트리와 business 트리가 밀접하게 결합되어 있어, View로직만 포함하거나 business 로직만 포함하는 노드를 구현하기 힘든 점
- View 트리를 중심으로 앱이 진행되는 단점, View에 의해 앱 상태가 동작되는 장점 -> RIBs 트리로 보완

### RIBs 아키텍처

![RIBs](https://user-images.githubusercontent.com/46097621/166393616-40bb9e09-0b87-44bd-ba6f-af9898a69db4.png)

- Router를 부르는 위치가 Presenter에서 Interactor로 이동
- business logic -> Router, Interactor
- view logic -> Presenter, View


## 참고자료
uber 개발자: https://eng.uber.com/new-rider-app-architecture/

개념: https://github.com/uber/RIBs/wiki







