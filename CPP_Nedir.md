# C++ Nedir?
C++, C programlama dilinin üzerine inşa edilmiş, güçlü ve çok amaçlı bir programlama dilidir.  
C diline **Nesne Yönelimli Programlama (Object-Oriented Programming - OOP)** özellikleri kazandırarak daha modüler, yeniden kullanılabilir ve sürdürülebilir yazılım geliştirilmesini sağlar.

---

# C++ Program Yapısı
C++ programları temel olarak **sınıflar (class)** ve **fonksiyonlardan (function)** oluşur.

- `std::cout` : Standart çıktı (output) akış nesnesidir ve ekrana veri yazdırmak için kullanılır.  
- `std::` : Bir **namespace (isim alanı)** belirtir. `using namespace std;` ifadesi ile kullanımı sadeleştirilebilir.  
- `<<` : **Stream insertion (akış ekleme) operatörüdür**, sağındaki veriyi çıktı akışına gönderir.

---

# Struct (Yapı)
`struct`, farklı veri tiplerini bir araya getirerek yeni bir veri tipi tanımlamayı sağlar.

**Temel Özellikler:**
- Tanım `;` ile sonlandırılmalıdır.  
- Her üyenin (field) adı benzersiz olmalıdır.  
- Farklı struct'lar aynı üyelere sahip olabilir.  
- Bir struct, kendisini işaret eden bir üye (pointer) içerebilir.  
- Üyelere erişim:
  - Normal nesnelerde: `.` operatörü  
  - Pointer ile: `->` operatörü  

---

# Class (Sınıf)
`class`, nesne yönelimli programlamanın temel yapı taşıdır.

**Özellikler:**
- `{}` blokları arasında tanımlanır ve `;` ile sonlandırılır.  
- Veri (özellikler) ve davranışları (metotlar) bir arada tutar.  
- Erişim kontrolü sağlar.

**Erişim Belirteçleri:**
- `public` → Her yerden erişilebilir  
- `private` → Sadece sınıf içinden erişilebilir  
- `protected` → Türetilmiş sınıflardan erişilebilir  

---

# Constructor (Yapıcı Fonksiyon)
Constructor, bir sınıftan nesne oluşturulurken otomatik olarak çağrılan özel bir fonksiyondur.

**Özellikler:**
- Sınıf ile aynı isme sahiptir  
- Geri dönüş tipi yoktur  
- Parametre alabilir  
- Nesne oluşturulurken sınıf üyelerini başlatır (initialize eder)

---

# Destructor (Yıkıcı Fonksiyon)
Destructor, bir nesne yok edilmeden önce çalışan özel bir fonksiyondur.

**Özellikler:**
- İsminin başında `~` bulunur  
- Parametre alamaz  
- Geri dönüş tipi yoktur  
- Aşırı yükleme (overloading) yapılamaz  
- Kaynakların serbest bırakılması için kullanılır (örn. bellek temizleme)

---

# Scope Resolution Operator (`::`)
`::` operatörü, bir sınıfın veya namespace'in üyelerine açıkça erişmek için kullanılır.

**Kullanım Amaçları:**
- Sınıf dışından üye fonksiyon tanımlamak  
- Aynı isimli üyeler arasında ayrım yapmak  
- Namespace erişimi sağlamak  

---

# Erişim Alanları (Scope)
C++'ta değişkenlerin ve fonksiyonların erişilebilirliği belirli kapsamlar (scope) ile tanımlanır.

## 1. Class Scope
- Bir sınıf içerisinde tanımlanan tüm üyeler bu kapsamdadır.

## 2. File Scope (Global Scope)
- Sınıf dışında tanımlanan değişken ve fonksiyonları kapsar.  
- Programın farklı noktalarından erişilebilir.

## 3. Function Scope
- Bir fonksiyon içinde tanımlanan değişkenler yalnızca o fonksiyon içerisinde geçerlidir.  
- Fonksiyon dışından erişilemez.

---
