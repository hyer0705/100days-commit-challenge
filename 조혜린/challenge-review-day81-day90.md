# 지난 10일 나의 목표는?!

- [x] 우테코 프리코스 열심히 참여하기
- [x] 주 3회 이상 3km 러닝하기
- [ ] 오후 10시 30분에 커밋 내역 인증하기

# 10일 돌아보면 잘한 점

- 우테코, 알바를 하면서 챌린지에 참여했는데 이번 10일 동안은 꾸준히 잔디를 심었다.

# 10일 돌아보며 아쉬운 점

- 처음에 세웠던 목표에서 코테 문제에 대해서 잔디를 심으려고 했으나 우테코를 시작하고 매일 코드리뷰한 것을 통해 잔디를 인증했다. 코드 리뷰도 많이 도움이 됐지만...? 그래도 원래 목표하던 것을 공부해서 인증하는게 좋지 않을까?

# 10일 동안 공부한 내용

- 코드 리뷰를 통해 알게 된 개념

  - 매직 넘버: 코드 내에서 어떤 의미를 담고 있지만, 숫자 그대로 사용되어 그 의미가 명확히 드러나지 않는 숫자를 말한다.

    ```javascript
    // before
    function calculateDiscount(price) {
      if (price > 100) {
        // 여기서 100이 매직 넘버입니다.
        return price * 0.9; // 10% 할인
      }
      return price;
    }

    // after
    const DISCOUNT_THRESHOLD = 100;
    const DISCOUNT_RATE = 0.9;

    function calculateDiscount(price) {
      if (price > DISCOUNT_THRESHOLD) {
        return price * DISCOUNT_RATE;
      }
      return price;
    }
    ```

- Jest 를 사용하여 테스트 코드를 작성하며 알게 된 개념

  - 단위 테스트: 특정 "단위"(보통 함수나 메서드처럼 작은 코드 조각을 의미)를 개별적으로 테스트하는 방법
  - 메서드

    - expect(): 테스트할 값을 전달하는 메서드. 예를 들어, expect(value)라고 쓰면, value가 어떤 결과여야 하는지 검증할 수 있음.
      ```javascript
      expect(3 + 2).toBe(5);
      ```
    - test.each(): 여러 가지 경우의 수를 반복해서 테스트할 때 사용. 예를 들어, 동일한 함수에 다양한 입력값을 넣고 테스트할 때 유용함.
      ```javascript
      test.each([
        [1, 2, 3],
        [4, 5, 9],
      ])("add(%i, %i) should return %i", (a, b, expected) => {
        expect(a + b).toBe(expected);
      });
      ```
    - toBe(): 값이 정확히 일치하는지를 확인. 숫자나 문자열과 같은 기본 자료형을 비교할 때 사용함
      ```javascript
      expect(2 + 2).toBe(4);
      ```
    - toEqual(): 객체나 배열의 값이 같을 때 사용하는 메서드. toBe는 기본 자료형만 비교하므로, 객체나 배열을 비교할 때는 toEqual을 사용함.

    ```javascript
    expect({ name: "Lucy" }).toEqual({ name: "Lucy" });
    ```

    - toHaveBeenCalledWith(): 특정 함수가 어떤 인자와 함께 호출되었는지 확인할 때 사용. 함수가 예상한 대로 호출됐는지 검증함.

    ```javascript
    const mockFunction = jest.fn().mockReturnValue(3); // add 함수를 모킹하여 반환값 3 설정

    mockFunction(1, 2);
    expect(mockFunction).toHaveBeenCalledWith(1, 2); // 호출된 인자 확인
    expect(mockFunction()).toBe(3); // 반환값 3 확인
    ```

    - expect.stringContaining(): 문자열이 특정 텍스트를 포함하는지 확인할 때 사용. 특정 문구가 결과에 포함되어야 하는지 확인할 때 유용함.

    ```javascript
    expect("Hello, world!").toEqual(expect.stringContaining("world"));
    ```

# 앞으로 10일 동안 나의 목표는?!

- [ ] 우테코 프리코스 4주차 미션 열심히 참여하기~
- [ ] 주 3회 이상 3km 러닝 혹은 헬스장에서 운동
- [ ] 코딩테스트 3문제 풀이하고 잔디 인증하기
