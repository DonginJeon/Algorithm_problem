- 1014
```
- in : 실제 숫자가 포함되어 있느냐를 보려면 str형태로 바꾸어보면 좋음
```


- 1013

```
- 이중 리스트를 닥셔너리로 만듦
def solution(snippet, message):
    # 메시지를 공백 단위로 단어 리스트로 변환
    words = message.split()
    
    # snippet을 딕셔너리로 변환
    snippet_dict = {abbr: full for abbr, full in snippet}
    
    # 각 단어를 순회하면서 대치가 필요한 경우 대치
    for i in range(len(words)):
        if words[i] in snippet_dict:
            words[i] = snippet_dict[words[i]]
```
```
- 정규표현식 및 join

import re

def solution(snippet, message):
    m_list = re.split(r'(\s+|[!@#$%^&*().,?])', message) 
    
    for i in range(len(m_list)):
        # 단어가 대치될 단어에 해당하는지 확인
        for pair in snippet:
            if m_list[i] == pair[0]:
                # 대치 목록에 있으면 해당 단어를 대치 단어로 변경
                m_list[i] = pair[1]
    
    # 대치된 단어 리스트를 다시 문자열로 합쳐서 반환
    return ''.join(m_list)
```

```
- 최대공약수 : math.gcd(a,b)
```

```
- 순회한 문자가 특정 문자를 포함하고 있는지 : all(c in '05' for c in str(num))
```


- 1012

```
여러개로 끊기
re.split(r'[!@#$%^&*().,? ]+', message)
```

```
sorted() 함수:

sorted() 함수는 파이썬 내장 함수로, 리스트를 정렬해 새로운 리스트를 반환합니다.
정렬 시 어떤 기준으로 정렬할지 결정하는 key 파라미터를 사용할 수 있습니다. 여기서 key로는 특정 함수(혹은 람다 함수)를 제공할 수 있습니다. 이 함수는 리스트의 각 원소에 적용되어, 그 값을 기준으로 정렬하게 됩니다.
lambda 함수:

lambda x: (abs(x - n), -x) 부분은 익명 함수(람다 함수)입니다. 이 함수는 리스트의 각 원소 x에 대해 (abs(x - n), -x) 튜플을 반환합니다.
이 튜플을 이용해 두 가지 기준으로 정렬하게 됩니다:
abs(x - n): x가 n으로부터 얼마나 떨어져 있는지(절대 거리)를 계산합니다. 거리가 가까울수록 우선순위가 높아집니다.
-x: 거리가 같은 경우, 더 큰 수가 먼저 오도록 내림차순으로 정렬하기 위해 -x 값을 사용합니다. 즉, 음수 기호를 붙여 더 큰 값이 우선 정렬되도록 합니다.
```

- 1008

```
array = [1, 2, 3, 3, 3, 4]
count = [0] * (max(array)+1)
for i in array:
    count[i] += 1

빈 0 리스트를 만들고 최대값 수만큼 만들면 숫자 범위만큼 0이 생김. 반복문으로 1씩 더하면 각 숫자의 출현 수를 셀 수 있음

```

- 1006

```
좌표를 가지고 문제를 푸는 경우
direction = [(-1, 0), (1, 0), (0, -1), (0, 1), (-1, -1), (-1, 1), (1, -1), (1, 1)]
> 방향 정하기 - 리스트로 만들어서
danger_board = [[0] * n for _ in range(n)]
> 크기 만큼 다 0으로 찬 행렬 만들기
```

```
from collections import Counter
등장한 원소의 개수 세기
```

```
import math
a, b = 6, 15
math.lcm(a, b)
최소공배수 구하기
```

- 1003

```
- 숫자를 끊기
  list(map(int,str(order)))
- sorted로 끊어진 문자열
  ''.join(sorted(my_string.lower())) 이걸로 합칠 수 있음
```

- 0905

```
문자열에서 숫자만 찾고 싶을때, isdigit을 하면됨
```

- 0823

```
왼쪽에 오는 특정문자 제거
.lstrip('0')
```

- 0821

```
- .sort()를 사용하면 이를 실행하고 밑에서 리스트를 가지고 인덱싱을 해야 특정값을 가져올 수 있음.
```

- 0819

```
- 배열 내에서 공통이 되는 원소의 수를 찾을 때는 교집합을 활용하면 쉽게 찾을 수 있다.
- 딕셔너리
  - 빈 딕셔너리를 만들고 키와 벨류를 나중에 입력해도 그 딕셔너리 안으로 들어가게 된다.
```

- 0818

  ```
  - not in을 잘 활용하면 안에 있는 것을 뺄 수 있음
  - list(range(a,b))를 활용하면 1씩 추가된 리스트를 만들 수 있음
  - .sort() => 리스트안에 문자를 정렬(알파벳이면 사전순)
  ```

- 0814

  ```
  - 특정 문자를 빈 문자로 만들고 싶을 때, 문자열.replace(특정문자,"")
  - if문 대신 딕셔너리를 잘 활용하는 것도 좋다
  - 순서를 지정할때 전체에서 1을 빼고 싶으면 그냥 -1을 작성하면 됨
  ```

- 0808

  ```
  - 슬라이싱 문제
  - [시작:끝:간격]
  - [::-1]
  - 끝까지로 지정하고 싶으면 비워두면 됨->[n:] : n부터 끝까지
  - 리스트 끼리는 그냥 += 로 더해주면 됨
  ```

- 0807

  ```
  문자열1 in 문자열2
  -> 포함되어 있는지 확인
  ```

  ```
  - continue

  for 문의 조건을 깨고 다음을 실행
  ```

* 0805
  ```
  - enumerate(for 문에서 range 대신 사용)
    >>> for i, letter in enumerate(['A', 'B', 'C'], start=1):
    ...     print(i, letter)
    ...
    1 A
    2 B
    3 C
  ```
