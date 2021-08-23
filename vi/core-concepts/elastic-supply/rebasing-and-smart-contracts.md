# Rebasing & Hợp đồng thông minh

Nếu bạn đang sử dụng ví đa chữ ký hoặc hợp đồng thông minh khác muốn tham gia rebasing OUSD thì bạn phải gọi hàm`rebaseOptIn ()` OUSD. Điều này chỉ áp dụng với hợp đồng thông minh vì ví EOA tiêu chuẩn được đăng ký tự động.

{% hint style="info" %}
Ví nhiều đa chữ ký hoặc các hợp đồng thông minh khác phải gọi`rebaseOptIn ()`để kiếm được lợi nhuận.
{% endhint %}

Theo mặc định, OUSD được giữ trên các hợp đồng thông minh sẽ không nhận được lợi nhuận trừ khi hợp đồng thông minh được opts-in. Điều này làm tăng khả năng kết hợp của OUSD trong DeFi vì nhiều giao thức không được thiết kế để xử lý trường hợp số dư thay đổi. Đối với các giao thức DeFi khác, OUSD hoạt động giống như bất kỳ ERC-20 bình thường trừ khi bạn yêu cầu nó thay đổi. Đây là một thuộc tính đặc biệt hữu ích cho các dự án tạo lập thị trường tự động \ (AMM's \) như Uniswap.

Hợp đồng thông minh phải được opt-in để nhận được lợi nhuận thông qua cơ chế rebase. Điều này khắc phục sự cố mở rộng nguồn cung trên AMM trong khi cho phép ví đa chữ ký và các hợp đồng thông minh khác có cơ hội tham gia và kiếm được lợi nhuận.

{% hint style="warning" %}
Nếu bạn đang triển khai một hợp đồng và định gọi lệnh `rebaseOptIn ()`để kiếm lợi nhuận, bạn không thể gọi nó từ phương thức khởi tạo của hợp đồng. Hợp đồng phải được triển khai trước khi được gọi.
{% endhint %}

Nếu bạn đang sử dụng ví đa chữ ký như [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) hoặc [Gnosis Safe](https://gnosis-safe.io/), bạn sẽ cần địa chỉ hợp đồng ủy quyền [](../../smart-contracts/registry.md) [ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805) tương ứng. Sau khi thêm địa chỉ hợp đồng, bạn sẽ có thể gọi hàm `rebaseOptIn ()` để chọn tham gia kiếm lợi nhuận thông qua rebase hoặc`rebaseOptOut ()` để tắt tính năng này.




