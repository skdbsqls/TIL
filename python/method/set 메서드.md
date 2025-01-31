# Set
고유한 항목들의 정렬되지 않은 컬렉션

```python
my_set = set()
my_set = {2, 3, 5}
```

### 1. `add` 
: 세트에 데이터를 추가한다.
```python
my_set = {1, 2, 3}

my_set.add(4)
print(my_set) # {1, 2, 3, 4}

# 이미 있는 데이터는 무시한다.
my_set.add(2)
my_set.add(3)
print(my_set) # {1, 2, 3, 4}
print(len(my_set)) # 4
```

### 2. `remove` 
: 세트에서 데이터를 제거한다.
```python
my_set = {1, 2, 3}

my_set.remove(2) 
print(my_set) # {1, 3}

# remove는 반환값을 가지지 않는다.
print(my_set.remove(3)) # None

# 해당하는 항목이 없을 경우
print(my_set.remove(3)) # KeyError: 3
```

### 3. `pop` 
: 세트에서 임의의 요소를 제거하고 반환한다.
```python
my_set = {'a', 'b', 1, 2, 3}

print(my_set.pop()) # 1
print(my_set.pop()) # 2
print(my_set.pop()) # 3

print(my_set) # {'a', 'b'}
```