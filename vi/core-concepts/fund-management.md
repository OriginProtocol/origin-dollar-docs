# Quản lý quỹ

Hợp đồng thông minh OUSD tổng hợp tất cả các khoản stablecoin của người dùng vào pool tài sản đầu tư. Funds are then allocated across one or more** **earning strategies at any given moment in time. Vault tìm kiếm các chiến lược năng suất cao nhưng cũng tìm cách duy trì sự đa dạng hóa trên nhiều chiến lược. Đa dạng hóa giúp loại bỏ lỗi cục bộ và giảm thiểu rủi ro.

Khác với Yearn Vaults, TokenSets hoặc Zapper, người dùng không cần lựa chọn các chiến lược đơn lẻ. Tất cả các stablecoin đã ký gửi và do đó, tất cả các token OUSD đều là token có thể thay thế được. Sau khi chương tính năng quản trị ra mắt, những quyết định này sẽ được đề xuất bởi người nắm giữ token quản trị mạng OUSD. Chủ sở hữu OGN được khuyến khích tham gia tạo và bỏ phiếu các đề xuất cho giao thức trong [cổng quản trị OGN](https://vote.originprotocol.com).

**Chiến lược tạo lợi nhuận**

Các chiến lược kiếm sẽ chuyển vốn tới nhiều nền tảng DeFi khác nhau. Vault sẽ xác định chiến lược nào đang hoạt động và ước tính lợi nhuận thu về của nguồn vốn gửi đi. Các chiến lược này sẽ được nâng cấp và cải tiến theo thời gian.

**Chiến lược**

Phiên bản ban đầu của hợp đồng thông minh OUSD Vault cung cấp cho mỗi chiến lược hợp lệ một trọng số đơn giản từ 0% đến 100% để thực hiện phân bổ tài sản đơn giản. Các trọng số này sẽ được thay đổi thường xuyên thông qua các bản cập nhật của Origin trong ngắn hạn và dài hạn sẽ theo cơ chế quản trị phi tập trung.

**Đa dạng hóa**

Đa dạng hóa trên nhiều [nền tảng](supported-strategies/) DeFi sẽ làm giảm rủi ro cho hợp đồng thông minh và các rủi ro hệ thống khác. Hợp đồng thông minh sẽ tính toán các APY hiện tại và dự kiến nhằm nỗ lực mang lại lợi nhuận cạnh tranh cho người nắm giữ OUSD. Theo thời gian, hợp đồng Vault sẽ được nâng cấp để chuyển đổi một cách thông minh và tự động giữa các chiến lược mà không cần bất kỳ sự can thiệp thủ công nào. Ví dụ: Vault sẽ tự động luân chuyển vốn giữa các chiến lược cho vay khác nhau để tối ưu hóa lợi tức.

Tuy nhiên, chúng tôi vẫn kỳ vọng rằng các thông số rủi ro hoặc quyết định về việc liệu các chiến lược nhất định có nên được đưa vào hay không sẽ sẽ được thực hiện thông qua cơ chế phiếu bầu quản trị. 
