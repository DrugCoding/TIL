# TIL (Today I Learned)
# 절대 규칙
- 무슨 일이 있어도 하루 1commit
- 간단하게라도 꼭 정리하기
---
## 7/5 - Git의 시작
- 로컬저장소 만드는 단계
  - git init
  - git add
  - git status
  - git commit -m "커밋 메시지"
  - git log (--oneline , -2 --oneline)

## 7/6 - Github의 시작
- 원격저장소 만들기
  - Your repositories 에 들어가서 만든다.
- 로컬저장소에 원격저장소 등록
  - git remote add origin <원격저장소 주소>
    - 주소가 잘 들어갔는지 확인 명령어 : git remote -v
- 로컬저장소의 커밋을 원격저장소로 올리기
  - git push origin master
- git pull 과 git clone
  - 로컬저장소가 있을 때 pull / 통째로 받아와야 할 때 clone
  
## 7/7 - Git branch 그리고 협업
- branch 생성
  - git branch "branch name"
- branch 이동
  - git chechout "branch name"
    - 브랜치 생성과 동시에 이동 : git checkout -b "branch name"
- branch 목록 확인
  - git branch
- branch 이동해서 작업 후 marge
  - git checkout "blabla" --add commit--> git checkout master --> git marge blabla (꼭 원래의 HEAD에 와서 marge 할 것)
- branch 삭제
  - git branch -d "blabla" (다 쓴 branch는 제거해도 commit이 사라지지는 않음)
- branch conflict(브랜치 충돌)
  - 혼자 쭉 하는경우/다른 파일을 수정하는 경우 상관없음
  - 같은 파일을 수정하는 경우 conflict 일어남
    - 충돌 된 부분 수정 --> git add . --> git commit (code 보고 닫는다)

## 7/11 - Python 의 기초

> 컴퓨터`[Computer]`(Caulation(계산)+Remember(기억))
>
> 프로그래밍`[Programmng]`(명령어의 모음(집합))
>
> 언어 (컴퓨터에게 명령하는 말)

``````
선언적 지식(declarative knowledge) - 사실에 대한 내용
명령적 지식(imperative knowledge) - How-to
``````

- Python 의 특징
  - 동적 타이핑 언어 - 변수에 별도의 타입 지정이 필요 없음
  - **객체 지향 프로그래밍(Object Oriented Programming)**

> 코드는 위에서 아래로 / 오른쪽에서 왼쪽으로

- Python 문법 (숫자[정수 실수 복수] , 문자 , Bool[True False] , None)

  - 모든 결과는 ```print('hello')``` 를 해야 보여진다.

  - 변수(Variable)는 할당 연산자`=`를 동해 할당 된다.

  - `#` 는 컴퓨터는 못보는 메모, 주석

  - `0`은 False `1`은 True

  - 정수`int`  , 실수 `float` (소수점) , `str`문자열

  - `%`나머지 ,  `//`몫  ,  `**`거듭제곱

  - `<=`이하 , `>=`이상 , `==`같다 , `!=`같지않다

  - 인덱싱 첫 번째 자리는 `0`이다 , 거꾸로 하면 끝자리부터 `-1` `-2` `-3`(마지막 자리는 `-1`)

    ```python
    fruit = 'abcde'
    print(fruit[1:3])
    # bc
    
    fruit = 'abcde'
    print(fruit[-1])
    # e
    
    fruit = 'abcde'
    print(fruit[2:5:2])
    # ce
    
    fruit = 'abcde'
    print(fruit[3:1:-1])
    # dc
    
    fruit = 'abcde'
    print(fruit[:3])
    # abc # :(기본)부터 3자리
    
    fruit = 'abcde'
    print(fruit[1:])
    # bcde # 1부터 끝까지 
    
    [::] = 처음부터 끝까지 abcdef
    [::-1] = 뒤집기 fedcba
    
    'a' in 'apple'
    # True
    ```

  - `len`글자길이 , 

## 7/12

## 7/13 - 함수(def)

- 함수는 반드시 값을 하나만 return한다
  - return이 없는 경우에도 None을 반환한다
- return과 동시에 종료된다

## 7/14 - 문자열/리스트/

- 문자열

  - .split() --> 문자열 쪼개기
    - 문자열을 쪼개서 리스트로 반환
  - .join(['3', '5']) --> 문자열 붙이기
    - #35
  - 문자열 변경 .replace(old, new[,count])

  - 'apple'.find('p') # 1  , fine('k')시 -1 출력

- 리스트
  - .append('값')                   -
  - .extend(['appel', 'banana']) - 차례대로 맨 뒤에 추가하기 
    - 주의 .extend('apple') --> ['a','p','p','l','e'] 꼭 리스트 형식으로 넣기           
  - .insert(i, x) - i 위치에 x('apple')값을 추가                 
  - .remove('값')   
  - .sort() - 리스트 정렬
  - .count('값') - 리스트에서 항복 ''가 몇 개 존재하는지 **갯수**를 반환
  - .pop() - 리스트 가장 오른쪽에 있는 항목을 반환 후 제거                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 
  - .index('값') - '값'의 위치를 반환 #0,1,2,3,4,5  
    - .reverse() - 순서를 반대로 뒤집는다 (정렬 아님)

## 7/15 - 모듈

## 7/18  - 딕셔너리 마무리 & 디버깅 & 에러와 예외

``````python
# 딕셔너리 추가
result = {}
result['a'] = 0
print(result) # {'a':0}

word = 'banana'

result = {}

for char in word:
    print(char)
    # 키가 없으면 1으로 초기화를 하고
    if char not in result:
        result[char] = 1
    # 키가 있으면 기존 값에 더하자
    else:
        result[char] = result[char] + 1
# 츌력결과        
print(result)
# b
# a
# n
# a
# n
# a
{'b':1, 'a':3, 'n':2}        
``````

- **디버깅**(주석&출력 / VScode / 파이썬시뮬)
- 에러(Error)
  - 문법 에러(Syntax Error) - 표시된 line을 시점으로 띄어쓰기 따옴표 등등 확인
  - TypeError - 정수 실수 문자 등등
  - ValueError - 타입은 올바르나 값이 적절하지 않거나 없는 경우(코드가 잘못 됨)
  - IndexError - 목록보다 넘어서는 걸 출력하고자 했을 때
  - KeyError - 딕셔너리 활용과정 (키가 없어서)
  - ModuleNotFoundError - 존재하지 않는 모듈을 import 하는경우
  - IndentationError - 스페이스, 탭 등등
  - Keyboardinterrupt - 임의로 코드가 계속 돌 때 (Ctrl + c 로 종료)
