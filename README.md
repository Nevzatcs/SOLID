# SOLID

## Class and Object
Basit bir şekilde açıklamak gerekirse: 
Sınıfı, bir evin planı gibi düşünelim. Evin kapı, dolap rengi gibi özellikleri ve kapısının açılma şekli gibi fonksiyonları olabilir. Nesne de aslında bu plana göre inşa edilen tüm evlerdir. Buna araba örneği de dahil edilebilir. 

SOLID prensipleri, yazılım geliştirirken bakımı, anlaşılması kolay olan ve sürdürülebilir kod yazmamızı sağlayan prensiplerdir. Bu prensiplere uyarak; daha az hatalı,  kaliteli kodlar ortaya çıkarabiliriz.

S - Single Responsibility Principle

Her sınıfın yalnızca bir sorumluluğu olmalıdır. Böylelikle, bir fonksiyonumuz sadece bir işi yapar. Bu sayede daha yönetilebilir bir yapı kurmuş oluruz.  Bu kurala uymazsak ilerleyen süreçte kodumuz kontrol edemeyeceğimiz seviyede büyür ve kodun içinde kayboluruz. 
Örnek vermek gerkirse:

public class Car {
    public void printColour() {}
    public double calculatePrice() {}
    public void saveCarToDb() {}
}

Gördüğümüz gibi Car sınıfımızın 3 tane sorumluluğu var. Bu durumda SRP yi ihlal etmiş oluyoruz. 3 sorumluluğu ayrı sınıflara bölerek SRP yi takip etmiş oluruz.

O - Open Closed Principle

Nesnelerimiz, gelişime açık değişime kapalı olmalıdır. Nesnemizin mevcuttaki davranışına dokunmadan, yeni özellikler kazandırabilmeliyiz. 

L - Liskov Substitution Principle

Ana sınıftaki nesnelerin, alt sınıftaki nesnelerle yer değiştirdiğinde aynı davranışı sergilemesi gerekmektedir. Yani, bu değişiklik programın akışını bozmamalıdır. Bu prensibe göre, ana sınıfın nesnesini oluşturmak yerine alt sınıfın nesnensini oluşturursan problem yaşamamalısın.
Örnek vermek gerekirse; komşunun kuşunu besledin ve kuş öldü. Kuşun yerine oyuncak kuş koymak sorunu çözmeyecek.LSP, ihmal edilmiş olacak.

I - Interface Segregation 

Nesneler, kullanmadıkları interface lere bağımlı olmamaya zorlanmamalıdır. Ihtiyaç olunmayan metodların interfacede deklare edilmesi interface imizi gereksiz yere şişirir. Yani, farklı sorumluluklar için özelleştirilmiş farklı arayüzler kullanmalıyız.

D - Dependency Inversion

Üst seviyeli sınıflar, alt seviyeli sınıflara bağımlı olmamalıdır. Soyutlamalara bağımlı olmalıdır. Böylece, alt sınıfta yapılan değişiklikler üst sınıfı etkilemez ve üst sınıfta yapılan değişiklik alt sınıfta bir davranış bozukluğuna yol açmaz. 
