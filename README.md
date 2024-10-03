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
