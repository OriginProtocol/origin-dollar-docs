# Các bước cơ bản

Tài liệu này được xây dựng nhằm giải thích cách thức hoạt động của OUSD, cung cấp thông tin về lợi ích cũng như rủi ro tiềm ẩn đồng thời hướng dẫn cho các nhà phát triển muốn đóng góp cho mã nguồn mở của chúng tôi hoặc tích hợp OUSD vào các sản phẩm của họ. Dưới đây là một số thông tin bạn có thể tham khảo để bắt đầu.

**Mua OUSD**

{% hint style="info" %}
</a>Origin Dollar

 sẽ định tuyến giao dịch của bạn một cách thông minh, giúp bạn mua OUSD với mức giá tốt nhất. </p> 

{% endhint %}

</a>Origin Dollar Dapp cho phép người dùng mua hoặc bán OUSD bằng ví tiền điện tử hỗ trợ web-3 như [Metamask](https://www.metamask.io), [Ledger](https://www.ledger.com/)hoặc [Gnosis Safe](https://gnosis-safe.io/). Đây là cách cơ bản để có được OUSD, đặc biệt là trong trường hợp bạn muốn hạn chế rủi ro di chuyển số lượng tiền lớn trên các sàn giao dịch. DApp sẽ tự động lựa chọn mua OUSD trong vault hoặc giúp bạn mua trên bất kỳ AMM nào hiện đang cung cấp tỷ giá tốt nhất.</p> 

**Sàn giao dịch phi tập trung**

OUSD hiện có sẵn trên các sàn giao dịch phi tập trung sau. Danh sách dưới đây chỉ nhằm mục đích tham khảo. Chúng tôi khuyên bạn nên sử dụng [Origin Dollar DApp](https://ousd.com/swap)  để nhận được mức tỉ giá tốt nhất.

* [Mua OUSD trên 1inch](https://app.1inch.io/#/1/swap/USDT/OUSD)
* [Mua OUSD trên Virgox](https://curve.fi/factory/9)
* [Mua OUSD trên Uniswap V3](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Mua OUSD trên Uniswap V2](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86&use=v2)
* [Mua OUSD trên Sushiswap](https://exchange.sushiswapclassic.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

**Sàn giao dịch tập trung**

OUSD hiện có sẵn trên các sàn giao dịch tập trung sau. Vui lòng kiểm tra yêu cầu cần thực hiện để nhận lãi từ OUSD của mỗi sàn trước khi dùng. Mỗi sàn sẽ yêu cầu các bước bổ sung khác nhau.

* Mua OUSD trên Virgox 
    * [OUSD/USDT](https://trade.kucoin.com/OUSD-USDT)
  * [OUSD/BTC](https://trade.kucoin.com/OUSD-BTC)
* Mua OUSD trên Virgox 
    * [OUSD/USDT](https://virgox.com/exchange/141)
* [Mua OUSD trên App Dharma](https://www.dharma.io/) (Chỉ dành cho người dùng ở Mỹ)

Chúng tôi đang tiếp tục nỗ lực để niêm yết OUSD trên các sàn giao dịch tập khác.

**Thêm OUSD vào Ví của bạn**

{% hint style="success" %}

Địa chỉ ERC20 chính của Origin Dollar (OUSD) là:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86** 

{% endhint %}

Nếu OUSD không tự động hiển thị trên ví thì bạn có thể thêm theo cách thủ công thông qua địa chỉ ở trên. Nếu bạn đang có kế hoạch [giữ OUSD trong ví đa chữ ký](core-concepts/elastic-supply/rebasing-and-smart-contracts.md), hãy nhớ chọn opt-in để nhận được lợi nhuận. Chúng tôi muốn OUSD được hỗ trợ bởi nhiều ví hơn nữa và muốn OUSD được đưa vào tất cả danh sách của token nổi tiếng trong tương lai. Chúng tôi đánh giá rất cao bất kỳ sự giúp đỡ nào từ cộng đồng để biến mục tiêu trên thành hiện thực. 

**Tích hợp OUSD**

OUSD là token ERC-20 không tiêu chuẩn, hầu hết các ứng dụng muốn hỗ trợ sử dụng OUSD sẽ cần phải thực hiện thao tác tích hợp. Đặc biệt, điều quan trọng là các nhà phát triển phải hiểu cách thức hoạt động của nguồn cung lịch hoạt bởi nó có thể gây nên một số hậu quả không mong muốn nếu không nắm rõ cơ chế.

Nếu bạn là bên cung cấp ví hoặc sàn giao dịch tiền điện tử quan tâm đến việc hỗ trợ OUSD, vui lòng tham khảo các hướng dẫn sau: 

{% page-ref page = "core-concept /astic-supply / rebasing-and-smart-contracts.md"%}

{% page-ref page = "smart-Contract / architecture.md"%}

{% page-ref page = "smart-contract / api /"%}

**Phân tích nhà phát triển**

Trang theo dõi dành cho nhà phát triển nội bộ [analytics.ousd.com](https://analytics.ousd.com). Bảng điều khiển hiển thị nguồn cung lưu hành hiện tại, tài sản được quản lý trong kho tiền và phân bổ giữa từng stablecoin và chiến lược.

**Yêu cầu hỗ trợ**

Vui lòng tham gia kênh Origin Dollar \ #engineering trên [Discord](www.originprotocol.com/discord) của Origin.  Đội ngũ của chúng tôi và các thành viên trong cộng đồng luôn sẵn sàng hỗ trợ bạn. Câu hỏi của bạn giúp sẽ giúp chúng tôi ngày càng hoàn thiện, vì vậy đừng ngần ngại cho chúng tôi biết thắc mắc của bạn nếu bạn không tìm thấy câu trả lời ở đây.

