<!-- $theme: default -->

# 코코옹 1주차 자료

---

## 코딩이란?

- 컴퓨터에게 일을 시키기 위해 프로그래밍 언어를 작성하는 일
- 자연어 -> 엄청 잘 정제된 어떤 언어(프로그래밍 언어)

---

## 파이썬은 어떻게 굴러가나요?

- Interpreter(해석기)가 코드를 한 줄 씩 읽고, 해당 코드에 해당하는 동작을 수행
- 우리가 책을 한 문장씩 읽어 나가는 것과 비슷!
- 코드 한 줄 = 한 문장(작동 단위)

```
<할 일 목록>
냉장고를 열어!
콜라를 꺼내!
벌컥벌컥 마셔!
콜라를 내려놓아!
냉장고 문을 닫아!
```

---

## 첫 프로그램

- [repl.it](https://repl.it)에서 작성해보아요

``` python
print('Hello World')
a = 1
b = 2
a + b
```

---

## 첫 프로그램 (with 주석)

``` python
print('Hello World') # 화면에 Hello World를 표시해!
a = 1 # a는 1이야!
b = 2 # b는 2야!
a + b # a 더하기 b
```
- a = 1 / a + b를 콘솔 창에 입력했을 때 차이가 나는 이유는?

---

## Statements / Expressions
- 우리가 컴퓨터에게 말 할 수 있는 문장의 종류
- Statement: 값으로 표현 될 수 없는 문장
  ``` python 
  a = 1 # a는 1이야!
  b = 2 # b는 2야!
  ```
- Expression: 값이 될 수 있는 문장
  ``` python 
  a + b # a 더하기 b!
  b - a # b 빼기 a!
  ```

---

## 변수

- 어쩌면 자연어의 대명사와 비슷한 역할?
- Expression을 잠시 담아놓을 수 있다
- 덕분에 프로그램을 여러 문장으로 나눌 수 있고, 읽기 쉬워짐
``` python
radius = 2 # 반지름은 2야!
height = 5 # 높이는 5야!
PI = 3.141592 # 원주율은 3.141592라고 할래!

volume = radius * radius * PI * height
# 부피는 반지름 x 반지름 x 원주율 x 높이라고 할게!
print(volume) # 그럼 부피는?
```
``` python
2 * 2 * 3.141592 * 5 # 변수가 없을 경우 한 줄에서 승부봐야함
```

---

## 함수

- 변수가 명사적인 것을 정의한다면, 함수는 동사적인 것(절차)을 정의
- 자주 반복되는 절차에 이름을 붙이고, 따로 관리할 수 있게 해줌
- 수학에서의 함수의 모양을 빌려 쓰면 되겠다!

```
입을 벌려
혀를 내밀어
혀를 집어넣어
입을 닫아
입을 벌려
혀를 내밀어
혀를 집어넣어
입을 닫아
```
```
메롱은 (입을 벌려, 혀를 내밀어, 혀를 집어넣어, 입을 닫아)
메롱
메롱
```

---

## 함수의 구성

![함수의 모양](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3b/Function_machine2.svg/485px-Function_machine2.svg.png)
- 수학에서의 함수와 유사한 모양
- Input, Output, **내부 작동**으로 이루어짐
- 세 개 다 존재할 필요는 없음

---

## 파이썬에서의 함수 정의

``` python
def add_two(x): # input x
    x = x + 2 # 내부 작동
    return x # output # 왜 이름이 return 일까?

a = 1
b = add_two(1)
print(b)
```
``` python
def calc_volume(radius, height):
    return radius * radius * 3.141592 * height
  
volume1 = calc_volume(4, 7)
volume2 = calc_volume(5, 6)
```
---

## 왜 :쓰고 다음 줄에 띄어써..?

- 블럭(코드 뭉치)을 나타내는 표현
- 같은 높이에 있는 아이들은 같은 레벨
- 지금 쓰고 있는
  - 이거와
    - 비슷해요

``` python
def add_10(number): # number에 10을 더해!
    def add(n1, n2): # number1과 n2를 더해!
        return n1 + n2 # output은 n1 + n2
    return add(number, 10) # output은 add(number, 10) !

add_10(4) # 4에 10을 더해!
```

---

## Input, Output, 내부 작동이 다 있을 필요는 없다

``` python
def return_10(): # input 없음
    return 10
    
def mirror(a): # 내부 작동 없음
    return a
    
def eat(something): # output 없음
    something = something - 1
    print('먹었다')
```

## print 함수
``` python
def print(something):
    화면에 something을 표시해!
```
---

## 자료형

- Data Type
- 프로그램 내에서의 데이터의 종류
- 내부에 여러 함수와 데이터 탑재
  예) 'aaabbbccc'.replace('b', 'e') -> 'aaaeeeddd'
- 예시
  - 참/거짓
  - 정수
  - 실수
  - 문자열(텍스트)
  - 리스트

---

## 참/거짓 자료형(Boolean)

- 말 그대로 True와 False
- 어따 쓰는 지는 나중에 보아요
``` python
a = 1
b = 2
c = 1

a == b # a랑 b랑 같니? False
a == c # a랑 c랑 같니? True
a < b # a가 b보다 작니? True
a <= b # a가 b보다 작거나 같니? True
d = a > b # a가 b보다 크니? False
print(d)
```

---

## 정수/실수 자료형

- 숫자를 다루기 위해 존재
- 사칙연산 가능

``` python
# 너 보다 내가 더 커
your_height = 160 # 넌 160
my_height = 161 # 난 1

difference = my_height - your_height
# 우리 끼리끼리끼리 딱 1cm 차이
```

``` python
x + y
x - y
x * y # x × y
x / y # x ÷ y
x ** y # x ^ y
x % y # x mod y
```

---

## 문자열 자료형

- 문자의 배열,나열: 컴퓨터의 텍스트 표시 방법이 문자를 숫자로 바꾸고, 그것을 나열하는 것이라 이렇게 부름
- 텍스트 자료를 담아둘 때 사용(SNS 글이라던가)

``` python
sentence_1 = '배가 고파. '
sentence_2 = "밥을 먹자."

novel = sentence_1 + sentence_2 # '배가 고파. 밥을 먹자'
```

---

## 리스트
  
- 자료들을 담는 주머니
- SNS 게시글들을 모아놓았다가 하나씩 가져와서 분석해야 한다던가
- 자연어의 '..들'을 표현할 때 사용

``` python
name1 = '최송아'
name2 = '최병훈'
name3 = '김승현'
name4 = '송대훈'
name5 = '최지수'

friday_class_names = [name1, name2, name3, name4, name5]
# 금붕어반 이름들!
```

---

## 리스트 활용

``` python
sat_class_names = []
sat_class_names.append('류휘승')
sat_class_names.append('이유경')
sat_class_names.append('박수인')
sat_class_names.append('조민주')
sat_class_names.append('이태윤')
sat_class_names.append('박보경')

# sat_class_names = [
#    '류휘승', '이유경', '박수인', '조민주', '이태윤', '박보경'
# ]

first_name = sat_class_names[0]
# first_name은 sat_class_names의 1번째 값!
second_name = sat_class_names[1]
# second_name은 sat_class_names의 2번째 값!
```
``` python
def append(something):
    리스트에 something을 추가해!
```

---

## 조건문

- 자연어의 '만약 ~하다면'
- 어떠한 상태에 따라서 다른 작업을 수행
- 블록을 사용해 영역을 구분

``` python
all = 15 # 모든 코싸인 발제의 수는 15!
absent = 6 # 그 중에 결석은 6번이네
out = False # 일단 기본 값은 False야!

if (absent / all) > (1 / 3): # 만약 결석이 1/3 이상이면
    out = True # 넌 out!
```

---

## 조건문 확장
- 여러 조건을 동시에 적용하거나
- 어떤 조건에도 해당되지 않았을 때의 블럭도 지정가능

``` python
today = '목요일'

def get_schedule(day):
  if today == '목요일':
      return '코싸인'
  elif today == '금요일': # elif = else if
      return '코코옹 금붕어반'
  elif today == '토요일':
      return '코코옹 토끼반'
  else:
      return '탱자탱자 놀기'
  
my_schedule = get_schedule(today)
print(my_schedule)
```

---

## 반복문

- 같은 작업을 몇 번이라도 반복하고 싶을 때 사용

```
메롱!
메롱!
메롱!
메롱!
메롱!
```
```
(메롱)을 5번 해!
```

---

## for 반복문

- 반복문의 일종
- 어떠한 값의 변화를 기준으로 반복작업이 실행될 경우

``` sh
제 1의 아해가 무섭다고 그리오
제 2의 아해가 무섭다고 그리오
제 3의 아해가 무섭다고 그리오
제 4의 아해가 무섭다고 그리오
제 5의 아해가 무섭다고 그리오
...
```
``` python
for n in range(1, 100): # [1, 2, 3, ... , 99]
    print('제' + n + '의 아해가 무섭다고 그리오')
```

---

## for 활용

- in 다음에는 list와 같은 집합 자료형이 온다

``` python
scores = [100, 90, 80, 70, 60]
sum = 0
for score in scores:
    sum += score # sum = sum + score
average = sum / len(scores)
print(average)
```
``` python
def len(길이를가지는어떤 something):
	return something의 길이
```

---

## 정리

- 인터프리터
- 변수
- 함수
- 자료형
- 조건문
- 반복문(for)

---

# 끝!
- 공지사항은 카톡으로 전해드릴게요!