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

---
  
## TCP Güvenli İletişim Örneği

TCP ile güvenli veri gönderimini iade taahhütlü posta gibi düşünün. İade taahhütlü postada gönderdiğiniz mektup ile birlikte sizizn tarafınızdan doldurulan alıcının ve sizin bilgilerinizin olduğu bir kartta alıcıya gönderilir.
Alıcı mektup ile beraber bu kartı alınca bu kartı imzalar ve sizin adresinize geri gönderir, böylece siz alıcının mektubunuzu aldığından emin olursunuz.

---

TCP'de bu üç ana aşamanın gerçekleşmesi için bazı ara durumlar da gerçekleşmektedir. Bu ara durumlar aşağıdaki gibi sıralanmaktadır.

####  LISTEN
Sunucu tarafından bir TCP bağlantı isteğinin beklenildiği durumdur. Dinleme modu olarak adlandırılır.

#### SYN-SENT
Karşı tarafa TCP bağlantısı isteği gönderildikten sonra karşı taraftan bağlantı isteğine cevap verilmesi beklenilen durum olarak adlandırılır.

#### SYN-RECEIVED
SYN bayrağı ile yapılan bağlantı isteğine sunucunun SYN-ACK bayrağı ile cevap vermesi aşamasından sonraki bekleme durumu olarak adlandırılır.

#### ESTABLISHED
Bağlantı kurulduktan sonra gelen veri transferinin yapıldığı durumdur.

#### FIN-WAIT-1
Sunucu ve istemci tarafındaki bekleme durumudur.

#### FIN-WAIT-2
Karşı taraftan TCP bağlantısının bitirilme isteğinin beklendiği durumdur.

#### CLOSE-WAIT
Sunucu ve istemci tarafından bağlantı kapatma talebinin beklendiği durumudur.

#### CLOSING
Karşı tarafa bağlantının bitirilmesine dair bir ACK bayrağı gönderildikten sonra bağlantının bitmesini bekleme durumu olarak adlandırılır.

#### LAST-ACK
Sunucu ve istemci tarafında ACK beklendiği durumdur.

#### TIME-WAIT
Bekleme durumudur.

#### CLOSED
TCP bağlantısının tamamen bittiği durum olarak adlandırılır.

---

## TCP Bayrakları

![TCP-flag](https://github.com/kaaneeksi/TCP-UDP/blob/main/G%C3%B6rseller/TCP-bayraklar%C4%B1.png?raw=true)
