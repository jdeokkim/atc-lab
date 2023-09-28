## 동적 계획법

동적 계획법 (dynamic programming, DP)란 **주어진 문제를 여러 개의 작은 문제들로 쪼개고, 이 작은 문제들을 해결하여 얻은 해답을 재활용**해 주어진 문제를 푸는 알고리즘을 뜻한다. 동적 계획법은 **주로 어떤 조건을 만족하는 모든 경우의 수를 구하는 문제** (조합론, 백트래킹?) 또는 **최솟값이나 최댓값을 구하는 문제** (그리디 알고리즘?)가 나왔을 때 고려해볼 수 있는 전략이다.

## 메모이제이션

동적 계획법에서 **각각의 작은 문제에 대한 해답을 저장해두면** 나중에 이 문제들에 대한 해답이 필요할 때 미리 저장해둔 값을 이용하여 불필요한 계산을 피할 수 있는데, 이것을 메모이제이션 (memoization) 또는 캐싱 (caching)이라고 한다.

## 문제 해결 전략

1. 주어진 문제를 해결하기 위해 이 문제를 어떤 기준으로 작게 쪼갤 것인지를 결정한다. 즉, 각각의 작은 문제를 표현할 수 있는 핵심적인 내용이 무엇인지를 찾는다. 
2. 각각의 작은 문제를 해결하기 위한 기본 단계를 정의하고, 작은 문제들 간의 관계를 통해 점화식을 세워 주어진 문제를 해결한다.

## 연습 문제

<details>
<summary>펼치기 / 접기</summary>

- [x] [dp_a](https://atcoder.jp/contests/dp/tasks/dp_a)
- [ ] [dp_b](https://atcoder.jp/contests/dp/tasks/dp_b)
- [ ] [dp_c](https://atcoder.jp/contests/dp/tasks/dp_c)
- [ ] [dp_d](https://atcoder.jp/contests/dp/tasks/dp_d)
- [ ] [dp_e](https://atcoder.jp/contests/dp/tasks/dp_e)
- [ ] [dp_f](https://atcoder.jp/contests/dp/tasks/dp_f)
- [ ] [dp_g](https://atcoder.jp/contests/dp/tasks/dp_g)
- [ ] [dp_h](https://atcoder.jp/contests/dp/tasks/dp_h)
- [ ] [dp_i](https://atcoder.jp/contests/dp/tasks/dp_i)
- [ ] [dp_j](https://atcoder.jp/contests/dp/tasks/dp_j)
- [ ] [dp_k](https://atcoder.jp/contests/dp/tasks/dp_k)
- [ ] [dp_l](https://atcoder.jp/contests/dp/tasks/dp_l)
- [ ] [dp_m](https://atcoder.jp/contests/dp/tasks/dp_m)
- [ ] [dp_n](https://atcoder.jp/contests/dp/tasks/dp_n)
- [ ] [dp_o](https://atcoder.jp/contests/dp/tasks/dp_o)
- [ ] [dp_p](https://atcoder.jp/contests/dp/tasks/dp_p)
- [ ] [dp_q](https://atcoder.jp/contests/dp/tasks/dp_q)
- [ ] [dp_r](https://atcoder.jp/contests/dp/tasks/dp_r)
- [ ] [dp_s](https://atcoder.jp/contests/dp/tasks/dp_s)
- [ ] [dp_u](https://atcoder.jp/contests/dp/tasks/dp_u)
- [ ] [dp_v](https://atcoder.jp/contests/dp/tasks/dp_v)
- [ ] [dp_w](https://atcoder.jp/contests/dp/tasks/dp_w)
- [ ] [dp_x](https://atcoder.jp/contests/dp/tasks/dp_x)
- [ ] [dp_y](https://atcoder.jp/contests/dp/tasks/dp_y)
- [ ] [dp_z](https://atcoder.jp/contests/dp/tasks/dp_z)

---

- [ ] [abc208_b](https://atcoder.jp/contests/abc208/tasks/abc208_b)
- [ ] [abc153_d](https://atcoder.jp/contests/abc153/tasks/abc153_d)
- [ ] [abc247_c](https://atcoder.jp/contests/abc247/tasks/abc247_c)
- [ ] [abc139_c](https://atcoder.jp/contests/abc139/tasks/abc139_c)
- [ ] [abc229_c](https://atcoder.jp/contests/abc229/tasks/abc229_c)
- [ ] [abc203_c](https://atcoder.jp/contests/abc203/tasks/abc203_c)
- [ ] [abc148_d](https://atcoder.jp/contests/abc148/tasks/abc148_d)
- [ ] [sumitb2019_c](https://atcoder.jp/contests/sumitrust2019/tasks/sumitb2019_c)
- [ ] [agc037_a](https://atcoder.jp/contests/agc037/tasks/agc037_a)
- [ ] [abc115_c](https://atcoder.jp/contests/abc115/tasks/abc115_c)
- [ ] [abc136_c](https://atcoder.jp/contests/abc136/tasks/abc136_c)
- [ ] [keyence2021_b](https://atcoder.jp/contests/keyence2021/tasks/keyence2021_b)
- [ ] [abc274_c](https://atcoder.jp/contests/abc274/tasks/abc274_c)
- [ ] [abc214_c](https://atcoder.jp/contests/abc214/tasks/abc214_c)
- [ ] [hhkb2020_c](https://atcoder.jp/contests/hhkb2020/tasks/hhkb2020_c)
- [ ] [abc121_c](https://atcoder.jp/contests/abc121/tasks/abc121_c)
- [ ] [abc120_c](https://atcoder.jp/contests/abc120/tasks/abc120_c)
- [ ] [abc301_c](https://atcoder.jp/contests/abc301/tasks/abc301_c)
- [ ] [arc088_a](https://atcoder.jp/contests/arc088/tasks/arc088_a)

---

- [ ] [abc245_c](https://atcoder.jp/contests/abc245/tasks/abc245_c)
- [ ] [abc260_c](https://atcoder.jp/contests/abc260/tasks/abc260_c)
- [ ] [agc029_a](https://atcoder.jp/contests/agc029/tasks/agc029_a)
- [ ] [abc240_c](https://atcoder.jp/contests/abc240/tasks/abc240_c)
- [ ] [agc012_a](https://atcoder.jp/contests/agc012/tasks/agc012_a)
- [ ] [abc174_d](https://atcoder.jp/contests/abc174/tasks/abc174_d)
- [ ] [abc185_d](https://atcoder.jp/contests/abc185/tasks/abc185_d)
- [ ] [arc075_a](https://atcoder.jp/contests/arc075/tasks/arc075_a)
- [ ] [agc019_a](https://atcoder.jp/contests/agc019/tasks/agc019_a)
- [ ] [abc242_c](https://atcoder.jp/contests/abc242/tasks/abc242_c)
- [ ] [arc109_b](https://atcoder.jp/contests/arc109/tasks/arc109_b)
- [ ] [abc232_d](https://atcoder.jp/contests/abc232/tasks/abc232_d)
- [ ] [abc116_c](https://atcoder.jp/contests/abc116/tasks/abc116_c)
- [ ] [abc289_d](https://atcoder.jp/contests/abc289/tasks/abc289_d)
- [ ] [abc211_c](https://atcoder.jp/contests/abc211/tasks/abc211_c)
- [ ] [abc189_c](https://atcoder.jp/contests/abc189/tasks/abc189_c)
- [ ] [arc080_a](https://atcoder.jp/contests/arc080/tasks/arc080_a)
- [ ] [abc131_d](https://atcoder.jp/contests/abc131/tasks/abc131_d)
- [ ] [arc081_a](https://atcoder.jp/contests/arc081/tasks/arc081_a)
- [ ] [abc286_d](https://atcoder.jp/contests/abc286/tasks/abc286_d)
- [ ] [agc013_a](https://atcoder.jp/contests/agc013/tasks/agc013_a)
- [ ] [agc035_a](https://atcoder.jp/contests/agc035/tasks/agc035_a)
- [ ] [abc178_c](https://atcoder.jp/contests/abc178/tasks/abc178_c)
- [ ] [abc187_d](https://atcoder.jp/contests/abc187/tasks/abc187_d)
- [ ] [arc128_a](https://atcoder.jp/contests/arc128/tasks/arc128_a)
- [ ] [arc082_b](https://atcoder.jp/contests/arc082/tasks/arc082_b)
- [ ] [abc220_d](https://atcoder.jp/contests/abc220/tasks/abc220_d)
- [ ] [arc108_b](https://atcoder.jp/contests/arc108/tasks/arc108_b)
- [ ] [abc143_d](https://atcoder.jp/contests/abc143/tasks/abc143_d)
- [ ] [keyence2019_c](https://atcoder.jp/contests/keyence2019/tasks/keyence2019_c)
- [ ] [abc149_d](https://atcoder.jp/contests/abc149/tasks/abc149_d)
- [ ] [abc291_d](https://atcoder.jp/contests/abc291/tasks/abc291_d)
- [ ] [agc032_a](https://atcoder.jp/contests/agc032/tasks/agc032_a)
- [ ] [agc008_a](https://atcoder.jp/contests/agc008/tasks/agc008_a)
- [ ] [abc173_d](https://atcoder.jp/contests/abc173/tasks/abc173_d)
- [ ] [arc068_a](https://atcoder.jp/contests/arc068/tasks/arc068_a)
- [ ] [abc180_d](https://atcoder.jp/contests/abc180/tasks/abc180_d)
- [ ] [abc248_c](https://atcoder.jp/contests/abc248/tasks/abc248_c)
- [ ] [abc129_c](https://atcoder.jp/contests/abc129/tasks/abc129_c)


---

- [ ] [abc261_d](https://atcoder.jp/contests/abc261/tasks/abc261_d)
- [ ] [abc061_c](https://atcoder.jp/contests/abc061/tasks/abc061_c)
- [ ] [agc017_a](https://atcoder.jp/contests/agc017/tasks/agc017_a)
- [ ] [agc011_a](https://atcoder.jp/contests/agc011/tasks/agc011_a)
- [ ] [abc204_d](https://atcoder.jp/contests/abc204/tasks/abc204_d)
- [ ] [arc113_c](https://atcoder.jp/contests/arc113/tasks/arc113_c)
- [ ] [abc125_d](https://atcoder.jp/contests/abc125/tasks/abc125_d)
- [ ] [sumitb2019_d](https://atcoder.jp/contests/sumitrust2019/tasks/sumitb2019_d)
- [ ] [abc266_d](https://atcoder.jp/contests/abc266/tasks/abc266_d)
- [ ] [arc095_b](https://atcoder.jp/contests/arc095/tasks/arc095_b)
- [ ] [abc267_d](https://atcoder.jp/contests/abc267/tasks/abc267_d)
- [ ] [abc222_d](https://atcoder.jp/contests/abc222/tasks/abc222_d)
- [ ] [abc178_d](https://atcoder.jp/contests/abc178/tasks/abc178_d)
- [ ] [abc271_d](https://atcoder.jp/contests/abc271/tasks/abc271_d)
- [ ] [keyence2020_b](https://atcoder.jp/contests/keyence2020/tasks/keyence2020_b)
- [ ] [abc174_c](https://atcoder.jp/contests/abc174/tasks/abc174_c)
- [ ] [abc274_d](https://atcoder.jp/contests/abc274/tasks/abc274_d)
- [ ] [arc065_a](https://atcoder.jp/contests/arc065/tasks/arc065_a)
- [ ] [agc043_a](https://atcoder.jp/contests/agc043/tasks/agc043_a)
- [ ] [agc016_a](https://atcoder.jp/contests/agc016/tasks/agc016_a)
- [ ] [abc195_d](https://atcoder.jp/contests/abc195/tasks/abc195_d)
- [ ] [abc085_d](https://atcoder.jp/contests/abc085/tasks/abc085_d)
- [ ] [abc230_d](https://atcoder.jp/contests/abc230/tasks/abc230_d)
- [ ] [abc312_d](https://atcoder.jp/contests/abc312/tasks/abc312_d)
- [ ] [abc202_d](https://atcoder.jp/contests/abc202/tasks/abc202_d)
- [ ] [abc153_e](https://atcoder.jp/contests/abc153/tasks/abc153_e)
- [ ] [abc160_e](https://atcoder.jp/contests/abc160/tasks/abc160_e)
- [ ] [abc263_d](https://atcoder.jp/contests/abc263/tasks/abc263_d)
- [ ] [abc318_d](https://atcoder.jp/contests/abc318/tasks/abc318_d)
- [ ] [abc281_d](https://atcoder.jp/contests/abc281/tasks/abc281_d)
- [ ] [arc067_b](https://atcoder.jp/contests/arc067/tasks/arc067_b)
- [ ] [abc216_e](https://atcoder.jp/contests/abc216/tasks/abc216_e)
- [ ] [abc253_e](https://atcoder.jp/contests/abc253/tasks/abc253_e)
- [ ] [abc219_d](https://atcoder.jp/contests/abc219/tasks/abc219_d)
- [ ] [abc099_c](https://atcoder.jp/contests/abc099/tasks/abc099_c)
- [ ] [arc110_c](https://atcoder.jp/contests/arc110/tasks/arc110_c)
- [ ] [abc129_d](https://atcoder.jp/contests/abc129/tasks/abc129_d)
- [ ] [abc244_e](https://atcoder.jp/contests/abc244/tasks/abc244_e)
- [ ] [arc109_c](https://atcoder.jp/contests/arc109/tasks/arc109_c)
- [ ] [agc049_b](https://atcoder.jp/contests/agc049/tasks/agc049_b)
- [ ] [arc119_b](https://atcoder.jp/contests/arc119/tasks/arc119_b)
- [ ] [arc118_b](https://atcoder.jp/contests/arc118/tasks/arc118_b)
- [ ] [arc064_a](https://atcoder.jp/contests/arc064/tasks/arc064_a)
- [ ] [abc188_e](https://atcoder.jp/contests/abc188/tasks/abc188_e)

--- 

- [ ] [abc262_d](https://atcoder.jp/contests/abc262/tasks/abc262_d)
- [ ] [abc251_e](https://atcoder.jp/contests/abc251/tasks/abc251_e)
- [ ] [abc180_e](https://atcoder.jp/contests/abc180/tasks/abc180_e)
- [ ] [abc179_d](https://atcoder.jp/contests/abc179/tasks/abc179_d)
- [ ] [abc261_e](https://atcoder.jp/contests/abc261/tasks/abc261_e)
- [ ] [arc092_a](https://atcoder.jp/contests/arc092/tasks/arc092_a)
- [ ] [abc103_d](https://atcoder.jp/contests/abc103/tasks/abc103_d)
- [ ] [abc183_e](https://atcoder.jp/contests/abc183/tasks/abc183_e)
- [ ] [abc270_d](https://atcoder.jp/contests/abc270/tasks/abc270_d)
- [ ] [abc137_d](https://atcoder.jp/contests/abc137/tasks/abc137_d)
- [ ] [abc201_d](https://atcoder.jp/contests/abc201/tasks/abc201_d)
- [ ] [abc134_e](https://atcoder.jp/contests/abc134/tasks/abc134_e)
- [ ] [abc135_d](https://atcoder.jp/contests/abc135/tasks/abc135_d)

</details>

## 참고 자료

- [dp-book.com: Dynamic Programming for Computing Contests](https://dp-book.com/Dynamic_Programming.pdf)
- [youtube.com: Dynamic Programming lecture #1](https://www.youtube.com/watch?v=YBSt1jYwVfU&ab_channel=ErrichtoAlgorithms)
- [youtube.com: Dynamic Programming lecture #2](https://www.youtube.com/watch?v=1mtvm2ubHCY&ab_channel=ErrichtoAlgorithms)