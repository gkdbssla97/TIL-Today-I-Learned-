덱(Dequeue)은 데이터 값을 저장하는 기본적인 구조로, 일차원의 선형 자료구조이다.
덱은 스택(Stack)과 큐(Queue)의 연산을 모두 지원하는 자료구조로, 양 끝에서 모두 삽입과 삭제가 가능한 큐라고 생각하면 된다.
나머지 부가적인 덱의 길이를 반환하는 연산이나 덱이 비어있는지 확인하는 연산 등은 스택과 큐에 구현되어 있는 연산들과 유사하게 구현된다.

# 예시코드
from collections import deque

d = deque()
print(type(d)) # <class 'collections.deque'>


## 스택이나 큐처럼 덱의 오른쪽에서 요소 삽입 : append
for i in range(10):
    d.append(i)
print(d) 

->deque([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])


## 덱의 왼쪽에서 요소 삽입 : appendleft
d.appendleft(10)
print(d) 

-> deque([10, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9])


## 덱 중간에 요소 삽입 : insert
d.insert(5, 11)
print(d) 

-> deque([10, 0, 1, 2, 3, 11, 4, 5, 6, 7, 8, 9])


## 덱 왼쪽/오른쪽에 iterable한 객체를 통째로 append 하여 연장시키는 연산 : extendleft / extend
d.extend([0, 0, 0])
print(d) 

-> deque([10, 0, 1, 2, 3, 11, 4, 5, 6, 7, 8, 9, 0, 0, 0])

d.extendleft([0, 0, 0])
print(d) 

-> deque([0, 0, 0, 10, 0, 1, 2, 3, 11, 4, 5, 6, 7, 8, 9, 0, 0, 0])


## 스택처럼 덱의 오른쪽에서 요소 삭제 : pop
for i in range(10):
    d.pop()
print(d) 

-> deque([0, 0, 0, 10, 0, 1, 2, 3])


## 큐처럼 덱의 왼쪽에서 요소 삭제 : popleft
for i in range(3):
    d.popleft()
print(d) 

-> deque([10, 0, 1, 2, 3])


## 작업을 완료한 후에는 일반적인 리스트처럼 이용할 수도 있다
print(list(d)) 
[10, 0, 1, 2, 3]