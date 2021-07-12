# Tạo lập thị trường

**Sở hữu cổ phần của bạn trong các sàn giao dịch phi tập trung**

Các nhà tạo lập thị trường tự động (AMMs) đã nhanh chóng trở thành hình thức sàn trao đổi phi tập trung được ưa thích trên mạng Ethereum. Điều này một phần là do khó khăn trong việc hỗ trợ đặt lệnh giao dịch trên các DEX xây dựng trên Ethereum 1.0 vẫn có thể cạnh tranh được với trải nghiệm tức thời và trượt giá thấp trên các sàn giao dịch tập trung. Hơn nữa, các nhà tạo lập thị trường tự động như như Uniswap tương đối thân thiện với người dùng với mức phí gas khá thân thiện.

AMM chỉ có thể kích hoạt các thị trường mới khi những người cung cấp thanh khoản cung cấp thanh khoản (ví dụ: nhiều token sử dụng cho các bể hoặc cặp giao dịch nhất định). Đổi lại việc cung cấp thanh khoản, người cung cấp thanh khoản được thưởng phí giao dịch khi những người dùng khác khi họ swap token. Ví dụ: khi các nhà giao dịch hoán đổi USDT lấy USDC trên Uniswap, họ hiện đang bị tính phí 0,3% trên phí gas. Các khoản phí này được phân phối theo tỷ lệ cho các nhà cung cấp thanh khoản trên cặp USDT-USDC dựa trên phần trăm tổng thanh khoản mà họ đã cung cấp.

{% hint style="info" %}
[Tổn thất vĩnh viễn](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) là một yếu tố rủi ro quan trọng được chú trọng, nhưng mối lo ngại này phần lớn được giảm bớt do OUSD chỉ cung cấp thanh khoản cho các stablecoin có giá trị tương đương.
{% endhint %}

Giao thức OUSD định tuyến USDT, USDC và DAI đến các nhóm thanh khoản hiệu suất cao được xác định bởi khối lượng giao dịch và token thưởng (ví dụ: Balancer thưởng token BAL cho người cung cấp thanh khoản). Lợi tức sau đó được chuyển cho người nắm giữ OUSD.

Chúng tôi hiện tích hợp với trình tạo lập thị trường tự động sau:

{% page-ref page="../supported-strategies/curve.md" %}

Chúng tôi dự kiến tích hợp với trình tạo lập thị trường tự động sau:

{% page-ref page="../supported-strategies/uniswap.md" %}

{% page-ref page="../supported-strategies/balancer.md" %}





