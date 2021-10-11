# Khoá thời gian (timelock)

{% hint style="danger" %}
Khoá thời gian hiện đã được áp dụng nhưng thời gian đang để là 1 phút. Tính năng này cho phép cộng đồng có quyền phản hồi nếu phát hiện ra bất kỳ vấn đề nghiêm trọng nào trong hợp đồng. Khoá thời gian được điều chỉnh bởi 5 trên tổng 8 chữ ký của Origin.
{% endhint %}

Hợp đồng timelock sẽ có hiệu lực trong khoảng 48 giờ trước khi các thay đổi trong hợp đồng OUSD được chính thức áp dụng. Khoá thời gian có thể được gọi bởi chúng tôi thông qua biểu biểu quyết chữ ký và là chủ sở hữu của [ERC-20](../architecture.md), [Vault](vault.md) và [Các chiến lược](strategies.md). Việc trì hoãn thời gian thực thi thay đổi hợp đồng thông minh cho phép người dùng có thời gian rút khỏi giao thức khi nhận thấy bất kỳ thay đổi đáng nghi ngờ nào của người sở hữu hoặc chỉ đơn giản là bạn không thích các thay đổi được đề xuất.

{% hint style="info" %}
Timelock là một biện pháp an toàn cho phép chủ sở hữu OUSD rút tiền nếu họ phản đối bất kỳ đề xuất nâng cấp nào đối với giao thức trong vòng 48 giờ kể từ thời điểm đề xuất.
{% endhint %}

OUSD đang sử dụng một phiên bản sửa đổi 1 vài chi tiết nhỏ của [Compound TimeLock](https://compound.finance/docs/governance) đã được [kiểm toán bởi OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). Hai điểm khác biệt đáng chú ý là:

1. OUSD will initially use a shorter wait period (48 hours) than Compound (72 hours) to allow for a faster response if any issues are discovered.
2. Một số quyết định, chẳng hạn như phân bổ lại tiền giữa các chiến lược hiện tại và khoá tiền gửi có thể được thực hiện ngay lập tức mà không cần chờ 48 giờ. Trường hợp này sẽ áp dụng khi có 1 lỗ hổng nghiêm trọng được phát hiện.



