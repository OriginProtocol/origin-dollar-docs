# Pasokan Elastis

**Pasokan Elastis. Harga Stabil.**

OUSD bekerja secara berbeda dari kebanyakan token. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Instead, the contracts constantly adjust the monetary supply and automatically updates the balance in every token holder’s wallet to reflect the yield that has been earned by the protocol.&#x20;

{% hint style="info" %}
Anggap saja sebagai bunga yang bertambah di rekening bank Anda. Unit akun dan nilai dolar AS tidak berubah. Anda hanya mendapatkan lebih banyak dolar AS dari waktu ke waktu saat Anda memperoleh bunga.
{% endhint %}

![](../../.gitbook/assets/ousd\_docs\_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD 100% didukung oleh stablecoin lain dan tidak memiliki tantangan yang sama untuk mempertahankan pasak terhadap dolar. Given the ease of minting and redeeming OUSD, we can count on arbitrageurs to ensure the peg is maintained.&#x20;
2. Rebasing OUSD hanya akan meningkatkan pasokan karena jumlah OUSD yang dicetak terkait dengan keuntungan yang diperoleh dari strategi yang mendasarinya. Pokok Anda dilindungi selama tidak ada yang salah dengan protokol pinjaman / AMM dan stablecoin yang mendasarinya. Saldo OUSD Anda tidak akan pernah berkurang, tetapi nilainya bisa turun jika ada kegagalan pada sistem yang mendasarinya.
3. Unlike Ampleforth, which only rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebase dipicu secara teratur saat pengguna berinteraksi dengan kontrak OUSD. Chainlink Keepers ensure at least one rebase occurs every day.

**Memicu rebase secara manual**

Siapa pun dapat memicu rebase kapan saja dengan [memanggil fungsi rebase di vault](https://etherscan.io/address/originvault.eth#writeProxyContract). Anda dapat melakukan ini di Etherscan dengan menghubungkan dompet web3.
