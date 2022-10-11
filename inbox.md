# Inbox

- Here you can write disorganised notes to be categorised later
- Bullet points are useful, but it could be free form text as well
- Sometimes it's better to just get things off your mind quickly, rather than stop to think where it belongs
- But don't let this list get too long
- Move information to more specific documents and link to them.
  - This helps you navigate between documents quickly
  - For example, you can `Cmd`+`Click` (`Ctrl`+`Click` in Windows) this: [[todo]]
- Some notes don't end up making sense the next day
- That's ok, you can just delete them!
  - You can always find them in your git history, if you really need it!



# 6.Java Dersi
encapsulationı anlamak basit ama IRL farklı. Ne private ne de get set tamamen yetmiyor. biraz da dışardan gizleme obfustacation mı neydi buna bi bak.

- Abstraction:
  - Karmaşık işleyişi dışarıdan gizlemek.
  - Inheritance polymorphism karmaşıklığı değil.
  - Her değişkeni private yazmaya alış.
  - SağTık - SOurce - generate getter setter!
  - Karmaşa varsa abstraction kaçınılmaz.
  - OOP için zorunlu değil. Hoca için encapsu, inheri ve polymor
  - bir class'tan instance alırken sağ tarafı yazsan verdiği hatadan sol tarafı bilgsayara yazdırabilirsin.
  - Arka planda bilinmeyen bir algoritmanın çalışması esas encapsu olarak görüyor hoca. 
- Mutability:
  - Mutasyona uğrayabilme.
  - Immutable olmak class değişkenlerinin değişememesidir.
  - Classta her şeyi immutable yapmanın anlamı yok.
  - Nasıl immutable yapabiliriz?
    - Setter metodu yazmayız ama class içinde hala erişim vardır.
    - Final yapabiliriz, ama o zaman asla değer değişmez. En azından ilk değeri bir defa almak istiyoruz.
    - O zaman constructor metodu classa yazıp ona da dışarıdan değişken alabiliriz. Değişken final olur ama değeri dışarıdan instance alırken gelir ve o instance için değişmez.
    - İmmutable koşulları:
      - Değişken private olacak
      - Değişken final olacak
      - Setter metodu olmayacak
      - Class'ın final olması(Ultimate Immutability)
- Staticler:
  - Static değişmeyen değildir.
  - Erişim belirleyici de değil static.
  - Static ve final ara belirleyiciler gibi.
  - Static metod veya değişkene new yapmadan erişim sağlar. yani bir instance başatmadan dümdüz class adıyla çalıştırılabilir. Fakat bu tehlikeli. 
  - Static değişkenler classa yapışıktır. Yani yeni instance almadan kullanılan class direk olarak classı değiştiriyor ve yeni instance almanın bir anlamı olmuyor.
  - neden static önemli? Çünkü o olmasa main method gibi instance almadan çalışması gereken yapılar çalışmaz. Mesela main method varken main methoda bir constructor yazsan da çalışmaz.
  - Her yerden aynı değişkene erişmek istesek kullanabileceğimiz bir yapı ama bu OOP için ters bir olay.
  - Static için hocaya göre hiçbir gerek yok. Kullanmayalım kardeşim.
- Bir sonraki derse polymorphism ve inheritance olacak, evvelden kurcalayabilirsin.
- 

