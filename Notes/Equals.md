# Equals

İki objenin eşit olup olmadığını anlamak için kullanılan method. Normalde iki objenin değerini değil referansını karşılaştırıyor ve uygun boolean değerini döndürüyor. Fakat stringler, integerlar gibi classlarda bu method tanımlanırken özellikle aldığı değişkenlerin değerini karşılaştırması için modifiye edilir. java.util.Objects pakedinden gelme bir methoddur.
Custom classlarda da equals metodu değişkenleri doğru karşılaştıracak şekilde yeniden tanımlanmalı. İleride hataya sebep olur, arraylist, hashcode gibi yapılar doğru çalışmaz. 

[[Method]]
[[Java]]
[[String]]
[[Hashcode]]
[[Reference]]
[[java.util]]
[[Object]] 
