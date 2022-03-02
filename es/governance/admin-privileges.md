# Privilegios de Administrador

Los contratos inteligentes de OUSD están diseñados para que el propietario pueda actualizarlos. El equipo de Origin utiliza dos contratos de billetera multifirma Gnosis diferentes para realizar cambios en el protocolo. Estas carteras multifirma han sido [auditadas por OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), el equipo de Origin y otros. &#x20;

{% hint style="info" %}
Las acciones administrativas que retrasan el tiempo les dan a los usuarios la oportunidad de salir de OUSD si sus administradores se vuelven maliciosos, se ven comprometidos o hacen un cambio que a los usuarios no les gusta.
{% endhint %}

### Admin

El administrador principal es un contrato multifirma 5 de 8 que se requiere para realizar cualquier cambio de código en el protocolo. OUSD solo se puede actualizar desde esta billetera multi-sig de 5 de 8. Las claves de este multi-sig están en manos de personas con vínculos estrechos con la empresa, y ni siquiera los fundadores de Origin que actúan juntos tienen suficiente control para ejecutar las funciones de propietario por su cuenta. In addition, the OUSD contracts are owned by a [timelock](../smart-contracts/api/timelock.md) which places a 48 hour time deplay before any changes to the protocol can be made.&#x20;

### Strategist

Some functionality, such as rebalancing funds between strategies or pausing deposits, can be triggered without the timelock and with far fewer signers. Esto permite que el equipo de Origin reaccione más rápidamente ante las condiciones del mercado o las amenazas a la seguridad. These signers, known as Strategists,  have the ability to execute a limited number of functions __ with only 2 of 9 signers.

The strategist multisig can take the following actions on the vault.

* reallocate
* setVaultBuffer
* setAssetDefaultStrategy
* withdrawAllFromStrategy
* withdrawAllFromStrategies
* pauseRebase
* pauseCapital
* unpauseCapital

### Future

Having these admin privileges is necessary in the early days to ensure that the protocol is secure and optimized for earning yields while minimizing risks. We expect to release multiple iterations of our smart contracts in the first several months of the protocol's existence.

Once several upgrade cycles have been completed, we intend to transfer ownership from our company control to a decentralized governance contract, thereby allowing the community to vote and participate in future protocol updates.
