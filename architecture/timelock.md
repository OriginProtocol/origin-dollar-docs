# Timelock

Same contact as the Compound Timelock.

72 hour wait period before code can be executed.  The timelock can be called by our multisig and is the owner of our ERC-20, Vault and Strategies contracts.

{% hint style="info" %}
The timelock prevents the Origin team from being able to run off with your money while they are working towards decentralized governance.
{% endhint %}

Two notable differences:

* Once the 72 hours have passed, anyone is free to actually execute the call, not just the owner of the contract
* Deposits \(but not withdrawals\) can be immediately frozen without requiring the 72 waiting period. This is in case a major vulnerability is discovered. 



