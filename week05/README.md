5주차 - Docker 기초 학습 정리

1. 학습 목표
Docker의 기본 개념을 이해하고 이미지와 컨테이너의 차이를 정리한다.

2. 학습 내용

Docker란?
Docker는 애플리케이션과 실행에 필요한 환경을 컨테이너로 묶어 여러 환경에서 비슷하게 실행할 수 있도록 도와주는 플랫폼이다.

이미지와 컨테이너
- 이미지: 컨테이너를 만들기 위한 읽기 전용 템플릿
- 컨테이너: 이미지로부터 만들어져 실행되는 인스턴스

주요 명령어
- docker --version : Docker 버전 확인
- docker images : 이미지 목록 확인
- docker ps : 실행 중인 컨테이너 확인
- docker logs : 컨테이너 로그 확인
- docker stop : 컨테이너 중지
- docker rm : 컨테이너 삭제

3. 실습 정리
nginx 이미지를 이용해 컨테이너를 실행하고 웹 브라우저에서 접속하는 실습을 학습했다.

예시 명령어:
docker run -d -p 8080:80 --name web nginx

브라우저에서 http://localhost:8080 으로 접속하면 웹 페이지를 확인할 수 있다.
