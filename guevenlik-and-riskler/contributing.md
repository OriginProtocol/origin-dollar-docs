# Katkı

**% 100 Açık kaynak**

OUSD tamamen açık kaynaklı bir projedir ve her türden katkıyı memnuniyetle karşılıyoruz. Sorunları bildirmekten, kodlara katkıda bulunmaktan ve topluluğumuzu geliştirmemize yardımcı olmaktan yardım etmenin birçok yolu vardır.

Halka açık çalışıyoruz ve şirketimiz Discord herkese açık. Sorularınız varsa veya başlamak için yardıma ihtiyacınız varsa, Discord OUSD kanallarımız ekibimizden ve topluluğumuzdan yardım almak için en iyi yerdir.

## Gelişme süreci

Branşlaşma stratejimiz [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/)benzer, ancak tüm geliştirmemizi `ana` dalında yapıyoruz ve yayınlanan kod için `kararlı` dalımız var.

Geliştirme akışınız şöyle görünmelidir:

1. İlginç bir konu bulun ve iletişim kurun! Lütfen `#engineering` [Discord](https://discord.gg/jyxpUSe) kanalına ne üzerinde çalışmak istediğinizi bildirin.
2. Discord'da [çekirdek ekip üyesine](https://github.com/orgs/OriginProtocol/teams/core/members) üye ping atın ve [katılımcı ekibimize eklenmesini isteyin](https://github.com/orgs/OriginProtocol/teams/contributors). Aksi takdirde, ilgili depoyu çatallamanız ve özellik dallarını kendi çatalınıza itmeniz gerekir.
3. Soruna bir yorum ekleyin veya kendi kendinize atayın, böylece istemeden aynı görev üzerinde çalışan birden fazla katılımcımız olmasın.
4. `ana` dalıyla başlayın ve mevcut bir özelliğe katkıda bulunmadığınız sürece yeni bir özellik dalını kontrol edin.
5. Uygun [kodlama stilini](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) izleyin ve harika bir kod yazın.
6. `ana` en son kaydetmeleri alın ve kodunuzun başladığınızdan beri birleştirilen diğer tüm çalışmalarda çalıştığını onaylayın.
7. Branşınızı yukarı akış havuzuna  \(ör. Https: //github.com/OriginProtocol/  \[repo \] \) gönderin, böylece diğer katkıda bulunanlar gerekirse kolayca çalışabilir.
8. Lütfen sağ sütundaki "İnceleyenler" in yanındaki dişli çark simgesini tıklayarak PR'da bir inceleme talep edin.

`ana` dalı kilitlenir, böylece yalnızca [çekirdek ekibin](https://github.com/orgs/OriginProtocol/teams/core) üyeleri çekme isteklerinizi birleştirebilir. Diğer güvenilir katılımcılar tarafından meslektaş incelemesi yapılan çekme talepleri hızlı bir şekilde takip edilecek ve daha hızlı birleştirilecektir! Uygun gözden geçirenler için `#engineering` Discord kanalını kontrol edin.

## Kodlama Stili

Depolarımızda çeşitli programlama dilleri kullanıyoruz. Katkıda bulunurken, lütfen mevcut kodlama kurallarını takip edin ve varsa depodaki CONTRIBUTING.md dosyasına bakın.

JavaScript için, [güzel](https://prettier.io/)aracılığıyla otomatik olarak uygulanan [NPM stil](https://docs.npmjs.com/misc/coding-style)kullanıyoruz.

Solidity için iki boşluklu girintiler kullanıyoruz.

## Protokol Tasarımı

Protokol veya uygulama tasarım önerilerini değerlendirirken şunları arıyoruz:

* Bu tasarım önerisinin çözdüğü sorunun bir açıklaması
* İlgili değiş tokuşların tartışılması
* Diğer mevcut çözümlerin gözden geçirilmesi
* İlgili literatüre bağlantılar  \(RFC'ler, makaleler, vb. \)
* Önerilen çözümün tartışılması

Lütfen protokol tasarımının zor ve titiz bir çalışma olduğunu unutmayın. Mevcut literatürü gözden geçirmeniz ve genelleştirilmiş kullanım örnekleri üzerinde düşünmeniz gerekebilir.

## Topluluk Rehberleri

Origin topluluğunu harika, büyüyen ve işbirliğine dayalı tutmak istiyoruz. Böyle kalması için yardımınıza ihtiyacımız var. Buna yardımcı olmak için, bir bütün olarak topluluk için bazı genel yönergeler geliştirdik:

* Nazik olun: Topluluk üyelerine karşı nazik, saygılı ve kibar olun: hiçbir bölgesel, ırksal, cinsiyet veya diğer taciz hoş görülmeyecektir. İyi insanları kötü olanlardan daha çok severiz
* Çeşitliliği ve katılımı teşvik edin: Geçmişleri ve katkılarının kapsamı ne olursa olsun, topluluğumuzdaki herkesin hoş karşılandığını hissetmesini sağlayın ve topluluğumuza katılımı teşvik etmek için mümkün olan her şeyi yapın.
* Yasal tutun: Temel olarak, kimsenin başını belaya sokmayın. Yalnızca sahibi olduğunuz içeriği paylaşın, özel veya hassas bilgileri paylaşmayın ve yasaları çiğnemeyin.
* Konudan ayrılmayın: Doğru kanala gönderi paylaştığınızdan emin olun ve konu dışı tartışmalardan kaçının. Bir sorunu güncellediğinizde veya potansiyel olarak çok sayıda insana gönderdiğiniz bir e-postaya yanıt verdiğinizde unutmayın. Lütfen güncellemeden önce bunu göz önünde bulundurun. Ayrıca kimsenin spam'i sevmediğini de unutmayın.

## Sorunları Bildirme

Origin'in kodunda veya belgelerinde hatalar, hatalar veya tutarsızlıklar bulursanız, lütfen bir GitHub sorunu doldurarak bize bildirin. Hiçbir sorun çok küçük değil. Tpyo'larımızı düzeltmemize yardım edin!

## Güvenlik sorunları

OUSD hala erken geliştirme aşamasındadır, bu da protokolde veya uygulamalarımızda sorunlar olabileceği anlamına gelir. Güvenlik açıklarını çok ciddiye alıyoruz. Bir güvenlik sorunu fark ederseniz, lütfen hemen dikkatimizi çekin!

Bir güvenlik açığı bulursanız lütfen raporunuzu özel olarak [security@originprotocol.com](mailto:security@originprotocol.com) gönderin veya Keybase&lt;/a&gt;

@joshfraser'a şifreli bir mesaj gönderin. Lütfen genel bir sorun bildirmeyin. Sorumlu açıklama ve hata ödülleri için uygunluk yönergelerimizi gözden geçirdiğinizden emin olun.&lt;/p&gt;

## **Topluluk İyileştirme**

Origin, teknolojimizle olduğu kadar toplulukla da ilgilidir.

Dokümantasyonumuzu iyileştirmek, platformumuzla arayüz oluşturmak için yeni araçlar oluşturmak, sözcüğü yeni kullanıcılara yaymak, yeni kullanıcıların kurulumuna yardımcı olmak ve çok daha fazlası için sürekli yardıma ihtiyacımız var.

Yardım etmek isterseniz lütfen iletişime geçin. [Discord](https://www.originprotocol.com/discord) `genel` kanalımız, fikirleri paylaşmak ve yardım etmek için gönüllü olmak için harika bir yerdir.

## Tam Zamanlı Pozisyonlar

Origin, ara sıra yarı zamanlı veya tam zamanlı pozisyonlar için geliştiricileri işe alır.

Projeye zaten katkıda bulunmaya başlamış kişileri işe alma konusunda güçlü bir tercihimiz var. Ekibimizde tam zamanlı bir pozisyon istiyorsanız, en iyi şansınız ekibimizle iletişim kurmak ve kod katkıda bulunmaya başlamaktır. En azından birleştirilen birkaç çekme talebiniz olmadıkça size mühendislik ekibimizde tam zamanlı bir pozisyon teklif etmemiz pek olası değildir.

İlgileniyorsanız, [Origin Protokolü iş listelerine bakın](https://angel.co/originprotocol/jobs). Eğer başka yollarla yardım etmek isterseniz, sizin fikirlerini veren lütfen [bizim ikilik var kanalına](https://www.originprotocol.com/discord).

