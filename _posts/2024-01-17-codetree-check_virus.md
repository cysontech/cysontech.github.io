---
title: "코드트리: 바이러스 검사 문제 풀이"
excerpt: "코테 기출풀이"

categories:
  - samsung
tags:
  - 삼성코테기출
---

# 바이러스 검사

### 문제 링크

https://www.codetree.ai/training-field/frequent-problems/problems/virus-detector?&utm_source=clipboard&utm_medium=text

### 문제풀이 코드

```python
n = int(input())
r_list = list(map(int, input().split()))
boss_max, emp_max = map(int, input().split())
ans = 0

for r in r_list:
    ans += 1
    if r < boss_max:
        r = 0
    else:
        r -= boss_max
    ans += r // emp_max
    if r%emp_max != 0:
        ans += 1

print(ans)
```

### 나의 풀이

팀장이 무조건 필요하고,  
검사자 수의 '최소' 값을 구해야 하므로  
각 가게마다 전체 인원 수에서 먼저 팀장이 검사 가능한 인원을 빼고,  
나머지를 팀원들이 검사 가능한 인원으로 나누어 필요한 사람의 수를 구하는 방식으로 문제를 풀었다.

### 유의할 점

원래 가게에 있는 사람 수가,  
팀장이 검사 가능한 인원 보다 적은 경우를 유의해야 한다.

### 느낀점

문제를 풀 때 쉬운 문제여도 방심하지 말고 여러가지 경우의 수를 꼭 짚어보자.
