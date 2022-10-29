# Heap Memory

Burada bilgisayarlar dair iki tabir olduğundan olay karışabiliyor. Aynı durumun daha fenası Stack için de geçerli.

**The Heap** RAM'deki bir alanın adı. **A Heap** ise bir çeşit Veri Yapısının adı.
Burada THE HEAP'ten bahsedeceğiz. Nam-ı diğer Dynamic Memory.  

*Runtime* esnasında primitive olmayan typeların, objelerin *değerlerinin* tutulduğu hafızadır. Stack aksine belirli bir erişim kuralı yoktur, tüm threadler tarafından erişilebilir. Fakat bu memory leak, fragmentation gibi çeşitli sıkıntıları beraberinde getirir.  

Heap denmesinin sebebi bir yığın halince sıra gözetmeden atanmış bir hafıza olması ve istenilen biçimde atanabilmesi(allocate) veya serbest bırakılabilmesidir(de-allocate).

Burada Stack'teki gibi kullanılmayan ögelerin otomatik temizliği yapılmaz. Bunu sağlayabilmek için Garbage Collector adı verilen yapılar kullanırız. Garbage Collector kullanılmayan eski objeleri heapten kaldırır ve hafıza tekrar kullanılabilir hale gelir. Bu sistem için heapte objeler Young Generation, Old Generation gibi kategorize edilirler.

Heap memory Stack'e göre oldukça büyüktür, fakat erişimi(processing time) daha yavaştır.

Runtimeda kullanılır ve runtime'ın sonuna kadar mevcuttur.

Çok fazla method çağıran işlemler ve kötü yazılmış recursive yapılar hafızayı tüketebilir. Bu durumda Heap için OutOfMemory hatası, Stack için stackoverflow hatası alınır.

[[Stack Memory]]
[[Heap Data Structure]]
[[Stack Data Structure]]
[[Runtime]]
[[Type]]
[[Object]]
[[Garbage Collector]]
[[Generations]]
[[Processing Time]]
[[Java]]