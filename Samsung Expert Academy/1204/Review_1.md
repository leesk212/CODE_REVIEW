# Code

```cpp
#include <iostream>
#include <vector>
#include <algorithm>
#include <cmath>
#include <string>
using namespace std;
 
int main() {
    ios_base::sync_with_stdio(false);
    cin.tie(0);
    cout.tie(0);
    int T;  //Testcase 갯수 받기
    cin >> T; //Testcase 입력 받기
    for (int testcase = 1; testcase <= T; testcase++) { //Testcase 가 몇개 들어올지 모르니까, 전체 iteration 돌수 있게 수행
        int arr[101] = { 0 }; // 각 학생의 점수가 0~100점 내 이니까, 커버가 가능하도록 수행
        int a;
        cin >> a; //현재 Testcase number 입력받기
        for (int i = 0; i < 1000; i++) { 
            int b;
            cin >> b;
            arr[b]++;
        }
        int max = 0;
        int ans = 0;
        for (int i = 0; i < 101; i++) { //가장 갯수가 많은 것 찾기
            if (arr[i] >= max) {
                ans = i;
                max = arr[i];
            }
        }
        cout << "#" << testcase << " " << ans << "\n";
    }
     
    return 0;
}
```
# Review
* 0점부터 100점까지를 Array로 두어서, 그 점수 별 갯수를 판별
* 전체 갯수를 sort하고, 다시 확인하는 식은 메모리 낭비


