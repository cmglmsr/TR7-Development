---
layout: post
title:  "Local File Inclusion"
date:   2023-01-05 09:00:00
isStaticPost: false
language: "English"
---

![Local File Inclusion](/TR7-Website/6.jpeg)


#### **Local File Inclusion**

- **Local File Inclusion Atağı Nedir?** 

LFI ve diğer pek çok güvenlik açığından kaçınmak için kullanıcı girdisine güvenmemelisiniz. Web sitenize veya web uygulaması kodunuza yerel dosyalar eklemeniz gerekiyorsa, izin verilen dosya adları ve konumlarından oluşan beyaz bir liste kullanmalısınız. Bu dosyalardan hiçbirinin, dosya yükleme işlevleri kullanılarak saldırgan tarafından değiştirilemeyeceğinden emin olunmalıdır. Kullanıcıların dosyaları güvenle okumasına veya indirmesini sağlamak için ipuçları;

- **Local File Inclusion Nasıl Çalışır?**

Genellikle açmak istediğiniz dosyanın yolu, dosyanın içeriğini bir dizgi (string) olarak döndüren ya da mevcut web sayfasına yazdıran ya da belgeye dahil eden ve ilgili dilin bir parçası olarak ayrıştıran bir işleve gönderilir.

- **Local File Inclusion Nasıl Anlaşılır?**
LFI’yı tespit etmenin en etkili yolu otomatik bir güvenlik açığı tarayıcısı kullanmaktır. Elbette bu tür güvenlik açıkları manuel sızma testi yoluyla tespit edinile bilinir, fakat çok daha fazla zaman ve kaynak gerektirir.

- **Local File Inclusion atak tipleri;**

  - Dilin Tercümanı Tarafından Ayrıştırılacak Dosyaları Dahil Etme
  - Bir Sayfaya Yazdırılan Dosyaları Dahil Etme
  - İndirme Olarak Sunulan Dosyaları Dahil Etme

- **Local File Inclusion Saldırılarından Korunmak**

LFI ve diğer pek çok güvenlik açığından kaçınmak için kullanıcı girdisine güvenmemelisiniz. Web sitenize veya web uygulaması kodunuza yerel dosyalar eklemeniz gerekiyorsa, izin verilen dosya adları ve konumlarından oluşan beyaz bir liste kullanmalısınız. Bu dosyalardan hiçbirinin, dosya yükleme işlevleri kullanılarak saldırgan tarafından değiştirilemeyeceğinden emin olunmalıdır.

Kullanıcıların dosyaları güvenle okumasına veya indirmesini sağlamak için ipuçları;

- Dosya yollarınızı güvenli bir veritabanına kaydetmeli ve her biri için bir kimlik atamalısınız, bu şekilde kullanıcılar yalnızca kimliklerini görüntülemeden veya değiştirmeden görebilirler.

- Beyaz bir dosya listesi kullanmalı ve diğer tüm dosya adlarını ve yolları yok saymalısınız.

- Dosyaları web sunucusuna dahil etmek yerine, içeriklerini mümkün olduğunca veritabanında saklamalısınız.

- Sunucuya otomatik olarak indirme başlıklarını göndermesini ve örneğin /download/ gibi belirli bir dizindeki dosyaları yürütmemesini söylemelisiniz. Bu şekilde, indirmek için ek kod yazmaya gerek kalmadan kullanıcıyı doğrudan sunucudaki dosyaya yönlendirebilirsiniz.


