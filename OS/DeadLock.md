# Dead Lock
- 프로세스가 자원을 얻지 못해 다음 처리를 하지 못하는 상태로 `교착 상태`라고도 함
- 시스템적으로 한정된 자원을 여러 곳에서 사용하려고 할 때 발생
## 발생 조건
- 교착 상태는 4가지 조건이 동시에 성립 할 때 발생
    - 상호 배제(Mutual Exclusion) : 한 자원은 한 번에 한 프로세스만 사용할 수 있어야함
    - 점유 대기(Hold and Wait) : 프로세스 자원을 가진 채 다른 자원을 기다릴 수 있음
    - 비선점(No Preemption) : 다른 프로세스에 할당된 자원은 사용이 끝날 때까지 강제로 빼앗을 수 없음
    - 순환 대기(Circular Wait) : 프로세스의 집합에서 각 프로세스는 순환적으로 다음 프로세스가 필요로하는 자원을 가지고 있음
## 해결 방법
- 예방(Prevention) : 4가지 발생 조건이 하나라도 발생하지 못하게 함
- 회피(Avoidance) : 알고리즘이 데드락이 발생하지 않도록 적용
- 회복(Recovery) : 교착상태가 발생하면 해결
- 무시(Ignore) : 회복과정의 성능저하가 더 심하면 무시