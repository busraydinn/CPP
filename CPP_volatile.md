# `volatile` Nedir? Ne İşe Yarar? Neden Kullanırız?

`volatile`, bir değişkenin değerinin **program akışı dışında değişebileceğini** derleyiciye bildiren bir anahtar kelimedir.

Bu değişiklikler şunlardan kaynaklanabilir:

- ISR (Interrupt Service Routine – Kesme Fonksiyonu)
- Donanım register'ları (Memory-Mapped I/O)
- Başka bir thread
- DMA gibi harici donanım birimleri

---

## 🔧 Neden Gerekli?

Derleyiciler optimizasyon yaparken değişkenleri RAM yerine CPU içindeki **register'larda** tutabilir.

Bu performans açısından iyidir ancak bazı durumlarda sorun oluşturur:

- Donanım bir register değerini günceller
- CPU ise eski değeri register’da tutmaya devam eder
- Program güncel veriyi göremez

`volatile` kullanarak derleyiciye şunu söylemiş oluruz:

> “Bu değişken her an dışarıdan değişebilir, her erişimde bellekten oku/yaz.”

---

## 🧠 Teknik Olarak Ne Yapar?

`volatile`:

- Değişkenin register’da cache’lenmesini engeller
- Her erişimde gerçek bellek okuması/yazması yapılmasını zorlar
- Derleyici optimizasyonlarını sınırlar
- Dead Code Elimination gibi optimizasyonları engelleyebilir

---
