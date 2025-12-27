# evcilhayvanbakim
# 🐾 Sanal Evcil Hayvan Oyunu (C)

Bu proje, **C programlama dili** kullanılarak geliştirilmiş, **menü tabanlı bir sanal evcil hayvan simülasyonudur**.  
Oyuncu, evcil hayvanının temel ihtiyaçlarını karşılayarak onun hayatta kalmasını sağlamaya çalışır.

---

## 🎯 Projenin Amacı

Bu projenin amacı:

- Dizilerle veri yönetimi
- Fonksiyon kullanımı
- Menü tabanlı kullanıcı etkileşimi
- Koşul ifadeleri (`if`, `switch`)
- Program akışı ve durum kontrolü

konularını uygulamalı olarak öğretmektir.

---

## 🐶 Oyun Mantığı

Oyuncu bir **sanal evcil hayvan** sahiplenir ve ona bir isim verir.  
Evcil hayvanın çeşitli **durum değerleri** vardır ve bu değerler zamanla azalır.

Amaç:
> Evcil hayvanın **ölmeden** bakımını yapmak ve ihtiyaçlarını karşılamaktır.

---

## 📊 Evcil Hayvan Durumları

Durumlar tek bir dizi içinde tutulur:

| İndeks | Durum |
|------|------|
| 0 | Uyku |
| 1 | Tokluk |
| 2 | Susuzluk |
| 3 | Sevgi |
| 4 | Sosyalleşme |
| 5 | Tuvalet |
| 6 | Sağlık |
| 7 | Hijyen |

Tüm değerler **0 – 10** aralığında tutulur.

---

## ☠️ Oyun Kaybetme Koşulları

Aşağıdaki durumlardan **biri gerçekleşirse oyun sona erer**:

- Sağlık = 0
- Hijyen = 0
- Sevgi = 0
- Uyku = 0
- Tokluk = 0
- Susuzluk = 10
- Tuvalet = 10

---

## 🧩 Oyun Menüsü ve Fonksiyonlar

### 📋 Ana Menü Seçenekleri

1. Durumu Göster  
2. Yemek Ver  
3. Su Ver  
4. Oyun Oyna  
5. Uyandır  
6. Temizle  
7. Veterinere Götür  
8. Tuvalete Çıkar  
0. Oyundan Çık  

---

### 🍽️ Yemek Verme
- Yaş mama
- Kuru mama
- Vitamin

Tokluk, sağlık ve hijyen değerlerini etkiler.

---

### 🚰 Su Verme
- Su
- İksir
- Meyve suyu

Susuzluk, sağlık ve tuvalet değerlerini etkiler.

---

### 🎾 Oyun Oynama
- Yürüyüş
- Top oyunu
- Tarama

Sevgi, sağlık ve hijyen üzerinde etkilidir.

---

### 😴 Uyku
- 8 saat uyuma
- 3 saat uyuma
- Kısa kestirme

Uyku ve sağlık değerlerini artırır.

---

### 🧼 Temizlik
- Kum temizleme
- Diş fırçalama
- Duş aldırma

Hijyen ve sağlık artar.

---

### 🏥 Veteriner
- Sağlık, hijyen ve sosyalleşme maksimuma çıkar.

---

## 🔄 Durum Güncelleme Sistemi

Her işlemden sonra:

- Tüm durumlar **1 azalır**
- Değerler **0–10 arasında sınırlandırılır**
- Ölüm koşulları kontrol edilir

Bu sistem oyuna **zorluk ve gerçekçilik** katar.

---

## 🛠️ Derleme ve Çalıştırma

### Linux / macOS / WSL
```bash
gcc evcilhayvan.c -o evcilhayvan
./evcilhayvan
