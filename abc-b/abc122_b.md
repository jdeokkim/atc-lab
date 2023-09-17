# [abc122_b (ATCoder)](https://atcoder.jp/contests/abc122/tasks/abc122_b)

<details>
  <summary>알고리즘 분류</summary>
  
  *implementation, string*
</details>

<br />

## 풀이 과정

입력받은 문자열의 각 문자를 하나씩 확인하고, 문제 조건에 맞지 않는 문자가 나오면 현재 문자열의 길이를 `0`으로 설정한다.

<br />

## 소스 코드

```c
#include <stdio.h>
#include <stdlib.h>

#define MAX_INPUT_SIZE 11

int main(void) {
    char s[MAX_INPUT_SIZE];

    scanf("%s", s);

    int len = 0, result = -1;

    for (int i = 0; s[i] != '\0'; i++) {
        len = (s[i] == 'A' || s[i] == 'C' || s[i] == 'G' || s[i] == 'T')
            ? len + 1
            : 0;

        if (result < len) result = len;
    }

    printf("%d\n", result);

    return 0;
}
```