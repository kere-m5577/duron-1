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
