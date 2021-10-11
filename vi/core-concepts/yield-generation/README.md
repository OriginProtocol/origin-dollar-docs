# Nguồn tạo lợi nhuận

**Canh tác năng suất tự động**

While the Cambrian explosion of new lending and automated market maker pools has fueled total value locked (TVL), it has also made it increasingly challenging for yield farmers to manually allocate capital in efficient and optimal ways.

[Yearn](https://yearn.finance) has demonstrated that smart contracts can automate the rebalancing of funds across various strategies to optimally earn lending interest, market-making fees, and rewards tokens. Theo thời gian, các chiến lược mới sẽ được triển khai nhằm tối đa hóa lợi nhuận, giảm thiểu rủi ro và tính phụ thuộc.

![Tìm kiếm lợi nhuận tự động trên giao thức OUSD](../../.gitbook/assets/ousd_earnings_graphic.png)

OUSD sử dụng các chiến lược cấp cao sau đây để tạo ra lợi nhuận:

{% content-ref url="lending.md" %}
[lending.md](lending.md)
{% endcontent-ref %}

{% content-ref url="market-making.md" %}
[market-making.md](market-making.md)
{% endcontent-ref %}

{% content-ref url="rewards.md" %}
[rewards.md](rewards.md)
{% endcontent-ref %}

OUSD is able to generate higher yields than competing protocols due to a combination of important design decisions that amplify the rewards that are returned to OUSD holders:

* Phí khi rút Ousd sẽ được gửi về pool như 1 phần thưởng cho cho những người nắm giữ lâu dài
* Oracle giá ưu tiên nhóm hơn cá nhân, một lần nữa thưởng cho những người nắm giữ lâu dài
* Hợp đồng thông minh phải chọn opt-in theo cách thủ công để kiếm được lợi nhuận. Điều này cho phép giao thức tạo ra nhiều lợi nhuận nhất có thể.
* Các chiến lược thông minh cân bằng rủi ro và lãi suất thay vì sử dụng các chiến lược 1 cách ngẫu nhiên.
