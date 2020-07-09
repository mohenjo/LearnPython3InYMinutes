# Learn Python3 in Y Minutes  

[Learn Python3 in Y Minutes](https://learnxinyminutes.com/docs/python3/)의 한글버전 (비공식 번역본)입니다.  

## 참조 사항

다음 사항으로 인해 원본과 구성이 다를 수 있습니다.
 - PEP8 기준 편집
 - 예외 발생 부분 처리 후 주석화
 - 내용 설명을 위한 신규 주석 추가
 - 출력 표시 내용 일부 변경
 - 코드 구현 일부 변경

## 최종 업데이트  

- 원본: https://learnxinyminutes.com/docs/python3/
- 원본 기준일: 2019.02
- 번역 최종 업데이트: 2019.03.04

## 기여자

 - 번역: [박햇님](https://github.com/mohenjo)
 - 원본 기여자에 대해서는 상기 원본의 주소를 참조하시기 바랍니다.


## 라이선스  

<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/"><img alt="크리에이티브 커먼즈 라이선스" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/3.0/88x31.png" /></a><br />이 저작물은 <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">크리에이티브 커먼즈 저작자표시-동일조건변경허락 3.0 Unported 라이선스</a>에 따라 이용할 수 있습니다.

-----

# [Learn X in Y minutes](https://learnxinyminutes.com/)

### Where X=python3

코드는 여기서 다운로드 할 수 있습니다:  [learnpython3.py](https://github.com/mohenjo/LearnPython3InYMinutes/raw/master/learnpython3.py) (RIght Click & Save Link As)

파이썬은 1990년 대 초 Guido van Rossum에 의해 개발되었으며, 현존하는 가장 인기있는 프로그래밍 언어 중 하나입니다. 저는 파이썬의 명확한 문법을 사랑합니다. 파이썬의 코드는 기본적으로 실행 가능한 의사코드입니다.

다음 연락처로 피드백을 주시면 매우 감사하겠습니다: 트위터 [@louiedinh](http://twitter.com/louiedinh) 또는 louiedinh(구글메일)

참고: 이 글은 파이썬 3에 해당하는 내용을 담고 있습니다. 이전 방식의 파이썬 2.7을 배우고 싶다면 [이곳](http://learnxinyminutes.com/docs/python/)을 확인하시기 바랍니다.

```python
# 한 줄 주석은 '#' 기호로 시작합니다.

""" 여러 줄 주석은 세 개의 " 또는 '를 사용합니다.
    주로 코드 문서화에 자주 사용됩니다.
"""

####################################################
# 1. 기본 자료형 및 연산자
####################################################

# 숫자
3  # => 3

# 산술 연산은 일반적으로 사용하는 방법과 동일합니다.
1 + 1  # => 2
8 - 1  # => 7
10 * 2  # => 20
35 / 5  # => 7.0

# 정수 나눗셈은 내림을 사용합니다.
5 // 3  # => 1
-5 // 3  # => -2
5.0 // 3.0  # => 1.0 # 실수에도 동일하게 적용됩니다.
-5.0 // 3.0  # => -2.0

# 나눗셈 연산의 결과는 항상 실수입니다.
10.0 / 3  # => 3.3333333333333335

# 나머지 연산
7 % 3  # => 1

# 거듭제곱 연산 (x**y: x의 y승)
2 ** 3  # => 8

# 괄호 내 연산이 우선됩니다.
(1 + 3) * 2  # => 8

# 부울(참, 거짓) 값도 기본 자료형입니다. (첫글자 대문자 유의)
True
False

# 'not' 키워드
not True  # => False
not False  # => True

# 부울 연산자 ('and'와 'or'는 소문자)
True and False  # => False
False or True  # => True

# 'True'와 'False'는 실제로 각각 1과 0의 값을 갖습니다.
True + True  # => 2
True * 8  # => 8
False - 5  # => -5

# 부울 값에 대한 비교 연산자는 'True', 'False'의 실제 값을 이용합니다.
# 0 == False  # => True
# 1 == True  # => True
# 2 == True  # => False
# -5 != False  # => True
# 단, pep8에서는 True, False에 대한 비교 연산자를 권장하지 않습니다.

# 정수형에 대해 부울 논리 연산자를 적용하면, 각 정수형을 부울 값으로
# 캐스팅(형 변환) 후 논리 연산을 수행합니다. 그러나 캐스팅 이전의 값을 반홥합니다.
# 부울 연산자('bool', 'and', 'or')와 비트연산자('&', '|')를 혼돈하기 쉽습니다.
bool(0)  # => False
bool(4)  # => True
bool(-6)  # => True
0 and 2  # => False and True => 0 (False)
-5 or 0  # => True or False => -5 (True)

# 값 일치: '=='
1 == 1  # => True
2 == 1  # => False

# 값 일치하지 않음: '!='
1 != 1  # => False
2 != 1  # => True

# 비교 연산자
1 < 10  # => True
1 > 10  # => False
2 <= 2  # => True
2 >= 2  # => True

# 비교 연산자 + 논리 연산자
1 < 2 and 2 < 3  # '1 < 2 < 3'과 같이 쓸 수 있습니다. => True
2 < 3 and 3 < 2  # '2 < 3 < 2'와 같이 쓸 수 있습니다. => False
# 다음과 같이 연결하여 사용할 수 있습니다.
1 < 2 < 3  # => True
2 < 3 < 2  # => False

# 'is'와 '=='
# 'is'는 두 개의 변수가 같은 객체를 가리키는지를 확인하고,
# '=='는 두 개의 변수가 같은 값을 갖는지 확인합니다.
a = [1, 2, 3, 4]  # 변수 a에 리스트 [1, 2, 3, 4]를 지정합니다.
b = a
b is a  # => True, a와 b는 동일 리스트 객체를 참조합니다.
b == a  # => True, a와 b에 지정된 리스트 객체는 동일하여, 값이 동일합니다.
b = [1, 2, 3, 4]  # 변수 b에 (내용은 같지만) 새로운 리스트를 지정합니다.
b is a  # => False, a와 b는 동일 객체를 가라키지 않습니다.
b == a  # => True, 다만 그 값은 동일합니다.

# 문자열은 " 또는 '로 이루어집니다.
"This is a string."
'This is also a string.'

# 문자열도 더하기 연산이 가능합니다.
"Hello " + "world!"  # => "Hello world!"
# (변수명이 아니라) 문자열끼리는 더하기 연산자 없이 연결 가능합니다.
"Hello " "world!"  # => "Hello world!"

# 문자열(string)은 문자(char)의 리스트처럼 접근할 수 있습니다.
"This is a string"[0]  # => 'T'

# 문자열의 길이는 다음과 같이 구합니다.
len("This is a string")  # => 16

# '.format'은 문자열 포맷팅에 사용됩니다:
"{} can be {}".format("Strings", "interpolated")
# => "Strings can be interpolated"

# 문자열의 반복 입력을 줄이기 위해 다음처럼 응용할 수 있습니다.
"{0} be nimble, {0} be quick, {0} jump over the {1}" \
    .format("Jack", "candle stick")
# => "Jack be nimble, Jack be quick, Jack jump over the candle stick"

# 숫자 대신 이름을 지정할 수도 있습니다.
"{name} wants to eat {food}".format(name="Bob", food="lasagna")
# => "Bob wants to eat lasagna"

# Python 2.5 이하 버전과의 호환성을 위해 이전 방식의 포맷팅을 사용할 수 있습니다.
"%s can be %s the %s way" % ("Strings", "interpolated", "old")
# => "Strings can be interpolated the old way"

# Python 3.6 이상에서는 'f문자열' 포맷팅을 사용할 수 있습니다.
name = "Reiko"
f"She said her name is {name}."  # => "She said her name is Reiko"
# 중괄호 안에 오는 파이썬 문은 평가되어 문자열을 구성합니다.
f"{name} is {len(name)} characters long."

# 'None'은 (싱글톤) 객체입니다.
None  # => None

# 객체를 'None'에 비교할 때는 '=='(값 일치)가 아니라 'is'를 사용하는데,
# 모든 'None'은 동일한 identity를 가집니다.
"etc" is None  # => False
None is None  # => True

# 'None', '0', 및 빈 문자열/리스트/사전/튜플에 대한 부울 함수는 'False' 값을 가지며
# 이외의 모든 값은 'True'입니다.
bool(0)  # => False
bool("")  # => False
bool([])  # => False
bool({})  # => False
bool(())  # => False

####################################################
# 2. 변수 및 컬렉션
####################################################

# 파이썬은 'print' 함수를 제공합니다.
print("I'm Python. Nice to meet you!")  # => I'm Python. Nice to meet you!

# 'print' 문 출력의 마지막에는 기본적으로 개행 문자(새로운 줄)가 추가되는데
# 'end' 옵션을 이용하여 이를 변경할 수 있습니다.
print("Hello, World", end="!")  # => Hello, World!
print()  # 빈 줄을 출력합니다.

# 다음과 같이 콘솔로부터 데이터를 입력 받습니다.
input_string_var = input("Enter some data: ")  # 'input'은 문자열을 반환합니다.
# 참조: 이전 버전의 파이썬에서는 'input' 대신 'raw_input' 함수를 사용했습니다.

# 파이썬은 동적언어 이므로 변수의 형 선언 없이 할당만 하면 됩니다.
# 변수 네이밍은 소문자단어를 밑줄로 결합하는 snake_case 규칙을 따릅니다.
some_var = 5
some_var  # => 5

# 할당되지 않은 변수에 접근하면 예외(오류)를 발생시킵니다.
# 예외 처리에 대해서는 '흐름 제어' 부분에서 다룹니다.
# some_unknown_var  # 왼쪽의 문을 실행하면 'NameError' 예외를 발생시킵니다.

# 삼항 연산자(Ternary operator)
# 참조: C의 '<expression> ? <value if true> : <value if false>
"yahoo!" if 3 > 2 else 2  # => "yahoo!"

# 리스트는 시퀀스(sequence) 자료형(순서가 있는 자료형)입니다.
li = []  # 빈 리스트
other_li = [4, 5, 6]  # 리스트 값 할당

# 'append(값)' 문으로 리스트의 마지막에 자료를 추가합니다.
li.append(1)  # li = [1]
li.append(2)  # li = [1, 2]
li.append(4)  # li = [1, 2, 4]
li.append(3)  # li = [1, 2, 4, 3]
# 'pop()' 문으로 마지막 자료를 삭제합니다. (마지막 자료값이 반환됩니다)
li.pop()  # 반환값 3, li = [1, 2, 4]
# 아래와 같이 다시 추가하면,
li.append(3)  # li = [1, 2, 4, 3]

# 인덱스를 통해 리스트 항목에 접근 가능합니다.
li[0]  # => 1
# 마지막 항목은 아래와 같이 접근할 수도 있습니다.
li[-1]  # => 3

# 인덱스의 범위를 벗어나면 'IndexError' 예외를 발생시킵니다.
# li[4]  # => 'IndexError' 예외 발생

# 리스트 슬라이싱을 사용하여 리스트 요소의 범위에 접근할 수 있으며,
# 슬라이싱이 적용된 복사본이 반환됩니다.
# 리스트 슬라이싱은 다음과 같이 사용합니다: 리스트명[시작 인덱스:끝 인덱스:스텝]
# 슬라이스의 시작 인덱스는 포함되고, 끝 인덱스는 포함되지 않습니다.
li[1:3]  # => [2, 4]
# 끝 범위를 생략하면 리스트의 마지막까지 범위에 포함됩니다.
li[2:]  # => [4, 3]
# 시작 범위를 생략하면 리스트의 처음(인덱스 0)부터 범위에 포함됩니다.
li[:3]  # => [1, 2, 4]
# 리스트의 처음부터 끝까지, 요소를 하나씩 건너뛰어 반환합니다.
li[::2]  # =>[1, 4]
# 리스트를 뒤집어서 반환합니다.
li[::-1]  # => [3, 4, 2, 1]

# 얕은 복사(shallow copy): 주소만 복사. 원본과 사본이 같은 주소를 참조함
# 깊은 복사(deep copy): 새로운 자료공간을 구성한 후 내용 복사
# 슬라이스를 이용해서 깊은 복사를 수행합니다.
li2 = li[:]  # li == li2 이지만, (li2 is li) is False.

# 요소 삭제: 'del' 리스트명[인덱스]
del li[2]  # li = [1, 2, 3]

# 요소 삭제: 리스트명.remove(값), 해당 값을 가진 첫 번째 요소 삭제
li.remove(2)  # li = [1, 3]
# li.remove(2)  # 값 2는 존재하지 않으므로 'ValueError' 예외가 발생합니다.

# 특정 인덱스에 값 삽입: 리스트명.insert(인덱스, 추가할 값)
li.insert(1, 2)  # li = [1, 2, 3]

# 특정 값의 인덱스 반환: 리스트명.index(값)
li.index(2)  # => 1
# li.index(4)  # 값 4는 존재하지 않으므로 'ValueError' 예외가 발생합니다.

# '+' 연산으로 두 개의 리스트를 합친 결과를 반환합니다.
# 다음에서 li와 other_li는 변경되지 않습니다.
li + other_li  # => [1, 2, 3, 4, 5, 6]

# 'extend' 함수로 합칠 수도 있습니다. 다음에서는 li가 변경됩니다.
li.extend(other_li)  # li = [1, 2, 3, 4, 5, 6]

# 리스트 내 요소 존재 여부 확인을 위해 'in' 키워드를 사용할 수 있습니다.
1 in li  # => True

# 리스트의 길이는 'len(리스트명)'으로 구할 수 있습니다.
len(li)  # => 6

# 튜플(Tuples)은 리스트와 유사하나, 불변(immutable) 자료형입니다.
tup = (1, 2, 3)
tup[0]  # => 1
# tup[0] = 3  # 튜플은 불변이므로 'TypeError' 예외를 발생시킵니다.

# 튜플의 요소가 하나인 경우 튜플임을 명시적으로 나타내기 위해 요소 뒤에 ','를
# 삽입합니다. 빈 튜플은 '()'와 같이 표시합니다.
type(1)  # => <class 'int'>
type((1,))  # => <class 'tuple'>, 'type((1))' => <class 'int'>
type(())  # => <class 'tuple'>

# 리스트와 관련된 연산자 대부분을 튜플에도 사용할 수 있습니다.
len(tup)  # => 3
tup + (4, 5, 6)  # => (1, 2, 3, 4, 5, 6)
tup[:2]  # => (1, 2)
2 in tup  # => True

# 다음과 같이 할당하는 것을 튜플(리스트) 언패킹(unpacking)이라고 합니다.
a, b, c = (1, 2, 3)  # a = 1, b = 2, c = 3
# 다음과 같이 언패킹을 응용할 수 있습니다. (asterik(*)에 유의)
a, *b, c = (1, 2, 3, 4)  # a = 1, b = [2, 3], c = 4
# 아래와 같이 튜플의 괄호를 생략하여도 무방합니다.
d, e, f = 4, 5, 6  # d = 4, e = 5, f = 6
# 이를 응용하여 다음과 같이 두 변수의 값을 교환할 수 있습니다.
e, d = d, e  # d = 5, e = 4

# 사전형식(Dictionary)은 키(key)-값(value)으로 매핑된 쌍의 집합입니다.
empty_dict = {}  # 빈 사전형식
filled_dict = {"one": 1, "two": 2, "three": 3}  # 사전형식 값 할당

# 사전형식의 키는 일정한 해시 값을 갖는 불변(immutable) 형식이어야 합니다.
# 불변 형식에는 숫자, 문자, 튜플 등이 있습니다.
# invalid_dict = {[1, 2, 3]: "123"}
# => "TypeError: unhashable type: 'list'"를 발생시킵니다.
valid_dict = {(1, 2, 3): [1, 2, 3]}

# '사전명[키이름]'으로 값에 접근합니다.
filled_dict["one"]  # => 1

# 'keys()' 메서드를 통해 키(key)들의 iterable(순회 가능한) 객체를 구할 수 있습니다.
# 'list(iterable)' 함수를 이용하여 이를 리스트 형식으로 변환할 수 있습니다.
# 참조 - 파이썬 3.7 미만의 버전에서는 사전형식에 키가 추가된 순서와 keys()의
# 요소 순서가 다를 수 있습니다. 3.7 버전부터는 사전에 키가 추가된 순서대로 keys()가
# 구성됩니다.
list(filled_dict.keys())  # => ["three", "two", "one"] in Python <3.7
list(filled_dict.keys())  # => ["one", "two", "three"] in Python 3.7+

# 'values()' 메서드를 통해 값(value)들의 iterable 객체를 얻을 수 있습니다.
# 참조 - 값의 순서에 대해서도 상기의 참조 사항이 동일하게 적용됩니다.
list(filled_dict.values())  # => [3, 2, 1]  in Python <3.7
list(filled_dict.values())  # => [1, 2, 3] in Python 3.7+

# 키 존재 여부 확인을 위해 'in' 키워드를 사용할 수 있습니다.
"one" in filled_dict  # => True
1 in filled_dict  # => False

# 키가 존재하지 않는 경우 'KeyError' 예외를 발생시킵니다.
# filled_dict["four"]  # KeyError

# 'get()' 메서드를 사용하면 KeyError'를 피할 수 있습니다.
filled_dict.get("one")  # => 1
filled_dict.get("four")  # => None
# 키가 존재하지 않을 경우 기본값을 반환하도록 할 수 있습니다.
filled_dict.get("one", 4)  # => 1
filled_dict.get("four", 4)  # => 4

# 'setdefault()'는 키가 존재하지 않을 경우 설정된 값을 해당 키에 할당합니다.
filled_dict.setdefault("five", 5)  # filled_dict["five"] = 5 <= 키 미존재
filled_dict.setdefault("five", 6)  # filled_dict["five"] = 5 <= 키 존재

# 사전형식에 자료 추가
filled_dict.update({"four": 4})
# => {"one": 1, "two": 2, "three": 3, "four": 4}
filled_dict["four"] = 4  # 자료 추가의 다른 방법

# 사전형식에서 키 삭제
del filled_dict["one"]  # 'one'이라는 키를 삭제합니다.

# 파이썬 3.5부터는 '**'를 이용하여 사전형식을 언패킹할 수 있습니다.
{'a': 1, **{'b': 2}}  # => {'a': 1, 'b': 2}
{'a': 1, **{'a': 2}}  # => {'a': 2}

# set형은 집합자료형(순서 없음, 중복 없음)입니다.
empty_set = set()
# 다음과 같이 set형에 값을 할당할 수 있습니다. 괄호의 형태는 사전형식과 동일하나
# set형은 값으로만 이루어져 있습니다.
some_set = {1, 1, 2, 2, 3, 4}  # some_set = {1, 2, 3, 4}

# 사전형식과 마찬가지로 set형의 요소는 불변형식(immutable)이어야 합니다.
# invalid_set = {[1], 1}  # "TypeError: unhashable type: 'list'"를 발생시킵니다.
valid_set = {(1,), 1}

# set형에 요소 추가
filled_set = some_set  # 얕은 복사(참조 복사)가 이루어집니다.
filled_set.add(5)  # filled_set = {1, 2, 3, 4, 5}
# 이 때, some_set = {1, 2, 3, 4, 5}으로 변경됩니다.
# set형은 중복된 요소를 가지지 않으므로
filled_set.add(5)  # filled_set = {1, 2, 3, 4, 5}으로 변경되지 않습니다.

# set형에 대한 '&'(AND) 연산은 교집합(intersection)을 반환합니다.
other_set = {3, 4, 5, 6}
filled_set & other_set  # => {3, 4, 5}
# filled_set.intersection(other_set)과 동일합니다.

# '|'(OR) 연산은 합집합(union)을 반환합니다.
filled_set | other_set  # => {1, 2, 3, 4, 5, 6}
# filled_set.union(other_set)과 동일합니다.

# '-' 연산은 차집합(difference)을 반환합니다.
{1, 2, 3, 4} - {2, 3, 5}  # => {1, 4}
# {1, 2, 3, 4}.difference({2, 3, 5})와 동일합니다.

# '^'(XOR) 연산은 대칭차집합(symmetric difference)을 반환합니다.
{1, 2, 3, 4} ^ {2, 3, 5}  # => {1, 4, 5}
# {1, 2, 3, 4}.symmetric_difference({2, 3, 5})와 동일합니다.

# 두 set형에 대해 (진)부분집합 여부는 다음과 같이 판단합니다.
{1, 2} >= {1, 2, 3}  # => False
{1, 2} <= {1, 2, 3}  # => True

# 값 존재 여부 확인을 위해 'in' 키워드를 사용할 수 있습니다.
2 in filled_set  # => True
10 in filled_set  # => False

####################################################
# 3. 흐름 제어 및 순회 가능 객체(iterable)
####################################################

# 우선 변수를 하나 정의해봅시다.
some_var = 5

# 파이썬에서는 코드블럭을 나타내기 위해 '반드시' 들여쓰기(indentation)를 합니다.
# 일반적으로 들여쓰기는 탭이 아니라 4개의 공백을 권장합니다. 동일한 파일 내에서
# 들여쓰기와 탭을 절대 혼용하지 마십시오.
# 'if' 문은 아래와 같이 사용합니다.
if some_var > 10:
    print("some_var is totally bigger than 10.")
elif some_var < 10:  # 조건에 따라 'elif 조건' 문은 생략될 수 있습니다.
    print("some_var is smaller than 10.")  # 이 부분이 출력됩니다.
else:  # 'else' 문도 조건에 따라 생략될 수 있습니다.
    print("some_var is indeed 10.")

"""
for 문으로 리스트, 튜플, 사전, set, 문자열 등의 요소에 대한 순회가 가능합니다.
아래의 명령은 다음과 같이 출력됩니다:
    dog is a mammal
    cat is a mammal
    mouse is a mammal
"""
for animal in ["dog", "cat", "mouse"]:
    # 'format()' 문으로 문자열을 보간(interpolate)할 수 있습니다.
    print("{} is a mammal".format(animal))

"""
'range(숫자)'는 0부터 해당 숫자까지(포함하지 않음) iterable한 집합을 반환합니다.
아래의 명령은 다음과 같이 출력됩니다:
    0
    1
    2
    3
"""
for i in range(4):
    print(i)

"""
'range(시작숫자, 끝숫자)'는 시작숫자부터 끝숫자까지(포함하지 않음) iterable한
집합을 반환합니다.
아래의 명령은 다음과 같이 출력됩니다:
    4
    5
    6
    7
"""
for i in range(4, 8):
    print(i)

"""
'range(시작숫자, 끝숫자, 스텝)'는 시작숫자부터 끝숫자까지(포함하지 않음) 스텝만큼
건너뛴 iterable한 집합을 반환합니다. 스텝이 명시되지 않으면 기본값은 1입니다.
아래의 명령은 다음과 같이 출력됩니다:
    4
    6
"""
for i in range(4, 8, 2):
    print(i)

"""
'while' 문은 조건이 만족하는 동안 계속 수행됩니다.
아래의 명령은 다음과 같이 출력됩니다:
    0
    1
    2
    3
"""
x = 0
while x < 4:
    print(x)
    x += 1  # x = x + 1과 동일한 표현입니다.

# 'try'/'except' 문으로 예외를 처리합니다.
try:
    # "raise" 문으로 예외를 발생시킬 수 있습니다.
    raise IndexError("This is an index error")
except IndexError as e:
    pass  # pass문은 아무런 동작을 실행하지 않습니다.
    # 단순한 예외 처리를 위해 이렇게 사용할 수 있습니다.
except (TypeError, NameError):  # 여러 개의 예외를 동시에 처리할 수도 있습니다.
    pass
else:
    # 예외가 발생하지 않으면 'else' 다음의 코드 블럭이 실행됩니다.
    # 반드시 'except' 블럭 다음에 와야 하며, 생략 가능합니다.
    print("All good!")
finally:  # 이 코드 블럭은 예외 발생의 여부와 상관없이 실행됩니다.
    print("We can clean up resources here")

# Instead of try/finally to cleanup resources you can use a with statement
# 파일의 입출력 등과 같이 최종적으로 리소스의 해제가 필요한 처리의 경우,
# 'try'/'except' 구문을 통해 예외가 발생하더라도 리소스를 해제해주어야 합니다.
# 'with' 문을 사용하면 예외 발생 여부에 상관없이 리소스가 해제됩니다.
with open("myfile.txt") as f:
    for line in f:
        print(line, end='')
    print()

# 파이썬에서는 iterable이라고 하는 순회 가능한 추상 객체를 제공합니다.
# 'range' 메서드의 반환값 또한 iterable입니다.

filled_dict = {"one": 1, "two": 2, "three": 3}
our_iterable = filled_dict.keys()
print(our_iterable)  # => dict_keys(['one', 'two', 'three'])
# our_iterable 역시 iterable 인터페이스를 제공하는 객체입니다.

# 따라서 다음과 같이 순회할 수 있습니다.
for i in our_iterable:
    print(i)  # 'one', 'two', 'three'를 출력합니다.

# 그러나, 인덱스로 요소에 직접 접근할 수는 없습니다. (인덱싱을 지원하지 않습니다)
# our_iterable[1]  # 'TypeError'를 발생시킵니다.
# 인덱싱이 가능한 객체로 변환하면 요소 접근이 가능해집니다.

# iterable은 반복(순회) 가능한 추상 객체이며, 'iter(iterable)'에 의해
# iterator(반복자)를 생성할 수 있습니다.
our_iterator = iter(our_iterable)

# iterator 객체는 순회 중인 위치를 기억하며, 요소의 다음 값은 'next()' 메소드에
# 의해 구할 수 있습니다.
next(our_iterator)  # => 'one'
# 'one' 까지 순회한 것을 기억하고 있습니다.
next(our_iterator)  # => 'two'
next(our_iterator)  # => 'three'

# iterator에서 더 반환할 요소가 없을 경우, 'StopIteration' 예외를 발생시킵니다.
# next(our_iterator)  # 'StopIteration' 발생

# 'list()' 등과 같이 인덱싱이 가능한 객체로 변환하면 요소 접근이 가능해집니다.
list(filled_dict.keys())  # => ["one", "two", "three"]


####################################################
# 4. 함수/메서드
####################################################

# 'def' 키워드를 사용하여 함수를 정의합니다.
def add(x, y):
    print("x is {} and y is {}".format(x, y))
    return x + y  # 'return' 문으로 값을 반환합니다.


# 다음과 같이 함수 호출 인자를 지정합니다.
add(5, 6)  # => x = 5, y = 6 이므로, 호출 반환 값은 11입니다.

# 키워드 인자를 사용해 함수를 호출할 수도 있습니다.
add(y=6, x=5)  # 이 때는 인자의 순서를 지키지 않아도 됩니다.


# 참조. 함수 정의 시의 입력으로 전달되는 값을 매개변수(parameter)라 하고,
# 함수 호출 시에 전달하는 값을 인자 또는 인수(argument)라고 하나, 보통 혼용합니다.


# 함수의 매개변수가 몇 개인지 모를 때는 다음과 같은 방법을 사용합니다.
# 이를 positional arguments라고 합니다.
def varargs(*args):
    return args


varargs(1, 2, 3)  # => (1, 2, 3)


# '*' 표시가 두 개 사용된 매개변수는 keyword arguments(키워드 인자)라고 합니다.
def keyword_args(**kwargs):
    return kwargs


# 함수 호출 시 kwargs는 사전형식으로 취급되고, key = value 형식의 입력 인수가
# 해당 사전형식에 저장됩니다.
keyword_args(big="foot", loch="ness")  # => {"big": "foot", "loch": "ness"}


# 두 가지를 혼용할 수 있지만, keyword는 positional 앞에 올 수 없습니다.
def all_the_args(*args, **kwargs):
    print(args)
    print(kwargs)


"""
'all_the_args(1, 2, a=3, b=4)'는 다음과 같이 출력됩니다:
    (1, 2)
    {"a": 3, "b": 4}
"""

# 함수를 호출할 때, 컨테이너 타입의 데이타를 아래와 같이 언패킹('*', '**' 사용)하여
# 전달할 수 있습니다
args = (1, 2, 3, 4)
kwargs = {"a": 3, "b": 4}
all_the_args(*args)  # 'all_the_args(1, 2, 3, 4)'와 동일합니다.
all_the_args(**kwargs)  # 'all_the_args(a=3, b=4)'와 동일합니다.
all_the_args(*args, **kwargs)  # 'all_the_args(1, 2, 3, 4, a=3, b=4)'


# 함수는 여러 개의 반환 값을 가질 수 있습니다. (튜플 형식)
def swap(x, y):
    return y, x  # 'return (y, x)'와 동일합니다.


x = 1
y = 2
x, y = swap(x, y)  # => x = 2, y = 1
# 괄호를 사용하여 '(x, y) = swap(x,y)'와 같이 표현할 수도 있습니다.

# 함수-변수의 유효 범위(scope)
x = 5  # 함수 외부에서 선언된 변수는 해당 함수에 대한 전역(global) 변수입니다.


def set_x(num):
    # 아래의 'x'는 위에서 선언된 변수와 다른 (이름만 같은) 지역(local) 변수입니다.
    x = num  # => 아래의 코드를 통해 x = 43이 대입됩니다.
    print(x)  # => 43


def set_global_x(num):
    global x  # 전역 변수 'x'를 사용하겠다는 의미입니다.
    print(x)  # => 따라서 5가 출력되고
    x = num  # 전역변수 'x'는 6으로 설정됩니다.
    print(x)  # => 6


set_x(43)
set_global_x(6)
print(f"global x = {x}")  # 'set_global_x'에서 전역변수 x의 값을 변경했습니다.


# 파이썬에서 함수는 퍼스트 클래스 함수(first class function)입니다. 이는 함수 자체를
# 인자로서 다른 함수에 전달하거나, 다른 함수의 결과값으로 반환할 수 있고, 함수를
# 변수에 할당하거나 데이터 구조안에 저장할 수 있다는 의미입니다.
def create_adder(x):
    def adder(y):
        return x + y

    return adder


add_10 = create_adder(10)
add_10(3)  # => 13

# 익명 함수(lambda function)는 다음과 같이 구현합니다.
(lambda x: x > 2)(3)  # => True
(lambda x, y: x ** 2 + y ** 2)(2, 1)  # => 5

# 내장된(built-in) 고차원 함수(higher-order function)을 사용할 수 있습니다.
list(map(add_10, [1, 2, 3]))  # => [11, 12, 13]
list(map(max, [1, 2, 3], [4, 2, 1]))  # => [4, 2, 3]
list(filter(lambda x: x > 5, [3, 4, 5, 6, 7]))  # => [6, 7]

# 다음은 리스트 컴프리헨션(comprehension)의 예입니다.
# comprehension은 iterable한 오브젝트를 생성하기 위한 파이썬의 syntactic sugar
# (간편 표기법) 중 하나로서 리스트형식, set형식, 사전형식, 생성자(generator) 등에
# 적용 가능합니다. 반복문을 통해 comprehension을 구현할 수도 있습니다.
[add_10(i) for i in [1, 2, 3]]  # => [11, 12, 13]
# [1, 2, 3]의 각 요소 'i'에 대해 'add_10(i)'를 적용한 값을 리스트로 반환합니다.
[x for x in [3, 4, 5, 6, 7] if x > 5]  # => [6, 7]
# [3, 4, 5, 6, 7]의 각 요소 'x'에 대해 'x > 5'인 조건을 만족하는 'x'를 구해
# 리스트로 반환합니다.

# set형식과 사전형식에는 다음과 같이 사용합니다.
{x for x in 'abcddeef' if x not in 'abc'}  # => {'d', 'e', 'f'}
# 'abcddeef'의 요소 'x'(각 문자)에 대해 'abc'에 포함돼 있지 않는 'x'를 구해
# set형식으로 반한홥니다.
{x: x ** 2 for x in range(5)}  # => {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
# 'range(5)' (0, 1, 2, 3, 4 입니다)의 요소 'x'에 대해
# key = 'x', value = 'x ** 2'인 사전형식을 반환합니다.

####################################################
# 5. Modules(모듈)
####################################################


# 모듈(실행코드의 꾸러미)의 사용(import)
import math  # 일반적으로 import 문은 파일 최상단에 위치하는 것을 권장합니다.

# 위와 같이 임포트한 경우 함수의 사용은 '모듈명.함수명(인자)'와 같이 사용합니다.
print(math.sqrt(16))  # => 4.0

# 모듈로부터 특정 함수를 임포트 하는 것도 가능합니다.
from math import ceil, floor

# 위와 같이 임포트한 경우 모듈명 없이 함수명의 직접 호출이 가능합니다.
# 이 경우 함수명의 충돌이 일어나지 않도록 유의하여야 합니다.
print(ceil(3.7))  # => 4.0
print(floor(3.7))  # => 3.0

# 모듈로부터 특정 함수가 아니라 모든 함수를 임포트 할 수 있습니다.
# 그러나 권장되는 방법은 아닙니다.
# from math import *

# 임포트 된 모듈명을 아래와 같이 축약해서 사용할 수 있습니다.
import math as m

math.sqrt(16) == m.sqrt(16)  # => True

# 파이썬의 모듈은 함수, 변수, 클래스 등으로 구성된 일반적인 파이썬 파일입니다.
# 별도로 관리할 함수, 변수, 클래스 등을 분리된 파일로 저장하고 임포트하여 사용할 수
# 있습니다. 이 때, 모듈명은 파이썬 파일명입니다.
# 참조. math, sys 등의 모듈은 속도를 위해 C 언어로 제작되어 파이썬 인터프리터에
# 내장되어 있습니다.

# 모듈 내에 저장된 함수들과 속성 등은 'dir(모듈명)'으로 확인할 수 있습니다.
import math

dir(math)


# 현재 파이썬 소스 디렉토리 내에 'math.py'라는 별도의 파일이 있다고 하면,
# 'import math'에 의해 파이썬 내장 모듈(math)대신 해당 파일이 임포트 됩니다.
# 즉, 로컬 폴더가 파이썬 내장 라이브러리 폴더보다 우선권을 가집니다.


####################################################
# 6. Classes(클래스)
####################################################

# 'class' 구문을 통해 클래스를 구현합니다.
class Human:  # 클래스명의 첫 글자로 대문자를 사용하기를 권장합니다.
    # 클래스의 속성은 해당 클래스의 모든 인스턴스(객체)와 공유됩니다.
    species = "H. sapiens"  # 클래스 변수입니다. 인스턴스 간에 공유됩니다.

    # '___init__()'은 객체지향프로그래밍(OOP) 관점에서 생성자(constructor) 또는
    # 초기자(initializer)에 해당합니다.
    # 앞 뒤에 있는 두 개의 언더스코어('__')는 미리 정의되어 있는 특별한 메소드들을
    # 사용자가 재정의할 수 있게 하여, 객체의 생성, 표현 및 연산에 도움을 줍니다.
    # 이러한 메서드들을 매직 메서드(magic method)라고 합니다. 이러한 매직 메서드에는
    # __init__, __str__, __repr__, __add__,.. 등이 있으며, 언더스코어가 두 개
    # 붙으므로 DUNDER(Double UNDERscore) 메서드라고도 합니다. 매직 메소드명은
    # 해당된 용도로만 사용하기를 권장합니다.
    def __init__(self, name):
        # 'self.'가 붙은 변수 명은 인스턴스 변수입니다.
        # 인스턴스 변수 'self.name'에 생성자의 인자인 'name'이 할당됩니다.
        self.name = name
        self._age = 0  # 다른 인스턴스 변수도 정의했습니다.

    # 인스턴스 메서드는 첫 번째 파라미터로 'self'(인스턴스 객체 자신)을 사용합니다.
    # 일반적으로 인스턴스 자신을 나타내는 'self'를 사용하지만, 다른 이름을
    # 사용해도 됩니다.
    # 'Human' 클래스의 인스턴스를 'h = Human(name)'로 생성했을 때,
    # 'h.say(msg)'와 같이 호출합니다.
    def say(self, msg):
        print("{name}: {message}".format(name=self.name, message=msg))

    # 호출시 인자가 없는 인스턴스 메서드의 정의입니다.
    def sing(self):
        return 'yo... yo... microphone check... one two... one two...'

    # 클래스 메서드는 모든 인스턴스간에 공유됩니다. 클래스를 나타내는 'cls'를
    # 첫 번째 파라미터로 사용합니다. 인스턴스 메서드와 마찬가지로 'cls'대신 다른
    # 이름을 사용해도 됩니다.
    # 클래스 메서드를 호출하기 위해서는 'Human.get_species()' 또는
    # '인스턴스명.get_species()' 라고 표현합니다. (객체에서도 접근이 가능합니다)
    # 뒤에서 설명하겠지만, 클래스 메서드에는 '@classmethod'라는
    # 데코레이터(decorator)를 붙입니다.
    @classmethod
    def get_species(cls):
        return cls.species  # 클래스 변수를 반환합니다.

    # 정적 메서드는 클래스나 인스턴스 객체의 참조 없이 사용 가능하며, 객체에서도
    # 접근이 가능함에 유의해야 합니다.
    # 클래스와 별도로 둘 수도 있으나, 클래스에 관련된 메서드를 정적 메서드로 구현
    # 하는 것이 좋습니다.
    # 정적 메서드에는 '@staticmethod'라는 데코레이터를 붙입니다.
    @staticmethod
    def grunt():
        return "*grunt*"

    # 객체지향의 특성 상 인스턴스 변수에 직접 접근하는 것보다, 해당 변수를
    # 은닉('_'는 private 변수임을 나타냅니다)하고 프로퍼티(property)를 통해
    # 접근하는 것이 안전합니다.
    # 아래는 'self._age'에 직접 접근하지 않고 읽기 전용으로 'self._age'의 값을
    # 반환하는 getter 프로퍼티입니다. '인스턴스명.age'로 값을 얻을 수 있습니다.
    # getter 프로퍼티에는 '@property'라는 데코레이터를 붙입니다.
    @property
    def age(self):
        return self._age

    # 다음은 '인스턴스명.age'을 통해 'self._age'에 값을 지정하는
    # setter 프로퍼티의 구현입니다.
    # setter 프로퍼티에는 '@메서드명.setter'라는 데코레이터를 붙입니다.
    @age.setter
    def age(self, age):
        self._age = age

    # 다음은 딜리터(deleter) 프로퍼티의 구현입니다.
    @age.deleter
    def age(self):
        del self._age

    # 파이썬의 객체 지향은 느슨하므로 반드시 getter, setter 프로퍼티를 구현할
    # 필요는 없습니다.


# 파이썬 인터프리터는 소스 파일의 코드를 처음부터 실행합니다.
# 아래의 'if __name__..' 조건부 안의 코드블럭은 본 소스 파일이 모듈로 임포트 되지
# 않은 경우에만 (즉, '__name__'의 값이 '__main__'인 경우에만) 실행됩니다.
if __name__ == '__main__':
    # 'Human' 클래스의 인스턴스는 다음과 같이 생성합니다.
    i = Human(name="Ian")
    i.say("hi")  # "Ian: hi"
    j = Human("Joel")
    j.say("hello")  # "Joel: hello"
    # 'i'와 'j'는 'Human' 클래스의 인스턴스입니다. 즉, 'Human'의 객체들입니다.

    # 클래스 메서드의 호출
    # '클래스명.클래스 메서드'의 형식으로 호출합니다.
    # '인스턴스 변수명.클래스 메서드'의 접근도 가능합니다.
    i.say(i.get_species())  # "Ian: H. sapiens"
    Human.species = "H. neanderthalensis"  # 클래스 변수의 변경
    i.say(i.get_species())  # => "Ian: H. neanderthalensis"
    j.say(j.get_species())  # => "Joel: H. neanderthalensis"

    # 정적 메서드의 호출
    print(Human.grunt())  # => "*grunt*"
    # 정적 메서드를 인스턴스 객체에서 호출할 수도 있으나, '클래스명.정적 메서드'처럼
    # 호출하는 것이 바람직합니다.
    # print(i.grunt())

    # 프로퍼티의 사용
    i.age = 42  # setter
    # getter
    i.say(i.age)  # => "Ian: 42"
    j.say(j.age)  # => "Joel: 0"
    # deleter
    del i.age
    # i.age # => '_age'가 삭제되었으므로 'AttributeError' 예외가 발생합니다.


####################################################
# 6.1 Inheritance(상속)
####################################################

# 상속을 통해 부모 클래스에서 정의된 메서드와 변수들을 자식 클래스(들)에서 사용할 수
# 있게 됩니다.

# 앞에서 정의한 'Human' 클래스를 부모 클래스로 하여, 자식 클래스인 'Superhero'
# 클래스를 선언하도록 하겠습니다. 자식 클래스는 자신 만의 클래스 변수, 메서드 등을
# 가질 수도 있고 부모 클래스의 변수들인 'species', 'name', 프로퍼티 'age' 및 
# 'sing', 'grunt' 등의 메서드들도 사용할 수 있습니다.

# 모듈화의 예를 들기 위해 위에서 선언한 클래스를 별도의 파일(예를 들어 'human.py')에
# 위치시키고, 다음과 같이 임포트 할 수 있습니다.
# from human import Human  # human.py에서 Human 클래스를 임포트 합니다.
# 다른 파이썬 파일에서 함수 또는 클래스를 사용하기 위해서는 다음과 같이 표시합니다.
# from "파일명(확장자 제외)" import "함수명/클래스명"

# 상속을 위해서는 클래스 선언 시 괄호 안에 부모 클래스 명(들)을 적습니다.
class Superhero(Human):
    # 자식 클래스가 부모 클래스의 모든 정의를 변경없이 상속하여 그대로 사용할 경우
    # 자식 클래스 선언부 바로 다음에 'pass' 문을 사용하면 됩니다.
    # pass

    # 부모 클래스의 속성은 오버라이딩(overriding, 덮어쓰기) 가능합니다.
    species = 'Superhuman'

    # 자식 클래스는 부모 클래스의 생성자와 그 파라미터를 자동으로 상속 받습니다.
    # 또한, 추가 파라미터를 정의할 수도 있고 생성자를 오버라이딩 할 수도 있습니다.
    # 다음의 생성자는 'name' 파라미터를 받아 부모 클래스('Human')의 생성자를
    # 호출하고, 추가적으로 'movie', 'superpowers' 파라미터를 받아 인스턴스
    # 변수를 정의합니다:
    def __init__(self, name, movie=False,
                 superpowers=["super strength", "bulletproofing"]):
        # 'Superhero' 클래스의 인스턴스 변수를 정의합니다.
        self.fictional = True
        self.movie = movie
        self.superpowers = superpowers

        # 'super()' 메서드를 통해 부모 클래스 메서드에 접근 가능합니다.
        # 이 경우 자식 클래스에 의해 '__init__' 메서드가 오버라이딩 되었으며,
        # 부모 클래스의 생성자/메서드는 다음과 같이 접근합니다:
        super().__init__(name)
        # 'super(Superhero, self).__init__(name)'과 동일하며,
        # 'Human.__init__(self, name)'처럼 호출할 수도 있습니다.

    # 'sing' 메서드 오버라이딩
    def sing(self):
        return 'Dun, dun, DUN!'

    # 인스턴스 메서드의 추가
    def boast(self):
        for power in self.superpowers:
            print("I wield the power of {pow}!".format(pow=power))


if __name__ == '__main__':
    sup = Superhero(name="Tick")

    # 인스턴스 타입 체크 방법
    if isinstance(sup, Human):
        print('I am human')  # 'sup'은 'Human'의 인스턴스이기도 합니다.
    if type(sup) is Superhero:
        print('I am a superhero')
        # type(sup) = <class '__main__.Superhero'>

    # 객체지향 프로그래밍에서 클래스의 다중 상속 시 어떤 순서로 메서드를
    # 탐색할지(우선 사용할지)는 중요한 문제입니다. 파이썬의 메소드 탐색 순서는
    # MRO(Method Resolution search Order)를 따릅니다.
    # 메서드 탐색 순서는 '클래스명.__mro__' 또는 '클래스명.mro()'으로 확인할 수
    # 있습니다.
    print(Superhero.__mro__)  # 또는 'print(Superhero.mro())'
    # (<class '__main__.Superhero'>, <class '__main__.Human'>, <class 'object'>)
    # 'Human' 클래스를 별도의 파일로 하여 임포트한 경우 다음과 같이 나타납니다.
    # (<class '__main__.Superhero'>, <class 'human.Human'>, <class 'object'>)

    # 상속된 메서드의 호출
    # 사용되는 속성 'species'은 자식 클래스에서 오버라이딩되었습니다.
    print(sup.get_species())  # => Superhuman

    # 오버라이딩 된 메서드의 호출
    print(sup.sing())  # => Dun, dun, DUN!

    # 상속된 메서드의 호출
    sup.say('Spoon')  # => Tick: Spoon

    # 자식 클래스에만 존재하는 메서드의 호출
    sup.boast()
    # => I wield the power of super strength!
    # => I wield the power of bulletproofing!

    # 프로퍼티의 구현 또한 상속됩니다.
    sup.age = 31
    print(sup.age)  # => 31

    # 자식 클래스에만 존재하는 인스턴스 변수입니다.
    print('Am I Oscar eligible? ' + str(sup.movie))


####################################################
# 6.2 Multiple Inheritance(다중상속)
####################################################

# 다음의 클래스를 구현합니다.
class Bat:
    species = 'Baty'

    def __init__(self, can_fly=True):
        self.fly = can_fly

    # 이 클래스도 'say' 메서드를 가집니다.
    def say(self, msg):
        msg = '... ... ...'
        return msg

    # 다른 메서드도 가집니다.
    def sonar(self):
        return '))) ... ((('


if __name__ == '__main__':
    b = Bat()
    print(b.say('hello'))
    print(b.fly)


# 'Bat' 클래스가 'bat.py' 파일에, 'Superhero' 클래스가 'superhero.py' 파일에
# 정의되었다고 가정하면, 다음과 같이 임포트할 수 있습니다.
# from superhero import Superhero
# from bat import Bat


# 'Superhero' 클래스와 'Bat' 클래스로부터 다중 상속을 받는 'Batman' 클래스를
# 정의합니다.
class Batman(Superhero, Bat):

    def __init__(self, *args, **kwargs):
        # '(*args, **kwargs)'는 메서드 인자를 의미합니다.
        # 상속 시 부모 클래스의 생성자는 'super().__init__(*args, **kwargs)'와
        # 같이 호출합니다. 이는 'super(클래스명, self).__init__(*args, **kwargs)'
        # 과 동일합니다.
        # 다중 상속에서의 'super().__init__(*args, **kwargs)'는 MRO 리스트의
        # 역순으로 상위 클래스부터 호출됩니다.
        # 이 방식은 (피해야 할) 다이아몬드 상속 시에도 부모 클래스의 생성자가
        # 중복으로 호출되는 것을 막아주며, 코드의 유지보수에도 유리합니다.
        # 그러나 여기에서는 다중 상속을 설명하고 있으므로, 아래의 예에서는
        # 각 부모 클래스의 생성자를 명시적으로 호출하였습니다. (다중 상속에서 아래와
        # 같은 방법은 예기치 않은 결과를 반환할 수 있습니다)
        Superhero.__init__(self, 'anonymous', movie=True,
                           superpowers=['Wealthy'], *args, **kwargs)
        Bat.__init__(self, *args, can_fly=False, **kwargs)
        # 인스턴스 변수를 오버라이딩합니다.
        self.name = 'Sad Affleck'

    def sing(self):
        return 'nan nan nan nan nan batman!'


if __name__ == '__main__':
    sup = Batman()

    # MRO 리스트를 반환합니다.
    print(Batman.__mro__)  # => (<class '__main__.Batman'>,
    # <class '__main__.Superhero'>, <class '__main__.Human'>,
    # <class '__main__.Bat'>, <class 'object'>)
    # 위에서 'Superhero', 'Human', 'Bat' 클래스를 모듈화 했다면 '__main__' 대신에
    # 해당 모듈명이 표시될 것입니다.

    # 부모 클래스에 구현된 (상속받은) 메서드를 호출하게 됩니다.
    print(sup.get_species())  # => Superhuman

    # 오버라이딩된 메서드를 호출합니다.
    print(sup.sing())  # => nan nan nan nan nan batman!

    # MRO 리스트의 순서에 따라 메서드를 호출합니다.
    sup.say('I agree')  # => Sad Affleck: I agree

    # 'Bat' 클래스에만 존재하는 메서드입니다.
    print(sup.sonar())  # => ))) ... (((

    # 프로퍼티의 구현도 상속됩니다.
    sup.age = 100
    print(sup.age)  # => 100

    # 'Batman' 클래스의 생성자에서 'Bat'(부모 클래스) 생성자 파라미터의 'can_fly'의
    # 기본값을 오버라이딩 했습니다.
    print('Can I fly? ' + str(sup.fly))  # => Can I fly? False


####################################################
# 7. 고급
####################################################

# 제너레이터(generators)는 lazy evaluation(느긋한 계산)을 가능하게 합니다.
# lazy evaluation은 계산의 결과값이 필요할 때까지 계산을 늦추는 기법입니다.
def double_numbers(iterable):
    for i in iterable:
        yield i + i  # yield 문으로 하나씩 반환합니다.


# 제너레이터는 다음 단계 계산에 필요한 데이터만을 로드하기 떄문에 메모리 효율이
# 좋습니다. 이를 통해 실행을 더 빠르게 할 수 있고, 무한 자료 구조를 사용할 수
# 있습니다.
# 침조. 파이썬3에서는 'xrange' 문이 'range'문으로 대체되었습니다.
for i in double_numbers(range(1, 900000000)):  # `range`는 제너레이터입니다.
    print(i)
    if i >= 30:
        break

# 리스트 comprehension과 마찬가지로, 제너레이터에도 comprehension을 사용할 수
# 있습니다.
values = (-x for x in [1, 2, 3, 4, 5])
for x in values:
    print(x)  # -1 -2 -3 -4 -5 순으로 출력합니다.

# 제너레이터를 리스트로 캐스팅(형변환)할 수 있습니다.
values = (-x for x in [1, 2, 3, 4, 5])
gen_to_list = list(values)
print(gen_to_list)  # => [-1, -2, -3, -4, -5]


# 데코레이터(decorator)
# 데코레이터에 의해 기존에 정의된 함수의 기능을 확장할 수 있습니다.
# 참조. 보다 쉬운 이해를 위해 데코레이터 부분은 Learn Python3 in Y Minutes
# (https://learnxinyminutes.com/docs/python3/)과 다른 코드로 구현했습니다.

# 다른 함수의 실행을 알리는 'notify()' 함수를 구현해봅니다.
def notify(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        print(f"{func.__name__} 함수가 실행되었습니다.")
        return result

    return wrapper


# 실행할 함수입니다.
def function1(n):
    return n * 2


# 'function1()'에 대해서는 다음과 같이 적용합니다.
check_time = notify(function1)
print(check_time(7))


# 이 때 'notify'를 적용할 함수가 여러 개라면, 각 함수에 대해 같은 작업을 중복해야
# 합니다. 따라서 다음과 같이 함수 정의 시 데코레이터를 사용하면 편리합니다.
@notify
def function2(n):
    return n * 3


@notify
def function3(n):
    return n * 4


print(function2(7))
print(function3(7))

```

## 더 배울 준비가 됐습니까?

### 무료 온라인 자료

- [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/)
- [Ideas for Python Projects](http://pythonpracticeprojects.com/)
- [The Official Docs](http://docs.python.org/3/)
- [Hitchhiker’s Guide to Python](http://docs.python-guide.org/en/latest/)
- [Python Course](http://www.python-course.eu/index.php)
- [First Steps With Python](https://realpython.com/learn/python-first-steps/)
- [A curated list of awesome Python frameworks, libraries and software](https://github.com/vinta/awesome-python)
- [30 Python Language Features and Tricks You May Not Know About](http://sahandsaba.com/thirty-python-language-features-and-tricks-you-may-not-know.html)
- [Official Style Guide for Python](https://www.python.org/dev/peps/pep-0008/)
- [Python 3 Computer Science Circles](http://cscircles.cemc.uwaterloo.ca/)
- [Dive Into Python 3](http://www.diveintopython3.net/index.html)
- [A Crash Course in Python for Scientists](http://nbviewer.jupyter.org/gist/anonymous/5924718)

-----

Got a suggestion? A correction, perhaps?  [Open an Issue](https://github.com/adambard/learnxinyminutes-docs/issues/new)  on the Github Repo, or make a  [pull request](https://github.com/adambard/learnxinyminutes-docs/edit/master/python3.html.markdown)  yourself!

Originally contributed by Louie Dinh, and updated by  [62 contributor(s)](https://github.com/adambard/learnxinyminutes-docs/blame/master/python3.html.markdown).

[![Creative Commons License](https://i.creativecommons.org/l/by-sa/3.0/88x31.png)](https://creativecommons.org/licenses/by-sa/3.0/deed.en_US)
