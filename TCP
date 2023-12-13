# TCP 

TCP güvenilir bir **taşıma katmanı** (OSI/Transport) protokolüdür. TCP'de veriler segmentlere ayrılıp bir alıcıya gönderildikten sonra alıcıdan segmentlerin alındığına dair onay bekler, eğer onayı alırsa segmentlerin devamını gönderir,
onay alamazsa gitmeyen segmentleri tekrar gönderir. Böylelikle segmentler eksiksiz bir şekilde gitmiş olur. 

Yani TCP ile gönderilen veriler sorugulanır, her bir segmente bir segment numarası atandığı için kayıp veriler tespit edilip tekrardan gönderilir. 
**Bu özelliği ile UDP ye göre daha yavaş ama daha güvenli bir protokoldür.**

---

## TCP (Transmission Control Protocol) Nasıl Çalışır?

### 3-Way Handshake

TCP, bağlantı odaklı bir protokoldür. Kaynak cihaz hedef bir cihaza veri göndermeden önce bağlantı kurar. Buna **3 yollu el sıkışma yani (3 way handshake)** denir.

* Veri gönderecek cihaz  ilk önce iletişim kurmak için **Synchronzaiton (SYN)** mesajı gönderir.
* Bu isteği alan alıcı cihaz iletişim kurma isteğini onayladığına dair bir **SYN-ACK Mesajı** gönderir.
* Son olarak gönderici cihaz iletişimin başladğını onaylayan bir **Acknowledgement (ACK)** mesajı gönderir ve 3 yollu el sıkışma tamamlanır.


  ![handshake](https://github.com/kaaneeksi/TCP-UDP/blob/main/G%C3%B6rseller/3-way-handshake.jpg?raw=true)
