# study

## 목차
<details>
<summary>자료구조, 알고리즘</summary>
<div markdown="1">

1. [피보나치 수열](#1-피보나치-수열)
2. [Call by value &amp; Call by reference](#2-call-by-value--call-by-reference)
3. [시간복잡도와 공간복잡도](#3-시간복잡도와-공간복잡도)
4. [정렬과 시간 복잡도](#4-정렬과-시간-복잡도)
5. [배열과 연결리스트](#5-배열과-연결리스트)
6. [스택과 큐](#6-스택과-큐)
7. [DFS와 BFS](#7-dfs와-bfs)
8. [이진탐색](#8-이진탐색)
9. [트리와 그래프](#9-트리와-그래프)
10. [이진트리, 균형이진트리, 레드블랙트리](#10-이진트리-균형이진트리-레드블랙트리)
11. [Heap Tree](#11-heap-tree)
12. [B-Tree, B+Tree](#12-b-tree-btree)

</div>
</details>
<details>
    
<summary>운영체제</summary>
<div markdown="1">

1. [운영체제](#1-운영체제)
2. [메모리 구조](#2-메모리-구조)
3. [프로세스와 스레드](#3-프로세스와-스레드)
4. [CPU 스케줄러](#4-cpu-스케줄러)
5. [가상 메모리](#5-가상-메모리)
6. [데드락](#6-데드락)

</div>
</details>

</div>
</details>
<details>
    
<summary>네트워크</summary>
<div markdown="1">

1. [OSI 7계층](#1-osi-7계층)
2. [TCP와 UDP](#2-tcp와-udp)
3. [IP](#3-ip)
4. [DNS](#4-dns)
5. [로드밸런서](#5-로드밸런서)
</div>
</details>

</div>
</details>
<details>
    
<summary>데이터베이스</summary>
<div markdown="1">

1. [DBMS](#1-dbms)
2. [트랜잭션 특징](#2-트랜잭션-특징)
3. [NOSQL](#3-nosql)
4. [파티셔닝](#4-파티셔닝)
5. [샤딩](#5-샤딩)
</div>
</details>

</div>
</details>
<details>
    
<summary>웹</summary>
<div markdown="1">

1. [브라우저에 url 치면 일어나는 일](#1-브라우저에-url-치면-일어나는-일)
2. [쿠키와 세션](#2-쿠키와-세션)
3. [REST API와 RESTful](#3-rest-api와-restful)
4. [HTTP 응답코드](#4-http-응답코드)
5. [HTTPS](#5-https)
</div>
</details>

---

<details>
<summary>자료구조, 알고리즘</summary>
<div markdown="1">

## 1. 피보나치 수열
### 첫째 및 둘째 항이 1이며, 그 뒤의 모든 항은 바로 앞 두항의 합인 수열
예시) 1, 1, 3, 3, 5, 8, …
편의상 0번째 항을 0으로 두기도 함
<br/>
<br/>
<br/>

---
## 2. Call by value & Call by reference
| Call by value | Call by reference |
| --- | --- |
| 인자로 받은 값을 복사하여 처리 | 인자로 받은 값의 주소를 참조하여 직접 값에 영향을 줌 |
| 원본 값 수정 X | 원본 값 수정 O |
| 변수의 복사본이 전달됨 | 변수 자체가 전달됨 |
| 실제 인수가 다른 메모리 위치에 생성 | 실제 인수가 같은 메모리 위치에 생성 |
<br/>
<br/>
<br/>

---
## 3. 시간복잡도와 공간복잡도
### 시간 복잡도 : 알고리즘의 수행 시간 분석

- 특정 크기의 입력을 기준으로 할 때 필요한 연산의 횟수를 나타냄
- 성능 평가 Case
    - 최선의 경우 (Best Case)
    - 최악의 경우 (Worst Case)
    - 평균의 경우 (Average Case)
- 알고리즘이 복잡해질수록 평균 구하기 어려움 → 최악의 경우로 알고리즘 성능을 파악

### 공간 복잡도 : 알고리즘의 메모리 사용량 분석

- 프로그램 실행과 완료에 얼마나 많은 공간(메모리)가 필요한지를 나타냄
- 공간 (space)
    - 고정 공간 (알고리즘과 무관한 공간)
        - 코드가 저장되는 공간, 알고리즘 실행을 위해 시스템이 필요로 하는 공간 등
    - 가변 공간 (알고리즘과 밀접한 공간)
        - 변수를 저장하는 공간 등의 문제를 해결하기 위해 알고리즘이 필요로 하는 공간

| 시간 복잡도 | 공간 복잡도 |
| --- | --- |
| 얼마나 빠르게 실행되는지를 판단 | 얼마나 많은 자원(메모리 공간)이 필요한지를 판단 |

### 시간 복잡도와 공간 복잡도는 반비례하는 경향이 있음, 보통 알고리즘의 성능을 판단할 때는 시간 복잡도를 위주로 판단
<br/>
<br/>
<br/>

---
## 4. 정렬과 시간 복잡도
### 버블정렬(Bubble Sort)

- 시간 복잡도 : O(N^2)
- 배열의 첫 원소부터 순차적으로 진행하며, 현재 원소가 그 다음 원소의 값보다 크면 두 원소를 바꾸는 작업을 완전히 정렬 될 때까지 반복하는 정렬

### 선택정렬(Selection Sort)

- 시간 복잡도 : O(N^2)
- 배열을 탐색하며 가장 작은 원소를 배열 맨 앞의 원소와 교체, 그 다음으로 작은 원소를 찾아 다시 앞으로 보냄. 이 작업을 완전히 정렬 될 때까지 반복하는 정렬

### 삽입 정렬(Insertion Sort)

- 최선의 경우: O(n), 최악의 경우: O(n^2)
- 배열의 모든 요소를 앞에서 부터 차례대로 이미 정렬된 배열 부분과 비교하여, 삽입하는 작업을 반복하는 정렬

### 병합 정렬(merge Sort)

- 시간 복잡도: O(n log n)
- 배열을 절반씩 나누어 부분리스트가 하나만 남을 때까지 반복. 각각을 정렬한 후 다시 합쳐 정렬하는 작업을 반복하는 정렬

### 퀵정렬(Quick Sort)

- 최악의 경우: O(n^2), 평균의 경우(n log n)
- 배열 중 피벗이 될 원소를 임의의 기준으로 선정하고, 피벗 앞에는 피벗보다 작은 원소들이오고, 피벗 뒤에는 피벗보다 큰 원소들이  오도록 피벗을 기준으로 배열을 나눔. 이렇게 나눈 배열도 앞의 과정을 반복하여 결국 정렬된 상태의 배열이 되는 정렬

### 계수정렬(Counting Sort)

- 시간 복잡도: O(n+k)
- 각 요소의 배열 등장 횟수를 count해 누적합으로 나타낸는 배열을 만든 후 그 누적합으로 요소들의 index를 알아내 작은 숫자 순서대로 정렬하는 정렬

### 기수정렬(Radix Sort)

- 최악의 경우: O(w(n+k))
- 1의 자리, 10의 자리, 100의 자리 … 자리수를 기준으로 정렬하는 정렬
<br/>
<br/>
<br/>

---
## 5. 배열과 연결리스트
### 배열

- 같은 종류의 데이터들이 순차적으로 저장되어 있는 자료 구조
- 배열의 크기는 처음 생성할 때 정하며 이후에는 변경할 수 없음
- 빠른 접근이 요구되고, 데이터의 삽입과 삭제가 적을 경우 자주 사용됨
- 장점
    - 인덱스를 통한 빠른 접근
- 단점
    - 삽입, 삭제가 오래 걸림
    - 중간에 있는 데이터가 삭제되면 공간 낭비가 심함

### 연결리스트

- 각 노드가 데이터와 포인터를 가지고 한 줄로 연결되어 있는 방식으로 데이터를 저장하는 자료구조
- 메모리를 연속적으로 사용하지 않음
- 삽입과 삭제 연산이 잦고, 검색 빈도가 적을 때 자주 사용됨
- 장점
    - 삽입, 삭제에 용이함
- 단점
    - 임의 접근이 불가능하여, 처음부터 탐색을 진행해야함
<br/>
<br/>
<br/>

---
## 6. 스택과 큐
### 스택 (Stack)

- 차곡차곡 쌓아 올린 형태의 자료구조
- LIFO(Last In First Out) 방식, 후입선출
- 가장 마지막에 삽입된 자료가 가장 먼저 삭제
- 삽입 → ’push’, 삭제 → ‘pop’
- 삽입, 삭제가 이루어지는 곳 → ‘top’

### 큐 (Queue)

- 줄(놀이동산에서 **줄**을 서서 순서를 기다릴 때의 **줄**)
- FIFO(First In First Out) 방식, 선입선출
- 가장 먼저삽입된 자료가 가장 먼저 삭제
- 삽입 → ‘enqueue’, 삭제 → ‘dequeue’
- 삽입이 이루어지는 곳 → ‘front’, 삭제가 이루어지는 곳 → ‘rear’

### 우선순위 큐 (Priority Queue)

- 들어오는 순서와 상관없이 우선순위가 높은 데이터가 먼저 삭제
- 삽입 → ‘insert’, 삭제 → ‘delete’
- 구현 (시간 복잡도 상 힙이 유리)
    - 배열
        - 순서없는 : 삽입 → O(1), 삭제 → O(n)
        - 정렬된 :  삽입 → O(n), 삭제 → O(1))
    - 연결리스트
        - 순서없는 : 삽입 → O(1), 삭제 → O(n)
        - 정렬된 : 삽입 → O(n), 삭제 → O(1))
    - 힙(heap)
        - 삽입 → O(log n), 삭제 → O(log n)

### 원형 큐 (=환형 큐, Circular Queue, Ring Buffer)

- 선이 아닌 원의 형태를 가진 큐
- FIFO(First In First Out) 방식, 선입선출
- 삽입 → ‘enqueue’, 삭제 → ‘dequeue’
- 삽입 → rear + 1, 삭제 → front + 1

### 덱 (Deque, Double-ended Queue)

- 양쪽에서 추가, 삭제가 가능한 선형 구조의 자료구조
- 삽입이 이루어지는 곳 → ‘front’, 삭제가 이루어지는 곳 → ‘rear’
- enqueue, dequeue → O(1)
<br/>
<br/>
<br/>

---
## 7. DFS와 BFS
### DFS (Depth First Search, 깊이 우선 탐색)

- 그래프와 트리의 깊은 부분을 우선적으로 탐색하는 알고리즘
- 루트 노드(또는 임의의 노드)에서 최대한 깊이 내려간 뒤, 더 이상 갈 곳이 없으면 다음 분기로 넘어감

### BFS (Breadth First Search, 너비 우선 탐색)

- 그래프와 트리의 인점한 노드부터 탐색하는 알고리즘
- 시작 정점으로 인점한 정점을 먼저 방문하며 최대한 넓게 이동한 다음, 더 이상 갈 곳이 없으면 아래로 이동

| DFS | BFS |
| --- | --- |
| 현재 정점에서 갈 수 있는 점들까지 들어가면서 탐색 | 현재 정점에서 연결된 가까운 점들부터 탐색 |
| 스택 또는 재귀함수로 구현 | 큐를 이용해서 구현 |

### 대표적인 활용 문제

| 문제 | DFS | BFS |
| --- | --- | --- |
| 모든 정점을 방문하는 문제 | 유리 | 유리 |
| 경로의 특징을 저장하는 문제 | 유리 | 불리 |
| 최단거리 문제 | 불리 | 유리 |
<br/>
<br/>
<br/>

---
## 8. 이진탐색
### 이진탐색(Binary Search)

- 정렬된 배열이나 리스트에서 특정한 값을 찾는 알고리즘
- 배열의 중간에 있는 임의의 값을 중간값으로 선택하여 중간값을 기준으로 데이터들을 나눈다. 그후 중간값과 찾는 값을 비교하여 중간값보다 크면 우측을 대상으로하고, 작다면 좌측을 대상으로하여 다시 탐색한다.
- 반드시 데이터들이 일정한 순서로 정렬된 구조에서 사용가능
- 시간 복잡도 : O(log n)
- 장점
    - 검색 속도가 빠름
- 단점
    - 반드시 특정구조가 필요함 (정렬된 구조)
    - 검색대상의 생성, 수정에 취약 (추가적인 메모리 사용 X → 검색 대상을 수정, 추가하는 경우 탐색 시간 길어짐)
<br/>
<br/>
<br/>

---
## 9. 트리와 그래프
### 트리

- 노드와 노드간을 연결하는 간선으로 구성된 자료구조
- 두 개의 노드 사이에 반드시 1개의 경로
- 부모 - 자식 관계 성립 → 계층형 모델 (최상위 노드 = root)
- 노드가 N개 이면 간선 = N - 1개 (완전이진트리의 경우 각 레벨 k에 존재하는 노드는 2^k개)
- 방향성이 존재O,  사이클이 존재 X (비순환)
- 순회 종류 → 전위순회, 중위순회, 후위순회

### 그래프

- 노드와 노드간을 연결하는 간선으로 구성된 자료구조
- 순환 혹은 비순환 구조를 이룸
- 방향이 있는 그래프와 없는 그래프가 있음
- 루트 노드의 개념 X, 부모 - 자식 관계 계념 X
- 2개 이상의 경로 가능 (무방향, 방향, 양방향 가능)

| 특징 | 그래프 | 트리 |
| --- | --- | --- |
| 방향성 | 방향, 무방향 | 방향 |
| 사이클 | 순환, 비순환, 자기순환 | 비순환 |
| 루트노드 | 루트 개념 X | 한 개의 루트 O |
| 부모 - 자식 | 부모 - 자식 개념 X | 한 개의 부모노드 (루트 제외) |
| 모델 | 네트워크 모델 | 계층 모델 |
| 간선 수 | 자유 | N - 1 개 |
<br/>
<br/>
<br/>

---

## 10. 이진트리, 균형이진트리, 레드블랙트리
### 이진트리 (Binary Tree)

- 각 노드가 최대 2개의 자식노드를 가진 트리
- 종류
    - 이진 탐색 트리 (Binary Search Tree, BST)
        - 왼쪽 자식이 부모보다 작고 오른쪽 자식은 부모보다 큰 이진 트리
    - 정 이진트리 (full binary tree)
        - 모든 노드가 0개 또는 2개의 자식 노드를 갖는 트리
    - 완전 이진트리 (complete binary tree)
        - 마지막 레벨을 제외하고 모든 레벨이 완전히 채워져 있는 트리
    - 완전 이진 탐색 트리 (Complete binary search tree)
        - 완전 이진 트리의 성질을 가지는 이진 탐색 트리
    - 포화 이진 트리 (Perfect Binary Tree)
        - 모든 노드가 두개의 자식 노드를 가지고, 모든 리프 노드가 동일한 깊이를 갖는 트리
    - 편향 이진트리 (skewed binary tree)
        - 모든 노드가 왼쪽 또는 오른쪽으로 치우쳐 있는 트리

### 균형 이진 트리 (Balanced Binary Tree)

- 모든 노드의 좌우 서브 트리 높이 차이가 1만큼 나는 트리
- 균형 이진 탐색 트리 (Balanced Binary Search Tree)
    - 노드의 삽입과 삭제가 일어날 때 균형을 유지하도록 하는 트리
    - AVL 트리 (Adelson-Velsky and Landis, 높이 균형 이진 탐색 트리)
        - 스스로 균형을 잡는 이진 탐색 트리
        - Balance Factor(BF) 왼쪽 서브트리에서 오른쪽 서브트리의 높이를 뺀 값 (BF가 최대 1까지 차이나면 균형이 잡힘)
        - 삽입, 삭제 연산을 수행할 때 회전
        - 회전 종류
            - LL 회전
            - RR 회전
            - LR 회전
            - RL 회전

### 레드블랙 트리 (Red-Black Tree)

- 자가 균형 이진 탐색 트리
- 조건
    - 모든 노드는 빨간색 혹은 검은색
    - 루트 노드와 모든 리프 노드(NIL)는 검은색
    - 빨간색 노드의 자식은 검은색 (빨간색 노드가 연속으로 나올 수 없음)
    - 모든 리프 노드에서 루트 노드까지 가는 경로에서 만나는 검은색 노드의 개수는 같음
<br/>
<br/>
<br/>

---

## 11. Heap Tree
### 힙 트리 (Heap Tree)

- 완전 이진 트리의 일종, 우선순위 큐를 위해 만들어짐
- 종류
    - 최대 힙 (max heap)
        - 부모 노드의 키값 ≥ 자식노드의 키값
    - 최소 힙 (min heap)
        - 부모 노드의 키값 ≤ 자식노드의 키값
- 특징
    - 최대값과 최소값을 O(1)의 속도로 구할 수 있음
    - 배열을 이용하여 구현
    - 인덱스 1부터 시작
    - 인덱스
        - 왼쪽 자식의 인덱스 : (부모의 인덱스) * 2
        - 오른쪽 자식의 인덱스 : (부모의 인덱스) * 2 + 1
        - 부모의 인덱스 : (자식의 인덱스) / 2
- 데이터 삽입
    - max heap
        - 데이터를 맨 마지막 인덱스에 추가
        - 부모 노드보다 작다면 그대로 둠
        - 부모 노드보다 크다면 부모 노드와 위치를 바꿈
- 데이터 삭제
    - max heap
        - root 노드를 삭제
        - root 노드의 자리에 마지막 노드를 가져옴
        - heap을 재구성 (만약 자식 노드보다 크다면 그대로 두고, 작다면 자식노드와 값을 바꿈)
<br/>
<br/>
<br/>

---

## 12. B-Tree, B+Tree
### B-Tree

- 균형 잡힌 트리 (삽입, 삭제 시 특정 규칙에 맞게 재정렬)
- 특징
    - 한 노드의 키가 k개라면 자식 노드의 개수는 k + 1
    - 노드의 키는 항상 정령된 상태
    - 리프 노드가 아닌 노드는 항상 2개 이상의 자식 노드를 가짐
    - 모든 리프 노드들은 항상 같은 레벨
    - 각 노드는 여러 개의 키와 각 키에 대응하는 데이터를 가짐
    - 노드들의 키는 중복되지 않음
    - 각 노드는 자식 노드를 참조하는 포인터를 가짐

### B+Tree

- B-Tree의 모든 데이터를 순회하기 위해 리프 노드까지 갔다가 다시 부모 노드로 BackTracking하여 트리의 모든 노드를 방문하는 비효율을 보완하기 위한 것이 B+Tree
- 특징
    - 데이터는 리프 노드에만 저장
    - 리프 노드가 아닌 루트 노드나 중간 노드들은 자식 노드로 향하는 포인터만 가짐
    - 모든 리프 노드들은 linked list를 통해 서로 연결
    - 중간 노드들의 키를 통해 리프 노드를 찾아감 → 노드들이 갖는 키는 중복 가능
- 장점
    - 리프 노드가 아닌 노드들에 실제 데이터를 저장하지 않고 키에 따라 자식 노드로 향하는 포인터만 가질 수 있어서 **저장 공간 절약, 더 많은 포인터를 저장 가능**
    - 한 노드가 가질 수 있는 자식 노드의 최대 개수를 늘릴 수 있음 → 트리의 depth를 낮출 수 있음
    - Full scan시, linked list로 연결된 리프 노드들에 대해서만 읽기를 진행 → 시간 단축
- 단점
    - 실제 데이터까지 접근하기 위해서는 무조건 트리의 맨 아래에 있는 리프 노드까지 접근해야 함
    

|  | B-Tree | B+Tree |
| --- | --- | --- |
| 데이터 | 모든 노드에 저장 | 리프 노드에만 저장 |
| key | 중복 없음 | 중복 가능 |
| Full Scan | 모든 노드를 순회하며 탐색 | linked list를 통해 리프 노드만 선형 탐색 |
| key를 통한 검색 | 리프 노드까지 가지 않아도 되는 경우 있음 | 무조건 리프 노드까지 가야 함 |
| 높이 | 높음 | 낮음 |

<br/>
<br/>
<br/>

---
</div>
</details>

<details>
<summary>운영체제</summary>
<div markdown="1">

## 1. 운영체제
### 시스템의 자원과 동작을 관리하는 소프트웨어
### 프로세스, 저장장치, 네트워킹, 사용자, 하드웨어를 관리
<br/>
<br/>
<br/>

---

## 2. 메모리 구조
- Code : 소스코드
- Data : 전역변수, 정적변수 할당
- Heap : 사용자가 직접 동적으로 할당
- Stack : 함수의 호출정보, 지역변수, 매개변수 등 저장
<br/>
<br/>
<br/>

---

## 3. 프로세스와 스레드
- 프로세스 : 실행중인 프로그램 (예 : 유튜브 창)
    - 메모리와 CPU를 프로세스마다 할당받아서 사용

- 스레드 : 프로세스 안 실행 단위 (예 : 밑에서 움직이는 바, 좋아요)
    - 프로세스 안 다른 스레드와 메모리와 CPU를 공유해서 사용
<br/>
<br/>
<br/>

---

## 4. CPU 스케줄러
### 준비큐에 있는 프로세스에 대해 CPU 할당하는 방법
- 비선점 스케줄링
    - FCFS : 먼저 요청한 프로세스를 먼저 처리
    - SJF : 사용하는 시간이 짧은 프로세스 먼저 처리
- 선점 스케줄링
    - SRT : 남은 시간이 짧은 프로세스 먼저 처리
    - RR : time slice를 기반으로 스케줄링
<br/>
<br/>
<br/>

---

## 5. 가상 메모리
### 사용하는 부분만 메모리에 올리고, 나머지는 디스크에 보관
<br/>
<br/>
<br/>

---

## 6. 데드락
### 프로세스가 자원을 얻지 못해 다음 작업을 하지 못하는 상태
- 발생 조건
    - 상호 배제 : 자원은 한 번에 한 프로세스만 사용 가능
    - 점유 대기 : 자원을 점유하고 있으면서 자원을 추가로 점유하기 위해 대기하고 있어야함
    - 비선점 : 다른 프로세스에 할당된 자원을 끝날 때까지 강제로 빼앗을 수 없음
    - 순환 대기 : 점유한 자원을 대기하며 순환의 모습으로 대기해야함 (예 : P1은 P2가 점유한 자원을 대기, P2는 P3가 점유한 자원을 대기, P3는 P1이 점유한 자원을 대기)
<br/>
<br/>
<br/>

---
</div>
</details>

<details>
<summary>네트워크</summary>
<div markdown="1">
    
## 1. OSI 7계층
### 네트워킹에 대한 표준을 7계층으로 나눈것
- 1계층 물리 계층
- 2계층 데이터 링크 계층
- 3계층 네트워크 계층
- 4계층 전송 계층
- 5계층 세션 계층
- 6계층 표현 계층
- 7계층 응용 계층
  
<br/>
<br/>
<br/>

---

## 2. TCP와 UDP
- TCP : 신뢰성 높은 프로토콜
    - 데이터를 받았는지 확인 가능
    - UDP보다 속도가 느림
- UDP : 빠른 프로토콜
    - 데이터를 받았는지 확인 불가
    - 스트리밍 서비스에서 사용
  
<br/>
<br/>
<br/>

---

## 3. IP
### 인터넷에서 데이터 전달 프로토콜
- 비신뢰성 : 패킷의 완전한 전달을 보장하지 않음
- 비연결성 : 패킷을 보내는 길을 정하지 않음
  
<br/>
<br/>
<br/>

---

## 4. DNS
### 도메인 주소를 IP 주소로 변환해주는 시스템
  
<br/>
<br/>
<br/>

---

## 5. 로드밸런서
### 서버의 부하를 분산시켜주는 시스템
- L4 : 4계층 이하의 정보를 가지고 로드를 분산
- L7 : 응용 계층의 정보를 가지고 로드 분산
  
<br/>
<br/>
<br/>

---

</div>
</details>

<details>
<summary>데이터베이스</summary>
<div markdown="1">
    
## 1. DBMS
### 데이터베이스 내 데이터에 접근하도록 도와주는 시스템
  
<br/>
<br/>
<br/>

---

## 2. 트랜잭션 특징
### 데이터베이스 내 데이터에 접근하도록 도와주는 시스템
A : 원자성
- 부분적으로 실행되거나 중단되지 않는 것
  
C : 일관성
- 일관적인 DB상태를 유지하는 것
  
I : 격리성
- 트랜잭션 작업이 끼어들지 못하도록 보장하는 것
  
D : 지속성
- 트랜잭션은 영원히 반영되는 것
  
<br/>
<br/>
<br/>

---

## 3. NOSQL
### Not Only SQL, SQL을 보완한다는 의미
- 스키마가 없음
- 삽입, 조회 빠름
- 대량의 분산 데이터를 저장하는데 특화
  
<br/>
<br/>
<br/>

---

## 4. 파티셔닝
### 테이블을 컬럼 단위로 나누어 관리하는 기법
- update나 insert 같은 작업이 분산되어 성능 향상
- 테이블간 join 비용이 증가
- index를 별도로 파티셔닝할 수 없음
  
<br/>
<br/>
<br/>

---

## 5. 샤딩
### 테이블을 row단위로 분산하여 저장하는 방법
- Hash Sharding
- Dynamic Sharding
  
<br/>
<br/>
<br/>

---

</div>
</details>

<details>
<summary>웹</summary>
<div markdown="1">

## 1. 브라우저에 url 치면 일어나는 일
1. 브라우저에서 DNS 서버에서 도메인명으로 IP 주소를 가져오게 됨
2. HTTP Request 메시지 작성
3. OS의 프로토콜 스택에 메시지 전송 의뢰
4. 프로토콜 스택이 LAN에 제어정보를 붙인 패킷을 LAN어댑터에 넘김
5. LAN 어댑터는 전기신호로 변환시켜 LAN 케이블로 송출
6. 송신한 패킷은 허브, 스위치, 라우터를 경유
7. 프로바이더(ISP)에 전달
8. pop 거쳐서 인터넷 핵심부로 감
9. 고속 라우터들 사이로 서버까지 도달
10. 방화벽이 패킷을 검사
11. 캐시서버가 응답 데이터가 있는지 확인
12. 웹서버에 전송
13. 패킷을 추출해서 WAS에 전달
14. 응답 메시지를 만들어서 위의 방법대로 다시 클라이언트에게 전달
  
<br/>
<br/>
<br/>

---

## 2. 쿠키와 세션
### HTTP는 상태와 연결에 대한 정보를 저장하지 않아, 이를 도와주는 것
쿠키
- 사용자 정보가 기록된 텍스트 파일
- 브라우저에 저장되면서, 통신할 때 HTTP 헤더에 포함되어 전송
- 통신 중 정보가 노출될 수 있기 때문에 보안에 취약
세션
- 사용자의 정보를 서버에 저장
- 브라우저가 종료될 때까지 유지
- 서버에 저장되기 때문에 보안이 강함
  
<br/>
<br/>
<br/>

---

## 3. REST API와 RESTful
### REST 기반으로 서비스 API를 구현한 것
REST : 이름으로부터 자원의 정보를 주고받는 것
- 자원을 URI로 표현
- 자원에 대한 행위는 HTTP Method로 표현
RESTful : REST의 원리를 잘 따르는 시스템
- 자원을 URI로, 행위에 맞는 적절한 HTTP Method를 사용한 것이 RESTful한 메소드
- RESTful 하지 않은 것 : 예) CRUD기능 모두 POST로 처리한 것
  
<br/>
<br/>
<br/>

---

## 4. HTTP 응답코드
- 100 : 조건부 응답 (요청을 받아서 지금 처리하고 있음을 의미)
- 200 : Successful Response (Request가 성공적으로 처리되었음을 의미)
- 300 : Redirection (클라이언트를 지정된 위치로 이동하게 하는 것)
- 400 : 클라이언트 오류 (HTTP 요청이 잘못되거나 권한이 없을때 나타나게 됨)
- 500 : 서버 오류 (서버가 요청을 제대로 수행하지 못할때 발생)
  
<br/>
<br/>
<br/>

---

## 5. HTTPS
### 암호화 프로토콜을 사용하여 HTTP 통신을 안전하게 하는 프로토콜
- HTTP의 문제를 보완하고자 사용하는 것
- HTTP의 문제
    - 평문 통신을 해서 도청 가능
    - 통신상대를 확인하지 않아서 위장 가능
    - 완전성을 증명할 수 없어서 변조 가능
- HTTP에서 통신하는 소켓을 암호화 프로토콜을 사용하여 TCP와 통신하도록 함
- 암호화 프로토콜을 사용함으로써 암호화, 증명서, 변조 방지 가능
  
<br/>
<br/>
<br/>

---

</div>
</details>
