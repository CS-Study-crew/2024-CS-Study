# 2024-CS-Study
신입 개발자 면접 대비 CS 스터디 👨🏻‍💻👩🏻‍💻 🔥

## 👾 스터디 멤버

|                      [나지현](https://github.com/jihyunna)                      |                       [노소희](https://github.com/SO-HUII)                        |                       [이유진](https://github.com/2UJ1N)                        |                      [박다영]()                      |                      [채현영](https://github.com/CheHyeonYeong)                      |
|:-----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| <img src="https://github.com/CS-Study-crew/2024-CS-Study/assets/75558337/cb67efda-ffc6-4ec5-bed2-61cecb1cbf89" width="150">|  <img src="https://github.com/CS-Study-crew/2024-CS-Study/assets/109736890/b3ba0c47-c0a6-4584-9311-19b02eec58a6" width="150">  | <img src="https://github.com/42CSstudy/CS-Study/assets/83401978/6b1ca123-2b0b-4010-9b7d-39a2f782a0bc" width="150">| <img src="" width="150">  | <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR2_tJM7qeE088OpvDREun7uRzz-OYjl-2_fV3RFY0t2w&s" width="150">  | <img src="" width="150">  |

<br>

## 🤙 스터디 진행 방식

| 항목             | 내용                                                         |
| ---------------- | ------------------------------------------------------------ |
| **기간**         | 2024년 01월 19일 ~                                           |
| **장소**         | 스터디카페 or 서울시 청년 일자리센터 일자리카페                           |
| **요일 및 시간** | 매주 목요일 오전 10:00 ~ 오후 12:00 (약 2시간)            |
| **방식**         | 각 CS 과목의 키워드에 해당하는 지식을 학습하고, 자주 나오는 면접 질문의 답변을 정리한다.<br />한 챕터가 끝나면 해당 챕터에 대해 모의 면접을 진행한다.<br />|
| **규칙**         |- 불참은 전날 자정까지 사유와 함께 공지한다.<br />- 지각 - 10시5분 이후~ 30분 내 벌금 **1,000원** 이후 **3,000원**<br />- 과제 - 항목당 벌금 **1,000원**|

<br>

## 📋 각종 컨벤션

### 📁 패키지 구조

```
CS-study
    ├── database
    |   └── 01_관계형_데이터베이스.md
    |   └── ...
    |
    ├── network
    |   └── ...
    |
    ├── interview => 면접 질문 아카이빙
    |   ├── database_expected_question.md => 데이터베이스 면접 질문
    |   ├── os_expected_question.md
    |   └── ...
    ...
```



### 📍 커밋 및 PR

1. **커밋 메시지**

   ```
   커밋메세지: [카테고리] {커밋 메세지}
   ```
   ```
   docs: 파일 생성
   add: 파일 추가 - 이미지 파일 업로드
   chore: 파일 내부 수정
   rename: 파일명 수정
   fix: 오류 처리시
   ```

   - 작성 예시) `[OS] CPU 스케줄링 알고리즘`
   - 수정 예시) `rename: [OS] 이름 수정`

<br>

## 📌 목차

### 1️⃣ 자료구조(Data Structure)

- 배열 Array
- 연결 리스트 Linked List
- 벡터 Vector
- 스택 Stack
- 큐 Queue
- 그래프 Graph
- 트리 Tree
- 힙 Heap
- 맵 Map
- 셋 Set
- 해시 Hash
- 트라이 Trie
- B-Tree & B+Tree

### 2️⃣ 알고리즘(Algorithm)
- 거품 정렬 Bubble Sort
- 선택 정렬 Selection Sort
- 삽입 정렬 Insertion Sort
- 퀵 정렬 Quick Sort
- 병합 정렬 Merge Sort
- 힙 정렬 Heap Sort
- 기수 정렬 Radix Sort
- 계수 정렬 Count Sort
- 이분 탐색 Binary Search
- 해시 테이블 구현
- DFS & BFS
- 최장 증가 수열 LIS
- 최소 공통 조상 LCA
- 동적 계획법 Dynamic Programming
- 다익스트라 Dijkstra
- 비트마스크 BitMask

### 3️⃣ 운영체제
- 운영체제 소개
  - 운영체제 필요성
  - 운영체제 정의
  - 운영체제 역할
- 운영체제 구조
  - 커널
  - 시스템 호출
- 프로세스
  - 프로세스 개념
  - 프로세스 상태
  - 프로세스 제어 블록
  - 프로세스 문맥 교환
- 스레드
  - 스레드 개념
  - 멀티스레드의 구조
  - 멀티스레드의 장단점
  - 멀티 프로세스 VS 멀티 스레드
- CPU 스케줄링
  - 장기 스케줄링
  - 중기 스케줄링
  - 단기 스케줄링
- 스케줄링 알고리즘
  - FCFS
  - SJF
  - Round Robin
  - SRT
  - Priority scheduling
  - Multilevel Queue
  - Multilevel Feedback Queue
- 인터럽트
  - 인터럽트 개념
  - 동기적 인터럽트, 비동기적 인터럽트
  - 인터럽트 처리 과정
  - 인터럽트와 이중 모드
- 프로세스 동기화
  - 공유자원, 경쟁상태, 임계구역
  - 피터슨 알고리즘
  - 뮤텍스
  - 세마포어
  - 모니터
- 교착 상태(Deadlock)
  - 교착 상태 정의
  - 교착 상태 조건
  - 교착 상태 해결 방법
  - 식사하는 철학자 문제
- 메모리 관리
  - 메모리 관리 필요성
  - 고정 분할 방식
  - 가변 분할 방식
- 가상 메모리 개요
  - 가상 메모리 정의
  - 가상 메모리 필요성
  - 페이징 기법
  - 세그먼테이션 기법
- 가상 메모리 관리
  - 요구 페이징
  - 페이지 교체 알고리즘
    - FIFO
    - OPT
    - LRU

### 4️⃣ 데이터베이스(DB)

- 관계형 데이터베이스
  - 데이터베이스와 파일시스템의 차이
  - 관계형 데이터베이스의 개념과 장단점
  - DDL, DML, DCL, TCL
  - Key
- MySQL 아키텍처
  - innodb
  - 쿼리동작 방식
- Join
- 이상 현상과 정규화
- 트랜잭션
  - 트랜잭션 개념
  - ACID
  - Commit, Rollback
  - 트랜잭션 격리수준
  - LOCK, 교착상태
- 인덱스
  - 인덱스 개념
  - 인덱스 종류
  - Clustered index, Non-Clustered index
  - 인덱스 자료구조
- Master/Slave
- Sharding
- NoSQL
  - NoSQL의 개념
  - RDB VS NoSQL
  - Redis 동작원리

### 5️⃣ 네트워크 (Network)

- 네트워크 레이어
    - OSI 7계층
    - TCP/IP 4계층
    - IP
        - IPv4 vs IPv6
        - subnet
        - CIDR
- 통신
    - TCP
        - 흐름제어, 혼잡제어, 오류제어
        - 3-way-handshake, 4-way-handshake
    - UDP
    - HTTP
        - HTTP status code
        - HTTP method
        - HTTP 1.1, 2.0, 3.0
    - HTTPS, SSL/TSL
    - DNS
    - 기타 : socket, STOMP, SMTP (프로젝트에서 사용한 경우)
- Web
    - Web Server vs WAS
    - Web Server
        - apache vs nginx (동작원리)
        - SSL offloading
        - reverse proxy
        - load balancing
            - L7 vs L4
            - 알고리즘
    - Web cache
    - URI, URN, URL
    - Rest API
- 보안
    - CORS
    - XSS
    - SQL Injection
- 인증
    - cookie
    - session
    - JWT
