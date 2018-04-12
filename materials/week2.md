# 코코옹 2주차

---

## 저번 주에

- 인터프리터
- 변수
- 함수
- 자료형
- 조건문
- 반복문(for)

---

## 이번 주

- 자료형2
  - dictionary, tuple
- 반복문2
  - while, continue, break
- 예외처리
- 실습: 단어 수 세기

---

## Dictionary

- 말 그대로 사전
- key - value 형태로 이루어진 자료형

``` python
power = {'dog': 1, 'cat': 4, 'cow': 27}
if power['dog'] > power['cow']:
    print('강아지가 이김!')
else:
    print('소가 이김!')
    
power['tiger'] = 170
```

---

## Tuple

- list와 비슷한 집합 자료형
- list와 가장 큰 차이는 변경 불가능 하다는 점

``` python
list_example = [1, 2, 3]
tuple_example = (1, 2, 3)

list_example[0] == tuple_example[0]

list_example[0] = 4
tuple_example[0] = 4 # ERROR!

new_dict = {list_example: 7} # ERROR!
new_dict = {tuple_example: 7}
```

---

## While 반복문

- 어떠한 조건이 참일 때에만 반복

``` python
my_list = [1, 2, 3, 4, 5]

while not len(my_list) == 0:
    print(my_list.pop())
```

---

## 반복문 제어

``` python
odd_numbers = []
for number in range(100):
    if number % 2 == 0:
        continue
    else:
        odd_numbers.append(number)
        
    if len(odd_numbers) > 5:
        break
```

---

## 예외 처리

``` python
scores = [100, 27, 69, '70', 94, 80]
score_sum = 0

for score in scores:
    try:
        score_sum += score
    except:
        continue

print(score_sum)
```

---

## Word Count 예제