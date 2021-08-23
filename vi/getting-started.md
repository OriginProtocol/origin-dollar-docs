# Các bước cơ bản

Tài liệu này được xây dựng nhằm giải thích cách thức hoạt động của OUSD, cung cấp thông tin về lợi ích cũng như rủi ro tiềm ẩn đồng thời hướng dẫn cho các nhà phát triển muốn đóng góp cho mã nguồn mở của chúng tôi hoặc tích hợp OUSD vào các sản phẩm của họ. Dưới đây là một số thông tin bạn có thể tham khảo để bắt đầu.

**Mint và Redeem**

The OUSD Mint allows anyone to create or trade-in OUSD tokens using our [DApp](www.ousd.com) and a web-3 enabled cryptocurrency wallet like [Metamask](https://www.metamask.io). Đây là cách cơ bản để có được OUSD, đặc biệt hữu ích trong trường hợp bạn muốn hạn chế rủi ro di chuyển số lượng tiền lớn trên các sàn giao dịch.

**Mua trên trên sàn giao dịch**

Đối với giao dịch giá trị nhỏ, bạn nên mua OUSD trên các sàn giao dịch. Chúng tôi dự đoán rằng OUSD sẽ sớm được phổ biến rộng rãi trên các sàn giao dịch tập trung và phi tập trung khác.

Sàn giao dịch phi tập trung:

* [Buy OUSD on 1inch](https://app.1inch.io/#/1/swap/USDT/OUSD)
* [Buy OUSD on Curve](https://curve.fi/factory/9)
* [Buy OUSD on Uniswap v3](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Buy OUSD on Uniswap v2](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86&use=v2)
* [Buy OUSD on Sushiswap](https://exchange.sushiswapclassic.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

Sàn giao dịch tập trung:

* Mua OUSD trên KuCoin
  * [OUSD/USDT](https://trade.kucoin.com/OUSD-USDT)
  * [OUSD/BTC](https://trade.kucoin.com/OUSD-BTC)
* Mua OUSD trên Virgox
  * [OUSD/USDT](https://virgox.com/exchange/141)
* [Mua OUSD trên App Dharma App](https://www.dharma.io/) \(Chỉ dành cho người dùng ở Mỹ\)

**Thêm OUSD vào Ví của bạn**

{% hint style="success" %}
Địa chỉ ERC20 chính của Origin Dollar \ (OUSD \) là:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

Nếu OUSD không tự động hiển thị trên ví thì bạn có thể thêm theo cách thủ công thông qua địa chỉ ở trên. Nếu bạn đang có kế hoạch [giữ OUSD trong ví đa chữ ký](core-concepts/elastic-supply/rebasing-and-smart-contracts.md), hãy nhớ chọn opt-in để nhận được lợi nhuận. Chúng tôi muốn OUSD được hỗ trợ bởi nhiều ví hơn nữa và muốn OUSD được đưa vào tất cả danh sách của token nổi tiếng trong tương lai. Chúng tôi đánh giá rất cao bất kỳ sự giúp đỡ nào từ cộng đồng để biến mục tiêu trên thành hiện thực.

**Tích hợp OUSD**

OUSD là token ERC-20 không tiêu chuẩn, hầu hết các ứng dụng muốn hỗ trợ sử dụng OUSD sẽ cần phải thực hiện thao tác tích hợp. Đặc biệt, điều quan trọng là các nhà phát triển phải hiểu cách thức hoạt động của nguồn cung lịch hoạt bởi nó có thể gây nên một số hậu quả không mong muốn nếu không nắm rõ cơ chế.

Nếu bạn là nhà cung cấp ví hoặc sàn giao dịch tiền điện tử quan tâm đến việc hỗ trợ OUSD, vui lòng tham khảo các hướng dẫn sau:

{% page-ref page="core-concepts/elastic-supply/rebasing-and-smart-contracts.md" %}

{% page-ref page="smart-contracts/architecture.md" %}

{% page-ref page="smart-contracts/api/" %}

**Phân tích nhà phát triển**

Trang theo dõi dành cho nhà phát triển nội bộ [analytics.ousd.com](https://analytics.ousd.com). Bảng điều khiển hiển thị nguồn cung lưu hành hiện tại, tài sản được quản lý trong kho tiền và phân bổ giữa từng stablecoin và chiến lược.

**Yêu cầu hỗ trợ**

Vui lòng tham gia kênh Origin Dollar \ #engineering trên [Discord](www.originprotocol.com/discord) của Origin.  Đội ngũ của chúng tôi và các thành viên trong cộng đồng luôn sẵn sàng hỗ trợ bạn. Câu hỏi của bạn giúp sẽ giúp chúng tôi ngày càng hoàn thiện, vì vậy đừng ngần ngại cho chúng tôi biết thắc mắc của bạn nếu bạn không tìm thấy câu trả lời ở đây.

