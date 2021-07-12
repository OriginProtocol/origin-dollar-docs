# Nasıl çalışır

#### % 100 Destekli ve Kararlı

Origin Dollar \ (OUSD \), Ethereum ağı için ERC-20 uyumlu bir tokendır.

OUSD, USDT, USDC ve DAI gibi diğer sabit paralar tarafından 1: 1 desteklenen istikrarlı bir para birimidir. Sonuç olarak, 1 OUSD değer olarak her zaman 1 ABD dolarına çok yakın olmalıdır.

{% hint style="başarı" %}
1 OUSD = 1 USD
{% endhint %}

#### OUSD Basmak (minting)

Kullanıcılar mevcut stablecoin'lerini (şu anda USDT, USDC ve DAI \) resmi [Origin Dollar DApp](www.ousd.com)OUSD'ye çeviriyor. Verilen OUSD, derhal bileşik getiriyi tahakkuk etmeye başlar.

**OUSD'yi kullanma**

Kullanıcılar, [Origin Dollar DApp](www.ousd.com)kullanarak OUSD'larını istedikleri zaman diğer stabilcoinlere dönüştürebilirler. A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the vault. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from syphoning stablecoins from the vault in the event of mispricings of of the underlying assets. Bu ücret, uzun vadeli sahiplerini kısa vadeli spekülatörlere teşvik etmek için var.

Kullanımdan sonra, akıllı sözleşme hangi stabilcoin \ (ler) in kullanıcıya iade edileceğini belirleyecektir. In the current implementation, the vault will return coins in the same ratio as the current holdings. This lack of user optionality also protects the vault as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="uyarı" %}
% **0,5'lik bir çıkış ücreti vardır** ve kullanıcı hangi sabit paraları alacağını seçemez.
{% endhint %}

#### Bir**utomated Verim Tarım ( Yield Farming)**

OUSD, Bileşik, Aave, Uniswap, Dengeleyici ve Eğri gibi diğer DeFi protokollerine OUSD akıllı sözleşmesine yatırılan temel sabit paraları dağıtarak getiri üretir. It is expected there will be new diversified strategies added to the vault every month. Toplanan faiz, alım satım ücretleri ve ödül jetonları bir araya getirilir ve OUSD cinsinden getiriler üretmek için stabilcoinlere dönüştürülür. Zamanla, protokol, OUSD sahiplerine en iyi verimi sağlamak için varlıkları farklı likidite havuzlarına girip çıkaracaktır.

#### **Elastik Tedarik**

Oluşturulan getiriler, para arzının sürekli olarak yeniden finanse edilmesi yoluyla OUSD sahiplerine aktarılır. OUSD, protokolün ürettiği getiriye yanıt olarak para arzını sürekli olarak ayarlar. Bu, OUSD fiyatının 1 $ olarak sabit kalmasına izin verirken, token sahiplerinin cüzdanlarındaki bakiyeler, protokol tarafından kazanılan getirileri yansıtacak şekilde gerçek zamanlı olarak ayarlanır.

Sonuç, harcanması kolay, otomatik olarak aşırı büyük getiriler kazanan ve mevcut stabilcoinlerden daha fazla tutulması arzu edilen bir stablecoin'dir.

