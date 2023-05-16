---
layout: post
title:  "DNS Tünelleme"
date:   2023-01-05 09:00:00
isStaticPost: false
language: "English"
---

![DNS Tünelleme](/TR7-Website/11.jpeg)

#### **DNS Tünelleme**

- **DNS Tünelleme Nedir?**

DNS Tünelleme, DNS sorguları ve yanıtlarında diğer programların veya protokollerin verilerini kodlayan bir siber saldırı yöntemidir. DNS tünelleme genellikle saldırıya uğramış bir DNS sunucusuna eklenebilen ve uzak bir sunucuyu ve uygulamaları kontrol etmek için kullanılabilen veri yüklerini içerir. Ağ erişimi olan bir dahili DNS sunucusuna erişim gerektirdiğinden, DNS tünelleme, genellikle, risk altındaki sistemin harici ağ bağlantısına sahip olmasını gerektirir ve bir istemci-sunucu modeli aracılığıyla kötü amaçlı yazılımları ve diğer verileri tünellemek için DNS protokolünü kullanır.

- **Nasıl Çalışır?**

DNS, İnternet'in temel protokollerinden biridir. Sağladığı arama hizmetleri olmadan internette herhangi bir şey bulmak neredeyse imkansız denilebilir. Her yerel ağda –ve tüm internet ağında- hiyerarşik bir DNS yapısı vardır. Bir web sitesini ziyaret etmek için, web sitesini barındıran sunucunun IP adresini tam olarak bilmeniz gerekir, ki bu imkansızdır. Sonuç olarak, DNS trafiği İnternet'teki en güvenilir trafiklerden biridir. Kuruluşlar, dahili çalışanlarının harici siteleri ziyaret etmesi ve harici kullanıcıların web sitelerini bulması gerektiğinden, güvenlik duvarlarından trafiğin (hem gelen hem de giden) geçmesine izin verirler. DNS tünelleme, kötü amaçlı yazılımlara yönelik bir komut ve kontrol kanalı uygulamak için DNS isteklerini kullanır. Gelen DNS trafiği, kötü amaçlı yazılımlara komutlar taşıyabilirken, giden trafik hassas verileri sızdırabilir veya kötü amaçlı yazılım sağlayıcısının isteklerine yanıt verebilir, bunun sebebi DNS’in esnek bir yapıya sahip olmasıdır. Web siteleri alan adlarını aramak için tasarlandığından, hemen hemen her bilgi bir alan adı olabileceğinden DNS talebinin içerdiği veriler üzerinde çok az kısıtlama vardır. Bu istekler, saldırgan tarafından kontrol edilen DNS sunucularına gidecek şekilde tasarlanmıştır, istekleri alabilmelerini ve karşılık gelen DNS yanıtlarında cevap verebilmelerini sağlamaktadır. DNS tünelleme saldırılarının gerçekleştirilmesi kolaydır ve çok sayıda DNS tünelleme aracı mevcuttur. Bu, bilgisiz saldırganların bile bu tekniği bir kuruluşun ağ güvenliği çözümlerinden gizlice veri almak için kullanmasını mümkün kılmaktadır.

- **DNS Tünelleme Ataklarını Tespit Etmek**
Bir ağdaki bazı DNS tünelleme göstergeleri şunlardır:

**Olağandışı Alan Adı İstekleri:** DNS tünelleme kötü amaçlı yazılımı, istenen bir alan adı içindeki verileri kodlar. DNS talepleri içinde talep edilen alan adlarının incelenmesi, bir kuruluşun meşru trafiğinin DNS tünelleme girişiminden ayırt edilebilmesini sağlayabilir.

**Yüksek DNS Trafik Hacmi:**  Bir DNS talebindeki alan adının maksimum boyutu (253 karakter) vardır. Bu, bir saldırganın veri hırsızlığı gerçekleştirmek veya oldukça etkileşimli bir komut ve kontrol protokolü uygulamak için büyük olasılıkla çok sayıda kötü amaçlı DNS isteğine ihtiyaç duyacağı anlamına gelir. DNS trafiğinde ortaya çıkan artış, DNS tünellemesinin bir göstergesi olabilir.

- **Nasıl Korunur?**

DNS tünellemeye karşı koruma, bu girişimde bulunulan veri hırsızlığını algılayabilen ve engelleyebilen gelişmiş bir ağ tehdidi önleme sistemini ve böyle bir sistemin ağ trafiğinin denetlemesi ve kötü amaçlı ataklara yönelik trafiğin ve DNS trafiğine gömülebilecek kötü amaçlı içeriğin tanımlanmasını gerektirir.