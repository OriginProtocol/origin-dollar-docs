# Cara kerjanya

#### 100% Didukung dan Stabil

Origin Dollar \ (OUSD \) adalah token yang sesuai dengan ERC-20 untuk jaringan Ethereum.

OUSD adalah mata uang stabil yang didukung 1: 1 oleh stablecoin lain seperti USDT, USDC, dan DAI. Akibatnya, 1 OUSD seharusnya selalu mendekati nilai 1 USD.

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

#### Mencetak OUSD

Pengguna mengkonversi stablecoin mereka yang ada \ (saat USDT, USDC, dan DAI \) ke OUSD di resmi [Asal Dollar DAPP](www.ousd.com). OUSD yang diterbitkan mulai memperoleh hasil bunga majemuk segera.

**Menebus OUSD**

Pengguna dapat mengubah OUSD mereka kembali menjadi stablecoin lain kapan saja menggunakan [Origin Dollar DApp](www.ousd.com). Biaya keluar 0,5% dibebankan pada saat penebusan dan didistribusikan sebagai hasil tambahan kepada peserta yang tersisa di kumpulan. Biaya tersebut berfungsi sebagai fitur keamanan untuk mempersulit penyerang untuk memanfaatkan oracle yang tertinggal, mencegah mereka menyalahgunakan stablecoin dari kumpulan jika terjadi kesalahan harga pada aset yang mendasarinya. Biaya tersebut ada untuk memberi insentif kepada pemegang jangka panjang daripada spekulan jangka pendek.

Upon redemption, the smart contract will determine which stablecoin\(s\) to return to the user. In the current implementation, the pool will return coins in the same ratio as the current holdings. This lack of user optionality also protects the pool as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
There is a **0.5% exit fee** and the user doesn't get to pick which stablecoins they receive.
{% endhint %}

#### A**utomated Yield Farming**

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, Uniswap, Balancer, and Curve. It is expected there will be new diversified strategies added to the pool every month. Collected interest, trading fees, and rewards tokens are pooled and converted to stablecoins to produce OUSD-denominated yields. Over time, the protocol will move assets in and out of different liquidity pools in order to provide the best yield to the holders of OUSD.

#### **Elastic Supply**

The generated returns are passed on to the holders of OUSD via constant rebasing of the money supply. OUSD constantly adjusts the money supply in response to the yield the protocol has generated. This allows the price of OUSD to stay pegged at $1 while the balances in token holders' wallets adjust in real-time to reflect yields that have been earned by the protocol.

The end result is a stablecoin that is easy to spend, earns outsized yields automatically, and is more desirable to hold than existing stablecoins.

