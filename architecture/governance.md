# Governance

**Planning For Change**

As earning strategies will change over time, the OUSD smart contracts are designed to be owner upgradable.

For now, the OUSD contracts are owned by a 5 of 8 Gnosis muti-sig contract which has been [audited by OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), Origin’s team, and others. The keys to this multi-sig are held by individuals with close ties to the company, and not even the Origin founders acting together have enough control to execute owner functions on their own.

**Progressive Decentralization**

It is our intent to relinquish control and governance to the community as soon as possible.

In the meantime, we have implemented a [timelock](timelock.md) in front of all admin function calls, giving OUSD users time to withdraw their funds if any changes are made that they don't like.

