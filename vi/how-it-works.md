# Cơ chế hoạt động

#### Được hỗ trợ 100% và ổn định

Origin Dollar (OUSD) là token Erc-20 được xây dựng trên mạng Ethereum.

OUSD là tiền tệ ổn định được hỗ trợ 1:1 bởi các stablecoin khác như USDT, USDC và DAI. Do đó, 1 OUSD được duy trì gần ổn định với giá trị 1 USD.

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

#### Kiếm lợi nhuận từ OUSD

Người dùng chuyển đổi stablecoin hiện có của họ \ (hiện đang hỗ trợ USDT, USDC và DAI \) sang OUSD thông qua DApp </a>chính thức

Origin Dollar. Ngay sau khi được chuyển đổi, OUSD sẽ tạo ra lợi nhuận ngay gộp ngay tức thì.</p> 

**Quy đổi OUSD sang stablecoin khác**

Người dùng có thể chuyển đổi OUSD của họ sang các stablecoin khác bất kỳ lúc nào bằng cách sử dụng DApp </a>Origin Dollar. A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the vault. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from syphoning stablecoins from the vault in the event of mispricings of of the underlying assets. Khoản phí nêu trên còn nhằm mục tiêu để khuyến khích những người nắm giữ dài hạn hơn những người đầu cơ ngắn hạn.</p> 

Sau thực hiện lệnh quy đổi, hợp đồng thông minh sẽ xác định loại stablecoin sẽ được trả lại cho người dùng. In the current implementation, the vault will return coins in the same ratio as the current holdings. This lack of user optionality also protects the vault as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}

Người dùng sẽ bị tính **0,5%** phí khi chuyển đổi từ OUSD sang stablecoins và sẽ không được lựa chọn stablecoin mà họ nhận được. 

{% endhint %}



#### Tạo ra **lợi nhuận thụ động**

OUSD tạo ra lợi nhuận bằng cách chuyển các stablecoin được ký gửi vào hợp đồng thông minh OUSD tới các giao thức DeFi khác như Compound, Aave, Uniswap, Balancer và Curve. It is expected there will be new diversified strategies added to the vault every month. Tiền lãi thu được, phí giao dịch và token phần thưởng được tổng hợp lại và chuyển đổi thành stablecoin để tạo ra lợi tức bằng OUSD. Theo thời gian, giao thức sẽ di chuyển tài sản vào và ra khỏi các nhóm thanh khoản khác nhau để mang lại lợi nhuận tốt nhất cho người nắm giữ OUSD. 



#### **Cung linh hoạt**

Lợi nhuận được tạo ra được chuyển cho người nắm giữ OUSD thông qua cơ chế cung tiền linh hoạt. OUSD liên tục điều chỉnh nguồn cung tiền để đáp ứng với lợi suất mà giao thức đã tạo ra. Điều này cho phép giá OUSD được cố định ở mức 1 đô la trong khi số dư trong ví của chủ sở hữu OUSD điều chỉnh theo thời gian thực để phản ánh lợi nhuận mà giao thức kiếm được.

Kết quả cuối cùng sẽ một stablecoin dễ chi tiêu, tự động kiếm được lợi nhuận vượt trội và được nhiều người mong muốn nắm giữ hơn các loại stablecoin hiện có.

