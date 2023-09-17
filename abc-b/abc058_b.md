# [abc058_b](https://atcoder.jp/contests/abc058/tasks/abc058_b)

<details>
  <summary>알고리즘 분류</summary>
  
  *string*
</details>

## 풀이 과정

홀수 자리에 있는 문자와 짝수 자리에 있는 문자를 번갈아 출력해주면 된다.

## 소스 코드

```c
#include <stdio.h>
#include <stdlib.h>

#define MAX_INPUT_SIZE 51

int main(void) {
    char o[MAX_INPUT_SIZE], e[MAX_INPUT_SIZE];

    scanf("%s %s", o, e);

    int next = 0, i = -1;

    for (;;) {
        if (next % 2 == 0) {
            i = (next / 2);

            if (o[i] == '\0') break;

            putchar(o[i]);
        } else {
            i = (next - 1) / 2;

            if (e[i] == '\0') break;
            
            putchar(e[i]);
        }

        next++;
    }

    puts("");

    return 0;
}
```