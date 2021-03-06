# Spring 단어 모음집

### 스프링 DI(Dependecny Injection) : Setter



DI는 말 그대로 의존성을 " ***주입시켜준다*** "입니다. 객체를 직접 생성하는 게 아니라 외부에서 생성한 후 주입을 시켜주는 방식입니다.

일단 A라는 객체에서 B, C라는 객체를 이용할 때 두가지 방법이 있습니다. 

![image](https://user-images.githubusercontent.com/55625864/84354621-293a0d00-abfc-11ea-85c2-3a12fd962f3c.png)

**첫번째 방법**은 A객체가 B와 C객체를 New 생성자를 통해서 **직접 생성하는 방법**이고, 

**두번째 방법**은 **외부에서 생성 된 객체**를 setter()나 생성자를 통해 **사용하는 방법**입니다. 



두번째 방법의 그림을 보시면 **A객체에서 직접 생성하지 않고, 외부에서 생성된 객체를 setter( )혹은 생성자를 이용해서 사용**합니다. 이런걸 **"주입"**한다고 하며 **스프링에서 사용하는 방식(DI)**인거죠. 스프링은 다른 객체들이 사용하고, 다른 서비스를 위해 사용할 수 있는 클래스를 컨테이너 형태로 이 기능을 제공해줍니다. **A라는 객체에서 B, C객체를 사용(의존)할 때 A객체에서 직접 생성을 하는 것이 아닌 외부(IOC컨테이너)에서 생성된 B, C객체를 조립(주입)시켜 setter 혹은 생성자를 통해 사용**할 수 있는거죠.

![image](https://user-images.githubusercontent.com/55625864/84354843-88981d00-abfc-11ea-8855-161ece0bd60e.png)



**copy.right :** https://private.tistory.com/39

---

