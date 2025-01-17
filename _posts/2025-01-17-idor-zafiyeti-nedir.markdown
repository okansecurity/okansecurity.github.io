---
layout: post
title:  "IDOR Zafiyeti nedir?"
date:   2025-01-17 21:57:19 +0300
categories: jekyll update
---


Herkese merhaba arkadaşlar,

Bugün sizlerle beraber IDOR açığını inceleyeceğiz ve öğreneceğiz.


# IDOR nedir

İDOR (Insecure Direct Object Reference), Türkçesiyle Güvensiz Doğrudan Nesne Referansı anlamına gelir.

IDOR zafiyeti, bir kullanıcının normalde erişmemesi gereken kaynaklara, referans üzerinden doğrudan erişim sağlaması durumudur. Bu durum, bir tür Broken Access Control (Kırık Erişim Kontrolü) açığı olarak nitelendirilebilir.


# ÖRNEK IDOR ZAAFİYETİ

Bu örnekte, oldukça klasik bir durumu ele alacağız:

Bir web sitesine üye olduğumuzda, sistem bize bir kullanıcı kimliği ID tanımlar. Bu kimlik sayesinde kendi kullanıcı bilgilerimize ve içeriklerimize erişebiliriz. Örneğin:
`www.denemesite.com/my-notes?user_id=1256`
Burada `user_id=1256` kısmı bizim kullanıcı ID'mizdir ve `my-notes?` kısmı, kullanıcının notlarına erişim sağlanan bir bölüm olduğunu varsayalım.

Şimdi, tarayıcıdaki URL'deki ID'yi değiştirdiğimizi düşünelim:
`www.denemesite.com/my-notes?user_id=1000`
Bu durumda, `user_id=1000` başka bir kullanıcıya ait bir kimliktir. Peki, bu URL'yi kullanarak erişilen notlar kimin olacak? Tabii ki `user_id=1000` olan kullanıcıya ait notlar görüntülenecektir.

Eğer bu sorgu üzerinde yazılımcı tarafından herhangi bir kontrol veya doğrulama yapılmamışsa, bir saldırgan bu ID'yi değiştirerek başka bir kullanıcının notlarına erişebilir.

Bu basit bir örnek oldu biliyorum, ama durumu çok iyi özetleyen bir durum olacaktır.

Ufak bir not: Burada biz id numarasını örnek aldık, ama sizler o sırada bir dosyaya eriştiğinizde dosyanın adını değiştirmeyi deneyebilirsiniz, kim bilir belki çok gizli bir dosyayı bulmuşsunuzdur. 

#

IDOR tanımı bu kadar, geri kalanı sizin CTF çözerek ve bazı şeyleri kurcalayarak bulmanıza dayanır, sizin için 2 adet link bırakıyorum bu linklere gidiniz ve bu CTF'leri çözünüz.

PORTSWİGGER: <a href="https://portswigger.net/web-security/all-labs#access-control-vulnerabilities">https://portswigger.net/web-security/all-labs#access-control-vulnerabilities</a>
Port swigger CTF'lerinde bu konulara daha derinlemesine girebilirsiniz.

TRYHACKME: <a href="https://tryhackme.com/r/room/idor">https://tryhackme.com/r/room/idor</a>
Bu link üzerinden İDOR tanımını ve hashlerin nerede olduğunu görebilir ve basit bir idor ctf'i çözebilirsiniz.


Saygılarımla,
Okan Tümüklü..
