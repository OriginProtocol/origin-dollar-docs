# Rủi ro

{% hint style="danger" %}
Bạn chấp nhận rủi ro khi sử dụng Ousd. Hãy sử dụng nguồn vốn mà khi mất đi cũng không ảnh hưởng tới cuộc sống của mình.
{% endhint %}

Tương tự với bất kỳ sản phẩm DeFi tạo lãi suất nào khác, người dùng cần nắm rõ các rủi ro có thể có khi nắm giữ OUSD. Những rủi ro này có thể được phân thành 3 loại:

* Rủi ro hợp đồng thông minh
* Rủi ro tiềm ẩn của nền tảng bên thứ ba
* Rủi ro stablecoin

**Rủi ro hợp đồng thông minh OUSD**

Các hợp đồng thông minh của Ousd đã được [kiểm toán](audits.md) bởi nhiều công ty bảo mật uy tín. Mặc dù đã được kiểm toán, khả năng tồn tại lỗ hỗ có thể gây ảnh hưởng tới quỹ của người nắm giữ OGN là hoàn toàn có thể. Các hợp đồng liên quan đến toán học và logic phức tạp. Mặc dù chúng tôi đã thực hiện mọi biện pháp phòng ngừa để đảm bảo sự an toàn và bảo mật của hợp đồng thông minh, người dùng vẫn nên hiểu được các rủi ro tiềm ẩn và cân nhắc trước khi sử dụng. Origin Protocol sẽ không chịu trách nhiệm về bất kỳ tổn thất nào về tiền bạc, bất kể ai là người có lỗi.

**Rủi ro nền tảng của bên thứ ba**

OUSD được xây dựng dựa trên các nền tảng DeFi như Aave, Compound và Curve khác làm tăng thêm rủi ro hợp đồng thông minh. Chúng tôi đang chọn làm việc với các nền tảng đang quản lý hàng trăm triệu đô và đã nỗ lực tăng cường tính bảo mật giao thức của họ. Tuy nhiên, không có gì đảm bảo rằng các nền tảng Origin đang sử dụng sẽ không xảy ra lỗi và bất kỳ lỗi nào xảy ra với các chiến lược mà Origin sử dụng đều có thể dẫn đến mất mát cho người nắm giữ OUSD.

**Rủi ro của stablecoin**

Điều quan trọng cần lưu ý là OUSD chỉ mạnh ngang các đồng stablecoin đang hỗ trợ nó. Bất kỳ tổn thất xảy ra với các tài sản cơ bản (tài sản hỗ trợ) sẽ gây ra tổn thất tương tự đối với giá trị của OUSD. Mặc dù OUSD được thiết kế để duy trì tỉ lệ 1: 1 giữa số lượng OUSD và số lượng stablecoin hỗ trợ, điều này không đồng nghĩa với việc cơ chế này sẽ đảm bảo giá trị của các stablecoin này cũng như đồng stablecoin nào sẽ là stablecoin hỗ.

Điều quan trọng cần lưu ý là tất cả các stablecoin này tiềm ẩn các rủi ro tuy không đang kể đối với các bên liên quan. Đơn cử như Tether đã từng gặp phải răng rối liên quan đến thủ tục ngân hàng và đối mặt với không ít thách thức về việc tuân thủ quy định. Ngoài ra, cả USDT và USDC đều có "cửa sau" cho phép nhà phát hành có quyền đóng băng tiền trong ví của chủ sở hữu. Dai không được hỗ trợ bởi tài sản thế chấp là tiền pháp định, giá trị của nó cũng có thể bị ảnh hưởng bởi USDC được chấp nhận làm tài sản thế chấp để khai thác DAI.

_**OUSD là đang ở bản beta. Bạn chấp nhận rủi ro khi sử dụng OUSD Hãy sử dụng nguồn vốn mà khi mất đi cũng không ảnh hưởng tới cuộc sống của mình.**_

**Giảm thiểu rủi ro**

Chúng tôi đang tích cực làm việc với nhiều nhà cung cấp bảo hiểm DeFi và sẽ sớm công bố các kế hoạch bảo hiểm ban đầu để tăng cường bảo mật của giao thức. Ngoài kế hoạch cung cấp bảo hiểm và thực hiện các đợt [kiểm toán](audits.md) gần đây, chúng tôi đã cải thiện các quy trình nội bộ để hạn chế tối đa lỗ hổng.

Chúng tôi đã làm việc với [Certora](https://www.certora.com/) để bắt đầu chính thức xác minh các thuộc tính bảo mật khác nhau trong hợp đồng. Họ sẽ giúp Origin thiết lập xác minh tự động có thể chạy bất kỳ lúc nào chúng tôi cập nhật code của hợp đồng. Hiện chúng tôi cũng đã tự động kiểm tra các lỗi phổ biến bằng [Slither](https://github.com/crytic/slither) và [Echidna](https://github.com/crytic/echidna). Những biện pháp này sẽ cảnh báo nhóm của chúng tôi về các vấn đề bảo mật phổ biến ngoài các biện pháp mà chúng tôi tự xây dựng.

Việc kiểm hợp đồng thông minh diễn ra chặt chẽ hơn nhiều so với trước đây. Chúng tôi yêu cầu hai kỹ sư xem xét từng thay đổi theo 1 danh sách tiêu chí chi tiết và chúng tôi ưu tiên việc này hơn là phát triển tính năng mới.

Cuối cùng, chúng tôi chính thức [luân phiên](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) xem xét [vụ tấn công vào các dự án khác](https://github.com/OriginProtocol/security/tree/master/incidents), tìm hiểu rõ nguyên nhân để tránh trường hợp tương tự xảy ra với Origin.







