# Rebasing & Kontrak Cerdas

Jika Anda menggunakan dompet multi-sig atau kontrak pintar lain yang ingin berpartisipasi dalam aspek rebasing OUSD, Anda harus memanggil fungsi`rebaseOptIn()` OUSD. Ini hanya berlaku untuk kontrak pintar karena dompet EOA standar didaftarkan secara otomatis.

{% hint style="info" %}
Dompet multi-sig atau kontrak pintar lainnya harus memanggil`rebaseOptIn()`untuk mendapatkan hasil.
{% endhint %}

Secara default, OUSD yang diadakan pada kontrak pintar tidak akan berpartisipasi dalam sifat rebasing token dan akan kehilangan hasil apa pun kecuali kontrak pintar secara eksplisit ikut serta. Ini meningkatkan komposisi OUSD dalam DeFi karena banyak protokol tidak dirancang dengan harapan bahwa saldo mungkin berubah. Untuk protokol DeFi lainnya, OUSD berfungsi seperti ERC-20 normal lainnya yang berperilaku baik hingga Anda memintanya untuk mengubahnya. Ini adalah atribut yang sangat berguna untuk pembuat pasar otomatis \(AMM\) seperti Uniswap yang rusak ketika jumlah token yang mereka pegang berubah secara tak terduga.

Kontrak pintar harus secara eksplisit memilih untuk menerima hasil melalui mekanisme rebasing. Ini memperbaiki masalah dengan perluasan pasokan di AMM sementara masih memungkinkan dompet multi-sig dan kontrak pintar lainnya kesempatan untuk tetap berpartisipasi dan mendapatkan hasil.

{% hint style="warning" %}
Jika Anda menerapkan kontrak dan bermaksud memanggil`rebaseOptIn()`untuk mendapatkan hasil, Anda tidak dapat memanggilnya dari konstruktor kontrak. Kontrak harus disebarkan sebelum dapat dipanggil.
{% endhint %}

Jika Anda menggunakan dompet multi-sig seperti [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) atau [Gnosis Safe](https://gnosis-safe.io/), Anda memerlukan [alamat kontrak proxy untuk OUSD](../../smart-contracts/registry.md) dan [ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805)sesuai. Setelah Anda menambahkannya, Anda akan dapat memanggil fungsi `rebaseOptIn()` untuk memilih menerima hasil melalui rebasing atau`rebaseOptOut()` untuk mematikannya lagi.





