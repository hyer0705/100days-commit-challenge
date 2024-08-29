# 지난 10일 나의 목표는?!
- [x] 매일 1 commit 달성
- [x] 하루에 알고리즘 1문제 이상 풀기
- [x] 토이 프로젝트 기능 하나 이상 구현하기

# 10일 돌아보면 잘한 점
- 알고리즘 문제 풀이 후 다른 사람의 코드와 비교하는 시간을 가졌다.

# 10일 돌아보며 아쉬운 점
- 매일 1 commit을 달성하지 못했다.
- 지금껏 DP 문제를 너무 쉽게 본 것 같다. 더 공부가 필요한 .. 😅

# 10일 동안 공부한 내용
- Spring 웹 애플리케이션 계층 구조
  - **Domain** Model
    - 도메인 모델(객체)은 내가 개발하고자 하는 영역을 분석하고, 그 분석의 결과로 도출된 모델(객체)이라고 할 수 있다.
    - ex) 주문, 회원, 결제, 배송, 리뷰 등
  - **Repository** Leyer (Data Access Layer)
    - JPA, ORM을 주로 사용하는 계층이다.
    - DAO 인터페이스와 @Repository 어노테이션을 사용하여 작성된 DAO 구현 클래스가 이 계층에 속한다.
    - DB에 Data를 CRUD하는 계층이기도 하다.
  - **Service** Layer (Business Layer)
    - 애플리케이션 비즈니스 로직 처리와 비즈니스와 관련된 도메인 모델의 적합성 검증을 한다.
    - 트랜잭션을 관리한다.
    - Presentation Layer와 Data Access Layer 사이를 연결하는 역할로서 두 계층이 직접적으로 통신하지 않게 한다.
    - 나중에 Controller가 Service를 통해 회원가입과 데이터를 가져올 수 있게 된다. (Controller가 Service를 의존하는 관계)
  - Presentation Layer (**Controller**)
    - Presentation Layer는 브라우저 상의 웹 클라이언트의 요청 및 응답을 처리하는 계층이다.
    - Service Layer, Data Access Layer에서 발생하는 Exception을 처리해준다.


# 앞으로 10일 동안 나의 목표는?!
- [ ] 매일 1 commit 달성
- [ ] 토이 프로젝트 **게시글 작성** 기능 구현
- [ ] 창업 동아리 내 프로젝트 ui 디자인 끝내기