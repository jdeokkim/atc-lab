# [panasonic2020_b (Bishop)](https://atcoder.jp/contests/panasonic2020/tasks/panasonic2020_b)

<details>
  <summary>알고리즘 분류</summary>
  
  *implementation, math*
</details>

<br />

## 풀이 과정

체스판의 가로 길이 또는 세로 길이가 1일 때는 비숍이 대각선으로 이동할 수 없으므로, 이동 가능한 칸의 개수는 항상 1이 된다. 그 이외의 경우에는 체스판의 가로 길이와 세로 길이의 곱을 통해 체스판의 홀수 칸의 개수를 구할 수 있다.

<br />

## 소스 코드

```c
#include <stdio.h>
#include <stdlib.h>
 
int main(void) {
    long long int h, w;

    scanf("%lld %lld", &h, &w);

    long long int k = ((h * w) / 2LL) + ((h * w) % 2LL);

    if (h == 1LL || w == 1LL) k = 1LL;

    printf("%lld\n", k);
    
    return 0;
}
```