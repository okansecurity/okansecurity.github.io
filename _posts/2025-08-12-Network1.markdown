---
layout: post
title:  "Network Nedir?"
date:   2025-08-12 22:14:41 +0300
categories: jekyll update
---

# Network nedir?

Network ya da Türkçe adıyla ağ, birden fazla cihazın birbirleriyle veri alışverişi yapabilmesi için kurulan iletişim altyapısıdır. Yâni dostlarım bir ağ sayesinde bilgisayarlar, telefonlar, sunucular ve diğer cihazlar arasında bilgi paylaşımı gerçekleşir.

Veri, aklınıza gelebilecek her türlü iletilebilir bilgiyi kapsar: metin mesajları, dosyalar, fotoğraflar, videolar, oyunlarda karakter hareketleri, sensör ölçümleri, hatta yazılım güncellemeleri bile bu kapsama girer.

Cihazların birbirleriyle network kullanarak iletişim kurabilmesi için ağ cihazlarına, kablolara ve belirli kurallara ihtiyaç duyar. Biz bu kurallara protokol diyoruz. Ayrıntılı bilgiyi ilerleyen bölümlerde anlatacağım.

# Network Topolojileri Nedir ve nelerdir?

Network topolojileri, cihazların birbirlerine nasıl bağlandığını ve bu sayede iletişim yollarının nasıl oluştuğunu açıklar. Burada bazı topoloji türlerini anlatacak ve temel mantığı anlamanızı sağlayacağım. Daha fazla topoloji öğrenmek için araştırma yapabilirsiniz.

<h3>BUS toploloji</h3>

<img width="1031" height="469" alt="image" src="https://github.com/user-attachments/assets/d4870c3e-edd9-446e-bc9f-8a2511af6b2e" />

BUS Topolojisi, tek bir hat üzerinden, bu hattın düz bir şekilde uzanmasıyla oluşturulan bir bağlantı şeklidir. Resimde gördüğünüz gibi, bir kablo vardır ve bu kabloya bağlı cihazlar bulunur. Kablonun iki ucunda ise terminatör dediğimiz küçük parçalar yer alır. Bu parçalar, ağda veri yansımasını ve çarpışmaları önler, ileride belki ayrıntılı anlatırız dosltarım.

Örneğin, cihaz 1’den cihaz 5’e veri göndermek istediğimizde tek yaptığımız şey veriyi hatta yollamaktır. Veri, omurga üzerinden ilerlerken her cihaza “Sen cihaz 5 misin?” diye sorar. Eğer cihaz 5 değilse bir sonraki cihaza geçer; ta ki cihaz 5’i bulana kadar. Cihaz 5 bulunduğunda veri iletilir. Eğer cihaz 5 bu ağda yoksa, veri kablonun ucundaki terminatöre ulaşır ve orada sonlanır.

<h3>Ring topolojisi</h3>

<img width="894" height="635" alt="image" src="https://github.com/user-attachments/assets/0051856d-67a0-41ae-bc0f-24d5ba035c0d" />

Ring Topolojisi, halka şeklinde bir kablo üzerinde gerçekleşir. Resimde gördüğünüz gibi, bu kabloya cihazlar bağlanır. Cihazlar iletişim kurmak istediğinde, tıpkı BUS topolojisinde olduğu gibi veriyi omurgaya iletir. Veri, sıra sıra tüm cihazları dolaşarak doğru cihazı bulmaya çalışır.

<h3>Star Topoloji</h3>

<img width="959" height="581" alt="image" src="https://github.com/user-attachments/assets/564d0303-43e7-4ae2-b817-58d062a27409" />

Star Topolojisi, günümüzde en sık kullanılan topolojilerden biridir. Cihazlar, bir network cihazına (genellikle switch veya hub) bağlanarak birbirlerine bağlanır. Bu network cihazı sayesinde veri, diğer cihazlara uğramadan doğrudan hedef cihaza iletilir. Böylece veri daha hızlı ve güvenli bir şekilde yol alır, dostlarım.

Şimdi dostlarım, topolojileri ben buraya kadar anlatıyorum. Ancak lütfen sizler mesh, full-connected gibi diğer topolojileri de araştırıp öğreniniz. Çünkü burada sadece temel bilgileri aktarmakla yükümlüyüm; geri kalan tamamen sizin araştırmanıza kalmış.

Bu yazım buraya kadardı, bir sonraki yazımda ağ türlerinden devam edeceğim.
