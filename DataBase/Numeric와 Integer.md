# Numeric와 Integer



#### Numeric

- 정수 또는 소수 값을 저장할 수 있다.

  - 예를 들어 Numeric은 numeric(10, 2) 이렇게 선언할 수 있는데 이 뜻은 정수 10자리 소숫점 2자리로 표현할 수 있다는 것이다.

  - 소수점 2자리는 특정 값이 없으면 00으로 채워진다. 그말은 즉 값이 있던 없던 고정 데이터가 존재한다는 사실이다.

#### Integer

- 오직 정수만 저장할 수 있으며 크지 않은 정수를 처리할 때 사용된다.
- 특정 DBMS에서 int4, int8 이런식으로 지정되는데 모두 integer과 동일한 것이다. 다만 저장할 수 있는 Byte가 다르다.





보통 프로젝트를 진행하면 integer이 많이 안보인다.

보통 numeric를 사용하거나 serial를 사용한다.

이유는 간편하다. 물론 모든 쉬운 길에는 고생이 뒤 따르는 법.



#### 참조

- [[DB] Numeric과 Integer의 차이!](https://junyjsp.tistory.com/32)

