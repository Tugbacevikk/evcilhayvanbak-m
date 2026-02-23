## Virtual Pet Care Simulator (C)

Bu proje C programlama dili kullanılarak geliştirilmiş konsol tabanlı bir sanal evcil hayvan bakım simülasyonudur. Oyuncu bir evcil hayvana isim verir ve onun temel ihtiyaçlarını yöneterek hayatta kalmasını sağlamaya çalışır.

Proje, durum yönetimi (state management) ve menü tabanlı kullanıcı etkileşimi üzerine kurulmuştur.

## Proje Amacı

Bu projenin amacı:

C dili ile fonksiyon ve dizi kullanımı pratiği yapmak

Menü tabanlı bir sistem tasarlamak

Koşul ifadeleri ve kontrol akışını yönetmek

Durum temelli bir simülasyon modeli oluşturmak

Basit bir oyun döngüsü (game loop) kurmak

## Oyun Mekaniği

Oyuncu, evcil hayvanın aşağıdaki durum değerlerini yönetir:

Uyku

Tokluk

Susuzluk

Sevgi

Sosyalleşme

Tuvalet

Sağlık

Hijyen

Tüm değerler 0–10 aralığında tutulur ve yapılan işlemlere göre artar veya azalır.

Her işlem sonrasında:

Durum değerleri otomatik olarak güncellenir

Kritik seviyeler kontrol edilir

Kaybetme koşulları değerlendirilir

Kaybetme Koşulları

Aşağıdaki durumlardan biri gerçekleştiğinde oyun sona erer:

Sağlık = 0

Hijyen = 0

Sevgi = 0

Uyku = 0

Tokluk = 0

Susuzluk = 10

Tuvalet = 10

Bu sistem, oyuncuyu dengeli bir bakım yapmaya zorlayan bir kaynak yönetim mekanizması oluşturur.

## Oyun İçeriği

Ana menü üzerinden yapılabilecek işlemler:

Durumu göster

Yemek ver

Su ver

Oyun oynat

Uyandır

Temizle

Veterinere götür

Tuvalete çıkar

Oyundan çık

Her işlem, ilgili durum değerlerini etkileyen ayrı fonksiyonlar tarafından yönetilir.

## Teknik Detaylar

Program C dili ile yazılmıştır.

Durum değerleri bir dizi (int durum[8]) ile tutulmaktadır.

Her işlem sonrasında merkezi bir güncelleme fonksiyonu çağrılmaktadır.

Oyun, do-while döngüsü ile sürekli çalışan bir yapıdadır.

Program sonlandırma koşulları exit(0) ile yönetilmektedir.

Derleme ve Çalıştırma

Linux / macOS / WSL:

gcc evcilhayvan.c -o pet
./pet

Windows (MinGW):

gcc evcilhayvan.c -o pet.exe
pet.exe

## Geliştirme Önerileri

Global değişkenleri struct yapısına dönüştürme

Enum veya define ile durum indekslerini daha okunabilir hale getirme

Kullanıcı giriş doğrulama mekanizması ekleme

Kaydet / yükle sistemi ekleme

Modüler dosya yapısına geçiş

## Öğrenim Kazanımları

Bu proje ile:

Menü tasarımı

Durum tabanlı simülasyon

Fonksiyonel program akışı

Kontrol yapıları

Basit oyun mantığı oluşturma

konularında pratik deneyim kazanılmıştır.

## Geliştirici

Tuğba Çevik
