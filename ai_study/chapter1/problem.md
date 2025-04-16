## 문제 1: 리스트 조작하기

1부터 20까지의 숫자 중에서 짝수만 포함하는 리스트를 만들고, 각 숫자를 3배로 늘린 결과를 출력하세요. 리스트 컴프리헨션을 활용해보세요.

## 문제 2: 딕셔너리 다루기

다음과 같은 학생들의 점수 딕셔너리가 있습니다:

```python
scores = {'Alice': 85, 'Bob': 92, 'Charlie': 78, 'David': 95, 'Eva': 88}

```

1. 모든 학생 이름과 점수를 "이름: 점수" 형태로 출력하세요.
2. 가장 높은 점수를 받은 학생의 이름과 점수를 출력하세요.
3. 점수가 90점 이상인 학생들의 이름만 리스트로 만들어 출력하세요.

# 문제 1. format과 소수점
<hr>

아래 코드를 실행하고, 지시에 따라 코드를 작성하세요.
```python
import math,io,sys

def main(input_code):
    origin_stdout = sys.stdout
    sys.stdout = io.StringIO()

    try:
        exec(input_code)
        output = sys.stdout.getvalue().strip()
        answer = format(math.pi, ".6f")
        if output == answer:
            return f"Correct! (Output: {output})"
        else:
            return f"Incorrect! (Output: {output})"

    except Exception as e:
        return f"An Error Occurred during executing code. : {e}"

    finally:
        sys.stdout = origin_stdout
print("문제 : 숫자 출력 형식을 지정하는 방법을 이용해, 원주율의 값을 소수점 이하 6자리까지 출력하는 코드를 입력하세요. \n(입력 종료는 엔터 두 번)")
lines = []
while True:
    line = input()
    if line == "":
        break
    lines.append(line)

input_code = "\n".join(lines)
result = main(input_code)
print(result)
```

# 문제 2. 함수와 피보나치
<hr>


제 1항과 제 2항을 1이라 하고, 제 3항부터는 앞의 두 항의 합을 취하는 수열을 피보나치 수열이라고 한다.<br> 
예를 들어 제 3항은 2이며, 제 4항은 3이다.

### 입력 : 첫째줄에 두 수 a,b를 공백으로 구분하여 입력받고 (0 < a < b)

### 출력 : 첫째 줄에 구한 합을 출력한다. 



<hr>

#### Test Case 1)
	Input : 4 10
	Output : 139
	
#### Test Case 2)
	Input : 3 5
	Output : 10

#### Test Case 3)
	Input : 3 6
	Output : 18

#### Test Case 4)
	Input : 11 63
	Output : 17167680177421

# 📘 Python 코딩 문제 모음

---

## 🥇 1번 문제 - 가위바위보 결과 구현

### 📌 문제 설명

- A와 B는 **총 3번의 가위바위보 게임**을 진행합니다.
- 각 게임은 **비길 경우 다시 진행**하며, **승부가 나야 1게임**으로 인정됩니다.
- 각 라운드의 승자와 **비긴 횟수**, **최종 승자**, 그리고 **최종 승자의 이력**을 출력합니다.
- 가위바위보는 **랜덤**으로 결정합니다.

### ✅ 출력 예시
```
#   [ 1  라운드 승자 A , 비긴횟수 :  0 ]
#   [ 2  라운드 승자 A , 비긴횟수 :  0 ]
#   [ 3  라운드 승자 B , 비긴횟수 :  1 ]
#   ['최종 승리자 A']
#   A 가 낸 가위바위보 이력 : ['보', '가위', '보', '바위']
```


---

## 🥈 2번 문제 - Numpy 없이 3x3 행렬 만들기

### 📌 문제 설명

- 각 원소의 값이 **행 번호 + 열 번호**인 `3 x 3` 행렬을 생성하세요.
- 아래 내용을 함께 출력하세요:
  - **대각선 원소 배열** (왼쪽 위 → 오른쪽 아래)
  - **대각선 원소의 합**
  - **가장 큰 합을 가진 행**
  - **가장 작은 합을 가진 열**

### ✅ 출력 예시
```
#행렬렬 [[2, 3, 4], [3, 4, 5], [4, 5, 6]]
#대각원소소 [2, 4, 6]
#대각원소합합 12
#가장큰 행 [4, 5, 6]
#가장 작은은열 [2, 3, 4]
```

---

## 🥉 3번 문제 (심화)

- 프로그래머스 1단계 문제 중 하나를 선택하여 풀이하세요.
- 링크: [👉 프로그래머스 문제 모음](https://school.programmers.co.kr/learn/challenges?order=recent&levels=1&languages=python3&partIds=58464)

```python
# 정답 코드 작성 영역