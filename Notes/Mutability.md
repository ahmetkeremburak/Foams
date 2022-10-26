# Mutability

Mutasyona uğratılabilir demektir. Bir değişkenin değiştirilebileceği anlamına gelir.
Değiştirilemez olması durumunda değişkene **Immutable** diyoruz. En basitinden Stringler immutable'dır. Yani bir defa yazılıp tanımlandıklarında üzerlerinde değişiklik yapılamaz.
OOP için immutable değişkenlerin tanımlanması, kullanılması gereken durumlar olabiliyor. Adı üzerinde değişkenler değişebilmesi ile namzet, fakat bir değişkene ilk değeri verildikten sonra değiştirilememesi işimize yarayabilen bir durum.  
Örneğin bir kişinin TC numarası ilk değeri verildikten sonra değiştirilmez. Kişi classı için TC değişkeni tanımlanır ve ilk değer alır fakat bir daha değiştirilememesi gerekir. Bunu sağlamanın çeşitli yolları var.
- Değişkenler **final** olursa asla değişemezler. Fakat bu biraz riskli çünkü ilk değerlerini dışarıdan almamız gerekebilir.
- **Setter** methodlarını class içine yazmazsak ya da private yaparsak dışarıdan erişip değiştirilemez. Fakat class içinden hala değiştirilebilirler.
- Class için yazılan **constructor metodu** class instantiate edilirken yazılır. Bu metoda değişken olarak *final* tanımlanmış değişkeni yazabiliriz. Böylece class instantiate edildiğinde değişken ilk değerini alır fakat final olduğundan bir daha değişmez.
- Son olarak da değişkenin geldiği class tamamen final olabilir. Böylece içindeki hiçbir şey değişmez. Fakat bu çok ters bir durum olur.

[[Nesneye Dayalı Programlama Dili]]
[[final]]
[[Setter]]
[[Constructor Metodu]]