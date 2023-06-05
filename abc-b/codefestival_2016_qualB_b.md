# [codefestival_2016_qualB_b (Qualification simulator)](https://atcoder.jp/contests/code-festival-2016-qualb/tasks/codefestival_2016_qualB_b)

<details>
  <summary>알고리즘 분류</summary>
  
  *implementation*
</details>

<br />

## 풀이 과정

대회에서 합격 가능한 사람들의 수를 `q`에 저장하고, 학생의 종류를 나타내는 문자를 하나씩 입력받는다.

1. 입력받은 문자가 'a'인 경우, 일본 학생임을 뜻하므로 `q`의 값을 1 감소시킨다.
2. 입력받은 문자가 'b'인 경우, 유학생임을 뜻하므로 `q`의 값과 `b`의 값을 1 감소시킨다.
3. 'a'와 'b'를 제외한 다른 문자를 입력받은 경우, 일반인으로 간주하여 불합격 처리한다.

<br />

## 소스 코드

```c
#include <stdio.h>
#include <stdlib.h>

int main(void) {
    int n, a, b;

    scanf("%d %d %d ", &n, &a, &b);

    int q = a + b;

    for (int i = 0; i < n; i++) {
        char c = getchar();

        if (c == 'a') {
            puts((q > 0) ? "Yes" : "No");

            if (q > 0) q--;
        } else if (c == 'b') {
            puts(((q > 0) && (b > 0)) ? "Yes" : "No");

            if (q > 0 && b > 0) q--, b--;
        } else {
            puts("No");

            continue;
        }
    }

    return 0;
}
```