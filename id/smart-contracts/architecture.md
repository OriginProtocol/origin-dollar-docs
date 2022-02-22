# Arsitektur

![](../.gitbook/assets/ousd\_docs\_graphics\_3.png)

OUSD terdiri dari serangkaian kontrak pintar. Setiap kontrak ini dibungkus dalam kontrak proxy yang dapat ditingkatkan melalui protokol tata kelola.

Secara internal, kepemilikan dalam vault dilacak menggunakan sistem kredit yang mewakili persentase kepemilikan vault untuk setiap pemegang. Kontrak [ERC-20](api/erc-20-1.md) menangani konversi ke persyaratan USD saat melihat saldo atau memulai transfer antar dompet.

[Vault](api/vault.md) bertanggung jawab untuk mencetak dan membakar OUSD. Ini juga memberlakukan persentase aset yang disebarkan ke masing-masing [Strategi](../core-concepts/supported-strategies/) yang didukung. To optimize gas costs, the vault may maintain a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.

The Flipper is a smart contract for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may be empty on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Flipper uses around 45% less gas than Uniswap v3 due to its simplicity.

The Harvester contract collects reward tokens earned by the strategies, sells them, and sends the resulting stablecoins to the Dripper to be released to the vault. Anyone can call the harvest and earn 1% of the resulting USDT for doing so. This creates a self-incentivizing system that operates at a known fixed cost.

The Dripper contract buffers aproximately one week of reward token sales proceeds and makes it avaiable at a smooth rate to the vault. This keeps OUSD yield from being extremely spiky when harvests come in. The rate is recalculated at least once per day and is the rate that it would take to distribute the current dripper holdings out over a one week period.



