# Sequence Types
**여러 개의 값들**을 **순서대로 나열**하여 저장하는 자료형으로 대표적으로 `str`, `list`, `tuple`, `range` 가 있다.

## Sequence Types 특징
1. 순서(Sequence) : 값들이 순서대로 저장된다. (정렬X, 순서와 정렬은 다름)
2. 인덱싱(Indexing) : 각 값에 고유한 인덱스(번호)를 가지고 있으며, 인덱스를 사용하여 특정 위치의 값을 선택하거나 수정할 수 있다.
	- 인덱스는 '0'부터 시작한다.
	- 인덱스로 직접 접근해서 값을 가져오거나 수정할 수 있다.
3. 슬라이싱(Slicing) : 인덱스 범위를 조절해 부분적인 값을 추출할 수 있다.
4. 길이(Length) : `len()` 함수를 사용하여 저장된 값의 개수(길이)를 구할 수 있다.
4. 반복(Iteration): 반복문을 사용하여 저장된 값들을 반복적으로 처리할 수 있다.
- 결국 인덱싱, 슬라이싱, 길이, 반복은 전부 순서가 존재하기 때문에 가능한 특징이다.

# str(문자열)
문자들의 순서가 있는 **변경 불가능한** 시퀀스 자료형

## 문자열 표현
```python
print('Hello, World!')  # Hello, World!
print(type('Hello, World!'))  # str
```
- 문자열은 단일 문자나 여러 문자의 조합으로 이루어진다.
- 작은따옴표(') 또는 큰따옴표(")로 감싸서 표현한다.
- 작은따옴표(')와 큰따옴표(") 중 무엇을 사용하듯 상관은 없지만 섞어 쓰지 않고 일관적으로 하나만 쓰는 것이 좋다.

## 중첩 따옴표
```python
print(
    '문자열 안에 "큰따옴표"를 사용하려면 작은 따옴표로 묶는다.'
)  # 문자열 안에 "큰따옴표"를 사용하려면 작은 따옴표로 묶는다.
print(
    "문자열 안에 '작은따옴표'를 사용하려면 큰따옴표로 묶는다."
)  # 문자열 안에 '작은따옴표'를 사용하려면 큰따옴표로 묶는다.
```
따옴표 안에 따옴표를 표현할 경우
- 작은 따옴표가 들어 있는 경우는 큰따옴표로
- 큰따옴표가 들어 있는 경우는 작은따옴표로 문자열을 생성한다.

## Escape sequence
```python
# 철수야 '안녕'
print('철수야 \'안녕\'')

# 이 다음은 엔터
# 입니다.
print('이 다음은 엔터\n입니다.')
```
- Escape sequence란? 역슬래시(backslash) 뒤에 특정 문자가 와서 특수한 기능을 하는 문자 조합을 말한다.
- 파이썬의 일반적인 문법 규칙을 잠시 탈출한다는 의미이다.

### Escape sequence 종류
- `\n` : 줄 바꿈
- `\t` : 탭
- `\\` : 백슬래시
- `\'` : 작은 따옴표
- `\"` : 큰 따옴표표

## String Interpolation
```python
# String Interpolation "f-string"
bugs = 'roaches'
counts = 13
area = 'living room'

# Debugging roaches 13 living room
print(f'Debugging {bugs} {counts} {area}')
```
- String Interpolation란? 문자열 내에 변수나 표현식을 삽입하는 방법을 말한다.
- `f-strign`이란? 문자열에 `f` 또는 `F` 접두어를 붙이고 표현식을 `{expression}`로 작성하는 문법으로, 문자열에 파이썬 표현식의 값을 삽입할 수 있다. 

## 문자열의 시퀀스 특징
### 1. 인덱싱(indexing)
```python
my_str = 'hello'

print(my_str[1])  # e
print(my_str[-1]) # o
```
- 인덱스(index)란? 시퀀스 내의 값들에 대한 고유한 번호로, 각 값의 위치를 식별하는 데 사용되는 숫자이다.
- 인덱스는 [0]부터 시작한다.
- 인덱스는 역으로도 가능한데, 뒤에서부터 [-1]로 시작한다.

### 2. 슬라이싱(slicing)
```python
my_str = 'hello'

print(my_str[2:4])  # ll
print(my_str[:3])  # hel
print(my_str[3:])  # lo
print(my_str[0:5:2])  # hlo
print(my_str[::-1])  # olleh
```
- 슬라이싱이란? 시퀀스의 일부분을 선택하여 추출하는 작업으로, 시작 인덱스와 끝 인덱스를 지정하여 해당 범위의 값을 포함하는 새로운 시퀀스를 생성한다.
- 슬라이싱의 범위는 시작 인덱스의 요소부터 끝 인덱스의 요소 전까지이다.
- 시작은 생략 가능한데, 시작 인덱스가 생략하는 경우 경우 처음 요소부터 시작한다.
- 끝도 생략 가능한데, 끝 인덱스를 생략하는 경우 마지막 요소까지 포함한다.
- step을 지정하여 추출할 수 있다.
- step을 음수로 지정할 수도 있는데, 이를 이용하면 문자열을 한 번에 뒤집을 수 있다.
- [시작, 끝, 스텝]: 시작에서 끝까지 스텝씩 간다. 
- 즉, 스텝을 음수로 지정할 경우 시작 인덱스를 끝 인덱스보다 작은 수로 지정하면 안 된다.
- 마이너스, 빼면서 가는 것이기 때문에 시작 인덱스가 끝 인덱스보다 커야하겠지요..(?)
- 슬라이싱 꿀팁! 첫 번째 요소 앞부터 요소 간 공백을 세면 헷갈리지 않을 수 있다.

### 3. 길이
```python
my_str = 'hello'

print(len(my_str))  # 5
```
- `len()` 함수를 사용하여 저장된 값의 개수(길이)를 구할 수 있다.

### 4. 문자열은 불변(변경 불가)
```python
my_str = 'hello'

# TypeError: 'str' object does not support item assignment
my_str[1] = 'z'

# 재할당 (문자열을 바꾼 것이 아님)
my_str = "hzllo"
```
- 문자열은 시퀀스이면서 요소를 변경할 수 없다.

# list(리스트)
**여러 개의 값을 순서대로** 저장하는 **변경 가능한** 시퀀스 자료형
- 단, 순서와 정렬은 다르다는 점을 주의하자!

## 리스트 표현
```python
my_list_1 = [] # 0개 이상의 객체를 포함
my_list_2 = [1, 'a', 3.5, 'b', 5] # 어떤 자료형도 저장 가능
my_list_3 = [1, 2, 3, 'Python', ['hello', 'world']] # 리스트 안에 리스트도 가능(중첩 가능)
```
- 0개 이상의 객체를 포함하며 데이터 목록을 저장한다.
- 대괄호(`[]`)로 표기한다.
- 데이터는 어떤 자료형도 저장할 수 있다.

## 리스트의 시퀀스 특징
```python
my_list = [1, 'a', 3, 'b', 5]

# 인덱싱
print(my_list[1])  # a

# 슬라이싱
print(my_list[2:4])  # [3, 'b']
print(my_list[:3])  # [1, 'a', 3]
print(my_list[3:])  # ['b', 5]
print(my_list[0:5:2])  # [1, 3, 5]
print(my_list[::-1])  # [5, 'b', 3, 'a', 1]

# 길이
print(len(my_list))  # 5
```

## 중첩된 리스트 접근
```python
my_list = [1, 2, 3, 'Python', ['hello', 'world', '!!!']]

print(len(my_list))  # 5
print(my_list[4][2])  # !!!
print(my_list[4][-1])  # !!!
print(my_list[4][1][0])  # w
print(my_list[-1][1][0])  # w
```

## 리스트는 가변(변경 가능)
```python
my_list = [1, 2, 3]
my_list[0] = 100

print(my_list) # [100, 2, 3]

my_list_test = [1, 'world', 3]
my_list_test[1] = 100

print(my_list_test) # [1, 100, 3]
```

# tuple(튜플)
**여러 개의 값을 순서대로** 저장하는 **변경 불가능한** 시퀀스 자료형

## 튜플 표현
```python
my_tuple_1 = () # 0개 이상의 객체 포함
my_tuple_2 = (1,) # 단일 요소 튜플
my_tuple_test = (1) # 주의
my_tuple_3 = (1, 'a', 3, 'b', 5) # 어떤 자료형도 저장 가능

print(type(my_tuple_2)) # <class 'tuple'>
print(type(my_tuple_test)) # <class 'int'>
```
- 0개 이상의 객체를 포함하며 데이터 목록을 저장한다.
- 소괄호(`()`)로 표기한다.
- 데이터는 어떤 자료형도 저장할 수 있다.
- **단, 단일 요소 튜플을 만들 때는 반드시 Trailing comma(후행 쉼표)를 사용해야 한다.**

## 튜플 시퀀스 특징
```python
my_tuple = (1, 'a', 3, 'b', 5)

# 인덱싱
print(my_tuple[1])  # a

# 슬라이싱
print(my_tuple[2:4])  # (3, 'b')
print(my_tuple[:3])  # (1, 'a', 3)
print(my_tuple[3:])  # ('b', 5)
print(my_tuple[0:5:2])  # (1, 3, 5)
print(my_tuple[::-1])  # (5, 'b', 3, 'a', 1)

# 길이
print(len(my_tuple))  # 5
```
## 튜플은 불변(변경 불가)
```python
my_tuple = (1, 'a', 3, 'b', 5)

# TypeError: 'tuple' object does not support item assignment
my_tuple[1] = 'z'
```

## 튜플은 어디에 쓰일까?

### 1. 다중 할당
```python
x, y = 10, 20
print(x)  # 10
print(y)  # 20

# 실제 내부 동작
(x, y) = (10, 20)
```

### 2. 값 교환
```python
x, y = 1, 2
x, y = y, x

# 실제 내부 동작
temp = (y, x)  # 튜플 생성
x, y = temp  # 튜플 언패킹
print(x, y)  # 2 1
```

### 3. 그룹화
```python
student = ('Kim', 20, 'CS')
name, age, major = student  # 언패킹
print(name, age, major)  # Kim 20 CS
```
- 튜플의 불변 특성을 사용하여 **내부 동작과 안전한 데이터 전달***에 사용된다.
- 다중 할당, 값 교환, 그룹화, 함수 다중 반환 값 등

## 튜플 주의사항
```python
result = 100,
print(type(result)) # <class 'tuple'>
print(result) # (100,)
```

# range
**연속된 정수 시퀀스를 생성하는** 변경 불가능한 자료형

## range 기본 구문
```python
range(시작 값, 끝 값, 증가 값)
```
- 모든 매개변수는 정수만 사용 가능하다.

## range 매개변수별 특징
```python
my_range_1 = range(5)
my_range_2 = range(1, 10)
my_range_3 = range(5, 0, -1)

print(my_range_1)  # range(0, 5)
print(my_range_2)  # range(1, 10)
print(my_range_3)  # range(5, 0, -1)

# 리스트로 형 변환 시 데이터 확인 가능
print(list(my_range_1))  # [0, 1, 2, 3, 4]
print(list(my_range_2))  # [1, 2, 3, 4, 5, 6, 7, 8, 9]
print(list(my_range_3))  # [5, 4, 3, 2, 1]
```
- `range(n)` : 0부터 n-1까지 1씩 증가
- `range(n, m)` : n부터 m-1까지의 1씩 증가
- `range(n, m, step)` : n부터 m-1까지 step만큼 증가

## 증가 값 규칙
- 기본 증가 값은 1이다.
- 음수 중가 값의 경우 감소하는 수열을 생성한다.
- 양수 증가 값의 경우 증가하는 수열을 생성한다.
- 증가 값이 0이면 에러가 발생한다.

## 값의 범위 규칙
```python
# 시작 값이 끝 값보다 큰 경우 (정상)
print(list(range(5, 1, -1)))  # [5, 4, 3, 2]
# 시작 값이 끝 값보다 작은 경우
print(list(range(1, 5, -1)))  # []
```
- 음수 증가 시, 시작 값이 끝 값보다 커야 한다.

```python
# 시작 값이 끝 값보다 작은 경우 (정상)
print(list(range(1, 5)))  # [1, 2, 3, 4]
# 시작 값이 끝 값보다 큰 경우
print(list(range(5, 1)))  # []
```
- 양수 증가 시, 시작 값이 끝값보다 작아야 한다.

## range의 활용 예시
주로 **반복문**과 함께 활용한다.
```python
for i in range(1, 10):
    print(i)  # 1 2 3 4 5 6 7 8 9

for i in range(1, 10, 2):
    print(i)  # 1 3 5 7 9
```