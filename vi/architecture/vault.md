# Vault

Vault là điểm cốt lõi của giao thức. Kho tiền chịu trách nhiệm khai tác / hoàn trả OUSD, cân bằng lại quỹ giữa các chiến lược được hỗ trợ khác nhau và thanh lý token thưởng.

Các chức năng quan trọng nhất trên Vault là:

* `mint ()`cho phép chuyển đổi một stablecoin được hỗ trợ sang OUSD
* `mintMultiple ()`cho phép chuyển đổi nhiều stablecoin được hỗ trợ sang OUSD trong một lần gọi lệnh
* `Reds ()`cho phép đổi một lượng OUSD cụ thể cho các loại stablecoin được hỗ trợ khác.
* `RedAll ()`cho phép người dùng đổi toàn bộ số dư OUSD của họ để lấy các loại stablecoin được hỗ trợ khác. Điều này đặc biệt hữu ích vì số dư của người dùng không ngừng tăng lên khi lợi nhuận được tích lũy.
* `rebase ()`cập nhật số dư cho tất cả người dùng dựa trên giá trị của tài sản hiện được lưu trữ trong nhóm.
* `phân bổ ()`chuyển các tài sản đang quản lý vào [ chiến lược](strategies.md) chỉ định của chúng để tối đa hóa lợi suất và đa dạng hóa rủi ro.

Khi hoàn lại tiền, chính giao thức sẽ quyết định stablecoin nào sẽ được trả lại cho người dùng. Việc lựa chọn đồng coin nào sẽ được trả sẽ dựa trên tỷ lệ nội bộ của tài sản đang được giữ trong bể.



