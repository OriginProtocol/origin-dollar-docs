# Vote Delegation

There are two different ways that vote delegation plays a role in Origin Dollar Governance. First, veOGV holders must register to vote by either self-delegating or delegating their voting power to another Ethereum account. This is the result of a design decision to minimize gas costs for OGV stakers, many of whom do not intend to participate in governance directly. In the near future, this requirement will registration step will likely be integrated into all staking transactions so that new OGV stakers automatically self-delegate and are able to exercise voting power without submitting a separate transaction. You can follow the progress of this issue in [GitHub](https://github.com/OriginProtocol/ousd-governance/issues/312).

**How to Register** (on-chain)

* After acquiring OGV, stake it at [https://governance.ousd.com/stake](https://governance.ousd.com/stake).
* Visit [https://governance.ousd.com/register-vote](https://governance.ousd.com/register-vote), click "Register to Vote", and submit the transaction.

<figure><img src="../.gitbook/assets/Screen Shot 2022-12-28 at 11.33.32 PM.png" alt=""><figcaption><p><a href="https://governance.ousd.com/register-vote">Self-delegation at governance.ousd.com/register-vote</a></p></figcaption></figure>

Once veOGV holders are registered to vote, they may choose to delegate their voting power specifically for off-chain proposals on the [Origin Dollar Governance Snapshot Space](https://vote.ousd.com). Choosing this option does not strip the token holders of their voting power. The delegatee receives the extra voting power only on proposals the delegator has not voted on. This is convenient when users want someone they trust or even one of Origin's team members to make governance decisions regarding Origin's ecosystem. It is also useful when users have veOGV stored more safely in a hardware wallet and don’t want to go through the hassle of connecting it to the computer. A more accessible Ethereum wallet (e.g. MetaMask) can be used to vote by having voting power delegated to it from the hardware wallet.

**How to Delegate** (off-chain)

* Go to: [https://snapshot.org/#/delegate](https://snapshot.org/#/delegate).
* Type in the address or ENS name you want to delegate to.
* There is an option to limit the delegation power to only OUSD by selecting "Limit delegation to a specific space" and typing in “ousdgov.eth”.
* Click confirm to save your delegation.

<figure><img src="../.gitbook/assets/Screen Shot 2022-11-10 at 3.13.59 AM.png" alt=""><figcaption><p>Delegating your voting power only for the ousdgov.eth Snapshot space</p></figcaption></figure>

After completing these steps, the veOGV voting power is successfully delegated to the address specified.
