# Immutable Object

객체 지향 프로그래밍에 있어서 불변객체(immutable object)는 생성 후 그 상태를 바꿀 수 없는 객체를 말한다.

반대 개념으로는 가변(mutable) 객체로 생성 후에도 상태를 변경할 수 있다. 객체 전체가 불변인 것도 있고, C++에서 const 데이터 멤버를 사용하는 경우와 같이 일부 속성만 불변인 것도 있다. 또, 경우에 따라서는 내부에서 사용하는 속성이 변화해도 외부에서 그 객체의 상태가 변하지 않은 것 처럼 보인다면 불변 객체로 보기도 한다. 예를 들어, 비용이 큰 계산의 결과를 캐시하기 위해 메모이제이션(Memoization)을 이용하더라도 그 객체는 여전히 불변하다고 볼 수있다. 불변 객체의 초기 상태는 대개 생성 시에 결정되지만 객체가 실제로 사용되는 순간까지 늦추기도 한다.
불변 객체를 사용하면 복제나 비교를 위한 조작을 단순화 할 수 있고, 성능 개선에도 도움을 준다. 하지만 객체가 변경 가능한 데이터를 많이 가지고 있는 경우엔 불변이 오히려 부적절한 경우가 있다. 이 때문에 많은 프로그래밍 언어에서는 불변이나 가변 중 하나를 선택할 수 있도록 하고 있다.
-[위키백과](https://ko.wikipedia.org/wiki/불변객체)



**불변객체는 재할당은 가능하지만, 한번 할당하면 내부 데이터를 변경할 수 없는 객체**


**Immutable Object 만들기**

- Immutable Object를 만드는 기본적인 아이디어는 필드에 `final`을 사용하고, `Setter`를 구현하지 않는 것이다.

- 참조 변수도 불변 객체이어야 한다



**장점**

- 객체에 대한 신뢰도가 높아집니다. 객체가 한번 생성되어서 그게 변하지 않는다면 transaction 내에서 그 객체가 변하지 않기에 우리가 믿고 쓸 수 있기 때문이다.
- 생성자, 접근메소드에 대한 방어 복사가 필요없다.
- 멀티스레드 환경에서 동기화 처리없이 객체를 공유할 수 있다.

**단점**

- 객체가 가지는 값마다 새로운 객체가 필요합니다. 따라서 메모리 누수와 새로운 객체를 계속 생성해야하기 때문에 성능저하를 발생시킬 수 있다.