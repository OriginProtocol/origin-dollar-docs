# Timelock

{% hint style="danger" %}
The timelock will be added soon after everything is verified as working. Until then, the contracts will be governed by Origin's 5 of 8 multi-sig. This allows for a faster response if any critical issues are discovered.
{% endhint %}

The timelock contract enforces a 48 hour wait period before any changes to the OUSD contracts can be executed. The timelock can be called by our multi-sig and is the owner of our [ERC-20](erc-20.md), [Vault](vault.md), and [Strategies](strategies.md) contracts. Time-delaying admin actions gives users a chance to exit OUSD if its admins become malicious, are compromised, or make a change that the users do not like.

{% hint style="info" %}
The timelock is a safety measure that gives OUSD holders 48 hours to withdraw their funds if they have objections to any proposed upgrades to the protocol.
{% endhint %}

OUSD is using a slightly modified version of the [Compound Timelock](https://compound.finance/docs/governance) which has been [audited by OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The 3 notable differences are:

1. OUSD will initially use a shorter wait period \(48 hours\) than Compound \(72 hours\) to allow for a faster response if any issues are discovered.
2. Once the 48 hours have passed, anyone is free to execute the call, not just the owner of the contract.
3. Deposits \(but not withdrawals or transfers\) can be immediately frozen without requiring the 48 waiting period. This is in case a major vulnerability is discovered.





