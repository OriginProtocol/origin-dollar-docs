# Cung linh hoạt

**Cung linh hoạt. Giá ổn định.**

OUSD có cơ chế hoạt động khác với hầu hết các token khác. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Instead, the contracts constantly adjust the monetary supply and automatically updates the balance in every token holder’s wallet to reflect the yield that has been earned by the protocol.&#x20;

{% hint style="info" %}
Hãy coi đó là tiền lãi tích lũy trong tài khoản ngân hàng của bạn. Đơn vị tài khoản và giá trị của đô la Mỹ không thay đổi. Bạn chỉ nhận được nhiều đô la Mỹ hơn theo thời gian khi bạn kiếm được tiền lãi.
{% endhint %}

![](../../.gitbook/assets/ousd\_docs\_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD được hỗ trợ 100% bởi các stablecoin khác và không gặp phải thách thức tương tự khi phải duy trì tỷ giá cố định với đồng đô la. Given the ease of minting and redeeming OUSD, we can count on arbitrageurs to ensure the peg is maintained.&#x20;
2. Số lượng OUSD sẽ luốn tăng lên vì số lượng OUSD được mint gắn liền với lợi nhuận thực tế thu được từ các chiến lược. Tiền gốc của bạn được bảo vệ miễn là không có vấn đề gì xảy ra với các giao thức cho vay / AMM và stablecoin cơ bản. Số dư OUSD của bạn sẽ không bao giờ giảm, nhưng giá trị có thể giảm nếu hệ thống xảy ra lỗi.
3. Unlike Ampleforth, which only rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebase được kích hoạt thường xuyên khi người dùng tương tác với các hợp đồng OUSD. Chainlink Keepers ensure at least one rebase occurs every day.

**Kích hoạt rebase thủ công**

Bất kỳ ai cũng có thể kích hoạt rebase tại bất kỳ thời điểm nào bằng cách [gọi hàm rebase trên vault](https://etherscan.io/address/originvault.eth#writeProxyContract). Bạn có thể thực hiện việc này trên Etherscan bằng cách kết nối ví web3.
