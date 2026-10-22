7주차 - Docker Compose 학습 정리

1. 학습 목표
Docker Compose를 사용하여 여러 컨테이너를 함께 실행하고 관리하는 방법을 이해한다.

2. 학습 내용

Docker Compose란?
여러 컨테이너의 구성과 실행 방법을 compose.yaml 파일에 정의하고 함께 관리하는 도구이다.

주요 개념
- services: 실행할 서비스들을 정의한다.
- ports: 컨테이너 포트를 호스트에 연결한다.
- environment: 컨테이너에 환경 변수를 전달한다.
- volumes: 컨테이너가 데이터를 저장할 공간을 설정한다.
- depends_on: 서비스 간 의존 관계를 지정한다.

컨테이너 네트워크
같은 Compose 네트워크에 있는 서비스들은 서비스 이름을 이용해 서로 통신할 수 있다. 예를 들어 web 서비스가 redis 서비스에 연결할 때 IP 대신 redis라는 이름을 사용할 수 있다.

3. 주요 명령어

```bash
docker compose up -d
docker compose ps
docker compose logs web
docker compose restart web
docker compose down
```

4. 컨테이너 확장
web 서비스를 3개로 실행하려면 다음 명령어를 사용할 수 있다.

```bash
docker compose up -d --scale web=3
```

이 명령어는 web 서비스의 컨테이너 수를 3개로 설정하여 실행한다.
컨테이너 하나를 직접 중지하면 자동으로 3개가 유지되는 것은 아니므로 별도의 관리 방법이 필요할 수 있다.
