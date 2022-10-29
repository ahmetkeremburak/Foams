# Stack Memory

Stack hem bir data structure'ın hem de bir hafıza bölümünün adıdır. Bu notta hafıza kısmından bahsediyoruz.

Stack ya da *Call Stack* Runtime sırasında methodların sırayla çağırılıp initialize edildiği ve depolandığı, metodların içindeki primitive type değişkenlerin ve refence type değişkenlerin de reference kısımlarının depolandığı hafıza alanıdır.

Bahsedilen yapılar geçici olarak stackte depolanırlar. İşleri biten yapılar stackten pop metoduyla çıkarılır ve yeni elemanlar push metoduyla eklenir. Stack'te ilk giren eleman en altta kalır ve son giren eleman en üsttedir. Ekleme ve çıkarmalar üstten gerçekleşir. Buna **Last In First Out** yapısı denir. Hangi methodun nasıl girip çıkacapını otomatik olarak compiler belirler.

Stack, Heap'e kıyasla daha hızlı ve daha dengelidir fakat boyut olarak çok daha küçüktür. Çok fazla art arda işlem çağırılması ya da kötü yazılmış recursive işlemler stack yapısının alanının dolmasına sebep olabilir. Bu da stackoverflow hatasına sebep olur. Aynı durum Heap'te çok zor gerçekleşir fakat imkansız değildir. O zaman da OutOfMemory hatası alınır.


[[Heap Memory]]
[[Heap Data Structure]]
[[Stack Data Structure]]
[[Runtime]]
[[Type]]
[[Compiler]]
[[Java]]