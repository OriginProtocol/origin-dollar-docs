# Rủi ro

{% hint style="danger" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

Tương tự với bất kỳ công cụ lãi suất nào, OUSD cũng sẽ có thể chứa những rủi ro những rủi ro liên quan mà mọi người cần hiểu rõ. Những rủi ro này có thể được phân thành 3 loại:

* Rủi ro hợp đồng thông minh
* Rủi ro nền tảng cơ bản
* Rủi ro stablecoin

**Rủi ro hợp đồng thông minh**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic that may or may not be correct. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Rủi ro nền tảng**

OUSD được xây dựng dựa trên các nền tảng DeFi khác làm tăng thêm rủi ro hợp đồng thông minh. Chúng tôi đang chọn làm việc với các nền tảng có tài sản hàng trăm triệu đô la đang được quản lý và đã nỗ lực góp phần vào việc đảm bảo tính đúng đắt của giao thức của họ. Tuy nhiên, không có gì đảm bảo rằng các nền tảng cơ bản sẽ tiếp tục hoạt động như dự kiến và bất kỳ lỗi nào trong chiến lược cơ bản đều có thể dẫn đến mất mát cho người nắm giữ OUSD.

**Rủi ro của stablecoin**

Điều quan trọng cần lưu ý là OUSD chỉ mạnh ngang các đồng stablecoin đang hỗ trợ nó. Any loss of value in to an underlying assets will cause a similar loss to the value of OUSD. While OUSD is designed to maintain a one to one relationship between supply and number of backing stablecoins, it does not guarantee which stablecoins will make up that backing.

Điều quan trọng cần lưu ý là tất cả các stablecoin này tiềm ẩn các rủi ro tuy không đang kể đối với các bên liên quan. Đơn cử như Tether đã từng gặp phải răng rối liên quan đến thủ tục ngân hàng và đối mặt với không ít thách thức về việc tuân thủ quy định. Ngoài ra, cả USDT và USDC đều có "cửa sau" cho phép nhà phát hành có quyền đóng băng tiền trong ví của chủ sở hữu. Mặc dù DAI không có tính năng đóng băng như USDT và USDC, nhưng tài sản của nó cũng có thể bị ảnh hưởng tiêu cực bởi 2 đồng trên vì USDC được chấp nhận làm tài sản thế chấp để khai thác DAI.

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. Despite our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contract’s source code ourselves.







