# String

Programlama dillerinde metin, yazı tipi değişkenlerin tutulmasına yarayan objedir. Javada bir char arrayini temsil eden obje olarak çalışırlan. Bu tanım önemli ve dikkat edilmesi gereken bir tanım. Birçok metodları vardır.

Java'da stringler immutable'dır yani değiştirilemezler. Bir string değişkenini değiştirdiğimizde, her seferinde yeni bir  string instance'ı yaratılır.

Stringlerin değerleri hafızanın özel bir yerinde tutulur. Buraya String Constant Pool denir. Bir string yaratıldığında, stringin değeri bu pool'da bir yere işaret eder. Aynı değeri taşıyan başka bir string yaratıldığında da pool'da aynı yeri işaret eder ve bize aynı değeri döndürür. 

Fakat eğer stringler üzerinde bir oynama yapılırsa veya yeni bir instance olarak string oluşturulup içine aynı değer yazılırsa pool'da işaret ettiği değer değişir ve iki string'in içeriği birbirine eşit olsa bile "==" operatörüyle kontrol ediğinde "false" dönecektir. Bunun sebebi "==" operatörünün string içindeki değere değil, değişkenin hafızada işaret ettiği yere bakması ve ona göre karar vermesidir.
Bunun üstesinden gelmenin yolu equals() metodu kullanmaktan geçer. Bu metod içeriğini karşılaştırır. 


[[Java]]
[[Nesneye Dayalı Programlama Dili]]
[[Type]]
[[Değişken]]