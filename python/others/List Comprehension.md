# List Comprehension
간결하고 효율적인 리스트 생성 방법

```python
# 기존 방식(사용 전)
numbers = [1, 2, 3, 4, 5]
squared_numbers = []

for num in numbers:
    squared_numbers.append(num**2)

print(squared_numbers) # [1, 4, 9, 16, 25]
```
```python
# 리스트 컴프리헨션(사용 후)
numbers = [1, 2, 3, 4, 5]
squared_numbers = [num**2 for num in numbers]

print(squared_numbers) # [1, 4, 9, 16, 25]
```

## List Comprehension 활용 예시
- with 조건문
```python
# 기존 방식
evens = []
for x in range(10):
    if x % 2 == 0:
        evens.append(x)

print(evens)  # [0, 2, 4, 6, 8]

# 리스트 컴프리헨션
evens = [x for x in range(10) if x % 2 == 0]
print(evens)  # [0, 2, 4, 6, 8]
```
- 2차원 배열 생성 시(인접행렬 생성 시)
```python
data1 = [[0] * (5) for _ in range(5)]
print(data1)
# 또는
data2 = [[0 for _ in range(5)] for _ in range(5)]
print(data2)

"""
[[0, 0, 0, 0, 0],
 [0, 0, 0, 0, 0],
 [0, 0, 0, 0, 0],
 [0, 0, 0, 0, 0],
 [0, 0, 0, 0, 0]]
"""
```
**오히려 가독성이 떨어질 수도 있으니, Comprehension을 남용하지 말자!**
