---
layout: post
title:  "Session Hijacking"
date:   2023-01-05 09:00:00
isStaticPost: false
language: "English"
---

![Session Hijacking](/TR7-Website/10.jpeg)


#### **Session Hijacking**

- **Session Hijacking saldırısı nedir?**

Session Hijacking (oturum ele geçirme), bir kullanıcı oturumunun bir saldırgan tarafından ele geçirildiği bir saldırı türüdür. Bir oturum, örneğin bir uygulama hizmetine oturum açıldığında başlar ve oturum kapatıldığında sona erer. Saldırganın oturum çereziniz hakkında bilgi sahibi olma durumuna göre, saldırı, aynı zamanda çerez kaçırma veya çerez yan saldırısı olarak da adlandırılır. Bazen herhangi bir bilgisayar oturumu ele geçirilmesine rağmen, Session Hijacking en yaygın olarak tarayıcı oturumları ve web uygulamaları için geçerlidir.

- **Session Hijacking Saldırısı Nasıl Çalışır?**

Session Hijacking, bir saldırgan, çoğu web sitesinde bir oturumu sürdürmek için kullanılan HTTP çerezlerini çalarak tehlikeye atılmış bir etkin oturumdan yararlanmasıyla gerçekleşir. Başka bir yol ise saldırganın belirli bir kullanıcının kimlik bilgilerini kullandığından, uzak bir web sunucusundaki bilgilere yetkisiz erişim elde etmek için etkin bir oturumun tahmin etmesidir. Oturum belirteci veya HTTP başlığının güvenliği manipıle edilebilir ve bunlar oturum koklama (Session Sniffing) ve siteler arası komut dosyası çalıştırma (XSS) saldırılarını içerir.

- **Session Hijacking Saldırısı Nasıl Anlaşılır?**

Saldırgan sistemdeki varlığına dikkat çekmedikçe, oturum kaçırmanın çoğu zaman fark edilmesi zordur. Kullanıcı, bir saldırı sırasında birkaç belirti fark edebilir. Örneğin, istemci uygulama oturumu yani Telnet yanıt vermiyor veya donuyor. Başka bir belirti ise bilgisayarı yavaşlatan kısa süreli bir ağ etkinliğidir.

Diğer bir yaygın belirti, istemci uygulamasının bir süre askıda kalmasıdır, çünkü sunucuya veri gönderen saldırganla rekabet etme durumu vardır. Bu, programın kafasının karışmasına ve 4. Katmandan bir yanıt beklemesine neden olur. Bununla birlikte, normal ve hatta ileri düzey bilgisayar kullanıcıları bu belirtileri nadiren rapor ederler çünkü sorunlar uygulamaların çökmesi, meşgul sunucular veya ağır yük bırakan bağlantılar altındaki bir ağ gibi diğer yaygın sorunlara çok benzer

- **Nasıl Korunur?**

DNS tünellemeye karşı koruma, bu girişimde bulunulan veri hırsızlığını algılayabilen ve engelleyebilen gelişmiş bir ağ tehdidi önleme sistemini ve böyle bir sistemin ağ trafiğinin denetlemesi ve kötü amaçlı ataklara yönelik trafiğin ve DNS trafiğine gömülebilecek kötü amaçlı içeriğin tanımlanmasını gerektirir.

- **Session Hijacking atak tiplerinden bazıları;**

İki ana Session Hijacking türü vardır. Bunlar, Uygulama Katmanı Korsanlığı ve Taşıma Katmanı Korsanlığıdır.  Uygulama katmanı ele geçirmede, bir saldırgan, bir oturumu ele geçirmek için gereken oturum kimliğini çalar veya başarıyla tahmin eder. Bu tür oturum kaçırma, esas olarak HTTP kullanan oturumlarda ortaya çıkar. İki Uygulama Katmanı Saldırısı örneği, Man in the Middle ve bir proxy kullanan saldırıları içerir. Öte yandan, proxy saldırıları, bir saldırgan, ağ trafiğinin kendi kurduğu bir proxy üzerinden geçmesine neden olarak işlem sırasında oturum kimliğini yakaladığında meydana gelir. Taşıma Katmanı ele geçirme, TCP oturumlarında meydana gelir ve saldırganın istemci ile sunucu arasındaki iletişim kanalını veri alışverişi yapılamayacak şekilde kesintiye uğratır. Böylece korsan istemciye ve sunucuya meşru görünen hileli veri paketleri gönderebilir yani esasen oturumu devralabilir. IP spoofing, sayesinde, korsan, ağdaki bilgisayarlarla iletişim kurabilir. Blind Hijacking, bir saldırganın bir oturum sırasında iletişimi kesip kendi kötü amaçlı verilerini ya da komutlarını gönderdiği bir saldırıdır.

- **Session Hijacking Saldırılarından Korunmak**

- Tüm oturum trafiğinin SSL / TLS şifrelemesini sağlamak için HTTPS kullanmak. Bu, korsan kullanıcının trafiğini izliyor olsa bile düz metin oturum kimliğine müdahale edememesini sağlar. Tüm bağlantıların şifrelenmesini garanti etmek için HSTS'i (HTTP Katı Taşıma Güvenliği) kullanmak daha fazla güvenlik sağlar.

- İstemci tarafı komut dosyalarından tanımlama bilgilerine erişimi önlemek HttpOnlyiçin Set-CookieHTTP başlığını kullanarak özniteliği ayarlayın. Bu, XSS'yi ve tarayıcıya JavaScript enjekte etmeye dayanan diğer saldırıları önler. Ek güvenlik için Secureve SameSitedirektiflerinin belirtilmesi de önerilir.

- Web sunucuları, uzun ve rastgele oturum tanımlama bilgileri oluşturabilir, bu da rakip bir tanımlama bilgisinin ne olabileceğini tahmin etme şansını azaltır.

- Oturum kimliğine yetkisiz erişimi engelleyen kullanıcının tarayıcısı ile web sunucusu arasında uçtan uca şifreleme yapmak. VPN’ler, kişisel VPN çözüm araçlarını kullanarak yalnızca web sunucusuna gelen trafiği değil, her şeyi şifrelemek için de kullanılabilir.

- Bir oturum sona erdiğinde otomatik bir oturum kapatma olmalıdır ve ayrıca, kullanıcının farklı bir oturum kimliği kullanarak yeniden kimlik doğrulaması yapması istenmelidir.