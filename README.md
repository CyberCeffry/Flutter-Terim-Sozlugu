## Flutter Widget Türkçe Karşılıkları ve Özellikleri

### 1. Temel Widget’lar ve Türkçe Karşılıkları

| İngilizce Widget        | Türkçe Karşılığı            | Açıklama                                             |
| ----------------------- | --------------------------- | ---------------------------------------------------- |
| Container               | Kap                         | İçerik ve dekorasyon için kullanılan temel kutu.     |
| Text                    | Metin                       | Ekranda yazı göstermek için.                         |
| Row                     | Satır                       | Çocuk widget’ları yatay olarak hizalar.              |
| Column                  | Sütun                       | Çocuk widget’ları dikey olarak hizalar.              |
| Stack                   | Yığma / Üst Üste Bileşen    | Widget’ları üst üste koymak için.                    |
| Scaffold                | İskelet / Ana Sayfa Taslağı | AppBar, Drawer, Body gibi temel yapıyı sağlar.       |
| AppBar                  | Uygulama Çubuğu             | Üstteki başlık çubuğu.                               |
| FloatingActionButton    | Yüzen İşlem Düğmesi         | Ekranda belirgin şekilde kullanılan hareket düğmesi. |
| ListView                | Liste Görünümü              | Kaydırılabilir liste gösterimi.                      |
| GridView                | Izgara Görünümü             | Kaydırılabilir ızgara şeklinde liste.                |
| Image                   | Resim                       | Görsel göstermek için.                               |
| Icon                    | Simge                       | Küçük semboller, ikonlar.                            |
| Button / ElevatedButton | Düğme                       | Tıklanabilir butonlar.                               |
| TextField               | Metin Alanı                 | Kullanıcıdan veri almak için giriş alanı.            |
| Padding                 | Dolgu                       | Çevresine boşluk ekler.                              |
| Margin                  | Kenar Boşluğu               | Widget etrafında boşluk bırakır.                     |
| SizedBox                | Boyut Kutusu                | Sabit genişlik ve yükseklik sağlar.                  |
| Expanded                | Genişleyen                  | Alanı kalan boşluğa göre yayar.                      |
| Flexible                | Esnek                       | Çocuğun esnek şekilde alan kaplamasını sağlar.       |
| Card                    | Kart                        | Hafif gölgeli kutu, genellikle bilgi kartı olarak.   |
| Drawer                  | Menü / Yan Panel            | Yan panel açılır menü için.                          |
| SnackBar                | Bildirim Çubuğu             | Kısa mesaj göstermek için alt kısımda kayan bar.     |

### 2. Widget İçinde Kullanılan Özellikler (Property)

#### Örnek: Scaffold

```dart
Scaffold(
  appBar: AppBar(
    title: Text("Başlık"),
  ),
  body: Center(
    child: Text("Merhaba Flutter!"),
  ),
  floatingActionButton: FloatingActionButton(
    onPressed: () {},
    child: Icon(Icons.add),
  ),
  drawer: Drawer(
    child: ListView(
      children: [Text("Menü")],
    ),
  ),
)
```

| Property                 | Türkçesi / Anlamı         | Ne İşe Yarar                                 |
| ------------------------ | ------------------------- | -------------------------------------------- |
| appBar                   | Uygulama Çubuğu           | Üstteki başlık çubuğunu ekler.               |
| body                     | Gövde / İçerik            | Ekranın ana içeriği buraya gelir.            |
| floatingActionButton     | Yüzen İşlem Düğmesi       | Ekranda belirgin bir işlem düğmesi gösterir. |
| drawer                   | Yan Menü                  | Ekranın yanından açılan menü paneli.         |
| backgroundColor          | Arkaplan Rengi            | Scaffold’un arka plan rengini belirler.      |
| bottomNavigationBar      | Alt Navigasyon Çubuğu     | Alt kısımda sekme/tab menü.                  |
| resizeToAvoidBottomInset | Klavyeye göre boyutlandır | Klavye açıldığında ekranın boyutunu ayarlar. |

#### Text Widget Örnek

```dart
Text(
  "Merhaba",
  style: TextStyle(fontSize: 20, color: Colors.red),
  textAlign: TextAlign.center,
)
```

| Property  | Türkçesi       | Açıklama                              |
| --------- | -------------- | ------------------------------------- |
| style     | Stil           | Yazı tipi, boyut, renk vs.            |
| textAlign | Hizalama       | Metni sola, sağa veya ortaya hizalar. |
| overflow  | Taşma          | Taşan metni kesme, kaydırma vs.       |
| maxLines  | Maksimum Satır | Metnin kaç satır olacağını belirler.  |

#### Column / Row Widget

| Property           | Türkçesi           | Açıklama                                |
| ------------------ | ------------------ | --------------------------------------- |
| children           | Çocuklar           | İçine diğer widget’ları yerleştirir.    |
| mainAxisAlignment  | Ana eksen hizalama | Yatay veya dikey eksende hizalar.       |
| crossAxisAlignment | Yan eksen hizalama | Yan eksende hizalama yapar.             |
| mainAxisSize       | Ana eksen boyutu   | Alanı sarmalayan mı, yoksa maksimum mu? |

#### MaterialApp Örneği: home

```dart
MaterialApp(
  home: Scaffold(...),
)
```

* `home:` → Türkçesi: **ana sayfa / başlangıç sayfası**, uygulama açıldığında gösterilecek widget.
