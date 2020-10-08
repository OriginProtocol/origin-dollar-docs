# Elastik Tedarik

**Elastik Tedarik. Sabit Fiyat.**

OUSD, çoğu tokendan farklı çalışır. Yönetim altındaki varlıkların değeri arttıkça fiyat artışı yerine \ (Bileşik cTokens veya Yearn yTokens'te olduğu gibi), bir OUSD'nin değeri yaklaşık 1 $ 'da sabit kalır. Bunun yerine, sözleşmeler parasal arzı sürekli olarak ayarlar ve her bir token sahibinin cüzdanındaki bakiyeyi protokol tarafından kazanılan verimi yansıtacak şekilde otomatik olarak günceller.

{% hint style="bilgi" %}
Banka hesabınıza faiz tahakkuk ettiğini düşünün. ABD dolarının hesap birimi ve değeri değişmez. Faiz kazandıkça zamanla daha fazla ABD doları kazanırsınız.
{% endhint %}

![](../.gitbook/assets/ousd_docs_graphics_4.png)

Bu mekanizma, [Ampleforth](https://www.ampleforth.org/)tarafından benimsenen yeni yaklaşımdan esinlenmiştir, ancak vurgulanmaya değer bazı temel farklılıklar vardır:

1. OUSD, diğer stabilcoinler tarafından% 100 desteklenmektedir ve dolara sabitlemeyi sürdürme konusunda aynı zorluğa sahip olmayacaktır. OUSD'yi basmanın ve paraya çevirmenin kolaylığı göz önüne alındığında, pegin korunmasını sağlamak için arbitrajcılara güvenebiliriz.
2. OUSD geri ödemesi, basılan OUSD miktarı temel stratejiler tarafından kazanılan gerçekleşmiş kazançlara bağlı olduğundan, arzın artması yönünde büyük ölçüde önyargılıdır. Altta yatan sabit paralarla ortak olan fiyat dalgalanmaları dışında, OUSD bakiyenizin düştüğünü görmemelisiniz. Anaparanız, temel borç verme / AMM ve stabilcoin protokollerinde hiçbir şey ters gitmediği sürece korunur. Bakiyenizdeki herhangi bir büyük düşüş, sistemdeki bir sorunun göstergesi olacaktır.
3. Günde bir kez yeniden satış yapan Ampleforth'un aksine, OUSD'nin parasal arzı, getiri elde edildikçe gerçek zamanlı olarak sürekli güncellenir.

