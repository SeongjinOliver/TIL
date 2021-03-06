# AOP



### AOP

애플리케이션의 핵심적인 기능에서 **부가적인 기능을 분리해서 애스펙스(aspect)라는 독특한 모듈로 만들어서 설계하고 개발하는 방법**을 Aspect Oriented Programming 또는 약자로 AOP라 함.



AOP는 OOP만으로는 모듈화하기 힘든 부가기능을 효과적으로 모듈화하도록 도와주는 기술.



어떤 로직을 기준으로 핵심적인 관점, 부가적인 관점으로 나누어서 보고 그 관점을 기준으로 모듈화 하겠다는 것.



`부가적인 기능?`



#### 코드 분리

- 메소드 분리 
  - OOP에서의 메소드 분리와 차이점은?
- DI를 이용한 클래스 분리

---



#### 애스펙트(Aspect)

  부가기능 모듈화 작업.



#### 어드바이스(advice)

  부가 기능을 담은 오브젝트



#### 포인트컷(pointcut)

  메소드 선정 알고리즘을 담은 오브젝트



#### 어드바이저(advisor)

  advice + pointcut



---

#### 프록시(Proxy)





#### 고립된 단위 테스트





#### 참고

- [proxy pattern](https://refactoring.guru/design-patterns/proxy)