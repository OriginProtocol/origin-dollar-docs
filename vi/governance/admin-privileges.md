# Đặc quyền của quản trị viên

Các hợp đồng thông minh OUSD được thiết kế để có thể nâng cấp chủ sở hữu. Nhóm Origin sử dụng hai hợp đồng ví đa chữ ký Gnosis khác nhau để thực hiện các thay đổi đối với giao thức. Ví đa chữ ký này đã được [kiểm toán bởi OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), đội ngũ Origin, và các bên thứ 3 khác. &#x20;

{% hint style="info" %}
Việc trì hoãn thời gian thực thi thay đổi hợp đồng thông minh cho phép người dùng có thời gian rút khỏi giao thức khi nhận thấy bất kỳ thay đổi đáng nghi ngờ nào của người sở hữu hoặc chỉ đơn giản là bạn không thích các thay đổi được đề xuất.
{% endhint %}

Bất kỳ sự thay đổi về code của giao thức nào cũng cần có sự đồng ý của 5 trong tổng số 8 chữ ký hợp đồng. OUSD chỉ có thể được nâng cấp từ khi có sự đồng ý của 5 trên 8 ví đa chữ ký này. Điểm mấu chốt của hình thức đa chữ ký này là quyền quyết định sẽ không chỉ thuộc về sáng lập viên của Origin. In addition, the OUSD contracts are owned by the [timelock](../smart-contracts/api/timelock.md) which allows the Origin team to continue making changes to the protocol, but only after a time delay.&#x20;

Một số chức năng, chẳng hạn như tái cân bằng tiền giữa các chiến lược hoặc tạm dừng tiền gửi, có thể được kích hoạt mà không cần tới khoá thời gian và yêu cầu chữ ký từ ít hơn 5 người. Điều này cho phép nhóm Origin phản ứng nhanh hơn với các điều kiện thị trường hoặc các mối đe dọa bảo mật. These signers, known as Strategists,  have the ability to execute a limited number of functions __ with only 2 of 9 signers.

Đặc quyền quản trị viên là cần thiết trong giai đoạn đầu để đảm bảo giao thức được bảo mật và lợi nhuận được tối ưu đồng thời giảm thiểu rủi ro. Chúng tôi dự kiến sẽ tiếp tục cải tiến hợp đồng thông minh của Ousd trong vài tháng đầu.

Sau khi hoàn thành một số chu kỳ nâng cấp, chúng tôi có kế hoạch chuyển quyền sở hữu từ cơ chế công ty kiểm soát sang cơ chế kiếm soát bằng hợp đồng quản trị phi tập trung, từ đó cho phép cộng đồng bỏ phiếu và tham gia vào các cập nhật giao thức trong tương lai.
