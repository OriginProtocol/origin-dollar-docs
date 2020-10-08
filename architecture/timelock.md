# Khoá thời gian (timelock)

{% hint style="danger" %}
Thời gian sẽ sớm được thêm sau khi mọi chức năng được chứng minh là hoạt động tốt. Cho đến lúc đó, các hợp đồng sẽ được điều chỉnh bởi 5 trong 8 chữ ký (hình thức đa chữ ký) của Origin. Tính năng này cho phép cộng đồng có quyền phản hồi nếu phát hiện ra bất kỳ vấn đề nghiêm trọng nào trong hợp đồng.
{% endhint %}

Hợp đồng timelock sẽ có hiệu lực trong khoảng 48 giờ trước khi các thay đổi trong hợp đồng OUSD được chính thức áp dụng. Khoá thời gian có thể được gọi bởi chúng tôi thông qua biểu biểu quyết chữ ký và là chủ sở hữu của [ERC-20](erc-20.md), [Vault](vault.md) và [Các chiến lược](strategies.md). Việc trì hoãn thời gian thực thi thay đổi hợp đồng thông minh cho phép người dùng có thời gian rút khỏi giao thức khi nhận thấy bất kỳ thay đổi đáng nghi ngờ nào của người sở hữu hoặc chỉ đơn giản là bạn không thích các thay đổi được đề xuất.

{% hint style="info" %}
Timelock là một biện pháp an toàn cho phép chủ sở hữu OUSD rút tiền nếu họ phản đối bất kỳ đề xuất nâng cấp nào đối với giao thức trong vòng 48 giờ kể từ thời điểm đề xuất.
{% endhint %}

OUSD đang sử dụng một phiên bản sửa đổi 1 vài chi tiết nhỏ của [Compound TimeLock](https://compound.finance/docs/governance) đã được [kiểm toán bởi OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). 3 điểm khác biệt đáng chú ý là:

1. OUSD ban đầu sẽ sử dụng khoảng thời gian chờ ngắn hơn (48 giờ) so với Compound (72 giờ) cho phép phản hồi nhanh hơn nếu bất kỳ vấn đề nào được phát hiện.
2. Sau 48 giờ, bất kỳ ai cũng có thể tự do thực hiện gọi lệnh, không chỉ chủ sở hữu của hợp đồng.
3. Việc gửi tiền (không bao gồm rút tiền hay chuyển tiền) có thể bị đóng băng ngay lập tức mà không yêu cầu 48 giờ chờ đợi. Trường hợp này sẽ áp dụng khi có 1 lỗ hổng nghiêm trọng được phát hiện.





