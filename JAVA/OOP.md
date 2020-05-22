# OOP
- Object Oriented Programming의 약자
- 객체들이 서로 메시지를 주고 받으며 데이터를 처리
- 강한 응집력과 약한 결합력을 지향

## 장점
- 프로그램을 유연하고 변경이 용이하게 만듬
- 프로그램의 개발과 유지 보수를 간편하게 만듬
- 직관적인 코드 분석을 가능하게함

## 구성 요소
- ### 클래스(Class)
    - 동일한 속성과 행위를 갖는 객체들의 집합
- ### 객체(Object)
    - 클래스의 인스턴스
- ### 메서드(Method)
    - 클래스로부터 생성된 객체를 조작하는데 사용

## 특징
1. ### 추상화(Abstaction)
- 어떤 영역에서 필요로 하는 속성이나 행동을 추출하는 작업
- 구체적인 사물들의 공통적인 특징을 파악해서 하나의 개념으로 다루는 수단
- 구체적인 개념보다 추상적인 개념에 의존하면 변경사항에 유연하게 대처할 수 있음
2. ### 캡슐화(Encapsulation)
- 정보은닉을 통해 높은 응집도와 낮은 결합도를 갖음
    - 정보은닉(information hiding)
        - 필요가 없는 정보는 외부에서 접근하지 못하도록 제한
        - `private` 키워드
        - 클래스간의 결합을 줄여 코드 수정을 최소화
3. ### 일반화 관계(Generalization)
- 객체들의 공통점을 추출해서 새로운 객체를 만들어 내는 것
- 객체지향 프로그래밍 관점에서 `상속 관계`라함
- 일반화 관계는 자식 클래스를 외부로부터 은닉하는 `캡슐화`의 일종
    - 일반화 관계는 한 클래스 안에 있는 속성과 연산들의 캡슐화에 한정하지 않음
    - 자식 클래스의 캡슐화는 외부 클라이언트가 개별적인 클래스들과 무관하게 프로그래밍을 할 수 있도록함

#### 위임
- 두 클래스 사이에 'is a kind of' 관계가 성립하지 않을 때 상속을 사용하면 불필요한 속성이나 연산을 물려받음
    - 자료구조에 직접 접근하여 무결성 조건이 위배 될 수 있음
- 어떠한 클래스의 일부 기능만 재사용하고 싶은경우에 `위임(delegation)`을 사용
    - 자신이 직접 기능을 실행하지 않고 다른 클래스의 객체가 기능을 실행하도록 위힘하는 것
    - 일반화 관계는 클래스 사이의 관계지만 위임은 객체사이의 관계
- 위임을 사용해 일반화(상속)을 대신하는 과정
    1. 자식 클래스에 부모 클래스의 인스턴스를 참조하는 속성을 만들고 이 속성 필드를 this로 초기화
    2. 서브 클래스에 정의된 각 메서드에 1번에서 만든 위임 속성 필드를 참조하도록 변경
    3. 서브 클래스에서 일반화 관계 선언을 제거하고 위임 속성 필드에 슈퍼 클래스의 객체를 생성해 대입
    4. 서브 클래스에서 사용된 슈퍼 클래스의 메서드에도 위임 메서드 추가

4. ### 다형성(Polymorphism)
- 서로 다른 클래스의 객체가 같은 메시지를 받았을 때 각자의 방식으로 동작하는 능력
- 다형성 효과
    - 구체적으로 현재 어떤 클래스 객체가 참조되는지와 무관하게 프로그래밍을 할 수 있음
    - 자식 클래스가 추가되더라도 코드는 영향을 받지 않음
    - 즉, 코드를 간결하게 만들고 변화에 유연하게 대처할 수 있음

5. ### 피터 코드의 상속 규칙
- 상속의 오용을 막기 위해 상속의 사용을 엄격하게 제한하는 규칙
- 5가지 규칙이 있으며 어느 하나라도 만족하지 않으면 상속을 사용해서는 안됨
    1. 자식 클래스와 부모 클래스 사이는 `역할 수행` 관계가 아니어야함
    2. 한 클래스의 인스턴스는 다른 서브 클래스의 객체로 변환할 필요가 없어야함(자식간에 형변환X)
    3. 자식 클래스가 부모 클래스의 책임을 무시하거나 재정의하지 않고 확장만 수행해야함
    4. 자식 클래스가 단지 일부 기능을 재사용할 목적으로 유틸리티 역할을 수행하는 클래스를 상속하지 않아야함
    5. 자식 클래스가 역할, 트랜잭션, 디바이스 등을 특수화 해야함