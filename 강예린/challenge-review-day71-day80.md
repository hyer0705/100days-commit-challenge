# 지난 10일 나의 목표는?!
- [x] 중간고사 공부 열시미 하기 ..!

# 10일 돌아보면 잘한 점
- 중간고사 공부를 열시미 했다 !
- 매일은 아니지만, 중간고사 공부 전 스프링 공부를 조금씩 하는 시간을 가졌다 !

# 10일 돌아보며 아쉬운 점
- 매일 1 commit을 달성하지 못했다. 🥹

# 10일 동안 공부한 내용
### @Transactional
- **JPA의 모든 데이터 변경은 Transaction 안에서 이루어져야 한다.**
- public 메소드들이 transaction 안에서 수행된다.
- @Transactional을 따로 메소드에 선언해주면 메소드에 선언된 @Transactional이 우선권을 가진다.
- @Transactional(readOnly = true)
  - **readOnly = true** 👉🏻 JPA가 조회(읽기)하는 곳에서 성능을 최적화한다.
  - '**읽기**'가 아닌 '**쓰기**'를 목적으로 한 메소드에는 선언 **x**

### @Autowired
- Spring이 Spring Bean에 등록되어 있는 repository를 injection 해준다.

**종류**
- 생성자 injection
- setter injection
  <br> (이 부분은 공부를 따로 더 해야할 것 같아요 🤭)

### @AllArgsConstructor
- 모든 필드로 생성자를 만들어주는 어노테이션

### @RequiredArgsConstructor
- final로 선언한 필드로만 생성자를 만들어주는 어노테이션

# 앞으로 10일 동안 나의 목표는?!
- [ ] 중간고사 공부 더 열시미 하기 💪🏻