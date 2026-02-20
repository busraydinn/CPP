## 📌 Const vs Constexpr (C++)

C++’ta sabitler için iki temel seçenek vardır: `const` ve `constexpr`. Aralarındaki farkı bilmek modern C++ yazarken performans ve güvenlik açısından önemlidir.

```cpp
#include <iostream>

// constexpr -> derleme zamanında sabit
constexpr int BUFFER_SIZE = 1024;

// const -> runtime sabiti (compile-time olmayabilir)
const int maxClients = 100;

int main() {
    char buffer[BUFFER_SIZE];  // compile-time sabiti olduğu için güvenli
    std::cout << "Max clients: " << maxClients << std::endl;
    return 0;
}
```
## ⚡ Const ve Constexpr Kullanım Alanları

### 1️⃣ Genel Kullanım Alanları

| Tür        | Kullanım Alanı | Açıklama |
|------------|----------------|----------|
| `const`    | Sabit değerler | Runtime veya compile-time sabitler. Örn: kullanıcı girişi sonrası değişmeyecek değerler |
| `constexpr`| Compile-time sabitler | Dizi boyutları, template parametreleri, derleme zamanı hesaplamaları, matematiksel sabitler |

### 2️⃣ TCP Server / Network Programlama Örneği

| Tür        | Kullanım Alanı | Örnek |
|------------|----------------|-------|
| `constexpr`| Buffer boyutu | `constexpr int BUFFER_SIZE = 4096; char buffer[BUFFER_SIZE];` |
| `constexpr`| Sabit port numarası | `constexpr int PORT = 8080;` |
| `const`    | Maksimum client sayısı (runtime config olabilir) | `const int maxClients = config.getMaxClients();` |
| `const`    | Timeout veya ayar değerleri (config üzerinden) | `const int TIMEOUT_SEC = config.getTimeout();` |

### 💡 İpuçları

- Compile-time bilinen değerler → `constexpr`  
- Runtime’dan gelen veya config dosyasından okunan değerler → `const`  
- TCP server gibi network uygulamalarında buffer boyutları, port gibi değerler genellikle `constexpr` ile güvenli ve hızlı tutulur.  
