# Hướng dẫn tích hợp cho các sàn giao dịch

Các sàn giao dịch tập trung sẽ đóng một vai trò quan trọng trong việc giúp chúng tôi đạt đươc mục tiêu mang OUSD tới gần hơn với người dùng. Chúng tôi sẵn sàng hỗ trợ các sàn muốn tích hợp OUSD. Chúng tôi tin rằng OUSD sẽ là lựa chọn tuyệt vời nếu các sàn giao dịch đang tìm kiếm 1 stablecoin mang lại lợi nhuận cao.

Những tài liệu này là bước quan trọng để tìm hiểu cơ chế hoạt động của OUSD. Dưới đây là một số câu hỏi quan trọng cho các sàn giao dịch muốn tích hợp OUSD cần xem xét:

**Bạn có muốn tham gia kiếm lợi nhuận không?**

Chúng tôi giả định câu trả lời sẽ là có! Tuy nhiên, nếu chỉ đơn giản là. niêm yết OUSD mà không [tích hợp rebase](../core-concepts/elastic-supply/rebasing-and-smart-contracts.md) thì bạn sẽ không đạt được mục đích mong muốn. Đối với các sàn giao dịch muốn niêm yết OUSD, nhưng bị hạn chế về kỹ thuật, bạn có thể muốn khởi chạy phiên bản không rebase trước và sau đó các kỹ sư có thể thực hiện tiếp các bước tích hợp rebase. Để dừng tính năng rebase của OUSD, bạn có thể gọi `rebaseOptOut ()` từ mỗi ví EOA nắm giữ OUSD hoặc không làm gì nếu bạn đang lưu trữ OUSD trên các hợp đồng thông minh. OUSD sau khi tạm dừng rebase hoạt động giống như token ERC-20 bình thường.

**Are you storing customer balances on smart contracts (ie. multi-sigs) or EOA wallets?**

Bất kỳ hợp đồng thông minh nào đang nắm giữ OUSD cần phải opt-in hủ công để nhận được lợi nhuận bằng cách gọi hàm `rebaseOptIn ()`. Sở dĩ bạn phải thực hiện bước này vì bản chất [cung thay đổi](../core-concepts/elastic-supply/) và [tính năng rebase](../core-concepts/elastic-supply/rebasing-and-smart-contracts.md). Nếu sàn giao dịch của bạn đang lưu trữ tiền trong ví đa chữ ký, đừng quên thực hiện opt-in để kiếm lợi nhuận.

**Bạn có đang lưu số dư của người dùng vào bộ nhớ đệm không?**

OUSD tự động cập nhật giá trị được trả về bởi hàm `balanceOf ()` trên hợp đồng ERC20 mà đội ngũ chúng tôi xây dựng. Số dư của người dùng sẽ cập nhật ngẫu nhiên trong ngày khi giao thức tạo ra lợi nhuận mới. Miễn là bạn không lưu giá trị này vào bộ nhớ đệm, người dùng sẽ luôn thấy đúng số lượng OUSD mà họ đang nắm giữ.

**Bạn có đang trộn lẫn quỹ của người dùng không?**

Nếu bạn đang trộn lẫn quỹ của người dùng, bạn cần đảm bảo rằng họ nhận được lãi suất tương ứng tạo ra bởi giao thức. Có lẽ cách dễ nhất để làm điều này là theo dõi số dư của mỗi người dùng dưới dạng tỷ lệ phần trăm trên tổng tài khoản thay vì theo dõi qua số tiền cố định.

**Kế hoạch thanh khoản của bạn là gì?**

OUSD có thể được mint hoặc redeem bất kỳ lúc nào bằng cách sử dụng [Origin Dollar DApp](https://www.ousd.com)hoặc thực hiện trực tiếp từ các hợp đồng thông minh của Origin. Nếu bạn đang có kế hoạch tự cung cấp thanh khoản, bạn nên lưu ý rằng số lượng OUSD chính xác mà bạn sẽ nhận được để đổi lấy USDT, USDC hoặc DAI của bạn phụ thuộc vào tỷ giá hối đoái hiện tại được xác định bởi [oracles](../smart-contracts/api/oracle.md). Nếu bạn đang có kế hoạch đổi OUSD để lấy các stablecoin cơ bản, lưu ý rằng giao thức sẽ thu 1 khoản phí là 0.5% và sẽ trả về hỗn hợp tác stablecoin đang có trong pool. Chúng tôi khuyến khích các sàn giao dịch chuyển đổi qua các nền tảng khác như Uniswap hoặc Curve để tránh các khoản fee nêu trên. Nếu có thể, bạn nên thực hiện mint hoặc redeem số lượng lớn để tối thiểu hoá chi phí. 

