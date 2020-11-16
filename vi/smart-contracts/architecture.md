# Cấu trúc

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD được tạo thành từ một loạt các hợp đồng thông minh. Mỗi hợp đồng này được bao bọc trong một hợp đồng ủy quyền có thể được nâng cấp thông qua các giao thức quản trị.

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. Hợp đồng ERC-20 xử lý việc chuyển đổi sang USD khi dựa trên hoặc số tiền được chuyển giữa các ví.

[Vault](api/vault.md) chịu trách nhiệm khai thác và đốt OUSD. Nó cũng chịu trách nhiệm phân bổ tài sản tới từng [Chiến lược](../core-concepts/supported-strategies/) được hỗ trợ. Để tối ưu hóa chi phí khí gas, vault tiền duy trì một bộ nhớ đệm để cho phép hầu hết các khoản tiền gửi và tiền hoàn lại diễn ra mà chuyển vào / chuyển ra khỏi các chiến lược.



