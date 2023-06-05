# [abc121_b (Can you solve this?)](https://atcoder.jp/contests/abc121/tasks/abc121_b)

<details>
  <summary>알고리즘 분류</summary>
  
  *implementation*
</details>

<br />

## 풀이 과정

이중 반복문으로 각 소스 코드를 하나씩 검사한다.

<br />

## 소스 코드

```c
#include <stdio.h>
#include <stdlib.h>
 
int main(void) {
    int n, m, c;

    scanf("%d %d %d", &n, &m, &c);

    int *b = malloc(m * sizeof *b);

    for (int i = 0; i < m; i++) scanf("%d", &b[i]);

    int result = 0;

    for (int i = 0; i < n; i++) {
        int sum = c;

        for (int j = 0; j < m; j++) {
            int a;

            scanf("%d", &a);

            sum += a * b[j];
        }

        if (sum > 0) result++;
    }

    printf("%d\n", result);

    free(b);
    
    return 0;
}
```