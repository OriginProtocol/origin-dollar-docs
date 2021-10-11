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

OUSD được xây dựng dựa trên các nền tảng DeFi như Aave, Compound và Curve khác làm tăng thêm rủi ro hợp đồng thông minh. Chúng tôi lựa chọn làm việc với các nền tảng đang quản lý lên tới hàng tỉ đô và đã nỗ lực tăng cường tính bảo mật giao thức của họ. Tuy nhiên, không có gì đảm bảo rằng các nền tảng Origin đang sử dụng sẽ không xảy ra lỗi và bất kỳ lỗi nào xảy ra với các chiến lược mà Origin sử dụng đều có thể dẫn đến mất mát cho người nắm giữ OUSD.

**Rủi ro của stablecoin**

Điều quan trọng cần lưu ý là OUSD chỉ mạnh ngang các đồng stablecoin đang hỗ trợ nó. Bất kỳ tổn thất nào xảy ra với các tài sản cơ bản (tài sản hỗ trợ) sẽ gây ra tổn thất tương tự đối với giá trị của OUSD. Mặc dù OUSD được thiết kế để duy trì tỉ lệ 1: 1 giữa số lượng OUSD và số lượng stablecoin hỗ trợ, điều này không đồng nghĩa với việc cơ chế này sẽ đảm bảo giá trị của các stablecoin này cũng như đồng stablecoin nào sẽ là stablecoin hỗ.

Điều quan trọng cần lưu ý là tất cả các stablecoin này tiềm ẩn các rủi ro tuy không đang kể đối với các bên liên quan. Đơn cử như Tether đã từng gặp phải răng rối liên quan đến thủ tục ngân hàng và đối mặt với không ít thách thức về việc tuân thủ quy định. Ngoài ra, cả USDT và USDC đều có "cửa sau" cho phép nhà phát hành có quyền đóng băng tiền trong ví của chủ sở hữu. Dai không được hỗ trợ bởi tài sản thế chấp là tiền pháp định, giá trị của nó cũng có thể bị ảnh hưởng vì USDC và USDT được chấp nhận làm tài sản thế chấp để khai thác DAI.

**Giảm thiểu rủi ro**

Mặc dù không thể đảm bảo hợp đồng của chúng tôi là an toàn 100%, nhưng chúng tôi đã thực hiện mọi bước có thể để giảm thiểu nguy cơ mất tiền:

Hợp đồng và các chương trình được [kiểm toán ](audits.md)bởi các kiểm toán viên hàng đầu trong ngành.

Chúng tôi đã làm việc với 2 đơn vị cung cấp [Bảo hiểm Defi](insurance.md) để cung cấp bảo hiểm tuỳ chọn cho người nắm giữ OUSD.

We have retained [Certora](https://www.certora.com) to formally verify the various security properties of our contracts. Họ đã giúp Origin thiết lập xác minh tự động có thể chạy bất kỳ lúc nào chúng tôi cập nhật code của hợp đồng. Chúng tôi đã tự động kiểm tra các lỗi phổ biến bằng kiểm tra [Slither](https://github.com/crytic/slither) và [Echidna](https://github.com/crytic/echidna). Những biện pháp này sẽ cảnh báo chúng tôi về các vấn đề bảo mật phổ biến ngoài các biện pháp mà chúng tôi tự xây dựng.

Việc kiểm tra code của hợp đồng thông minh dễ ra cực kỳ nghiêm ngặt. Chúng tôi yêu cầu hai kỹ sư xem xét từng thay đổi theo 1 danh sách tiêu chí chi tiết và chúng tôi ưu tiên đảm bảo bảo mật hơn là phát triển tính năng mới.

Cuối cùng, chúng tôi chính thức [luân phiên](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) xem xét [vụ tấn công vào các dự án khác](https://github.com/OriginProtocol/security/tree/master/incidents), tìm hiểu rõ nguyên nhân để tránh trường hợp tương tự xảy ra với Origin. Chúng tôi nhận ra 1 điều là những kẻ tấn công thường khai thác cùng một lỗ hổng cơ bản trên nhiều dự án khác nhau. Bằng cách xem xét các lỗ hổng bảo mật của dự án khác, chúng tôi buộc mình phải cập nhật các mối đe dọa bảo mật mới nhất trong ngành và không ngừng học hỏi từ những sai lầm của họ.

**Hành động thay lời nói**

Nhiều thành viên của nhóm Origin bao gồm cả hai sáng lập viện đang nắm giữ một phần đáng kể tài sản cá nhân của họ trong OUSD. Tài khoản tiền mặt của Origin Protocol cũng đang nắm giữ hàng triệu đô la OUSD. Chúng tôi là người tạo ra sản phẩm và sẵn sàng đặt tiền của mình vào rủi ro với code chúng tôi đã viết.

