# [dp_a (Frog 1)](https://atcoder.jp/contests/dp/tasks/dp_a)

<details>
  <summary>알고리즘 분류</summary>
  
  *dp*
</details>

<br />

## 풀이 과정

TODO: ...

<br />

## 소스 코드

```c
#include <stdio.h>
#include <stdlib.h>

int main(void) {
    int n;

    scanf("%d", &n);

    int *stones = calloc(n + 1, sizeof *stones);

    for (int i = 1; i <= n; i++) scanf("%d", stones + i);

    int *dp = calloc(n + 1, sizeof *dp);

    dp[2] = abs(stones[2] - stones[1]);

    for (int i = 3; i <= n; i++) {
        int v1 = dp[i - 1] + abs(stones[i] - stones[i - 1]);
        int v2 = dp[i - 2] + abs(stones[i] - stones[i - 2]);

        dp[i] = (v1 < v2) ? v1 : v2;
    }

    printf("%d\n", dp[n]);

    free(dp), free(stones);

    return 0;
}
```