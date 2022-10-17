# final

Erişim kontrol modifierıdır. Bir metodun ya da  değişkenin ilk değerini aldıktan sonra dışarıdan bir etkiyle bir daha değiştirilemeyeceğini garantiler.  

Bu yapı superclasslarda kullanıldığında extensionlar tarafından ilk değerin verilip bir daha değiştirilememesine olanak sağlar. Bunu da constructor metodlar yoluyla yapar. Superclassın constructorunda final değişken için bir değer istendiği zaman extensionlar kendi constructorlarında <super()> diyerek üst sınıfta final yazılmış olan değişkeni ilklemek zorundalardır.

[[Inheritance]]
[[Constructor Metodu]]


