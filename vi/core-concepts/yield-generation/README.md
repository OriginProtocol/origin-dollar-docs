# Nguồn tạo lợi nhuận

**Canh tác năng suất tự động**

Bên cạnh sự bùng nổ của các nhóm tạo lập thị trường tự động và cho vay mới đã thúc đẩy tổng giá trị bị khóa (TVL), việc có quá nhiều bên cung cấp cùng 1 loại hình dịch vụ cũng khiến những người khai thác năng suất ngày càng gặp khó khăn trong việc phân bổ vốn một cách cách hiệu quả và tối ưu.

[Yearn](https://yearn.finance/) đã chứng minh rằng các hợp đồng thông minh có thể tự động hóa việc tái cân bằng quỹ theo nhiều chiến lược khác nhau để kiếm được lãi suất cho vay, phí tạo thị trường và token phần thưởng một cách tối ưu. Over time, new strategies will be deployed that maximize returns while minimizing risk and dependencies.

![](../../.gitbook/assets/ousd_docs_graphics_1.png)

OUSD uses the following high-level strategies for generating yield:

{% page-ref page="lending.md" %}

{% page-ref page="market-making.md" %}

{% page-ref page="rewards.md" %}

OUSD is able to generate higher yields than competing protocols due to a combination of important design decisions that amplify the rewards that are returned to OUSD holders:

* Exit fees are returned to the pool, rewarding long term holders
* Price oracles favor the collective over the individual, again rewarding long term holders
* Smart contracts must manually opt-in to earn yield. This allows the protocol to put more capital to work than would be otherwise possible.
* Smart strategies balance risk and reward more effectively than deploying capital in any single underlying strategy.

