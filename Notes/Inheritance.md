# Inheritance

Kalıtım anlamına gelen inheritance bir sınıfın başka bir sınıfın özellikleri üzerine almasını sağlar. Nesneler arası "is a" ilişkisi kurar. Kategorizasyon yapılan her nesnede kullanılabilir. Misal hayvanlar, insanlar, e-ticaret sitelerinde filtreler gibi.  

Her classın kendi kişiliği ve karakteri vardır. Bu yapı ile classların paylaştığı ortak özellikler bir üst classta, Superclass'ta, toplanabilir.Bu toplanan özellikleri üst class alttaki classlara *uzatır.* Syntaxı "class1(subclass) extends class2(superclass)" şeklinde yazılır ve class1 class2nin bir *extension*ı olur. Bir extension yalnızca bir tane üst classı extend edebilir. fakat bir üst class sayısız classa paylaşılabilir. Kalıtım alan classlar başka classlara kalıtım verebilir ve böylece bir silsile oluşturulabilir. Mesela Javada her class Object classından gelir. Bu da demek oluyor ki object classının metodlarını override edebiliriz.  

Yalnızca bir sınıf extend edebilme sebebi super metodu kullanıldığında bir üst classa bakmasıdır. Birden fazla üst class olursa nereye bakacağı karışabilir.

F4 ile bir classın ilgili olduğu classlar ve intercelere bakılabilir. <instanceof()> yapısı kullanılarak bir class başka classı extend ediyor mu öğrenilebilir.

[[Polymorphism]]
[[Override]]
[[final]]
[[Abstract Class]]

