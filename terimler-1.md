```dart
import 'package:flutter/material.dart';

void main(List<String> args) {
  runApp(const Deneme());
}

class Deneme extends StatelessWidget {
  const Deneme({super.key});
  //Ana Widget
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      //Home Ana Ekranı oluşturur
      //Scaffold ise bize hazır bir ekran yapısı sunar. Temiz bir sayfa açar.
      home: Scaffold(
        //AppBar bize bir başlık alanı verir Worddeki Üst Bilgi gibi düşünebiliriz.
        appBar: AppBar(
          //AppBar'ın arka plan rengini belirler.
          backgroundColor: const Color.fromARGB(255, 136, 174, 206),
          //AppBar'ın başlık metnini belirler.
          title: Text("Merhaba Dünya"),
          //AppBar'ın başlık metninin stilini belirler.
          titleTextStyle: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
        ),
        //Body ise bize ana içerik alanını verir. Body her yerde aynı anlam HMTL'deki <body> gibi düşünebiliriz.
        body:
            //center, içindeki widget'ı ekranın ortasına yerleştirir. Burada bir Container widget'ı kullanıyoruz.
            Center(
              //child, Center widget'ının içine yerleştirilen widget'ı belirtir. Burada bir Container widget'ı kullanıyoruz.
              child:
                  //Container, içeriği düzenlemek ve stil vermek için kullanılan bir widget'tır.
                  //Burada mavi bir arka plan ve "Merhaba Dünya" metni içeren bir Container oluşturuyoruz.
                  Container(
                    //height, Container'ın yüksekliğini belirler. Burada 200 piksel olarak ayarlanmıştır.
                    height: 200,
                    //width, Container'ın genişliğini belirler. Burada 200 piksel olarak ayarlanmıştır.
                    width: 200,
                    //color, Container'ın arka plan rengini belirler. Burada mavi bir renk kullanıyoruz.
                    color: Colors.blueAccent,
                    //child, Container'ın içine yerleştirilen widget'ı belirtir. Burada bir Text widget'ı kullanıyoruz.
                    child: Center(
                      child: const Text(
                        "Merhaba Dünya",
                        //style, Text widget'ının metin stilini belirler. Burada font boyutunu 30 olarak ayarlıyoruz.
                        style: TextStyle(fontSize: 30),
                        //textAlign, Text widget'ının metin hizalamasını belirler. Burada metni ortalayarak hizalıyoruz.
                        textAlign: TextAlign.center,
                      ),
                    ),
                  ),
            ),
        //FloatingActionButton ise bize ekranda hareketli bir buton verir.
        //Genellikle önemli bir işlemi gerçekleştirmek için kullanılır.
        floatingActionButton: FloatingActionButton(
          //onPressed, butona tıklandığında ne olacağını belirler. Burada debugPrint ile konsola "Tıklandı" yazdırıyoruz.
          onPressed: () {
            //debugPrint, konsola mesaj yazdırmak için kullanılır. Burada "Tıklandı" mesajını yazdırıyoruz.
            debugPrint("Tıklandı");
          },
          //backgroundColor, butonun arka plan rengini belirler. Burada açık mavi bir renk kullanıyoruz.
          backgroundColor: const Color.fromARGB(255, 136, 174, 206),
          //child, butonun içeriğini belirler. Burada bir artı simgesi (Icons.add) kullanıyoruz.
          child: const Icon(Icons.add),
        ),
      ),
    );
  }
}
```
