# zaman kilidi

{% hint style="danger" %}
Zaman kilidi, her şeyin çalıştığı doğrulandıktan hemen sonra eklenecektir. O zamana kadar, sözleşmeler Origin'in 5/8 çoklu işaretine tabi olacak. Bu, herhangi bir kritik sorun tespit edilirse daha hızlı bir yanıt sağlar.
{% endhint %}

Zaman kilidi sözleşmesi, OUSD sözleşmelerinde herhangi bir değişiklik yapılmadan önce 48 saatlik bir bekleme süresi uygular. Zaman kilidi, çoklu işaretimiz tarafından çağrılabilir ve [ERC-20](erc-20.md), [Vault](vault.md)ve [Strategies](strategies.md) sözleşmelerimizin sahibidir. Zaman geciktiren yönetici eylemleri, yöneticileri kötüye giderse, güvenliği aşılırsa veya kullanıcıların beğenmediği bir değişiklik yaparsa kullanıcılara OUSD'den çıkma şansı verir.

{% hint style="bilgi" %}
Zaman kilidi, protokolde önerilen yükseltmelere itirazları olması halinde OUSD sahiplerine fonlarını çekmeleri için 48 saat veren bir güvenlik önlemidir.
{% endhint %}

OUSD biraz değiştirilmiş bir versiyonu kullanılarak bir [Bileşik Timelock](https://compound.finance/docs/governance) olmuştur [OpenZeppelin tarafından denetlenmektedir](https://blog.openzeppelin.com/compound-finance-patch-audit/). 3 önemli fark:

1. OUSD, herhangi bir sorun tespit edilirse daha hızlı yanıt verebilmek için başlangıçta Bileşik \ (72 saat \) 'ten daha kısa bir bekleme süresi \ (48 saat \) kullanacaktır.
2. 48 saat geçtikten sonra, yalnızca sözleşmenin sahibi değil, herkes aramayı yürütmekte özgürdür.
3. Para yatırma işlemleri \ (ancak para çekme veya transferler değil \) 48 bekleme süresi gerekmeden anında dondurulabilir. Bu, büyük bir güvenlik açığının keşfedilmesi durumundadır.





