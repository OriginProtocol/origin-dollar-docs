# Các bước cơ bản

Tài liệu này được xây dựng nhằm giải thích cách thức hoạt động của OUSD, cung cấp thông tin về lợi ích cũng như rủi ro tiềm ẩn đồng thời hướng dẫn cho các nhà phát triển muốn đóng góp cho mã nguồn mở của chúng tôi hoặc tích hợp OUSD vào các sản phẩm của họ. Dưới đây là một số thông tin bạn có thể tham khảo để bắt đầu.

**Mint và Redeem**

OUSD Mint cho phép bất kỳ ai cũng có thể tạo hoặc giao dịch OUSD bằng cách sử dụng [DApp](www.ousd.com) và ví tiền điện tử hỗ trợ web-3 như [Metamask](https://www.metamask.io). Đây là cách cơ bản để có được OUSD, đặc biệt hữu ích trong trường hợp bạn muốn hạn chế rủi ro di chuyển số lượng tiền lớn trên các sàn giao dịch.

**Mua trên trên sàn giao dịch**

Đối với số tiền nhỏ, cách dễ nhất để bắt đầu kiếm tiền với OUSD là mua OUSD trên các sàn giao dịch phi tập trung như Uniswap. Các cặp hiện đang có sẵn:

* [Mua OUSD trên Uniswap](https://app.uniswap.org/#/swap?outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Mua OUSD trên Mooniswap](https://mooniswap.exchange/#/swap?outputToken=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

Ngoài ra, chúng tôi dự đoán rằng OUSD sẽ sớm được phổ biến rộng rãi trên các sàn giao dịch tập trung và phi tập trung khác.

**Thêm OUSD vào Ví của bạn**

{% hint style="success" %}
Địa chỉ ERC20 chính của Origin Dollar \ (OUSD \) là:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

Nếu OUSD không tự động hiển thị trên ví thì bạn có thể thêm theo cách thủ công thông qua địa chỉ ở trên. Chúng tôi muốn OUSD được hỗ trợ bởi nhiều ví hơn nữa và muốn OUSD được đưa vào tất cả danh sách của token nổi tiếng trong tương lai. Chúng tôi đánh giá rất cao bất kỳ sự giúp đỡ nào từ cộng đồng để biến mục tiêu trên thành hiện thực.

**Tích hợp OUSD**

OUSD là token ERC-20 không tiêu chuẩn, hầu hết các ứng dụng muốn hỗ trợ sử dụng OUSD sẽ cần phải thực hiện thao tác tích hợp. Đặc biệt, điều quan trọng là các nhà phát triển phải hiểu cách thức hoạt động của nguồn cung lịch hoạt bởi nó có thể gây nên một số hậu quả không mong muốn nếu không nắm rõ cơ chế.

Nếu bạn là nhà cung cấp ví hoặc sàn giao dịch tiền điện tử quan tâm đến việc hỗ trợ OUSD, vui lòng tham khảo các hướng dẫn sau:

{% page-ref page="smart-contracts/architecture.md" %}

{% page-ref page="smart-contracts/api/" %}

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies.

**Getting Help**

Please join the Origin Dollar \#engineering room in Origin's [Discord](www.originprotocol.com/discord) server.  Our team and members of our community look forward to helping you build. Your questions help us improve, so please don't hesitate to ask if you can't find what you are looking for here.

