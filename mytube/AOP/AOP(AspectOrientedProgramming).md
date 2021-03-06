# AOP(Aspect Oriented Programming)

Aspect Oriented Programing

관점 지향 프로그래밍

 

프로그래밍을 하다보면, 공통적인 기능이 많이 발생한다.

이러한 공통기능을 모든 모듈에 적용하기 위한 방법으로 상속을 이용한다.

상속도 좋은 방법이지만, JAVA에서는 다중 상속이 불가능하다.

 

이러한 모듈을 상속받아 공통 기능을 부여하기에는 한계가 있다.

그리고, 기능 구현부분에서

핵심코드와 공통기능코드가 섞여있어서

보기에도 불편하고, 효율성이 떨어진다.

 

이러한 이유로 AOP가 등장했다.

AOP방법은 핵심 기능과 공통 기능을 분리 시켜놓고,

공통 기능을 필요로 하는 핵심 기능들에서 사용하는 방식이다.

(핵심기능은 변화하지만, 공통기능은 다시 적용이 가능하다.)

 

즉, AOP는 핵심기능과 공통기능을 분리시킨다는 부분을 주의깊게 보자



**주요용어**

`Aspect` : 공통기능

`Advice` : Aspect의 기능 자체

`Jointpoint` : Advice를 적용해야 되는 부분(ex : 필드, 메소드 / 스프링에서는 메소드만 해당)

`Pointcut` : Jointpoint의 부분으로 실제로 Advice가 적용된 부분

`Weaving` : Advice를 핵심기능에 적용하는 행위



출처: https://hongku.tistory.com/114 [IT에 취.하.개.]