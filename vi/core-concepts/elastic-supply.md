# Cung linh hoạt

**Cung linh hoạt. Giá ổn định.**

OUSD có cơ chế hoạt động khác với hầu hết các token khác. Thay vì giá tăng khi giá trị của tài sản được quản lý tăng (như với Compound cTokens hoặc Yearn yTokens), giá trị của một OUSD vẫn không đổi ở khoảng $1. Thay vào đó, các hợp đồng liên tục điều chỉnh nguồn cung tiền và tự động cập nhật số dư trong ví của người nắm giữ token để phản ánh lợi nhuận mà giao thức kiếm được.

{% hint style="info" %}
Hãy coi đó là tiền lãi tích lũy trong tài khoản ngân hàng của bạn. Đơn vị tài khoản và giá trị của đô la Mỹ không thay đổi. Bạn chỉ nhận được nhiều đô la Mỹ hơn theo thời gian khi bạn kiếm được tiền lãi.
{% endhint %}

![](../.gitbook/assets/ousd_docs_graphics_4.png)

Cơ chế này được lấy cảm hứng từ phương pháp mới được thực hiện bởi [Ampleforth](https://www.ampleforth.org/), nhưng có một số điểm khác biệt nổi bật như sau:

1. OUSD được hỗ trợ 100% bởi các stablecoin khác và sẽ không gặp phải thách thức tương tự khi phải duy trì tỷ giá cố định với đồng đô la. Với việc dễ dàng khai thác và hoàn trả OUSD, chúng tôi có thể tin tưởng vào những người kinh doanh dựa trên chênh lệch giá để đảm bảo tỷ giá được duy trì.
2. OUSD rebasing should only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Any decrease in your balance would be an indication of trouble in the system.
3. Không giống như Ampleforth - nguồn cung chỉ được điểu chỉnh 1 ngày 1 lần, nguồn cung tiền tệ của OUSD liên tục được cập nhật theo thời gian thực khi lợi tức được tạo ra.

