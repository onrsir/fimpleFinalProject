## [Live Demo ()=>](https://enpara-form-onuryks.netlify.app/)

##### u: kodluyoruz  p:bootcamp109 - test coverage 70%

<h3 align="left">Languages and Tools:</h3>

###### No Bootstrap , Tailwind or etc , Pure SASS!

<p align="left"> <a href="https://www.w3schools.com/css/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a><a href="https://sass-lang.com" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sass/sass-original.svg" alt="sass" width="40" height="40"/> </a>  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://reactjs.org/" target="_blank"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> 
  <a href="https://jestjs.io/" target="_blank"> <img src="https://jestjs.io/img/jest.png" alt="jest" width="40" height="40"/> </a>
  <a href="https://git-scm.com/" target="_blank"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> </p>

#### Screen

![Screen1](https://user-images.githubusercontent.com/51006791/131472703-ef91b993-ee3f-4fe6-8d2e-4a9dbf11dd28.png)

![Screen2](https://user-images.githubusercontent.com/51006791/131472411-cb9a9379-5477-4629-9251-5824dbd76671.png)

<p align="center">
  <img src="https://user-images.githubusercontent.com/51006791/131469657-667772c5-6073-4611-b18a-f0fdbd9f3b62.png" width="300" height="160" />
  <img src="https://user-images.githubusercontent.com/51006791/131469724-e427430d-f566-4316-9201-8ba7a4b27029.png" width="300" height="160" />
  <img src="https://user-images.githubusercontent.com/51006791/131472411-cb9a9379-5477-4629-9251-5824dbd76671.png" width="300" height="160" />
<img src="https://user-images.githubusercontent.com/51006791/131471705-dfd04c75-7ebd-437e-86ea-2c4251e6be5c.png" width="300" height="160" />
</p>


### Başvuru / ticket yönetim sistemi

#### Genel Açıklama

Uygulamamız herkese açık bir başvuru formunun son kullanıcı tarafından doldurulması ile başlıyor.
Formu dolduran kullanıcıya başvurusunu takip edebilecegi bir kod veriliyor. Kullanıcı başvuru durumu sayfasından bu kod ile başvurusunun çözülüp çözülemedigini kontrol edebiliyor.

Kullanıcı adı ve şifre ile girilebilen bir ekrandan da yetkili kullanıcılar gelen başvuruları görüntüleyebiliyor cevaplanmamış başvurulara cevap yazıp durumunu çözüldü / iptal edildi / bekliyor vb gibi güncelleyebiliyor. Gerekirse eski kayıtlara ulaşabiliyor.

#### Detaylı Açıklama

##### Routes / Paths

- /basvuru-olustur (default)

  - Public endpoint.
  - Başvuru formunu herhangi bir kullanıcının doldurmasına imkan verir.
  - Başvuru formunda [Ad, Soyad, Yaş, TC, Başvuru Nedeni, Adres Bilgisi, Fotograflar/Ekler, Gonder] butonu yer alır.

- /basvuru-basarili (Basvuru formu doldurulduktan sonra gelen sayfa)

  - Ekranda bir teşekkür mesajı yer alır ve kullanıcıya başvuru detayları ile birlikte başvuru kodu verilir.

- /basvuru-sorgula

  - Ekranda başvuru kodu girilebilen bir input ve sorgula butonu vardır.

- /basvuru/{basvuruNo}

  - Ekranda başvuru varsa bilgileri, son durumu ve verilen cevap(lar) yer alır.
  - Başvuru numarası hatalıysa 404(bulunamadı) mesajı çıkar.

- /admin

  - Ekranda kullanıcı giriş formu vardır. (Rahat test edebilmemiz için u:kodluyoruz, p:bootcamp109 bilgileri ile giriş yapabilmeliyim.)

- /admin/basvuru-listesi

  - Başarıli giriş sonrası bekleyen (çözülmemiş/cevaplanmamış) başvuruların listesi yer alır ve basit bilgiler sunar. (Başvuru yapan, tarih)
  - Başvuru listesinde her elemenda başvuruyu görüntüle butonu vardır.

- /admin/basvuru/{basvuruNo}
  - Başvurunun durumu güncellenebilir ve başvuruya cevap yazılabilir.
  - Burada yazılan cevap son kullanıci tarafından basvuru/{basvuruNo} kısmından görüntülenebilmelidir.
