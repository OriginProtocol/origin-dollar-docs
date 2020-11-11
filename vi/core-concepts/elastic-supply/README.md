# Cung linh hoạt

**Cung linh hoạt. Giá ổn định.**

OUSD có cơ chế hoạt động khác với hầu hết các token khác. Thay vì giá tăng khi giá trị của tài sản được quản lý tăng (như với Compound cTokens hoặc Yearn yTokens), giá trị của một OUSD vẫn không đổi ở khoảng $1. Thay vào đó, các hợp đồng liên tục điều chỉnh nguồn cung tiền và tự động cập nhật số dư trong ví của người nắm giữ token để phản ánh lợi nhuận mà giao thức kiếm được.

{% hint style="info" %}
Hãy coi đó là tiền lãi tích lũy trong tài khoản ngân hàng của bạn. Đơn vị tài khoản và giá trị của đô la Mỹ không thay đổi. Bạn chỉ nhận được nhiều đô la Mỹ hơn theo thời gian khi bạn kiếm được tiền lãi.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Cơ chế này được lấy cảm hứng từ phương pháp mới được thực hiện bởi [Ampleforth](https://www.ampleforth.org/), nhưng có một số điểm khác biệt nổi bật như sau:

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. Với việc dễ dàng khai thác và hoàn trả OUSD, chúng tôi có thể tin tưởng vào những người kinh doanh dựa trên chênh lệch giá để đảm bảo tỷ giá được duy trì.
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.

