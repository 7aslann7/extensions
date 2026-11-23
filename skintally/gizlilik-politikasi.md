# SkinTally Gizlilik Politikası

[English](privacy-policy) · [SkinTally hakkında](./)

*Son güncelleme: 23 Kasım 2026*

## Kısaca

**Envanter verin tarayıcından hiç çıkmaz.** SkinTally'nin sunucusu yok. Envanterini, Steam hesabını, maliyetlerini ya da başka hiçbir şeyini göremeyiz: eklenti her şeyi senin cihazında saklar.

## SkinTally neleri saklar (yalnızca senin cihazında)

- CS2 envanterinin önbellekteki kopyası (tekrar ziyaretlerde Steam'e yeniden istek atılmasın diye)
- Önbellekteki fiyat kataloğu (Skinport satışları/ilanları, CSFloat fiyat listesi)
- Envanterinin günlük değer geçmişi
- Kâr/zarar defteri için girdiğin maliyetler ("Ödenen")
- Tercihler (dil, para birimi, değer tabanı, Steam modu)
- Baktığın Steam Market fiyatları (12 saat) ve takılı sticker/charm'ların İngilizce adları
- Takas teklifindeki karşı tarafın herkese açık CS2 envanteri (30 dakika)

Bunların hepsi tarayıcının eklenti deposunda durur. Dışa aktarabilir (popup → Verileri dışa aktar) ya da eklentiyi kaldırarak silebilirsin.

## Eklentinin yaptığı ağ istekleri

SkinTally **anonim** istekler yapar (hesap verisi, çerez ya da kimlik bilgisi içermez):

| Adres | Amaç |
|---|---|
| `steamcommunity.com/inventory/...` | Baktığın envanteri, senin tarayıcı oturumunla okur: Steam sayfasının kendisinin yaptığı isteğin aynısı |
| Takas teklifi sayfaları | Teklifteki ve takas penceresindeki iki tarafın item'larını Steam sayfasının zaten yüklediği veriden okur. Bu veride float, desen ve sticker olmadığı için karşı tarafın herkese açık CS2 envanterini Steam'den bir kez ister (onun envanter sayfasını açmakla aynı istek; senin tarayıcından, yalnız Steam'e). Sonuç 30 dakika cihazında tutulur, Steam yavaşlamamızı istediyse hiç istek atılmaz, gizli envanter sessizce atlanır. |
| Takas teklifleri listesi (gelen ve gönderilen) | Her teklifin hangi item'ları içerdiğini sayfadan okur, iki tarafın toplamını ve farkı gösterir. Salt okuma: hiçbir teklifi kabul etmez, reddetmez, arka planda yeni teklif aramaz. |
| Steam Market item sayfaları (CS2) | Kasa ya da kapsül sayfasında, Steam'in "Olası İçerik" listesinin yanına her item'ın fiyatını ve tüm aşınmalardaki fiyat aralığını yazar. Adlar sayfanın zaten içerdiği veriden gelir; ek istek yok. Salt okuma: hiçbir şey satın almaz, satmaz, emir vermez. |
| `steamcommunity.com/market/priceoverview` | Açtığın item'ın canlı Steam Market fiyatı; sayfadaki item'lar için yalnız "Steam" modunu açarsan; nakit pazarların (Skinport/CSFloat) fiyatlamadığı en çok 40 item için de, değersiz görünmesinler diye. Tek tek, Steam yavaşlamamızı isterse durarak; 12 saat cihazında hatırlanır |
| `steamcommunity.com/economy/itemclasshover` | Yalnızca SkinTally'nin sayfadan okuyamadığı adlar için: takılı bir sticker ya da charm'ın adı fiyatla eşleşmezse (örneğin Steam onu senin dilinde gösterdiği için) ya da takas teklifleri listende, Steam'in yalnız item'ın sınıf numarasını gösterdiği item'lar için. Steam'den o item'ın İngilizce market adını ister: envanter ziyareti başına en çok 30, takas teklifi başına 10, teklif listesi ziyareti başına 40 ve açılan item başına 6; 1,5 saniyede bir, çerezsiz ve Steam yavaşlamamızı istediyse hiç. Adlar cihazında hatırlanır, sonraki ziyaretlerde istek gerekmez. |
| `steamcommunity.com/market/sellitem` | **Yalnızca sen tıklayınca** ("Steam'de listele", item panelinde ya da satış listesinde): seçtiğin item'ları Steam Market'te satışa koyar, tıpkı Steam'in kendi Sat düğmesi gibi. Steam şart koştuğu için senin Steam oturumun ve Steam'in `sessionid` belirteciyle Steam'e gönderilir. Başka hiçbir yere bir şey gönderilmez. |
| `api.skinport.com/v1/items`, `/v1/sales/history` | Toplu, anonim fiyat kataloğu |
| `csfloat.com/api/v1/listings/price-list` | Çapraz kontrol için toplu, anonim fiyat listesi |
| `tcmb.gov.tr/kurlar/today.xml` | Fiyatları senin para biriminde göstermek için günlük döviz kurları |

Yukarıdaki Steam istekleri dışında (bunlar yalnız Steam'e, senin oturumunla, tıpkı Steam sayfasının yaptığı gibi gider) hiçbir istek Steam kimliğini, envanter içeriğini ya da herhangi bir kişisel veriyi içermez.

## Satış yardımcıları

Kendi envanterinde SkinTally, Steam Abonelik Sözleşmesi kutusunu işaretledikten sonra item panelinden tek item'ı ya da satış listenden en çok 20 item'ı listeleyebilir veya Steam'in kendi satış penceresini açabilir. Her ilan senin tıklamanla başlar ve Steam her birini yine Steam Mobile uygulamasında onaylatır. SkinTally hiçbir şeyi kendi kendine satmaz, yeniden listelemez ya da fiyatını değiştirmez.

## SkinTally'nin YAPMADIKLARI

- Analitik, telemetri ya da herhangi bir izleme yok
- Hiçbir SkinTally sunucusuna veri gönderilmez (böyle bir sunucu yok)
- Affiliate yönlendirmesi ya da bağlantı değiştirme yok
- Gezinme etkinliğin okunmaz: eklenti yalnız Steam envanter, takas teklifi, takas teklifleri listesi ve CS2 Market item sayfalarında çalışır
- Steam Web API anahtarı güvenlik kontrolü Steam'in anahtar sayfasını senin tarayıcında okur ve sonucu sana gösterir; anahtarın kendisi asla saklanmaz ya da gönderilmez

## İzinlerin açıklaması

- **storage**: yukarıda sayılan yerel önbellekler ve defterin
- **steamcommunity.com** (envanter, takas teklifi, takas teklifleri listesi ve CS2 Market item sayfaları; host izni olarak değil, içerik betiği olarak tanımlı): değer katmanını ve satış yardımcılarını çizmek için
- **api.skinport.com / csfloat.com / tcmb.gov.tr**: anonim fiyat ve kur verisi

## İletişim

Sorular için: [aslantnh@gmail.com](mailto:aslantnh@gmail.com) ya da SkinTally'nin Chrome Web Store sayfasındaki Destek sekmesi. Eklentinin kodu küçültülmeden paketlenir; yukarıdakilerin hepsini paketi okuyarak kendin doğrulayabilirsin.
