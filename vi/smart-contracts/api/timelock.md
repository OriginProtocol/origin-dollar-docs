# Khoá thời gian (timelock)

{% hint style="danger" %}
The timelock has been added but is currently set to 1 minute. This allows for a faster response if any critical issues are discovered. The timelock is governed by Origin's 5 of 8 multi-sig.
{% endhint %}

Hợp đồng timelock sẽ có hiệu lực trong khoảng 48 giờ trước khi các thay đổi trong hợp đồng OUSD được chính thức áp dụng. Khoá thời gian có thể được gọi bởi chúng tôi thông qua biểu biểu quyết chữ ký và là chủ sở hữu của [ERC-20](../architecture.md), [Vault](vault.md) và [Các chiến lược](strategies.md). Việc trì hoãn thời gian thực thi thay đổi hợp đồng thông minh cho phép người dùng có thời gian rút khỏi giao thức khi nhận thấy bất kỳ thay đổi đáng nghi ngờ nào của người sở hữu hoặc chỉ đơn giản là bạn không thích các thay đổi được đề xuất.

{% hint style="info" %}
Timelock là một biện pháp an toàn cho phép chủ sở hữu OUSD rút tiền nếu họ phản đối bất kỳ đề xuất nâng cấp nào đối với giao thức trong vòng 48 giờ kể từ thời điểm đề xuất.
{% endhint %}

OUSD đang sử dụng một phiên bản sửa đổi 1 vài chi tiết nhỏ của [Compound TimeLock](https://compound.finance/docs/governance) đã được [kiểm toán bởi OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The two notable differences are:

1. OUSD ban đầu sẽ sử dụng khoảng thời gian chờ ngắn hơn (48 giờ) so với Compound (72 giờ) cho phép phản hồi nhanh hơn nếu bất kỳ vấn đề nào được phát hiện.
2. Some actions, such a reallocating funds between existing strategies and freezing deposits can be called immediately without requiring the 48 waiting period. This is in case a major vulnerability is discovered.





