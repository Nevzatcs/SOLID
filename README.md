# SOLID

## Class and Object
Basit bir şekilde açıklamak gerekirse: 
Sınıfı, bir evin planı gibi düşünelim. Evin kapı, dolap rengi gibi özellikleri ve kapısının açılma şekli gibi fonksiyonları olabilir. Nesne de aslında bu plana göre inşa edilen tüm evlerdir. Buna araba örneği de dahil edilebilir. 

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
