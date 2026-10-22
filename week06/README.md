6주차 - Dockerfile 학습 정리

1. 학습 목표
Dockerfile을 이용해 애플리케이션 실행에 필요한 이미지를 직접 만들고, 빌드 과정을 이해한다.

2. 학습 내용

Dockerfile이란?
Docker 이미지를 만들기 위한 명령어를 작성한 파일이다. 필요한 환경과 실행 방법을 코드로 정의할 수 있다.

주요 명령어
- FROM: 기반이 되는 이미지를 지정한다.
- WORKDIR: 작업 디렉터리를 설정한다.
- COPY: 파일을 이미지 내부로 복사한다.
- RUN: 이미지 빌드 과정에서 명령어를 실행한다.
- CMD: 컨테이너가 시작될 때 기본으로 실행할 명령어를 지정한다.
- EXPOSE: 컨테이너가 사용하는 포트를 문서화한다.

3. 빌드와 실행
Dockerfile이 있는 디렉터리에서 이미지를 빌드한다.

```bash
docker build -t myapp:v1 .
docker images
```

이미지를 이용해 컨테이너를 실행한다.

```bash
docker run -d --name myapp -p 8080:80 myapp:v1
docker ps
```
