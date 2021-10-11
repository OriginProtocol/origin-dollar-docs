# Arsitektur

![](../.gitbook/assets/ousd_docs_graphics\_3.png)

OUSD terdiri dari serangkaian kontrak pintar. Setiap kontrak ini dibungkus dalam kontrak proxy yang dapat ditingkatkan melalui protokol tata kelola.

Secara internal, kepemilikan dalam vault dilacak menggunakan sistem kredit yang mewakili persentase kepemilikan vault untuk setiap pemegang. Kontrak [ERC-20](api/erc-20-1.md) menangani konversi ke persyaratan USD saat melihat saldo atau memulai transfer antar dompet.

[Vault](api/vault.md) bertanggung jawab untuk mencetak dan membakar OUSD. Ini juga memberlakukan persentase aset yang disebarkan ke masing-masing [Strategi](../core-concepts/supported-strategies/) yang didukung. Untuk mengoptimalkan biaya gas, vault mempertahankan penyangga untuk memungkinkan sebagian besar simpanan dan penebusan terjadi tanpa membongkar / melepas aset dari strategi.

OUSD Swap, aka "Flipper" is a smart contract that is provided by Origin for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may become bankrupt on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Origin Swap uses around 45% less gas than Uniswap v3 due to its simplicity.

