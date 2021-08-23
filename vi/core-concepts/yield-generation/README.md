# Nguồn tạo lợi nhuận

**Canh tác năng suất tự động**

Bên cạnh sự bùng nổ của các nhóm tạo lập thị trường tự động và cho vay mới đã thúc đẩy tổng giá trị bị khóa (TVL), việc có quá nhiều bên cung cấp cùng 1 loại hình dịch vụ cũng khiến những người khai thác năng suất ngày càng gặp khó khăn trong việc phân bổ vốn một cách cách hiệu quả và tối ưu.

[Yearn](https://yearn.finance/) has demonstrated that smart contracts can automate the rebalancing of funds across various strategies to optimally earn lending interest, market-making fees, and rewards tokens. Theo thời gian, các chiến lược mới sẽ được triển khai nhằm tối đa hóa lợi nhuận, giảm thiểu rủi ro và tính phụ thuộc.

![Automated yield farming on the OUSD protocol](../../.gitbook/assets/ousd_earnings_graphic.png)

OUSD sử dụng các chiến lược cấp cao sau đây để tạo ra lợi nhuận:

{% page-ref page="lending.md" %}

{% page-ref page="market-making.md" %}

{% page-ref page="rewards.md" %}

OUSD có thể tạo ra lợi suất cao hơn so với các giao thức đối thủ nhờ 1 được thiết kế đặc biệt, giúp khuếch đại phần thưởng trả cho chủ sở hữu OUSD:

* Phí khi rút Ousd sẽ được gửi về pool như 1 phần thưởng cho cho những người nắm giữ lâu dài
* Oracle giá ưu tiên nhóm hơn cá nhân, một lần nữa thưởng cho những người nắm giữ lâu dài
* Hợp đồng thông minh phải chọn opt-in theo cách thủ công để kiếm được lợi nhuận. Điều này cho phép giao thức tạo ra nhiều lợi nhuận nhất có thể.
* Các chiến lược thông minh cân bằng rủi ro và lãi suất thay vì sử dụng các chiến lược 1 cách ngẫu nhiên.
