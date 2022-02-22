# Cấu trúc

![](../.gitbook/assets/ousd\_docs\_graphics\_3.png)

OUSD được tạo thành từ một loạt các hợp đồng thông minh. Mỗi hợp đồng này được bao bọc trong một hợp đồng ủy quyền có thể được nâng cấp thông qua các giao thức quản trị.

Xét về cơ chế bên trong, quyền sở hữu trong kho tiền được theo dõi bằng hệ thống tín dụng thể hiện phần trăm quyền sở hữu của kho tiền cho mỗi chủ sở hữu. Hợp đồng ERC-20 xử lý việc chuyển đổi sang USD khi dựa trên hoặc số tiền được chuyển giữa các ví.

[Vault](api/vault.md) chịu trách nhiệm khai thác và đốt OUSD. Nó cũng chịu trách nhiệm phân bổ tài sản tới từng [Chiến lược](../core-concepts/supported-strategies/) được hỗ trợ. To optimize gas costs, the vault may maintain a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.

The Flipper is a smart contract for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. Hợp đồng này được sử dụng như cách thay thế để định tuyến các giao dịch của người dùng bắt nguồn từ ứng dụng web. It's important to note that this contract may be empty on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Flipper uses around 45% less gas than Uniswap v3 due to its simplicity.

The Harvester contract collects reward tokens earned by the strategies, sells them, and sends the resulting stablecoins to the Dripper to be released to the vault. Anyone can call the harvest and earn 1% of the resulting USDT for doing so. This creates a self-incentivizing system that operates at a known fixed cost.

The Dripper contract buffers aproximately one week of reward token sales proceeds and makes it avaiable at a smooth rate to the vault. This keeps OUSD yield from being extremely spiky when harvests come in. The rate is recalculated at least once per day and is the rate that it would take to distribute the current dripper holdings out over a one week period.



