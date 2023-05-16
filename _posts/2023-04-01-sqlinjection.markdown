---
layout: post
title:  "SQL Injection Saldırısı"
date:   2023-01-05 09:00:00
isStaticPost: false
language: "English"
---

![SQL Injection](/TR7-Website/7.jpeg)


#### **SQL Injection Saldırısı**

- **SQL Injection Atağı Nedir?**

SQL enjeksiyonu, bir saldırganın bir uygulamanın veritabanına yaptığı sorgulara müdahale etmesine olanak tanıyan bir web güvenlik açığıdır. Bu açık saldırganın normalde alamadığı verileri görüntülemesine izin verir. Bu, diğer kullanıcılara ait verileri veya uygulamanın kendisinin erişebildiği diğer verileri içerebilir. Çoğu durumda, bir saldırgan bu verileri değiştirebilir veya silebilir, bu da uygulamanın içeriğinde veya davranışında kalıcı değişikliklere neden olabilir.

- **SQL Injection Atağı Nasıl Çalışır?**

SQL, ilişkisel veritabanlarında depolanan verileri yönetmek için tasarlanmış bir sorgu dilidir ve verilere erişmek, değiştirmek ve silmek için kullanabilirsiniz. Birçok web uygulaması ve web sitesi, tüm verilerini SQL veritabanlarında depolar. Ayrıca bazı durumlarda, işletim sistemi komutlarını çalıştırmak için SQL komutlarını da kullanabilirsiniz. Bu yüzden sql injection saldırısı çok kötü sonuçlar doğurabilir.

SQL injection saldırısı yapmak için, saldırganın önce web sayfası veya web uygulamasında savunmasız kullanıcı bilgilerini(girdilerini) bulması gerekir. SQL injection güvenlik açığı olan bir web sayfası veya web uygulaması, bu tür kullanıcı girişini doğrudan bir SQL sorgusunda kullanır. Saldırgan, girdi içeriği oluşturabilir. Bu tür içerik genellikle kötü amaçlı (malicious payload) yük olarak adlandırılır. Saldırgan bu içeriği gönderdikten sonra, veritabanında kötü amaçlı SQL komutları yürütür.

- **SQL Injection Atağı Nasıl Anlaşılır?**

SQL injection saldırılarını tespit etmek için çeşitli stratejiler bulunmktadır. Bir veritabanı uygulamasının yayın adayı üzerinde gerçekleştirilen testler kümesine penetrasyon testi eklemek, tüm açık saldırı vektörlerinin iyi bir şekilde bağlanıp bağlanmadığını kontrol etmek ve veritabanının girişimleri algılayabilmesini sağlamak için giderek daha yaygın hale geldi. Bu, uygulamanızın ve veritabanınızın saldıra karşı direncini arttırır.

- **SQL Injection atak tiplerinden bazıları;**

- Ek sonuçlar döndürmek için bir SQL sorgusunu değiştirebileceğiniz gizli verileri çalma.

- Uygulamanın mantığına müdahale etmek için bir sorguyu değiştirebileceğiniz uygulama mantığını tersine çevirme.

- Farklı veritabanı tablolarından veri alabileceğiniz union saldırıları.

- Veritabanının sürümü ve yapısı hakkında bilgi alabileceğiniz veritabanını incelemek.

- Kör sql enjeksiyonu, kontrol ettiğiniz bir sorgunun sonuçlarının uygulamanın yanıtlarında döndürülmemesi.

- **SQL Injection Saldırılarından Korunmak**

Kullanıcı girdi(input) kanallarının bu tür saldırılar için ana vektör olduğu düşünüldüğünde, en iyi yaklaşım saldırı modellerini izlemek için kullanıcı girdilerini kontrol etmek ve incelemek. Sql enjeksiyonu önlemek için bazı yöntemler; Giriş doğrulama, parametreleştirilmiş sorgular, depolanmış prosedürler ve kaçış gibi önleme teknikleri, çeşitli saldırı vektörleriyle iyi çalışır. Bununla birlikte, SQL enjeksiyon saldırılarının modelindeki büyük farklılıklardan dolayı genelde veritabanlarını koruyamazlar. Bu nedenle, tüm temelleri kapsamak istiyorsanız, yukarıda belirtilen stratejileri güvenilir bir WAF (Web application firewall) ile uygulamalısınız. WAF'ın birincil avantajı, korumasız kalacak olan özel web uygulamaları için koruma sağlamasıdır.