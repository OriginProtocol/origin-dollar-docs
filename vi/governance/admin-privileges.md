# Đặc quyền của quản trị viên

Các hợp đồng thông minh OUSD được thiết kế để có thể nâng cấp chủ sở hữu. Nhóm Origin sử dụng hai hợp đồng ví đa chữ ký Gnosis khác nhau để thực hiện các thay đổi đối với giao thức. Ví đa chữ ký này đã được [kiểm toán bởi OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), đội ngũ Origin, và các bên thứ 3 khác. &#x20;

{% hint style="info" %}
Việc trì hoãn thời gian thực thi thay đổi hợp đồng thông minh cho phép người dùng có thời gian rút khỏi giao thức khi nhận thấy bất kỳ thay đổi đáng nghi ngờ nào của người sở hữu hoặc chỉ đơn giản là bạn không thích các thay đổi được đề xuất.
{% endhint %}

### Admin

Bất kỳ sự thay đổi về code của giao thức nào cũng cần có sự đồng ý của 5 trong tổng số 8 chữ ký hợp đồng. OUSD chỉ có thể được nâng cấp từ khi có sự đồng ý của 5 trên 8 ví đa chữ ký này. Điểm mấu chốt của hình thức đa chữ ký này là quyền quyết định sẽ không chỉ thuộc về sáng lập viên của Origin. In addition, the OUSD contracts are owned by a [timelock](../smart-contracts/api/timelock.md) which places a 48 hour time deplay before any changes to the protocol can be made.&#x20;

### Strategist

Some functionality, such as rebalancing funds between strategies or pausing deposits, can be triggered without the timelock and with far fewer signers. Điều này cho phép nhóm Origin phản ứng nhanh hơn với các điều kiện thị trường hoặc các mối đe dọa bảo mật. These signers, known as Strategists,  have the ability to execute a limited number of functions __ with only 2 of 9 signers.

The strategist multisig can take the following actions on the vault.

* reallocate
* setVaultBuffer
* setAssetDefaultStrategy
* withdrawAllFromStrategy
* withdrawAllFromStrategies
* pauseRebase
* pauseCapital
* unpauseCapital

### Future

Having these admin privileges is necessary in the early days to ensure that the protocol is secure and optimized for earning yields while minimizing risks. We expect to release multiple iterations of our smart contracts in the first several months of the protocol's existence.

Once several upgrade cycles have been completed, we intend to transfer ownership from our company control to a decentralized governance contract, thereby allowing the community to vote and participate in future protocol updates.
