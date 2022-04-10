# Python 문자열 비교 
> 완전 일치: ==, !=

2개의 문자열이 완전히 일치하는지 판정하기 위해서 == 연산자 사용.
일치하면 True, 일치하지 않을 시 False 반환.
```python
print('Hi' == 'Hi')
#True
print('asdf' == 'fdsa')
#False
print('ABC' == 'abc')
#False
```
> 부분일치: in, not in

문자열이 부분적으로 일치할 경우에는 in 연산자 사용.
```python
print('bbb' in 'aaabbbccc')
#True
print('111' in '123456')
#False
```
