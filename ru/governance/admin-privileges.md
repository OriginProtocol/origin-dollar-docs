# Права администратора

Смарт-контракты OUSD разработаны с возможностью улучшения владельцем. Команда Origin использует два разных контракта кошелька с мульти-подписями Gnosis для внесения изменений в протокол. Аудиты этих кошельков с мульти-подписями были проведены такими компаниями, как [OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), командой Origin и др. &#x20;

{% hint style="info" %}
Задержка действий администратора дает пользователям возможность выхода из OUSD, если его администраторы станут злонамеренными, будут скомпрометированы или внесут изменения, которые не нравятся пользователям.
{% endhint %}

### Admin

Основной администратор - это контракт с 5 из 8 подписей, которые требуются для внесения любых изменений кода в протоколе. OUSD можно обновить только из этого кошелька с 5 из 8 подписей. Ключи к этой мульти-подписке принадлежат лицам, имеющим тесные связи с компанией, и даже действующие вместе основатели Origin не обладают достаточным контролем, чтобы самостоятельно выполнять функции владельца. In addition, the OUSD contracts are owned by a [timelock](../smart-contracts/api/timelock.md) which places a 48 hour time deplay before any changes to the protocol can be made.&#x20;

### Strategist

Some functionality, such as rebalancing funds between strategies or pausing deposits, can be triggered without the timelock and with far fewer signers. Это позволяет команде Origin быстрее реагировать на рыночные условия или угрозы безопасности. These signers, known as Strategists,  have the ability to execute a limited number of functions __ with only 2 of 9 signers.

The strategist multisig can do the following actions on the vault:

* reallocate - move funds between strategies
* setVaultBuffer - adjust the amount of funds held outside strategies for cheaper redeems.
* setAssetDefaultStrategy - which strategy mints and redeems pull from for a particular strategy
* withdrawAllFromStrategy - remove funds from a single strategy and send them to the vault
* withdrawAllFromStrategies - remove funds from all active strategies and send them to the vault
* pauseRebase - pause all rebases
* pauseCapital - pause all mints and redeems
* unpauseCapital - allow all mints and redeems

### Future

Having these admin privileges is necessary in the early days to ensure that the protocol is secure and optimized for earning yields while minimizing risks. We expect to release multiple iterations of our smart contracts in the first several months of the protocol's existence.

Once several upgrade cycles have been completed, we intend to transfer ownership from our company control to a decentralized governance contract, thereby allowing the community to vote and participate in future protocol updates.
