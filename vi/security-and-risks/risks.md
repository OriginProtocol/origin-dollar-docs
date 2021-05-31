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

Điều quan trọng cần lưu ý là tất cả các stablecoin này tiềm ẩn các rủi ro tuy không đang kể đối với các bên liên quan. Đơn cử như Tether đã từng gặp phải răng rối liên quan đến thủ tục ngân hàng và đối mặt với không ít thách thức về việc tuân thủ quy định. Ngoài ra, cả USDT và USDC đều có "cửa sau" cho phép nhà phát hành có quyền đóng băng tiền trong ví của chủ sở hữu. While DAI does not have any direct backdoors, its assets can also be negatively impacted since USDC is accepted as collateral for minting DAI.

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. In addition to our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contracts' source code ourselves.







