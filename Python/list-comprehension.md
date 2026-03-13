# Python 리스트 컴프리헨션

## 개요

리스트 컴프리헨션은 기존 반복문보다 간결하게 리스트를 생성하는 Python 문법입니다.

## 기본 문법

```python
# 기본 형태
result = [표현식 for 변수 in 이터러블]

# 예시: 0~9의 제곱수 리스트
squares = [x ** 2 for x in range(10)]
print(squares)  # [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

## 조건 필터링

```python
# 조건을 추가하여 짝수만 필터링
evens = [x for x in range(20) if x % 2 == 0]
print(evens)  # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

## 중첩 컴프리헨션

```python
# 2차원 리스트 펼치기
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
flat = [num for row in matrix for num in row]
print(flat)  # [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

## 딕셔너리 / 셋 컴프리헨션

```python
# 딕셔너리 컴프리헨션
word_len = {word: len(word) for word in ["apple", "banana", "cherry"]}
print(word_len)  # {'apple': 5, 'banana': 6, 'cherry': 6}

# 셋 컴프리헨션
unique_squares = {x ** 2 for x in [-2, -1, 0, 1, 2]}
print(unique_squares)  # {0, 1, 4}
```

## 참고
- [Python 공식 문서 - List Comprehensions](https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions)
