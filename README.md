# SampleSmartContract
smart contract sample

very simple scenario

---------------------------

1. sendPointCustomerTotal을 이용하여 간단한 payment system을 구현함

smart contract의 핵심은 블럭체인 내부에서 모든 로직이 동작해야 한다는 점이다.
DB와 같은 lock scheme을 제공하지 않으므로 외부 프로그램에서 값을 읽게 되면 이는 블럭체인 동작에서 아무것도 보장하지 않는다.
수행 순서나 block 생성 등의 이슈로 인하여 외부 조회는 충분한 시간을 두고 진행해야 한다.(블럭 생성 주기 정도 권장)

스마트 컨트랙트의 특징은

1. 내부에서 강제로 state를 변화할 수 있다.
2. Deterministic 동작을 보장한다. (모든 노드에서 동일)
3. 수행 순서를 보장하지 않는다.
- DB유저로 생각해보면 모든 로직을 PSM으로 구현한 후 외부에서 Call만 수행하는 것과 같다.
- 이 경우 call의 순서는 네트워크 등의 문제로 실제 수행자의 순서와 동일하지 않다.
- 블럭체인도 유저의 수행 순서와 블럭에서의 수행 순서를 맞춰주지 않는다.

----------------------------
수행 방법
1. coinstack설치 (node.ini 활용), 또는 src에서 testcoin으로 변경
2. 특정 address에 coin충전(수수료)
3. ./install.sh
4. ./run.sh

----------------------------
가상 환경 수행 방법
1. ./test.sh

