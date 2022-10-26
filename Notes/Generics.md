# Generics

Javada class veya method tanımlarında kullanılan temsili tiplerdir. Bir classın yazımında ileride bir tipten fazla metod alabileceği düşünülüyorsa, kullanılacak değişken ya da geri döndürülecek değerin tipi "< T >" şeklinde yazılır ve soyut, temsili bir tip biçiminde class tanımlanırken kullanılabilir. 

Generics yazıldığında buraya object altında herhangi bir sınıf gelebilir demektir. Fakat bu sınıf class veya method çağırılırken spesifik olarak verilmelidir.

Misal:
    ArrayList kullanırken arraylistin hangi elemanları tutacığını söylemek için "ArrayList< String >" şeklinde yazıyoruz. Burada String yerine binbir türlü class gelebilir. Bu binbir türlü class esnekliğini Arraylistin tanımı yazılırken generic type kullanılmasından geliyor.

Java'da genellikle collectionlar generic type kullanarak yazılır çünkü içinde ne tutacakları çağırıldıkları zamanda yazılımcı tarafından belirlenir. Bunun dışında çok sık kullanılan yapılar değillerdir. Collections dışında concurrentlarda, futuretaskte generic type kullanılıyor.

[[Java]]
[[Collections]]
[[Type]]
[[Class]]
[[Method]]
[[placeholder]]