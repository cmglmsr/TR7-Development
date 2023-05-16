---
layout: post
title:  "Ping Of Death Atağı"
date:   2023-01-05 09:00:00
isStaticPost: false
language: "English"
---

![Ping Of Death](/TR7-Website/13.jpeg)


#### **Ping Of Death Atağı**

- **Ping of Death Atağı Nedir?**

Ölüm Pingi (diğer adıyla PoD), bir saldırganın basit bir ping komutu kullanarak hatalı biçimlendirilmiş veya büyük boyutlu paketler göndererek hedeflenen bilgisayarı veya hizmeti çökertmeye, kararsız hale getirmeye veya dondurmaya çalıştığı bir Hizmet Reddi (DoS) saldırısı türüdür.

İnternet Kontrol Mesajı Protokolü (ICMP) yankı yanıtı mesajı, "ping", bir ağ bağlantısını test etmek için kullanılan bir yöntemdir. İstek gönderildikten sonra eğer bağlantı çalışıyorsa, kaynak makine hedeflenen makineden bir yanıt alır.

- **Ping of Death Atağı Nasıl Çalışır?**

Bazı ping paketleri çok küçük olsa bile, IP4 ping paketleri çok daha büyüktür ve maksimum paket boyutu olan 65.535 bayt kadar olabilmektedir. Bazı TCP / IP sistemleri hiçbir zaman maksimumdan daha büyük paketleri işleyecek şekilde tasarlanmamıştır, bu durum da onları bu boyutun üzerindeki paketlere karşı savunmasız hale getirmektedir.

Kötü niyetli olarak büyük bir paket saldırgandan hedefe iletildiğinde, paket her biri maksimum boyut sınırının altında olan segmentlere bölünür. Hedef makine parçaları bir araya getirmeye çalıştığında, toplam boyut sınırını aşar ve bir arabellek taşması meydana gelebilir, bu da hedef makinenin donmasına, çökmesine veya yeniden başlamasına neden olur.

- **Ping of Death Saldırılarından Korunmak**

Bir saldırıyı durdurmanın tek çözümü, paketlerin yeniden birleştirilmesinden sonra paket boyutunun aşılmayacağından emin olmak için yeniden birleştirme sürecine kontroller eklemektir.

Diğer bir çözüm, maksimum değeri aşan paketleri işlemek için yeterli alana sahip bir bellek tamponu oluşturmaktır.

1998'den sonra oluşturulan cihazlar genellikle bu tür saldırılara karşı korunmaktadır fakat bazı eski ekipmanlar hala savunmasız olabilmektedirler. Microsoft Windows için IPv6 paketlerine yönelik yeni bir Ölüm Pingi saldırısı daha yakın zamanda keşfedilmiş ve 2013 ortalarında düzeltilmiştir.