---
layout: post
title:  "Man In The Middle"
date:   2023-01-05 09:00:00
isStaticPost: false
language: "English"
---
![Man In The Middle](/TR7-Website/2.jpeg)

#### **Man In The Middle**

- **Man In the Middle Atağı Nedir?**

Man in the middle (MitM) atağı üç varlık gerektiren bir ataktır. Bu roller; kurban, kurbanın iletişim kurmaya çalıştığı varlık ve kurbanın iletişimini kesen "ortadaki adam". Bu saldırı tipinde saldırgan kurban ve taraf arasındaki iletişimi gizlice dinler veya ikisi arasındaki trafiği değiştirmek için araya girer. Saldırganlar, oturum açma kimlik bilgilerini veya kişisel bilgileri çalmak, kurbanı gözetlemek veya iletişimleri veya verileri sabote edebilir.

- **Man In the Middle Atağı Nasıl Çalışır?**

Man in the middle saldırısı en eski siber güvenlik saldırılarından biridir. MitM saldırıları, iki tarafın bağlantısı arasında durmak ve trafiği gözlemlemek veya manipüle etmekten oluşur. Bu, yasal ağlara müdahale ederek ya da saldırganın kontrol ettiği sahte ağlar yaratarak olabilir. Ardından, saldırganın tercih ettiği hedefe doğru bu trafiği çalmak, değiştirmek veya yeniden yönlendirmek için güvenliği ihlal edilmiş trafik tüm şifrelemelerden arındırılır. Saldırganlar, kaydedildikten veya düzenlendikten sonra durdurulan trafiği sessizce gözlemleyebilir veya ihlal edilen kaynağı yeniden şifreliyor olabileceğinden, tespit edilmesi zor bir saldırı olabilir.

MitM, hedefe bağlı olarak çok çeşitli teknikleri ve potansiyel sonuçları kapsar. Örneğin, SSL soymada, saldırganlar kendisiyle sunucu arasında bir HTTPS bağlantısı kurar, ancak kullanıcıyla güvenli olmayan bir HTTP bağlantısı kurar, bu da bilgilerin şifreleme olmadan düz metin olarak gönderi ldiği anlamına gelir.

- **Man In the Middle Atağı Nasıl Anlaşılır?**

Man in the middle saldırılarının yakalanması zor olabilir fakat bazı bu saldırılar tespit edilmesi kolay dalgalanmalar yaratır. Bu yüzden geleneksel bilgelik bu durumlar için önemlidir. Saldırganlar, yeniden bağlanmaya çalıştığında kullanıcı adı ve parolayı ele geçirebilmeleri için kullanıcıların bağlantısını zorla keser. Beklenmedik veya tekrarlanan bağlantı kesilmelerini izleyerek bu tehlikeli davranışı olarak tespit edebilirsiniz.

Adres çubuğundaki herhangi bir şey az da olsa tuhaf görünüyorsa, iki kez kontrol edin. DNS saldırısı olabilir. Örneğin, adres isminde bir harf büyük olabilir. Hangi ağlara bağlandığınız konusunda çok dikkatli olun ve mümkünse halka açık Wi-Fi'dan. Saldırganlar, insanları bağlanmaları için "yerel ücretsiz kablosuz" gibi bilinen kimliklerle sahte ağlar oluşturur. Saldırganın Wi-Fi ağına bağlanırsanız, ağda gönderdiğiniz her şeyi kolayca görebilirler.

- **Man In the Middle Atak tiplerinden bazıları;**

- Yalnızca güvenli Wi-Fi yönlendiricilerine bağlanın veya kablosuz operatörünüzün şifreli bağlantısını kullanın. WPA2 güvenliğini kullanan yönlendiricilere bağlanın.

- End-point’ler ile VPN sunucusu arasındaki trafiği şifrelemek için bir VPN ekleyin (kurumsal ağda veya internette). Trafik şifreliyse, bir MiTM saldırganının onu çalması ya da değiştirmesi daha zordur.

- E-postalarınız, sohbetiniz ve görüntülü iletişiminiz için uçtan uca şifreleme kullanın. Parolalarınızı korumak ve parolaların yeniden kullanılmasını önlemek için bir parola yöneticisi kullanın.

- Yalnızca HTTPS bağlantılarına bağlanın, bu kuralı uygulamak için bir tarayıcı eklentisi kullanın.

- Mümkün olan her yerde çok faktörlü kimlik doğrulama kullanın.

- Kullanımdaki bir uzlaşmanın veya MitM tekniklerinin kanıtlarını tespit etmek için ağdaki etkinliği izleyin.



- ###### **Man In the Middle Saldırılarından Korunmak**

Sizi ve ağlarınızı MitM saldırılarından korumak için birkaç iyi uygulama vardır fakat hiçbiri %100 kusursuz değildir.


- **ARP Önbellek Zehirlenmesi**: Saldırganlar, bilgisayarınızı saldırganın bilgisayarının ağ geçidi olduğunu düşünmesi için kandırmak için bu sisteme yanlış bilgi enjekte eder. Ağa bağlandığınızda, saldırgan tüm ağ trafiğinizi ve trafiği gerçek hedefine iletir. Senin bakış açına göre her şey normal. Saldırgan, tüm paketlerinizi görebilir.

- **DNS Önbellek Zehirlenmesi**: DNS önbellek zehirlenmesi, saldırganın size farklı bir web sitesine yönlendiren sahte bir DNS girişi vermesidir. Google'a benzeyebilir, ancak Google değildir ve saldırgan sahte web sitesine girdiğiniz her türlü kişisel veriyi çalar.

- **HTTPS Adres Sahteciliği**: HTTPS, kullanıcıların verilerinin "güvenli" olduğunu bilmesinin yollarından biridir. En azından bir saldırganın düşünmenizi istediği şey budur. Saldırganlar, geçerli kimlik doğrulama sertifikalarına sahip meşru siteler gibi görünen HTTPS web siteleri kurarlar, ancak URL biraz farklı olacaktır. Örneğin, 'a' gibi görünen ancak olmayan bir unicode karakterine sahip bir web sitesi kaydedecekler. "Example.com" örneğiyle devam edersek, URL https://www.example.com gibi görünebilir, ancak "örnek" deki "a", yalnızca görünen geçerli bir unicode karakter olan bir kiril "a" dır. Farklı bir unicode değerine sahip arapça "a" gibi.

- **Wi-Fi Dinleme**: Saldırganlar, güvenli olmayan Wi-Fi ağlarındaki trafiği dinler veya insanları kandırmak için ortak isimlerle Wi-Fi ağları oluştururlar, böylece kimlik bilgilerini, kredi kartı numaralarını veya kullanıcıların o ağda gönderdiği diğer kişisel bilgileri çalabilirler.

- **Oturum Kaçırma**: Oturum ele geçirme, saldırganın bir web sayfasında (banka hesabı, e-posta hesabı vb.) oturum açmanızı izlediği ve ardından aynı hesaba tarayıcısından oturum açmak için oturum çerezinizi çaldığı bir MitM saldırısıdır.