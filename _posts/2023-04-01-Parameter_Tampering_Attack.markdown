---
layout: post
title:  "Parameter Tampering Atağı"
date:   2023-01-05 09:00:00
isStaticPost: false
language: "English"
---

![Parameter Tampering](/TR7-Website/17.jpeg)


#### **Parameter Tampering Atağı**

- **Parameter Tampering Atağı Nedir?**

Parametreler, URL sorgu dizeleri, form alanları ve çerezler kullanılarak geçirilir. Parametre kurcalama web tabanlı bir saldırı şeklidir, bir kullanıcı tarafından girilen URL veya Web sayfası form alanı verilerindeki belirli parametrelerin, saldırgan tarafından kullanıcının yetkisi olmadan değiştirilir. Bu, tarayıcıyı kullanıcının amaçladığından farklı bir bağlantıya, sayfaya veya siteye yönlendirir.

- **Parameter Tampering Atağı Nasıl Çalışır?**

Parametre kurcalamanın amacı form alanlarındaki parametreleri değiştirmektir. Kullanıcı bir HTML sayfasında seçim yaptığında, bunlar genellikle form alanı değerleri olarak depolanır ve HTTP isteği olarak Web uygulamasına gönderilir. Bu değerler, birleşik giriş kutusu, onay kutusu, radyo düğmesi, vb., Serbest metin veya gizli kullanılarak önceden seçilebilir. Bu değerlerin tümü bir saldırgan tarafından değiştirilebilir. Çoğu kez bu, sayfayı kaydetmek, HTML'i düzenlemek ve Web tarayıcısında sayfayı yeniden yüklemek kadar basittir.

Örneğin gizli alanlar, normalde web uygulamasına durum bilgisi sağlamak için kullanılan ve son kullanıcı tarafından görünmeyen parametrelerdir. Saldırganlar gizli alan değerini isteği doğrultusunda değiştirebilir.

Saldırgan, HTML formları sonuçlarını GET veya POST yöntemlerinden birini kullanarak gönderir. Yöntem GET, tüm form parametreleri ve bunların değerleri, kullanıcının gördüğü bir sonraki URL'nin sorgu dizesinde görünecektir. Böylece saldırgan bu sorgu dizesini değiştirebilir.

Parametre kurcalama basit ancak oldukça etkili olarak kabul edilir. Bu atak tipi veri ifşasıyla sonuçlanan çeşitli şekillerde gerçekleştirilebilir.

- **Parameter Tampering atak tiplerinden bazıları;** 

Parametre kurcalama basit ancak oldukça etkili olarak kabul edilir. Bu atak tipi veri ifşasıyla sonuçlanan çeşitli şekillerde gerçekleştirilebilir.

- Cookie : Cookie’ler, istemci tarafından değiştirilebilmekte ve URL istekleriyle sunucuya gönderilebilmektedir. Bu nedenle, saldırgan, cookie içeriğini değiştirmek için bundan yararlanabilir.

- Form alanları : Form alanı kurcalanması, bir saldırgan web sunucusuna gönderilen verileri kurallara aykırı bir şekilde değiştirerek bir formun davranışını değiştirmeye çalıştığında gerçekleşir.

- HTTP başlıkları : HTTP istek başlığında bulunan yönlendirme başlığı, isteğin kaynaklandığı web sayfasının URL'sini içerir. Fakat saldırganlar, referans başlığını orijinal bir siteden gelmiş gibi değiştirebilir. HTTP yanıtları oluşturma yeteneği, kullanıcılar arası kurcalama, web ve tarayıcı önbelleği zehirlenmesi, siteler arası komut dosyası oluşturma gibi ortaya çıkan çeşitli saldırılara izin verir.

- URL Manipülasyonu : URL, parametreler aracılığıyla hassas bilgiler ilettiğinde, bilgisayar korsanı bu sorgu dizesini değiştirebilir ve böylelikle kötü amaçlı eylemler gerçekleştirebilir.

- **Parameter Tampering Saldırılarından Korunmak**

Parametre kurcalaması, kullanıcı hakkında kişisel veya ticari bilgileri gizlice elde etmek için suçlular ve kimlik hırsızları tarafından kullanılabilir. Parametre tahrifinin önlenmesine yönelik önlemler, işlemin yürütülmesi için parametrenin gerçekten gerekli olup olmadığına bakılmaksızın, minimum ve maksimum izin verilen uzunluk, izin verilen sayısal aralık, izin verilen karakter dizileri ve kalıplarla ilgili standartlara uyduklarından emin olmak için tüm parametrelerin doğrulanmasını içerir.

Beyaz listeye alma biçimi, kara listeye almaktan daha etkilidir. Bir web uygulaması güvenlik duvarı , kullanımdaki site için doğru şekilde yapılandırılmış olması koşuluyla, parametrelerin değiştirilmesine karşı bir miktar koruma sağlayabilir. Ayrıca, parametre kurcalamasını önlemek için oturum çerezlerini şifrelemek de koruma sağlamaktadır. Genel olarak, bir bilgisayarın veya ağın parametre kurcalamaya karşı savunmasızlığı, katı bir uygulama güvenliği rutini uygulanarak ve güncel tutulmasını sağlanarak en aza indirilebilir.