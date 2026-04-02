# 🧸 playground_root

## 📑 목차
  1. [소개](#소개)
  2. [기능](#기능)
  3. [스택](#스택)
  4. [실행방법](#실행방법)

## 🪄 소개
  - MSA 및 이벤트 기반 비동기 구조 학습을 위한 개인 프로젝트
  - 대규모 트래픽을 감안한 아키텍처 설계, 성능 최적화 중점

## 🔮 기능
  1. 회원 서비스
  - 회원가입
  - 로그인
  - 로그아웃
  2. 채팅 서비스
  - 채팅방 CRUD
  - 채팅 송수신

## 🎡 스택
  <div>
    <img src="https://img.shields.io/badge/java-E84D3D?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
    <br/>
    <img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/redis-FF4438?style=for-the-badge&logo=redis&logoColor=white">
    <br/>
    <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white"> <img src="https://img.shields.io/badge/docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
  </div>

## ✔️ 실행방법
  ### 🏗️ 구조
  ```
  workspace_playground/
  ├─ docker-compose.yml
  ├─ .dockerignore
  ├─ .env
  ├─ auth-service/
  ├─ user-service/
  ├─ chat-service/
  ├─ gateway/
  └─ security-core/
  ```
  ### ▶️ 실행
  ```sh docker-compose up --build ```
  ### ⏹️ 종료
  ```sh docker-compose down ```
  ### ⚠️ 필요사항
  - docker와 docker-compose
  - 실행 중인 Redis & MySQL 컨테이너
    -> 컨테이너명: redis & mysql
  - 동일한 도커 네트워크
    -> 네트워크명: my-network
  - .env 파일<br/>
    EX)<br/>
    ```
    # .env 템플릿
    
    # 공통
    SPRING_PROFILES_ACTIVE=local
    
    # port
    AUTH_PORT=8081
    USER_PORT=8082
    CHAT_PORT=8083
    
    # redis
    REDIS_HOST=redis
    REDIS_PORT=6379
    
    # mysql
    MYSQL_HOST=mysql
    MYSQL_PORT=3306
    MYSQL_USERNAME=username
    MYSQL_PASSWORD=password
    # DB
    MYSQL_DB_AUTH=auth-service
    MYSQL_DB_USER=user-service
    MYSQL_DB_CHAT=chat-service
    ```
