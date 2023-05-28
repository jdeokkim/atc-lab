# [abc156_c](https://atcoder.jp/contests/abc156/tasks/abc156_c)

<details>
  <summary>알고리즘 분류</summary>
  
  *brute force*
</details>

<br />

## 풀이 과정

문제 조건에서 $X_i$의 범위가 $1 \leq X_i \leq 100$로 충분히 작기 때문에, $P = 1$일 때의 스태미나 합부터 시작해서 $P = 100$일 때의 스태미나 합까지 모든 경우의 수를 따지면서 최솟값을 찾으면 된다.

<br />

## 소스 코드

```c
#include <limits.h>
#include <stdio.h>
#include <stdlib.h>

#define MAX_COUNT 100

int main(void) {
    int n;

    scanf("%d", &n);

    int values[MAX_COUNT];

    for (int i = 0; i < n; i++)
        scanf("%d", values + i);

    int result = INT_MAX;

    for (int p = 1; p <= 100; p++) {
        int sum = 0;

        for (int i = 0; i < n; i++)
            sum += (values[i] - p) * (values[i] - p);

        if (result > sum) result = sum;
    }

    printf("%d\n", result);

    return 0;
}
```