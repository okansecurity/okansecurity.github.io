---
layout: post
title:  "HTTP, nasıl çalışır"
date:   2025-01-14 22:29:19 +0300
categories: jekyll update
---

Öncelikle herkese merhaba arkadaşlar, bu yazımda sizinle beraber HTTP'i derinlemesine öğreneceğiz.

<h1>HTTP nedir?</h1>

HTTP, tam adıyla (HyperText Transfer Protocol), OSI modelinin 7. katmanında yer alan bir server client iletişim modelini sağlayan uygulama protokolüdür. Web sayfalarının kullanıcılar tarafından erişilmesini ve görüntülenmesini sağlamak amacıyla kullanılır.
HTTPS, tam adıyla (HyperText Transfer Protocol Secure), HTTP'nin güvenli bir versiyonudur. Buda, HTTP verilerinin şifrelenerek iletilmesini sağlar. HTTP'S de genellike TLS/SSL gibi güvenlik protokolleri yer alır.

Bir web sitesini ziyaret ettiğimizde HTTP veya HTTPS kullanırız ve iletişim, istek-yanıt prensibine dayanır. Bu istek-yanıt yapısını anlamadan önce, URL kavramını öğrenmek daha sağlıklı olacaktır.

<h1>URL nedir?</h1>

URL, tam adıyla (Uniform Resource Locator), internet dünyasında bir kaynağa nasıl ve hangi yoldan erişileceğini belirten bir yapıdır. HTTP isteklerinde mutlaka URL'leri kullanırız ve bu sayede hangi kaynağa erişmek istediğimizi belirtiriz.
URL yapısını daha iyi anlamak isterseniz lütfek bu sayfalara gidiniz:  https://tr.wikipedia.org/wiki/URL  ,  https://medium.com/@ndbeladiya720/what-is-a-url-example-structure-of-url-92cda07a9dcc

#İstekler ve yanıtlar
HTTP ve HTTPS, client-server iletişim modelini kullanır. Bu modelde, client server'a istek gönderir, server ise bu isteğe karşılık yanıt verir.

<h2>HTTP isteği nedir?</h2>
Request yani istek, istemci tarafından web sunucusuna, istediği veriyi veya sayfayı rica ettiği bir istek türüdür. Amacı, hedef sunucudan belirli bir veri veya sayfayı almak için bir talepte bulunmaktır.

Örnek bir istek yapısını inceleyelim, ayrıntısına da girelim.

```
GET /posts HTTP/2
HOST: okansecurity.github.io
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64)

```

Gelelim bu yapıyı satır satır inceleyelim.

İlk satırdaki `GET /posts HTTP/2` ifadesinin ilk kısmındaki GET, kullanılan istek methodunu belirtir. İkinci kısımdaki /posts, isteğin hangi sayfaya veya kaynağa yönlendirilmesi gerektiğini gösterir. Son kısımdaki HTTP/1.1 ise, hangi HTTP protokolü sürümünün kullanıldığını belirtir.

Bu satırdan sonra header'lar gelir, bu sayede isteği ve gelen yanıtı daha iyi yapılandırır ve daha ayrıntılı bilgi almayı amaçlarız ve bir çok yararı bulunmaktadır.

HTTP methotlarını öğrenmek için bu kaynağa bir göz atın canolar: https://mbilgil0.medium.com/http-metotlar%C4%B1-http-request-methods-90d57d574dfa

İkinci satırdaki `HOST: okansecurity.github.io` kısmında, hangi web sitesi veya sunucuya istek gönderileceği belirtilir. Önemli olan nokta ise, HOST kısmından sonra iki nokta üst üste (:) işaretini koymanızdır.

Üçüncü satırda ise `User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64)` kısmında kullandığım tarayıcının sürümünü belirtiyorum.

dördüncü satırda ise boş alan bırakıyorumki sunucu isteğin bittiğini anlasın diye.

diğer header'ları görmek için lütfen buraya bir uğrayın: https://en.wikipedia.org/wiki/List_of_HTTP_header_fields



<h2>HTTP yanıtı nedir?</h2>
Htto yanıtı yani respon'u, web server'ın bizim isteğimize vermiş olduğu yanıttır.

örnek bir yanıt gösterelim.

```
HTTP/2 200 OK
Server: GitHub.com
Content-Type: text/html; charset=utf-8
Content-Length: 4223

<html>
  //kodlar
</html>
```
Gelelim bu yapıyı satır satır inceleyelim.

İlk satırdaki HTTP/2 200 OK kısmı, HTTP isteğimizin başarılı olup olmadığını gösterir. İlk kısım olan HTTP/2, sunucunun kullandığı HTTP sürümünü belirtir. Ardından gelen 200 ise bir HTTP durum kodudur ve yanındaki OK ifadesiyle birlikte işlemin başarılı olduğunu belirtir. Lütfen HTTP durum kodlarını iyice öğreniniz, çok işinize yarıyacak bu bağlantıya gidiniz: https://tr.wikipedia.org/wiki/HTTP_durum_kodlar%C4%B1

sonrasında http başlıkları bulunmaktdır.

`Server: GitHub.com` kısmı, sunucunun yazılımını sürümünü ve isminin bulunduğu kısımdır.
`Content-Type: text/html; charset=utf-8` kısmı bize  gönderilen bilginin türünü belirtiyor (örneğin, HTML, görseller, videolar, PDF, XML).
`Content-Length: 4223` kısmı bize verinin boyutunu beliriyor.
bir adet yine boşluk bırakmış sunucu, bu kısım bize yanıtın bittiğini ver istenilen verinin iletileceği anlamını belirtiyor. 
ardında HTML tag'i ile başlayan kısım ise bize istediğimiz bilgiyi sunuyor.

Lütfen, HTTP durum kodları, HTTP headerları gibi kavramları araştırınız.  linkleri yukarıda sizlere bıraktım.


Bugünlük benden bu kadar arkadaşlar, sizlere iyi geceler dilerim
Saygılarımla Okan Tümüklü.


