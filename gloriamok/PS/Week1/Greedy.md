# Greedy

# 그리디

## 관련 문제

- 동전 0 - [11047번: 동전 0 (acmicpc.net)](https://www.acmicpc.net/problem/11047)

### 해설

- **목표**
    - 목표 금액을 만들기 위해 필요한 동전 개수의 최솟값 구하기
- **해결**
    - 가장 큰 동전부터 시작하여, 목표 금액을 만들 수 있는 최대한의 동전 개수를 계산합니다.
    - **`sum`**을 현재 동전의 값으로 나눈 몫을 **`cnt`**에 더하고, **`sum`**을 현재 동전의 값으로 나눈 나머지로 업데이트합니다. 이 과정을 모든 동전에 대해 반복합니다.
- **예시**:
동전의 종류가 3개이고, 각각의 값이 1, 5, 10이며, 목표 금액이 28인 경우:
    - 10원 동전 2개 (20원)
    - 5원 동전 1개 (5원)
    - 1원 동전 3개 (3원)
    총 6개의 동전이 필요하므로, 결과는 **`6`**이 됩니다.

### 소스코드
```cpp
#include <iostream>
using namespace std;

int main() {
    int n, sum, money[10]{}, cnt = 0;
    cin >> n >> sum;
    for (int i = 0; i < n; i++) {
        cin >> money[i];
    }
    for (int i = n - 1; i >= 0; i--) {
        cnt += (sum / money[i]);
        sum %= money[i];
    }
    cout << cnt;
}
```