# Arsitektur

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD terdiri dari serangkaian kontrak pintar. Setiap kontrak ini dibungkus dalam kontrak proxy yang dapat ditingkatkan melalui protokol tata kelola.

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. Kontrak [ERC-20](api/erc-20-1.md) menangani konversi ke persyaratan USD saat melihat saldo atau memulai transfer antar dompet.

[Vault](api/vault.md) bertanggung jawab untuk mencetak dan membakar OUSD. Ini juga memberlakukan persentase aset yang disebarkan ke masing-masing [Strategi](../core-concepts/supported-strategies/) yang didukung. Untuk mengoptimalkan biaya gas, vault mempertahankan penyangga untuk memungkinkan sebagian besar simpanan dan penebusan terjadi tanpa membongkar / melepas aset dari strategi.



