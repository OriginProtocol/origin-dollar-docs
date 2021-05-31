# Đóng góp

**100% Mã nguồn mở**

OUSD là dự án mã nguồn mở hoàn toàn và chúng tôi hoan nghênh mọi đóng góp của toàn thể cộng đồng. Bạn có thể hỗ trợ đội ngũ chúng tôi bằng việc báo cáo sự cố bảo mật, đóng góp lập trình hay giúp chúng tôi cải thiện cộng đồng của mình.

Chúng tôi làm việc một cách công khai và tài khoản Discord luôn chào đón tất cả cá thành viên trong cộng đồng. Nếu bạn có câu hỏi hoặc cần trợ giúp, [các kênh Discord OUSD](https://discord.gg/jyxpUSe) là nơi tốt nhất để nhận hỗ trợ từ nhóm và cộng đồng của chúng tôi.

**Phân tích nhà phát triển**

Trang theo dõi dành cho nhà phát triển nội bộ [analytics.ousd.com](https://analytics.ousd.com). Bảng điều khiển hiển thị nguồn cung lưu hành hiện tại, tài sản được quản lý trong kho tiền và phân bổ giữa từng stablecoin và chiến lược.

#### Quá trình phát triển

Chiến lược phân nhánh của chúng tôi tương tự như [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), nhưng chúng tôi thực hiện tất cả quá trình phát triển của mình trong nhánh `chính` và có nhánh `ổn định` cho các mã lập trình đã được phát hành.

Bạn có thể tham khảo các bước sau nếu muốn đóng góp cho Origin:

1. Tìm một vấn đề thú vị và trao đổi với chúng tôi! Vui lòng ghé kênh `#engineering` [Discord](https://discord.gg/jyxpUSe) và cho chúng tôi biết bạn muốn làm gì.
2. Nhắn tin cho [thành viên của team](https://github.com/orgs/OriginProtocol/teams/core/members) trên Discord và yêu cầu được thêm vào nhóm [cộng tác viên](https://github.com/orgs/OriginProtocol/teams/contributors) của chúng tôi. Nếu không, bạn sẽ cần phải folk kho giữ liệu code (repo) liên quan và đẩy các nhánh tính năng vào folk riêng của bạn.
3. Thêm nhận xét về vấn đề hoặc tự phân bổ cho bản thân tránh tình trạng nhiều cộng tác viên cùng xử lý 1 nhiệm vụ.
4. Bắt đầu với nhánh `chính` và kiểm tra nhánh tính năng mới trừ khi bạn đang đóng góp vào một tính năng hiện có.
5. Viết code.
6. Kéo các cam kết mới nhất từ `nhánh chính` và xác nhận rằng mã lập trình của bạn hoạt động tốt với với bất kỳ công việc nào đã được tích hợp kể từ khi bạn bắt đầu.
7. Đẩy chi nhánh của bạn lên kho lưu trữ ngược dòng (tức là https: //github.com/OriginProtocol/ [repo]) để những người đóng góp khác có thể dễ dàng xử lý nó nếu cần.
8. Vui lòng yêu cầu đánh giá trong bài PR bằng cách nhấp vào biểu tượng bánh răng bên cạnh “Người đánh giá” ở cột bên phải.

Để hợp nhất code hợp đồng thông minh quan trọng, nó phải vượt qua danh sách tiêu chí sau:

*  Code được kiểm tra bởi 2 người đánh giá
*  Vươt qua bài kiểm tra unit
*  Vượt qua Slither không bị cảnh báo
*  Vượt qua kiểm tra Echidna

Nhánh `chính` bị khóa để chỉ các [ thành viên chính ](https://github.com/orgs/OriginProtocol/teams/core) của team có thể hợp nhất các yêu cầu kéo của bạn. Kéo các yêu cầu được đã được xem trước bởi những người đóng góp tin cậy khác sẽ nhanh và được hợp nhất nhanh hơn! Kiểm tra kênh `#engineering` trên Discord để tìm kiếm những người đánh giá thích hợp.

#### Kiểu lập trình

Chúng tôi sử dụng nhiều ngôn ngữ lập trình khác nhau trong kho lập trình. Khi đóng góp, vui lòng tuân theo các quy ước lập trình hiện có và tham khảo tệp CONTRIBUTING.md trong kho lưu trữ, nếu có.

Đối với JavaScript, chúng tôi sử dụng kiểu [NPM](https://docs.npmjs.com/misc/coding-style), được thực thi tự động thông qua [prettier](https://prettier.io/).

Đối với Solidity, chúng tôi sử dụng thụt lề hai dấu cách.

#### Thiết kế giao thức

Khi xem xét đề xuất giao thức hoặc thiết kế triển khai, chúng tôi đang tìm kiếm:

* Mô tả vấn đề mà bản đề xuất này sẽ giải quyết
* Thảo luận về những đánh đổi liên quan
* Xem xét các giải pháp hiện có khác
* Link đến tài liệu có liên quan (RFC, bài báo, v. v.)
* Thảo luận về giải pháp đề xuất

Xin lưu ý rằng thiết kế giao thức là công việc khó khăn và tỉ mỉ. Bạn có thể cần xem lại tài liệu hiện có và suy nghĩ qua các trường hợp sử dụng tổng quát.

#### Hỗ trợ cộng đồng

Chúng tôi luôn hướng tới duy trì một cộng đồng liên tục phát triển và hợp tác. Chúng tôi cần sự giúp đỡ của các bạn để đạt được mục tiêu kể trên. Nếu bạn muốn hỗ trợ chúng tôi phát triển cộng đồng, đây là một số nguyên tắc mà chúng tôi đề ra:

* Thái độ tốt: Lịch sự, tôn trọng với các thành viên trong cộng đồng: không phân biệt vùng miền, chủng tộc, giới tính hoặc các hành vi tương tự. Chúng tôi thích những người tử tế hơn những người xấu tính!
* Thái độ hoan nghênh: Làm cho mọi người trong cộng đồng của chúng tôi cảm thấy được chào đón không phân biệt tiểu sử và mức độ đóng góp của họ, làm mọi cách có thể để khuyến khích sự gắn kết của cộng đồng.
* Tuân thủ pháp luật: Về cơ bản, không để bất kỳ ai gặp rắc rối. Chỉ chia sẻ nội dung mà bạn sở hữu, không chia sẻ thông tin riêng tư hoặc thông tin nhạy cảm và không vi phạm pháp luật.
* Duy trì đúng chủ đề: Đảm bảo rằng nội dung được đăng lên các kênh 1 cách phù hợp, tránh gây thảo luận lạc đề. Hãy nhớ khi bạn cập nhật một vấn đề hoặc trả lời email mà bạn có khả năng gửi cho một số lượng lớn người nhận. Vui lòng kiểm tra thật kỹ trước khi thực hiện. Cần lưu ý rằng không ai thích bị làm phiền cả.

#### Báo cáo lỗi

Nếu bạn tìm thấy lỗi, nhầm lẫn hoặc mâu thuẫn trong mã hoặc tài liệu của Origin, vui lòng cho chúng tôi biết bằng cách gửi nội dung vấn đề đó trên GitHub. Không có vấn đề nào là quá nhỏ. Hãy giúp chúng tôi sửa lỗi dù chỉ là nhỏ nhất!

#### Vấn đề bảo mật

OUSD vẫn đang trong giai đoạn phát triển ban đầu, có nghĩa là có thể tồn tại vấn đề với giao thức hoặc trong việc triển khai của chúng tôi. Chúng tôi rất coi trọng các lỗ hổng bảo mật. Nếu bạn phát hiện ra một vấn đề bảo mật, vui lòng thông báo cho chúng tôi ngay lập tức!

Nếu bạn tìm thấy lỗ hổng bảo mật, vui lòng gửi báo cáo của bạn tới [security@originprotocol.com](mailto:security@originprotocol.com) hoặc gửi tin nhắn mã hóa đến [@joshfraser trên Keybase](https://keybase.io/joshfraser). Vui lòng KHÔNG gửi lỗi bảo mật mà bạn phát hiện được 1 cách công khai. Hãy nhớ xem lại nguyên tắc của chúng tôi về khai báo thông tin và đủ điều kiện nhận tiền thưởng khi tìm ra lỗi.

{% page-ref page="../security-and-risks/bug-bounties.md" %}

#### **Phát triển cộng đồng**

Duy trì và phát triển cộng đồng của Origin cũng quan trọng ngang với việc phát triển cộng nghệ.

Chúng tôi cần sự trợ giúp liên tục trong việc cải thiện tài liệu, xây dựng các công cụ mới phù hợp giao diện nền tảng của chúng tôi, truyền bá thông tin đến người dùng mới, giúp người dùng mới nắm bắt thông tin quan trọng ban đầu và hơn thế nữa.

Vui lòng liên hệ với chúng tôi nếu bạn muốn giúp đỡ. Kênh `general` của chúng tôi trên [Discord](https://www.originprotocol.com/discord) là một nơi tuyệt vời để chia sẻ ý tưởng và tình nguyện giúp đỡ chúng tôi.

#### Vị trí Toàn thời gian

Origin thi thoảng sẽ tuyển dụng các nhà phát triển cho các vị trí bán thời gian hoặc toàn thời gian.

Chúng tôi rất ưu tiên tuyển dụng những người đã có những đóng góp cho dự án. Nếu bạn muốn tham gia cùng chúng tôi với tư cách là nhân viên toàn thời gian thì cách tốt nhất để bắt đầu là tương tác với độ ngũ của Origin và bắt đầu đóng góp vào công việc lập trình. Rất ít khả năng chúng tôi sẽ offer bạn một vị trí toàn thời gian trong nhóm kỹ thuật trừ khi bạn đã có một vài đóng góp nhất định.

Nếu bạn muốn trở thành 1 thành viên trong đội ngũ, ghé thăm [danh sách việc làm tại Origin Protocol](https://angel.co/originprotocol/jobs). Nếu bạn muốn hỗ trợ theo cách khác, vui lòng đề xuất ý tưởng của bạn trên [kênh Discord](https://www.originprotocol.com/discord)của chúng tôi.



