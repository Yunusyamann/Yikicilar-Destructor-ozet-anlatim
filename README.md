# Yikicilar-Destructor-ozet-anlatim

C++ programlama dilinde, yıkıcılar (destructors), bir sınıf örneği (nesne) ömrü sona erdiğinde otomatik olarak çağrılan özel fonksiyonlardır. Yıkıcılar, bir sınıfın kaynaklarını (bellek, dosya tanıtıcıları, ağ bağlantıları vb.) serbest bırakmak veya temizlemek için kullanılır. Bir nesne yok edildiğinde, yıkıcı fonksiyon, nesneye ait kaynakları serbest bırakmak ve gerekli temizlik işlemlerini yapmak için kullanılır.

Yıkıcı fonksiyon, sınıf adının önüne "~" işareti konularak tanımlanır ve aynı ada sahip olur, ancak bir dönüş değeri yoktur ve parametre almaz. Herhangi bir parametreyle çağrılamaz, sadece nesnenin yaşam döngüsünün sonunda otomatik olarak çağrılır.

Aşağıda basit bir C++ örneği verilmiştir:


<pre style=”background-color: darkgrey; border: 2px dashed rgb(235, 243, 251); overflow: auto; padding: 5px; text-align: justify; width: 569.633px;”>
#include <iostream>
using namespace std;

class Kaynak {
public:
    Kaynak() {
        cout << "Kaynak oluşturuldu." << endl;
    }

    ~Kaynak() {
        cout << "Kaynak yok edildi." << endl;
    }
};

int main() {
    Kaynak kaynak;
    // İşlemler yapılabilir.
    return 0;
}

}</pre>

Bu örnekte, "Kaynak" adında bir sınıf tanımlanmıştır. Sınıfın yapıcısı (constructor) kaynak oluşturulduğunda çalışacak bir mesajı ekrana yazdırır. Yıkıcı fonksiyon ise kaynak nesnesi yok edildiğinde çalışacak bir mesajı ekrana yazdırır.

"main" fonksiyonunda bir "Kaynak" nesnesi oluşturulur ve işlemler yapılır. Program sona erdiğinde, "Kaynak" nesnesi otomatik olarak yok edildiğinde yıkıcı fonksiyon çağrılır ve "Kaynak yok edildi." mesajı ekrana yazdırılır.

Yıkıcılar, kaynakları düzgün bir şekilde serbest bırakmak veya temizlemek için kullanılır. Bu, bellek sızıntıları gibi kaynak tükenme sorunlarının önlenmesine yardımcı olur ve programın daha sağlam ve güvenilir olmasını sağlar.
