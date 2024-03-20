# study

## 목차
1. [피보나치 수열](#1-피보나치-수열)
2. [Call by value &amp; Call by reference](#2-call-by-value--call-by-reference)

---

## 1. 피보나치 수열
### 첫째 및 둘째 항이 1이며, 그 뒤의 모든 항은 바로 앞 두항의 합인 수열
예시) 1, 1, 3, 3, 5, 8, …
편의상 0번째 항을 0으로 두기도 함



## 2. Call by value & Call by reference
| Call by value | Call by reference |
| --- | --- |
| 인자로 받은 값을 복사하여 처리 | 인자로 받은 값의 주소를 참조하여 직접 값에 영향을 줌 |
| 원본 값 수정 X | 원본 값 수정 O |
| 변수의 복사본이 전달됨 | 변수 자체가 전달됨 |
| 실제 인수가 다른 메모리 위치에 생성 | 실제 인수가 같은 메모리 위치에 생성 |
