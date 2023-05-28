# [abc042_a](https://atcoder.jp/contests/abc042/tasks/abc042_a)

<details>
  <summary>알고리즘 분류</summary>
  
  *implementation*
</details>

<br />

## 풀이 과정

조건문을 이용해 세 숫자 중 2개가 5이고 나머지 하나가 7일 경우 "YES"를 출력하면 된다.

<br />

## 소스 코드

```c
#include <stdbool.h>
#include <stdio.h>
#include <stdlib.h>

int main(void) {
    int a, b, c;

    scanf("%d %d %d", &a, &b, &c);

    bool possible = (a == 5 && b == 5 && c == 7)
        || (a == 5 && b == 7 && c == 5)
        || (a == 7 && b == 5 && c == 5);

    puts(possible ? "YES" : "NO");

    return 0;
}
```