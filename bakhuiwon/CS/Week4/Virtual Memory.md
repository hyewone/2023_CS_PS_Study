# 💻 Virtual Memory

실제 메모리보다 많아 보이게 하는 기술이다.

예를들어 )\
실제 물리적 메모리가 8GB지만, 더 많은 양을 가진 프로그램을 실행시킬 수 있느는거다!

HOW?? )\
프로세스 전체를 메모리에 로드시키지 않는다. 플세스의 일부만 메모리에 로드하고, 나머지는 디스크에 두고나서 필요할 때마다 교체하면쓰는 방식으로 구현된다.\
=> 현재 필요한 page만 메모리에 올려 놓는다!
=> demand paging

### 🎈Demand Paging
Demand Paging이란, 실제로 필요할 때 page를 메모리에 올려 놓는다.
이를 통해 `cpu 이용률과 처리율이 높아져` 더 많은 사용자(프로세스)를 수용할 수 있다.

demand paging은 page table에서 해당 page가 메모리에 있는지 없는지를 나타내는 `valid-invalid bit`를 사용한다.\

bit가 invalid면? 메모리에 없는 page 의미.
bit가 valid면? 메모리에 있는 page 의미.
=> 처음 모든 page는 invalid로 초기화되었고, 주소변환 시 bit가


### 🎈장점

### 🎈단점