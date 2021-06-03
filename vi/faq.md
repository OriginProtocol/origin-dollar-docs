# Câu hỏi thường gặp

**Tôi có thể mua OUSD ở đâu?**

Ghé thăm [làm thế nào để bắt đầu](https://docs.ousd.com/getting-started) để tham khảo các lựa chọn.

**Chi phí để mint và redeem OUSD là bao nhiêu?**

Tương tự với các giao dịch trên Ethereum, người dùng sẽ cần Ether để tương tác với hợp đồng thông minh OUSD. Chúng tôi đã thực hiện các biện pháp tối ưu phí gas, nhưng các chi phí này có thể thay đổi tuỳ theo mạng Ethereum.

Bất cứ khi nào bạn mint hoặc redeem OUSD, sẽ có 1 tỉ giá hối đoái được áp dụng giữa OUSD và các stablecoin được nạp vào hoặc rút ra. Đọc thêm tại [Price Oracles](https://docs.ousd.com/core-concepts/price-oracles).

Để khuyến khích người dùng nắm giữ OUSD lâu dài và để bảo vệ giao thức khỏi các đợt tấn công, người dùng redeem OUSD sẽ chịu 1 khoản phí 0,5%. Đọc thêm tại [Cách thức hoạt động](https://docs.ousd.com/how-it-works).

**Số dư của tôi sẽ bắt đầu tăng từ lúc nào kể từ khi bắt đầu nắm giữ OUSD?**

Số lượng OUSD trong ví của bạn sẽ tăng lên sau mỗi đợt rebase. Đọc thêm tại [Elastic supply](https://docs.ousd.com/core-concepts/elastic-supply). OUSD hiện đang được rebase nhiều lần trong ngày.

**Why does OUSD not grow when it's held in Uniswap, SushiSwap, etc?**

By default, rebase events don't affect the supply of OUSD that is sitting in smart contracts. These contracts can opt in to receiving additional OUSD if they are capable of handling elastic supply tokens. You can read more about this in [Rebasing & Smart Contracts](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

**How is it possible for the APY to be so high?**

You can read about our various strategies in [Yield Generation](https://docs.ousd.com/core-concepts/yield-generation). We currently get most of the yield from harvesting rewards tokens \(namely COMP and CRV\). Additionally, the yield increases as more OUSD is held in smart contracts that do not opt into rebasing since the underlying collateral continues to earn for the average OUSD holder.

**Why is my balance increasing at a slower rate than the advertised APY?**

OUSD balances increase when the supply is rebased. But the size of each rebase varies wildly depending on how much the vault has earned since the last rebase. And while most rebases collect a small amount earnings from lending strategies, other rebases involve liquidating rewards tokens or collecting fees. As a result, the yield will vary significantly during short time periods.

**What about the hack? Is OUSD safe?**

On November 7th 2020, OUSD was exploited for 7M USD due to a previously undetected reentrancy bug. You can read more [details about the hack](https://medium.com/originprotocol/urgent-ousd-has-hacked-and-there-has-been-a-loss-of-funds-7b8c4a7d534c) on our blog as well as the [detailed compensation plan](https://medium.com/originprotocol/origin-dollar-ousd-detailed-compensation-plan-faa73f87442e) for taking care of the affected users. Origin Dollar was relaunched in December after completing multiple audits and security upgrades. You can learn more about the steps taken to secure the protocol in our [relaunch announcement](https://medium.com/originprotocol/origin-dollar-ousd-is-back-b8ee0c601dad).

