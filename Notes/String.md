# String

Programlama dillerinde metin, yazı tipi değişkenlerin tutulmasına yarayan objedir. Javada bir byte arrayini temsil eden obje olarak çalışırlar. Bu tanım önemli ve dikkat edilmesi gereken bir tanım. Stringler bir byte arrayi ama CharSequence interface'ini implement ediyor. Birçok metodları vardır.

Java'da stringler immutable'dır yani değiştirilemezler. Bir string değişkenini değiştirdiğimizde, her seferinde yeni bir  string instance'ı yaratılır. Bu sebeple string ekleme ve değiştirme işleri String üzerinden değil StringBuilder ve StringBuffer üzerinden yapılıyor. 

Stringlerin değerleri hafızanın özel bir yerinde tutulur. Buraya String Constant Pool denir. Bir string yaratıldığında, stringin değeri bu pool'da bir yere işaret eder. Aynı değeri taşıyan başka bir string yaratıldığında da pool'da aynı yeri işaret etmeye çalışır ve bize aynı değeri döndürür. 

Fakat eğer stringler üzerinde bir oynama yapılırsa veya yeni bir instance olarak string oluşturulup içine aynı değer yazılırsa pool'da işaret ettiği değer değişir ve iki string'in içeriği birbirine eşit olsa bile "==" operatörüyle kontrol ediğinde "false" dönecektir. Bunun sebebi "==" operatörünün string içindeki değere değil, değişkenin hafızada işaret ettiği adrese bakması ve ona göre karar vermesidir.
Bunun üstesinden gelmenin yolu equals() metodu kullanmaktan geçer. Bu metod içeriğini karşılaştırır. 


[[Java]]
[[Nesneye Dayalı Programlama Dili]]
[[Type]]
[[Değişken]]
[[Equals]]
[[StringBuilder]]
[[StringBuffer]]
[[String Pool]]
[[Mutability]]
[[Reference]]
[[Heap Memory]]
[[BufferedReader]]