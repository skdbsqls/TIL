# Non-sequence Types

# dict(딕셔너리)
**key-value 쌍**으로 이루어진 **순서와 중복이 없는** **변경 가능한** 자료형

## 딕셔너리 표현
```python
my_dict_1 = {}
my_dict_2 = {'key': 'value'}
my_dict_3 = {'apple': 12, 'list': [1, 2, 3]}

print(my_dict_1)  # {}
print(my_dict_2)  # {'key': 'value'}
print(my_dict_3)  # {'apple': 12, 'list': [1, 2, 3]}
```
- key는 변경 불가능한 자료형만 사용 가능하다.
- 불변 자료형 : `str`, `int`, `float`, `tuple`, `range` ...
- key는 해당 key값에 접근했을 때 해당하는 value를 준다고 보장해야 하는데, 변경 가능한 자료형을 사용할 경우 주소값이 변경되어 해당 value를 준다는 보장을 할 수 없기 때문에 변경 불가능한 자료형만 사용 가능하다.
- value는 모든 자료형이 사용 가능하다.
- 중괄호(`{}`)로 표기한다.

## 리스트와 딕셔너리
- 리스트는 선형 자료형으로 어떤 자료를 찾으려면 순서대로 하나씩 찾아가야 한다.
- 이러한 불편함을 극복하기 위해 각 데이터 요소에 이름을 붙여 한 번에 찾아가고자 딕셔너리 자료형이 등장했다.

## 딕셔너리 사용
```python
my_dict = {'apple': 12, 'list': [1, 2, 3]}

print(my_dict['apple']) # 12
print(my_dict['list']) # [1, 2, 3]

# 추가
my_dict['banana'] = 50
print(my_dict)  # {'apple': 12, 'list': [1, 2, 3], 'banana': 50}

# 변경
my_dict['apple'] = 100
print(my_dict)  # {'apple': 100, 'list': [1, 2, 3], 'banana': 50}
```
- key를 통해 value에 접근한다.
- 중복이 없다는 것은 key의 입장에서 없다는 것이다.
- key는 value를 찾기 위한 이름인데 중복이 있으면 안 되기 때문이다.
- 파이썬이 사용자의 편의를 위해 삽입 순서를 보장해줄 뿐, 딕셔너리 요소 간 순서가 존재하는 것은 아님을 잊지 말자!
- 딕셔너리는 순서가 없는 자료형이다!!

# set(세트)
**순서와 중복이 없는 변경 가능한** 자료형

## 세트 표현
```python
my_set_1 = set() # 빈 set를 만들 때 주의
my_set_2 = {1, 2, 3}
my_set_3 = {1, 1, 1} # 중복 할당은 가능하지만,

print(my_set_1)  # set()
print(my_set_2)  # {1, 2, 3}
print(my_set_3)  # 결과는 {1}, 왜? 중복을 허용하지 않기 때문
```
- 수학에서의 집합고 동일한 연산 처리가 가능하다.
- 중괄호(`{}`)로 표기한다.

## 세트의 집합 연산
```python
my_set_1 = {1, 2, 3}
my_set_2 = {3, 6, 9}

# 합집합
print(my_set_1 | my_set_2)  # {1, 2, 3, 6, 9}

# 차집합
print(my_set_1 - my_set_2)  # {1, 2}

# 교집합
print(my_set_1 & my_set_2)  # {3}
```
- 이러한 연산이 가능한 이유는 **세트는 중복이 없기** 때문이다.
- 세트 역시 순서가 존재하지 않는다. 즉, 인덱스로 접근할 수가 없다!
