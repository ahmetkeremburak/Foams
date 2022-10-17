# Constructor Metodu

Classların sahip olabileceği özel bir metoddur. Classlar instantiate edildiğinde ilk bu metod çağırılır ve çalıştırılır. Bu nedenle bu metod değişkenlere ilk değerini vermek için kullanılabilir.  
Özellikle inheritance'da superclassların constructor metodunda değişkenler initialize edildiğinde superclassın extensionları da kendi constructorlarını çağırıp <super()> metoduyla istenilen değişkenlere değerlerini vermek zorundadır. Bilhassa bu yöntem superclassta final olarak yazılan değişkenlere ilk değerlerini vermek üzere kullanılabilir.

[[Inheritance]]
[[final]]