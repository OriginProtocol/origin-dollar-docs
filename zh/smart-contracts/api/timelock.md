# 时间锁

{% hint style="danger" %}
The timelock has been added but is currently set to 1 minute. This allows for a faster response if any critical issues are discovered. The timelock is governed by Origin's 5 of 8 multi-sig.
{% endhint %}

在执行 OUSD 合同的任何更改之前，时间锁合约会强制执行 48 小时的等待期。 该时间锁可通过我们的多签被调用，并且是我们的 [ERC-20](../architecture.md)、 [保险库](vault.md) ，和 [策略](strategies.md) 合约的主人。 如果 OUSD 的管理员变得恶意，受到威胁或做出用户不喜欢的更改，则延时的管理员操作将给用户机会退出 OUSD。

{% hint style="info" %}
时间锁是一项安全措施，如果 OUSD 持有者反对协议的任何拟议升级，则可以使用这 48 小时的时间提取资金。
{% endhint %}

OUSD 使用的时间锁是 [Composite Timelock](https://compound.finance/docs/governance) 的略微修改版本，该版本已[由OpenZeppelin进行了审核](https://blog.openzeppelin.com/compound-finance-patch-audit/)。 The two notable differences are:

1. OUSD will initially use a shorter wait period (48 hours) than Compound (72 hours) to allow for a faster response if any issues are discovered.
2. Some actions, such a reallocating funds between existing strategies and freezing deposits can be called immediately without requiring the 48 waiting period. This is in case a major vulnerability is discovered.



