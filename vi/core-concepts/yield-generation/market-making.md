# Tạo lập thị trường

**Sở hữu cổ phần của bạn trong các sàn giao dịch phi tập trung**

Các nhà tạo lập thị trường tự động (AMMs) đã nhanh chóng trở thành hình thức sàn trao đổi phi tập trung được ưa thích trên mạng Ethereum. Điều này một phần là do khó khăn trong việc hỗ trợ đặt lệnh giao dịch trên các DEX xây dựng trên Ethereum 1.0 vẫn có thể cạnh tranh được với trải nghiệm tức thời và trượt giá thấp trên các sàn giao dịch tập trung. Hơn nữa, các nhà tạo lập thị trường tự động như như Uniswap tương đối thân thiện với người dùng với mức phí gas khá thân thiện.

AMM chỉ có thể kích hoạt các thị trường mới khi những người cung cấp thanh khoản cung cấp thanh khoản (ví dụ: nhiều token sử dụng cho các bể hoặc cặp giao dịch nhất định). Đổi lại việc cung cấp thanh khoản, người cung cấp thanh khoản được thưởng phí giao dịch khi những người dùng khác khi họ swap token. For example, when traders swap two tokens on Uniswap v3, they are currently charged anywhere between 0.05% and 1% on top of the gas fees. These fees are distributed pro-rata to liquidity providers of the pair based on the percentage of total liquidity that they have provided.

{% hint style="info" %}
[Tổn thất vĩnh viễn](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) là một yếu tố rủi ro quan trọng được chú trọng, nhưng mối lo ngại này phần lớn được giảm bớt do OUSD chỉ cung cấp thanh khoản cho các stablecoin có giá trị tương đương.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens \(e.g. Curve rewards CRV tokens to liquidity providers\). Lợi tức sau đó được chuyển cho người nắm giữ OUSD.

Chúng tôi hiện tích hợp với trình tạo lập thị trường tự động sau:

{% page-ref page="../supported-strategies/curve.md" %}





