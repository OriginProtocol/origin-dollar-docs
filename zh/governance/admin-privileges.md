# Admin Privileges

The OUSD smart contracts are designed to be owner upgradable.

At launch, the OUSD contracts are owned by a 5 of 8 Gnosis multi-sig contract which has been [audited by OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), Origin’s team, and others. The keys to this multi-sig are held by individuals with close ties to the company, and not even the Origin founders acting together have enough control to execute owner functions on their own.

Soon after launch, ownership will be transferred to the timelock. This will still allow the Origin team to make changes to the protocol from their multi-sig, but with a time delay.

Having admin privileges is necessary in the early days to ensure that the protocol is secure and optimized for earning yields while minimizing risks. We expect to release multiple iterations of our smart contracts in the first several months of the protocol's existence.

Once several upgrade cycles have been completed, we intend to transfer ownership from our company control to a decentralized governance contract, thereby allowing the community to vote and participate in future protocol updates.

