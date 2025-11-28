# C++ Nedir ?
C++ , C programlama dilinden geliştirilmiştir.
<br>C++ , C'ye Nesne Yönelimli Programlama (OOP) yeteneği kazandırmıştır.

# C++ Yapısı
C++ programları sınıf(class) ve fonksiyon (function) parçalarından oluşmaktadır.<br/>
"std::cout" standart output stream nesnesidir. ekrana çıktı verir. std:: namespace'in adını gösterir. usign ile kullanıldığında yazılması gerekmez.<br/>
"<<" stream ekleme operatörüdür. Sağındaki değeri output streame gönderir.
# Struct
Farklı veri tiplerini birleştirerek yeni bir veri tipi oluşturur. <br/>
Struct tanımı mutlaka";" ile sonlandırılmalıdır.<br/>
Bir struct yapısında her üyein adı farklı olmalıdır.<br/>
İki farklı struct aynı üyelere sahip olabilir.<br/>
Kendisini üye olarak alan bir struct yazılabilir.<br/>
Normal üyelere erişim sağlarken '.' , Pointer üyelere erişim '->' operatörü ile sağlanır.<br/>
# Class
Sınıf {} arasında tanımlaanır ve tanım ; ile sonlandırılmalıdır.<br/>
Sınıflar kendi üyelerinde erişimi sınırlandırabilirler.<br/>
Bu sınırlandırmaları erişim belirteçleri olan public,private,protected ile yaparlar. <br/>
# Constructor
Sınıf yapısının özel bir fonksiyondur. <br/>
Sınıf ismiyle aynı isme sahiptir. <br/>
Geri dönüş tipi yoktur. Parametre alabilirler. <br/>
Sınıftan bir nesne oluşturulurken çağırılırlar. Sınıf üyelerini hazırlarlar.<br/>
# Destructor
Sınıf isminin önüne ~ işareti konularak tanımlanır.<br/>
Nesne yok edilmeden önce yapılması gerekenleri yapar.<br/>
Fonksiyon aşırı yüklemesi yapılamaz. (Overloading) <br/>
Parametresi olamaz.
# Binary Scope Resolution (::)
Sınıfların üyelerine erişirken sınıf isminin de kullanılabilmesini sağlar. <br/>
Başka sınıflarında aynı isme sahip üyeleri olabileceği için geçerlidir. <br/>
# Erişim Alanı
Class Scope, File Scope , Fution Scope olmak üzere 3'e ayrılır.<br/>
Class Scope : Bir sınıfın üye ve fonksiyonları bu sınıf alanına sahiptir.<br/>
File Scope : <br/>
            Üye olmayan fonksiyonlar bu alanda tanımlanır.<br/>
            Erişim alanı içindeyken üye fonksiyonlara adlarıyla erişilebilir.<br/>
            Erişim alanı dışındayken üye fonksiyonlara nesne yada pointer araclığı ile erişilebilir.

