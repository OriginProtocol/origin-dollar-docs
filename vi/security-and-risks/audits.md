# Kiểm toán

**OUSD Vault, ERC-20 và Tổng quan hệ thống**

OUSD đã được kiểm toán bởi nhiều công ty bảo mật uy tín. Chúng tôi đã làm việc với cả [Trail of Bits](https://www.trailofbits.com/) và [Solidured](https://solidified.io/) để kiểm tra toàn bộ code của Origin Đô la. Báo cáo kiểm toán các đợt như sau:

* [Trail of Bits, OUSD Audit, tháng 12/2020](https://github.com/OriginProtocol/security/blob/master/audits/Trail%20of%20Bits%20-%20Origin%20Dollar%20-%20Dec%202020.pdf)
* [Solidified, OUSD Audit, tháng 12/2020](https://github.com/OriginProtocol/security/blob/master/audits/Solidified%20-%20Origin%20Dollar%20-%20Dec%202020.pdf)
* [Solidified, OGN staking Audit, tháng 12/2020](https://github.com/OriginProtocol/security/blob/master/audits/Solidified%20-%20OGN%20Staking%20-%20Dec%202020.pdf)

Token quản trị, Token Origin \ (OGN \), cũng đã được kiểm toán bởi Trail of Bits vào năm 2018:

* [Trail of Bits, OGN Audit, tháng 12/2018](https://github.com/OriginProtocol/security/blob/master/audits/Trail%20of%20Bits%20-%20Origin%20Marketplace%20and%20OGN%20Token%20-%20Nov%202018.pdf)

Ngoài ra, các chiến lược được sử dụng và các yếu tố phụ thuộc mà OUSD sử dụng đã được các biên thức ba kiểm toán kỹ lưỡng.

{% hint style="info" %}
OUSD only integrates strategies that have been carefully audited and battle-tested with significant capital over an extended period of time.
{% endhint %}

**Compound Strategy and Open Price Feed**

Compound has been audited by [Trail of Bits](https://www.trailofbits.com) and [OpenZeppelin](https://openzeppelin.com/) and formally verified by [Certora](https://www.certora.com/). Visit the Compound website for their [full list of audits](https://compound.finance/docs/security#audits) including the original code for the modified [Timelock](../smart-contracts/api/timelock.md) that OUSD is using.

**Aave Strategy**

Aave has been audited by [Trail of Bits](https://www.trailofbits.com), [OpenZeppelin](https://openzeppelin.com/), [ConsenSys Diligence](https://consensys.net/diligence/), [Certik](https://certik.io/), [MixBytes](https://mixbytes.io/), and [PeckShield](https://peckshield.com/). They have also been formally verified by [Certora](https://www.certora.com/). Visit the Aave website for [their full list of audits](https://docs.aave.com/developers/security-and-audits).

**Chiến lược Curve**

Curve đã được kiểm toán bởi [Trail of Bits](https://www.trailofbits.com) và [Quantstamp](https://quantstamp.com/). Truy cập vào trang web Curve để xem [danh sách đầy đủ các bên đã kiểm toán hợp đồng của họ](https://www.curve.fi/audits).

**Chainlink Oracle**

Chainlink đã được audit bởi [Quantstamp](https://github.com/smartcontractkit/chainlink/tree/bafa91c), [SigmaPrime](https://github.com/smartcontractkit/chainlink/tree/cee356), [Callisto](https://gist.github.com/yuriy77k/c3a70d212a7f9ecda715252e45073158)và [Nick Johnson](https://github.com/smartcontractkit/chainlink/tree/5327f9). 



