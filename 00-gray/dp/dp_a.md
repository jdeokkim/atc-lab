# [dp_a (Frog 1)](https://atcoder.jp/contests/dp/tasks/dp_a)

<details>
  <summary>알고리즘 분류</summary>
  
  *dp*
</details>

<br />

## 풀이 과정

개구리가 $i$번째 돌 위에 있다고 가정하자. 문제 지문에서 $i - 2$번째 돌에서 $i$번째 돌까지 이동하는 비용 또는 $i - 1$번째 돌에서 $i$번째 돌까지 이동하는 비용 외에는 추가적인 조건이 없으므로, 개구리가 $i$번째 돌에 도착하기까지 어떤 돌을 거쳐서 왔는지는 중요하지 않음을 알 수 있다.

따라서 개구리가 $n$번째 돌까지 이동하기 위해 필요한 최소 비용을 구하기 위한 점화식을 다음과 같이 세울 수 있다. 

$$
\begin{equation}
    f(n) =
    \begin{cases}
        0 \  (if \ n \le 1) \\
        |h_2 - h_1| \ (if \ n = 2) \\
        min(f(n - 2) + |h_{n - 2} - h_n|, f(n - 1) + |h_{n - 1} - h_n|) \ (if \ n > 2) \\
    \end{cases}
\end{equation}
$$

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
