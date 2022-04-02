# TIL-Today-I-Learned-
Python Grammar

<파이썬에서 리스트를 문자열로 일정하게 합쳐주는 join 함수>

1. ''.join(리스트)
2. '구분자'.join(리스트)

join 함수는 매개변수로 들어온 리스트에 있는 요소 하나하나를 합쳐서 하나의 문자열로 바꾸어 반환하는 함수이다.

- ''.join(리스트)

''.join(리스트)를 이용하면 매개변수로 들어온 ['a', 'b', 'c'] 이런 식의 리스트를 'abc'의 문자열로 합쳐서 반환해주는 함수이다.

- '구분자'.join(리스트)

'구분자'.join(리스트)를 이용하면 리스트의 값과 값 사이에 '구분자'에 들어온 구분자를 넣어서 하나의 문자열로 합쳐준다.
'_'.join(['a', 'b', 'c']) 라 하면 "a_b_c" 와 같은 형태로 문자열을 만들어서 반환해준다.

- python int형 리스트 join하기

output 출력 할 때 리스트를 적당히 다듬어서 출력할 일이 종종 있다. 
```python
num_list = [-1, 0, 1, 3, 4, 5, 9]

print(num_list)
# [-1, 0, 1, 3, 4, 5, 9]
print(" ".join(map(str, num_list)))
# -1 0 1 3 4 5 9

# print(" ".join(num_list))
# TypeError: sequence item 0: expected str instance, int found
```
> ## python 3.6.1 문서를 참고.  
>str.join(iterable)
Return a string which is the concatenation of the strings in the iterable iterable. A TypeError will be raised if there are any non-string values in iterable, including bytes objects. The separator between elements is the string providing this method.