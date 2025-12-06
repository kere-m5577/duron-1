#include <iostream>
#include <string>
using namespace std;


string UcusGuvenligiKontrolu (int yuk, int hiz, int yukseklik) {

  int pil =  100; // Başlangıç pil seviyesi
  pil -= (hiz /10 ) * 5; // Hiz değerine göre pil seviyesi

  //Pil seviyesi yazdirma ekranı
  cout << " Hesaplanan pil seviyesi: " << pil << endl;

  //1. yuk kontrolu
  if (yuk > 500 ) {
    return "Agir Yuk, Ucamaz ";
  }

  //2. Pil seviyesi kontrolu
  else if (pil< 30) {
    return "Pil seviyesi yetersiz uçarsan duşersin";
  }

 //3. Yukseklik kontrolu
 else if ( yukseklik > 200) {
    return " Radar sinyali disindasiniz, ucarsan dusersin";
 }

 else if ( yukseklik < 20) {

    return "Yukseklik guvenli lutfen ucun ucarsaniz dronunuz duser yeni dron satariz";
 }

 //Yum kosullar
 else {
    return "Ucus Guvenli ";
 }

}


int main (){

  const int  dronSayisi = 3;
  int yukler[dronSayisi];
  int hizlar[dronSayisi];
  int yukseklikler [dronSayisi];

  cout <<"Mini dron surusu ucus guvenligi programi "<< endl;


  // Kullanici verileri diziye giriyor. yukseklik hiz pil seviyesi vs
  for (int i = 0; i<dronSayisi; i++) {

    cout << "\ndron" << i+1 << "bilgileri giriniz: " << endl;
    cout <<"Yuk (gram): ";
    cin >> yukler [i];
    cout << "Hiz (m/s): ";
    cin >> hizlar [i];
    cout << "Yukseklik (m): ";
    cin >> yukseklikler[i];
  }

  cout << "\n dron surusu ucuz durumlari  " << endl;

  //Her dron icin sonucu hesapla ve yazdir
  for (int i=0; i< dronSayisi; i++)  {
    string sonuc = UcusGuvenligiKontrolu(yukler[i], hizlar[i], yukseklikler[i]);
    cout << "Drone " << i+1 << ": " << sonuc << endl;
  }


  return 0;

}




2222222...… bbbbbööööölllllüüüüümmmmm


#include <iostream>
#include <string>
using namespace std;

// Fonksiyon tanimi
string ucusGuvenligiKontrol(int yuk, int hiz, int yukseklik) {
    **int pil = 100; // Baslangic pil seviyesi**
    \*\*pil -= (hiz / 10) \\\* 5; // Hiz degerine gore pil azalmasi\*\*

    \\\*\\\*// Pil seviyesini yazdir\\\*\\\*

    \\\*\\\*cout << "Hesaplanan pil seviyesi: " << pil << endl;\\\*\\\*



    \\\*\\\*// 1. Yuk kontrolu\\\*\\\*

    \\\*\\\*if (yuk > 500) {\\\*\\\*

        \\\*\\\*return "Agir yuk, ucamaz!";\\\*\\\*

    \\\*\\\*}\\\*\\\*

    \\\*\\\*// 2. Pil seviyesi kontrolu\\\*\\\*

    \\\*\\\*else if (pil < 30) {\\\*\\\*

        \\\*\\\*return "Pil seviyesi dusuk, ucus guvensiz!";\\\*\\\*

    \\\*\\\*}\\\*\\\*

    \\\*\\\*// 3. Yukseklik kontrolu\\\*\\\*

    \\\*\\\*else if (yukseklik > 200) {\\\*\\\*

        \\\*\\\*return "Radar disi, ucus guvensiz!";\\\*\\\*

    \\\*\\\*}\\\*\\\*

    \\\*\\\*else if (yukseklik < 20) {\\\*\\\*

        \\\*\\\*return "Yukseklik guvensiz, ucus guvensiz!";\\\*\\\*

    \\\*\\\*}\\\*\\\*

    \\\*\\\*// Tum kosullar uygunsa\\\*\\\*

    \\\*\\\*else {\\\*\\\*

        \\\*\\\*return "Ucus guvenli!";\\\*\\\*

    \\\*\\\*}\\\*\\\*







}

// 2.3 Yuk dizisini siralama fonksiyonu (bubble sort)
void siralaYuk(int dizi[], int boyut) {
    **for (int i = 0; i < boyut - 1; i++) {**
        \*\*for (int j = 0; j < boyut - i - 1; j++) {\*\*
            \\\*\\\*if (dizi\\\\\\\[j] > dizi\\\\\\\[j + 1]) {\\\*\\\*

                \\\*\\\*int temp = dizi\\\\\\\[j];\\\*\\\*

                \\\*\\\*dizi\\\\\\\[j] = dizi\\\\\\\[j + 1];\\\*\\\*

                \\\*\\\*dizi\\\\\\\[j + 1] = temp;\\\*\\\*

            \\\*\\\*}\\\*\\\*

        \\\*\\\*}\\\*\\\*

    \\\*\\\*}\\\*\\\*







}



// 2.3 Yuk arama fonksiyonu (linear search)
int araYuk(int dizi[], int boyut, int aranan) {
    **for (int i = 0; i < boyut; i++) {**
        \*\*if (dizi\\\[i] == aranan) {\*\*
            \\\*\\\*return i; // bulundugu indexi dondur\\\*\\\*

        \\\*\\\*}\\\*\\\*

    \\\*\\\*}\\\*\\\*

    \\\*\\\*return -1; // bulunamadi\\\*\\\*







}

int main() {
    **const int droneSayisi = 7;**
    \*\*int yukler\\\[droneSayisi] = {350, 600, 200, 450, 500, 100, 400};\*\*
    \\\*\\\*int hizlar\\\\\\\[droneSayisi] = {40, 30, 80, 20, 50, 60, 155};\\\*\\\*

    \\\*\\\*int yukseklikler\\\\\\\[droneSayisi] = {50, 70, 150, 10, 210, 180, 90};\\\*\\\*

    \\\*\\\*string durumlar\\\\\\\[droneSayisi];\\\*\\\*



    \\\*\\\*cout << "=== Mini Drone Surusu Ucus Guvenligi Programi ===" << endl;\\\*\\\*



    \\\*\\\*// Her drone icin ucus guvenligini kontrol et\\\*\\\*

    \\\*\\\*for (int i = 0; i < droneSayisi; i++) {\\\*\\\*

        \\\*\\\*durumlar\\\\\\\[i] = ucusGuvenligiKontrol(yukler\\\\\\\[i], hizlar\\\\\\\[i], yukseklikler\\\\\\\[i]);\\\*\\\*

    \\\*\\\*}\\\*\\\*









    \\\*\\\*cout << "\\\\\\\\n--- Drone Surusu Ucus Durumlari ---" << endl;\\\*\\\*

    \\\*\\\*for (int i = 0; i < droneSayisi; i++) {\\\*\\\*

        \\\*\\\*cout << "Drone " << i + 1 << ": " << durumlar\\\\\\\[i] << endl;\\\*\\\*

    \\\*\\\*}\\\*\\\*



    \\\*\\\*// 2.3 Siralama ve arama islemleri\\\*\\\*

    \\\*\\\*cout << "\\\\\\\\n--- Yuk Dizisini Sirala ---" << endl;\\\*\\\*

    \\\*\\\*siralaYuk(yukler, droneSayisi);\\\*\\\*

    \\\*\\\*for (int i = 0; i < droneSayisi; i++) {\\\*\\\*

        \\\*\\\*cout << i + 1 << ". siradaki Drone yuk: " << yukler\\\\\\\[i] << endl;\\\*\\\*

    \\\*\\\*}\\\*\\\*



    \\\*\\\*// Yuk arama\\\*\\\*

    \\\*\\\*int arananYuk;\\\*\\\*

    \\\*\\\*cout << "\\\\\\\\nAramak istediginiz yuk degerini giriniz: ";\\\*\\\*

    \\\*\\\*cin >> arananYuk;\\\*\\\*



    \\\*\\\*int bulunanIndex = araYuk(yukler, droneSayisi, arananYuk);\\\*\\\*

    \\\*\\\*if (bulunanIndex != -1) {\\\*\\\*

        \\\*\\\*cout << "Yuk degeri bulundu. Drone indeks: " << bulunanIndex << endl;\\\*\\\*

    \\\*\\\*} else {\\\*\\\*

        \\\*\\\*cout << "Yuk degeri dizide bulunamadi." << endl;\\\*\\\*

    \\\*\\\*}\\\*\\\*



    \\\*\\\*return 0;\\\*\\\*







}

3.........BBBBÖÖÖÖLLLLLMMMMMMMMM



include <iostream>
#include <string>
using namespace std;

class Drone {
private:
    **int yuk;**
    \*\*int hiz;\*\*

    \*\*int yukseklik;\*\*

    \*\*int pil;\*\*









public:
    **// Yapici fonksiyon**
    \*\*Drone(int y, int h, int ys, int p) {\*\*

        \*\*yuk = y;\*\*

        \*\*hiz = h;\*\*

        \*\*yukseklik = ys;\*\*

        \*\*pil = p;\*\*

        \*\*cout << "Drone olusturuldu." << endl;\*\*

    \*\*}\*\*



    \*\*// Ucus guvenligi kontrol metodu\*\*

    \*\*string ucusGuvenligiKontrol() {\*\*

        \*\*pil -= (hiz / 10) \\\* 5;\*\*



        \*\*if (yuk > 500) {\*\*

            \*\*return "Agir yuk, ucamaz!";\*\*

        \*\*} else if (pil < 30) {\*\*

            \*\*return "Pil seviyesi dusuk, ucus guvensiz!";\*\*

        \*\*} else if (yukseklik < 20) {\*\*

            \*\*return "Yukseklik guvensiz, ucus guvensiz!";\*\*

        \*\*} else if (yukseklik > 200) {\*\*

            \*\*return "Radar disi, ucus guvensiz!";\*\*

        \*\*} else {\*\*

            \*\*return "Ucus guvenli! Kalan pil: %" + to\\\_string(pil);\*\*

        \*\*}\*\*

    \*\*}\*\*



    \*\*// Yuk degerini guncelleyen bir ornek metot\*\*

    \*\*void setYuk(int yeniYuk) {\*\*

        \*\*yuk = yeniYuk;\*\*

    \*\*}\*\*



    \*\*// Yikici fonksiyon\*\*

    \*\*~Drone() {\*\*

        \*\*cout << "Drone testi tamamlandi ve bellekten silindi." << endl;\*\*

    \*\*}\*\*



};

// Ana program
int main() {
    **cout << "=== Arda Alp'in Drone Ucus Test Programi ===" << endl;**

    \*\*Drone d1(350, 40, 50, 100);\*\*

    \*\*Drone d2(600, 30, 70, 100);\*\*

    \*\*Drone d3(100, 160, 180, 100);\*\*



    \*\*cout << "Drone 1: " << d1.ucusGuvenligiKontrol() << endl;\*\*

    \*\*cout << "Drone 2: " << d2.ucusGuvenligiKontrol() << endl;\*\*

    \*\*cout << "Drone 3: " << d3.ucusGuvenligiKontrol() << endl;\*\*



    \*\*cout << "=== Testler tamamlandi ===" << endl;\*\*



    \*\*return 0;\*\*



}
