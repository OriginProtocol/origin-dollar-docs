# Hak Istimewa Admin

Kontrak pintar OUSD dirancang agar dapat diupgrade oleh pemilik. Tim Origin menggunakan dua kontrak dompet multisig Gnosis yang berbeda untuk membuat perubahan pada protokol. Dompet multisig ini telah [diaudit oleh OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), tim Origin, dan lainnya. &#x20;

{% hint style="info" %}
Tindakan admin yang menunda waktu memberi pengguna kesempatan untuk keluar dari OUSD jika adminnya menjadi jahat, disusupi, atau membuat perubahan yang tidak disukai pengguna.
{% endhint %}

### Admin

Admin utama adalah kontrak multisig 5 dari 8 yang diperlukan untuk membuat perubahan kode apa pun pada protokol. OUSD hanya dapat ditingkatkan dari dompet multi-sig 5 dari 8 ini. Kunci multi-sig ini dipegang oleh individu yang memiliki hubungan dekat dengan perusahaan, dan bahkan pendiri Origin yang bertindak bersama tidak memiliki kontrol yang cukup untuk menjalankan fungsi pemilik sendiri. In addition, the OUSD contracts are owned by a [timelock](../smart-contracts/api/timelock.md) which places a 48 hour time deplay before any changes to the protocol can be made.&#x20;

### Strategist

Some functionality, such as rebalancing funds between strategies or pausing deposits, can be triggered without the timelock and with far fewer signers. Hal ini memungkinkan tim Origin untuk bereaksi lebih cepat terhadap kondisi pasar atau ancaman keamanan. These signers, known as Strategists,  have the ability to execute a limited number of functions __ with only 2 of 9 signers.

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
