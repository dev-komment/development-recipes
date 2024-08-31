## **객체지향 개발 5대 원리: SOLID**

&nbsp; 객체지향 개발 방법론은 설계가 복잡하다는 단점을 가지고 있지만, 입증된 객체지향 디자인 원리들을 사용하면 보다 `유지보수`가 용이하고, `유연`하며, `확장`이 쉬운 소프트웨어를 만들 수 있다. 이 원리들은 표준화 작업에서부터 아키텍처 설계에 이르기까지 다양하게 적용되는 원칙이다. 객체지향 개발을 할 때 지켜야 할 5대 원리, **`SOLID`** 에 대해 알아보자.

</br>

### **SRP** (단일책임의 원칙: Single Responsibility Principle)

> There should never be more than one reason for a Class to change.

: 작성된 클래스는 하나의 기능만 가지며 클래스가 제공하는 모든 서비스는 그 하나의 책임을 수행하는 데에 집중돼야 한다

- 어떤 변화에 의해 클래스를 변경해야 하는 이유는 오직 하나뿐 이어야함
  - 변경 시, 파급효과가 적으면 잘 지킨 것!
- SRP 원리를 적용하면 `책임 영역`이 확실해짐
- 객체지향 원리의 대전제인 OCP 원리뿐 아니라 다른 원리들을 적용하는 기초가 됨

</br>

### **OCP** (개방폐쇄의 원칙: Open Close Principle)

> You should be able to extend a Classes behavior, without modifying it.

: 소프트웨어의 구성요소(컴포넌트, 클래스, 모듈, 함수)는 확장에는 열려 있으나, 변경에는 닫혀 있어야 한다는 원리

- 변경을 위한 비용은 가능한 줄이고, 확장을 위한 비용은 가능한 극대화 해야 함
- 요구사항의 변경 및 추가사항이 발생해도 기존 구성요소는 수정이 일어나선 안됨
- 중요 메커니즘 → `추상화`와 `다형성`

</br>

### **LSP** (리스코프 치환의 원칙: Liskov Substitution Principle)

> Functions that use pointers or references to base Classes must be able to use objects of derived Classes with out knowing it.

: Base 클래스에서 파생된 Sub 클래스는 언제나 Base 클래스로 교체할 수 있어야 한다.

- Sub 클래스는 Base 클래스가 약속한 규약(`인터페이스` 등)을 지켜야 함
- 상속을 통해 재사용은 Base 클래스와 Sub 클래스 사이에 `IS-A 관계`가 있을 경우로만 제한돼야 함
- LSP는 OCP를 구성하는 구조가 됨

```Text
📝 용어 정리

IS-A
: 추상화들 사이의 포함 관계를 의미하며, 한 클래스 A가 다른 클래스 B의 Sub 클래스임을 의미한다.

HAS-A
: 구성 관계를 의미하며, 오브젝트 B가 오브젝트 A에 속한다, 즉 B가 A의 멤버 객체인 것을 의미한다.
```

</br>

### **ISP** (인터페이스 분리의 원칙: Interface Segregation Principle)

> Clients should not be forced to depend upon interfaces that they do not use.

: 어떤 클래스가 다른 클래스에 종속될 때에는 가능한 최소한의 인터페이스만을 사용해야 한다.

- SRP가 클래스의 단일책임을 강조한다면 ISP는 `인터페이스의 단일책임` 강조
- 인터페이스가 명확해지고, 대체 가능성이 높아짐

</br>

### **DIP** (의존관계 역전의 원칙: Dependency Inversion Principle)

> A. High level modules should not depend upon low level modules. Both should depend upon abstractions.

> B. Abstractions should not depend upon details. Details should depend upon abstactions.

: 상위 모듈은 하위 모듈의 구현에 의존해서는 안되며, 하위 모듈은 상위 모듈에서 정의한 추상 타입에 의존해야 한다.

- 구현 클래스에 의존하지 말고, `인터페이스에 의존`하라는 뜻
- 복잡하고 지난한 컴포넌트 간의 커뮤니케이션 관계를 `단순화`하기 위한 원칙

</br>

---

### **참고자료**

- Web
  - [@Inflearn 강의](https://www.inflearn.com/course/스프링-핵심-원리-기본편/dashboard)
  - [@mangkyu](https://mangkyu.tistory.com/194)
  - [@nextree](https://www.nextree.co.kr/p6960/)
  - [@minusi](https://minusi.tistory.com/entry/객체-지향적-관점에서의-has-a와-is-a-차이점)
