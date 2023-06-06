# [abc066_b (ss)](https://atcoder.jp/contests/abc066/tasks/abc066_b)

<details>
  <summary>알고리즘 분류</summary>
  
  *implementation, string*
</details>

<br />

## 풀이 과정

문자열의 최대 길이가 충분히 짧기 때문에, 마지막 문자를 하나씩 지우고 남은 문자열을 반씩 나누어 같은지를 비교하면 된다.

<br />

## 소스 코드

```c
#include <stdio.h>
#include <stdlib.h>

#define MAX_LENGTH 201
 
int main(void) {
    char s[MAX_LENGTH];

    int low = 0, high, mid;

    scanf("%s%n", s, &high); high -= 2;

    for (;;) {
        if ((high % 2) != 0) {
            mid = low + (high - low) / 2;

            int valid = 1;

            for (int i = 0; i <= mid; i++) {
                if (s[i] != s[(mid + 1) + i]) {
                    valid = 0;

                    break;
                }
            }

            if (valid) break;
        }

        high--;
    }

    printf("%d\n", high + 1);

    return 0;
}
```