# Client Side Routing(İstemci Tarafı Rotalama) w/ React Router v.5

Konular:

* React Router
* Link ve NavLink kullanarak belirli routelara bağlantı vermek
* Route Parametreleri Atama
* Componentlere Proplar göndererek Router render etme

## Talimatlar

### Görev 1: Proje Kurulumu

* [ ] Repoyu **Forklayın** , ve forku klonlayın.
* [ ] **Not** Çalıştıracağınız 2 server var o yüzden talimatları dikkatlice okuyun.
* [ ] **Root klasöründe**: `npm install` yazarak kütüphaneleri indirin.
* [ ] `npm start` ya da `node server.js` komutuyla çalıştırın. (Bu işlemle ilgili ilerleyen adımlarda daha açıklayıcı bilgiler bulacaksın)
* [ ] Başka bir terminal penceresinde `client` klasörüne girin ve `npm install` yazarak kütüphaneleri indirin.
* [ ] `client` klasöründeyken `npm start` yazarak client uygulamasını çalıştırın.

* [ ] Öncelikle uygulamanız client üzerinden çalışmaya başlayınca şuradaki gibi bir tarayıcı penceresi göreceksiniz:  [bknz](./Assets/filmler-anasayfa.png) `localhost:3000` (eğer 3000 portu boşta değilse 3001 portu kullanılabilir).

### Görev 2: MVP (MUÜ)

#### Tasarım Görselleri

Uygulamanızı bitirdiğinizde 2 adet route'u olacaktır:

* [ ] [route SS'/'](./Assets/ilk-route.png)
* [ ] [route SS '/filmler/:id'](./Assets/ikinci-route.png)

#### Route'ların uygulanması

[React Router 5 dökümantasyonu](https://v5.reactrouter.com/web/guides/quick-start)

* [ ] App componentine Route eklemek için hazılayın (`<Router>` & `<Switch>`)
* [ ] App dosyanıza 2 adet route ekleyin. (`<Route ... >`)
  * [ ] `Route` sıralaması hakkında sorun yaşamamak için `exact` propunu inceleyin: [Route exact prop dökümantasyonu](https://v5.reactrouter.com/web/api/Route/exact-bool)  
  * [ ] Birinci route'unuz `/` olacak ve `FilmListesi` bileşenini yükleyecek. Bu bileşene proplarla filmler apisinden alınan datayı aktarın.
  * [ ] Diğer route `/filmler/` parametresinden sonra `id` parametresini alacak (örnek: `/filmler/2`, `/filmler/3`). `id` dinamik olacak. Bu route `Film` bileşenini yükleyecek.

#### İşlevsellik Kazandırın

* [ ] Bir kullanıcı `FilmListesi` içindeki film cardına tıkladığında seçilen filmin detaylarını görebilmeli {`/movies/{tıklanılan film idsi}`.
* [ ] URL'den seçilen film idsini almak için `Film.js` dosyasının 7. satırını düzenlenemeniz gerekir.
* [ ] `KaydedilenlerListesi` bileşindeki `AnaSayfa` butonuna işlevsellik kazındırın, Anasayfaya geri dönmeli.
* [ ] Artık fil listesinde ileri geri ilerleyebiliyor olmalısın ve bir filmin detaylarını görebilmelisin.

### Görev 3: Esnek görevler

Eğer Görev 1 ve 2'yi tamamladıktan sonra bu göreve geçebilirsin.

#### Kodumuzu DRY olacak şekilde düzenleyin

* [ ] `Film`, `FilmDetayları` ve `FilmListesi` bileşenleri içindeki JSX'lerin oldukça benzer olduğunu farketmişsindir. `Film` bileşeninde "detaylı" görünümünde bulunan ana farklılık starların listesidir.
* [ ] `FilmCard.js` içinde bir Film Card'ı döndüren bir bileşen oluşturun. `Film` ve `FilmDetayları` bileşenlerini kaldırıp, yeni oluşturduğunuz `FilmCard` bileşeniyle uygulamayı yeniden geliştirin.
* [ ] Film Card, bir filmi star listesi olsun ya da olmasın görüntülemeye yetecek kadar esnek olmalıdır.

#### `Film Kaydet` işlevini ekleyin

* [ ] Halihazırda kullanmadığımız bir `Kaydedilenler Listesi` bileşenimizin olduğunu fark etmişsindir. Bu adımda bir film kaydetmek için bir işlevsellik ekleyeceksin. `Film` bileşenine `KaydedilenlerListesineEkle` fonksiyonunu gönderin. Daha sonra `Kaydet` butonuna bir click handler ekleyin. `Film.js` içindeki 24-27 satır arasındaki kodun başındaki yorum etiketini kaldırman gerekmektedir.

#### Kaydedilen Film listesini `Link` e çevirin

* [ ] Kaydedilen filmler, filmin kendisine linklenmelidir. `filmiKaydet` fonksiyonunun ne işe yaradığını düşünün.

#### Kaydedilen Film `Link` lerini `NavLink`e dönüştürün

* [ ] Navlink



https://developer.themoviedb.org/reference/discover-movie
api_key : eec2673ba714443e74178f87ba17d88d
API Read Access Token : eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJlZWMyNjczYmE3MTQ0NDNlNzQxNzhmODdiYTE3ZDg4ZCIsInN1YiI6IjYzYThjMzc3MGYyMWM2MDA3ODcxNTJmMSIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.mvF5XrBT7B0AJwPJekwVF7QoSkUBWfsuy9dTE90m9v8
Yapılacaklar;

ek detay sayfası için 3 farklı component oluşturun.
bu componentleri az da olsa stil ekleyin.
bu componentlerin içini alakalı veriler ile (api üzerinden gelen) 4 tane field ekleyin 1 tanesi resim olmalı.

![alt text](image-2.png)(main page router kısmı için eklendi bu sebeple boş)
![alt text](image-1.png)
![alt text](image.png)