# Singleton Pattern
- 어떤 클래스가 최초 한번만 메모리를 할당하고(Static) 그 메모리에 객체를 만들어 사용하는 디자인 패턴
- 객체를 하나만 생성하고 그 객체를 어디에서든 참조할 수 있음

## 역할이 수행하는 작업
- ### Singleton
    - 하나의 인스턴스만을 생헝하는 책임이 있음
    - getInstance 메서드를 통해 모든 클라이언트에게 동일한 인스턴스를 반환하는 작업을 수행

## 사용하는 이유
- 객체 생성을 한번만 하기 때문에 재사용이 가능해 메모리 낭비를 방지할 수 있음
- 싱글톤으로 생성된 객체는 전역성을 띄기 때문에 다른 객체와 공유 가능

## 문제점
- 멀티 스레드 환경에서 동기화 문제인 경합조건 발생
    - 경합조건
        - 메모리와 같은 동일한 자원을 2개 이상의 스레드가 이용하려고 경합하는 현상
- 싱글톤 인스턴스의 역할이 많거나 많은 데이터를 공유시킬 경우 다른 클래스의 인스턴스들간에 결합도가 높아져 `OCP` 위배