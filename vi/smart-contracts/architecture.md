# Cấu trúc

![](../.gitbook/assets/ousd_docs_graphics\_3.png)

OUSD được tạo thành từ một loạt các hợp đồng thông minh. Mỗi hợp đồng này được bao bọc trong một hợp đồng ủy quyền có thể được nâng cấp thông qua các giao thức quản trị.

Xét về cơ chế bên trong, quyền sở hữu trong kho tiền được theo dõi bằng hệ thống tín dụng thể hiện phần trăm quyền sở hữu của kho tiền cho mỗi chủ sở hữu. Hợp đồng ERC-20 xử lý việc chuyển đổi sang USD khi dựa trên hoặc số tiền được chuyển giữa các ví.

[Vault](api/vault.md) chịu trách nhiệm khai thác và đốt OUSD. Nó cũng chịu trách nhiệm phân bổ tài sản tới từng [Chiến lược](../core-concepts/supported-strategies/) được hỗ trợ. Để tối ưu hóa chi phí khí gas, vault tiền duy trì một bộ nhớ đệm để cho phép hầu hết các khoản tiền gửi và tiền hoàn lại diễn ra mà chuyển vào / chuyển ra khỏi các chiến lược.

OUSD Swap, hay còn gọi là "Flipper" là một hợp đồng thông minh do Origin cung cấp để người dùng swap giữa OUSD và DAI, USDC hoặc USDT với tỷ lệ 1: 1 cố định. Hợp đồng này được sử dụng như cách thay thế để định tuyến các giao dịch của người dùng bắt nguồn từ ứng dụng web. It's important to note that this contract may become bankrupt on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. Mặc dù bị giới hạn về chức năng, nhưng Origin Swap sử dụng ít gas hơn khoảng 45% so với Uniswap v3 nhờ tính đơn giản.

