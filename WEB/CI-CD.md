# CI/CD
## CI/CD 란?
- 애플리케이션 개발 단계를 자동화하여 애플리케이션을 보다 짧은 주기로 고객에게 제공하는 방법
- 기본 개념은 지속적인 통합, 지속적인 서비스 제공, 지속적인 배포
- 애플리케이션의 통합 및 테스트 단계에서부터 제공 및 배포에 이르는 라이프 사이클 전체에 걸쳐 지속적인 자동화와 모니터링을 제공

## CI
- 개발자를 위한 자동화 프로세스인 지속적인 통합(Continuous Integration)을 의미
- 새로운 코드 변경사힝이 정기적으로 빌드 및 테스트되어 공유 레포지토리에 통합되므로 여러명의 개발자가 동시에 작업 할 경우 충돌할 수 있는 문제를 해결

## CD
- 지속적인 서비스 제공(Continuous Delivery) 및 지속적인 배포(Continuous Deplyment)를 의미
- ### 지속적인 제공
    - 개발자들이 애플리케이션에 적용한 변경사항이 테스트를 거쳐 레포지토리에 자동으로 업로드 되는 것을 의미
    - 운영팀은 레포지토리에서 애플리케이션을 실시간 프로덕션 환경으로 배포 할 수 있음
    - 개발팀과 비지니스팀 간의 가시성과 커뮤니케이션 문제를 해결해줌
- ### 지속적인 배포
    - 개발자의 변경사항을 레포지토리에서 고객이 사용 가능한 프로덕션 황경까지 자동으로 릴리스 하는 것을 의미
    - 애플리케이션 제공 속도를 저해하는 수동 프로세스의 문제를 해결

## CI/CD의 필요성
- 모든 브랜치 소스 코드를 병합할 경우 반복적인 수작업으로 많은 시간이 소요됨
- 애플리케이션에 변경사항이 적용될 때 다른 개발자와의 충돌이 발견되면 `CI`를 통해 버그를 수정 할 수 있음
- 시스템과 애플리케이션을 최신 상태로 유지 할 수 있음