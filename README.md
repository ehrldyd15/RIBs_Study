# RIBs를 이용하고 토이프로젝트를 완성시켜보자!!

## _1. RIBs가 나온 배경._

### MVC

![MVC](https://user-images.githubusercontent.com/46097621/166392396-2c5a4e50-1b46-4720-a1c1-f1a0ddf89126.png)

- MVC를 사용할 때 새로운 기능이 늘어나며 앱의 복잡성 증가
- 모듈이 증가할수록, 테스트 하기 점점 어려워지는 현상
- 수 년 동안 MVC패턴 사용 -> 관리하기가 힘든 scale (하나의 ViewController파일에 300줄 -> 3000줄)
- massive view controllers (비즈니스 로직, 데이터 변경, 데이터 검증, 네트워크 로직, 라우팅 로직)
- 테스트가 어려운 구조 (if-else문으로 테스트)

### VIPER
