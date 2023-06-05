# [sumitb2019_b (Tax Rate)](https://atcoder.jp/contests/abc139/tasks/abc139_b)

<details>
  <summary>알고리즘 분류</summary>
  
  *implementation, math*
</details>

<br />

## 풀이 과정

이산 수학에서 배웠던 바닥 함수 (floor function)의 정의를 이용한다. 

문제 지문에 적혀있는 **"(rounded down to the nearest integer)"** 라는 설명을 통해, $N = \lfloor1.08 \times x\rfloor$임을 알 수 있다. 그런데 $N \leq 1.08 \times x < N + 1 \space (\because \lfloor x \rfloor = n \iff n \leq x < n + 1)$ (단, $n$은 정수, $x$는 실수) 이므로, $\frac{100 \times N}{108} \leq x < \frac{100 \times (N + 1)}{108}$를 만족하는 $x$의 값 중에서 정수인 것을 찾으면 된다.

<br />

## 소스 코드

```c
#include <stdio.h>
#include <stdlib.h>
 
int main(void) {
    int n;
 
    scanf("%d", &n);

    const double INVERSE_MULTIPLIER = 100.0 / 108.0;
    const double MULTIPLIER = 108.0 / 100.0;

    // `x`의 최솟값을 계산한다.
    double min_x = n * INVERSE_MULTIPLIER;
 
    int k = n * INVERSE_MULTIPLIER;

    // `min_x - k`가 0보다 크다는 것은 `min_x`가 부동 소수점 
    // 값이라는 것, 즉 `min_x`에 소수점 이하 부분이 존재한다는 
    // 것을 뜻하므로, `k`의 값을 증가시키고 `x`의 범위에 
    // 포함되는지를 확인한다.
    // if ((min_x - k) > 0) k++;
    if (min_x > k) k++;
    
    printf((int) (k * MULTIPLIER) == n ? "%d\n" : ":(\n", k);
    
    return 0;
}
```