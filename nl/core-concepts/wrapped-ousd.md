# Wrapped OUSD

{% hint style="info" %}
An audit of Wrapped OUSD is in progress. For now, please only use for  functionality and integration testing, not for investment.
{% endhint %}

Wrapped OUSD provides a non-rebasing version of OUSD that still earns yield. This may provide tax benefits in some locations, and may be easier to use as a building block for other contracts.

### How wrapped OUSD works

When you wrap OUSD by depositing it into WOUSD, you get back fixed number of wOUSD tokens. This number will not go up - you will have the same number of wOUSD tokens tomorrow as you had today. However the number of OUSD tokens that you can be unwrap will go up over time.

For example, if you wrap 10,000 OUSD, you might receive 9,423 wOUSD. If you hold for a while, you will still have 9,423 wOUSD, but when you unwrap the wOUSD it grew to unwrap to 11,500 OUSD.

Both OUSD and wOUSD earn at the same rate. wOUSD is a standard ERC20 token and can be transfered just like any other ERC20.

### To wrap OUSD

A UI for wrapping and unwrapping OUSD will be coming after the audit.

For now, you can use etherscan. You will need to two transactions.

1\) You will need to approve OUSD to transfer your funds to wrapped OUSD. Go to the OUSD contract on etherscan, and from the contracts tab, choose "Write as Proxy", then `allow()` the wOUSD proxy contract address to spend the amount of OUSD that you wish to wrap.

2\) Deposit OUSD to the wOUSD contract by going to the wOUSD proxy contract on etherscan, choosing  and from the contracts tab, choose "Write as Proxy", then `deposit()` the amount of OUSD you wish to wrap. Set your own address as the other parameters for this method (saying your address is where the new wOUSD should be sent.

### To unwrap OUSD

Unwrapping your wOUSD does not require any approvals, since you already hold the wOUSD in your wallet. You can either call `withdraw()` to specify the amount of OUSD you wish to take out, or use `redeem` to specify how much wOUSD you wish to unwrap. To unwrap all, just call \``` redeem` `` with the your current wOUSD balance. Set both of the remaining parameters ("from" and "to") to your own address.

### To find the value of your wrapped OUSD

&#x20;Call `maxWithdraw` on the wOUSD contract. This will show how much OUSD you could withdraw right now.
