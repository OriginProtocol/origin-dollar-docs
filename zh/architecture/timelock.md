# 时间锁

{% hint style="danger" %}
确保一切正常运作后，时间锁将很快的被添加。 在此之前，所有合约将由 Origin 的 5 of 8 多签钱包管理。 如果发现任何关键问题的话，这允许问题的迅速处理。
{% endhint %}

在执行 OUSD 合同的任何更改之前，时间锁合约会强制执行 48 小时的等待期。 该时间锁可通过我们的多签被调用，并且是我们的 [ERC-20](erc-20.md)、 [保险库](vault.md) ，和 [策略](strategies.md) 合约的主人。 如果 OUSD 的管理员变得恶意，受到威胁或做出用户不喜欢的更改，则延时的管理员操作将给用户机会退出 OUSD。

{% hint style="info" %}
时间锁是一项安全措施，如果 OUSD 持有者反对协议的任何拟议升级，则可以使用这 48 小时的时间提取资金。
{% endhint %}

OUSD 使用的时间锁是 [Composite Timelock](https://compound.finance/docs/governance) 的略微修改版本，该版本已[由OpenZeppelin进行了审核](https://blog.openzeppelin.com/compound-finance-patch-audit/)。 3个显着差异是：

1. OUSD 最初将使用比 Compound（72小时）更短的等待时间（48小时），以便在发现任何问题时更快地做出响应。
2. 48 小时过后，任何人都可以自由执行更改，而不仅仅是合约的主人。
3. 存款（不包括取款或转账）可以立即被冻结，而无需等待 48 小时的等待时间。 这是在发现关键漏洞的情况下。





