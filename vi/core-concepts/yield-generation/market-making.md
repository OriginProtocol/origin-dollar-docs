# Tạo lập thị trường

**Sở hữu cổ phần của bạn trong các sàn giao dịch phi tập trung**

Automated market makers (AMMs) have quickly risen as the preferred form of decentralized exchange on the Ethereum network. Điều này một phần là do khó khăn trong việc hỗ trợ đặt lệnh giao dịch trên các DEX xây dựng trên Ethereum 1.0 vẫn có thể cạnh tranh được với trải nghiệm tức thời và trượt giá thấp trên các sàn giao dịch tập trung. Hơn nữa, các nhà tạo lập thị trường tự động như như Uniswap tương đối thân thiện với người dùng với mức phí gas khá thân thiện.

AMMs can only enable new markets when liquidity providers supply liquidity (e.g. multiple tokens for given trading pairs or pools). Đổi lại việc cung cấp thanh khoản, người cung cấp thanh khoản được thưởng phí giao dịch khi những người dùng khác khi họ swap token. Ví dụ: khi các nhà giao dịch swap 2 token trên Uniswap v3, họ hiện đang bị tính phí từ 0,05% đến 1% ngoài phí gas. Các khoản phí này được phân phối theo tỷ lệ cho các nhà cung cấp thanh khoản dựa trên phần trăm tổng thanh khoản mà họ đã cung cấp.

{% hint style="info" %}
[Tổn thất vĩnh viễn](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) là một yếu tố rủi ro quan trọng được chú trọng, nhưng mối lo ngại này phần lớn được giảm bớt do OUSD chỉ cung cấp thanh khoản cho các stablecoin có giá trị tương đương.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens (e.g. Curve rewards CRV tokens to liquidity providers). Lợi tức sau đó được chuyển cho người nắm giữ OUSD.

Chúng tôi hiện tích hợp với trình tạo lập thị trường tự động sau:

{% content-ref url="../supported-strategies/curve.md" %}
[curve.md](../supported-strategies/curve.md)
{% endcontent-ref %}



