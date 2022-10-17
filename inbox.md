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



# 6.Java Dersi(Notlar)
encapsulationı anlamak basit ama IRL farklı. Ne private ne de get set tamamen yetmiyor. biraz da dışardan gizleme obfustacation mı neydi buna bi bak.

- Abstraction:
  - Karmaşık işleyişi dışarıdan gizlemek.
  - Inheritance polymorphism karmaşıklığı değil.
  - Her değişkeni private yazmaya alış. --> bu encapsulation
  - SağTık - SOurce - generate getter setter! --> encapsulation
  - Karmaşa varsa abstraction kaçınılmaz.
  - OOP için zorunlu değil. Hoca için encapsu, inheri ve polymor
  - bir class'tan instance alırken sağ tarafı yazsan verdiği hatadan sol tarafı bilgsayara yazdırabilirsin.
  - Arka planda bilinmeyen bir algoritmanın çalışması esas encapsu olarak görüyor hoca.--> yani encapsulation için abstraction esas diyor. 
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

# 7.Java Dersi (12.10.2022)
## Inheritance
- Javanın her yerine yayılmış kavram.
- Inheritance kalıtımdır ama biyoloji gibi değil.
- Kategorizasyon yapılan her şey olabilir. Hayvanlar, ilaçlar, e-ticaret sitelerindeki filtreler.
- OOPnin 3 temel ayağından biri 
- Inh nesneler arası ilişkidir. "IS A" ilişkisi kurar.
- Bir sınıfın başka bir sınıfın özelliklerini alması.
- **Ödev olarak gerçek hayattan aklımıza gelen herhangi bir inheritance uygulaması yazmak**
- Inheritance ortak özellikleri olan yerlerde kullanacağız
- Kodlar tekrar ettiğinde, method isimleri tekrar ettiğinde, kod copy paste yaptığımızda inheritance kullanılabileceğini fark etmeliyiz.
- Kodlar birbirine benzese de inheritance olacak diye bir kaide yok.
- Her classın kişiliği, karakteri olur.
- Kredi kartı ve banka kartı çok benziyor. Bu ikisi için bir parent yazılabilir.
- İki class için parent class yazılacağı zaman ortak özellikleri dikkate alınır. Bu özellikler parent class'te toplanır.
- Parent yazıldıktan sonra child classlara '"Child class" extends "Parent Class"' şeklinde yazılır.
- Child classlar için artık Parent class'in extensionlarıdır diyebiliriz.
- Banka kartı ve kredi kartı extends kart. Yani banka kartı ve kredi kartı, kart classının extensionlarıdır.
- Peki isimleri aynı ama içerikleri farklı metodlar varsa? O zaman @Override yazıp sonra metodu yazacağız.
- Parent child dediklerime Superclass ve Subclass diyorlar.
- Superclass > Subclass yani superclass içinde daha çok metod var.
### Kalıtımın Kalıtımı
- Kredi kartının daha da özelleşebileceği durumlar olabiliyor, mesela platin kart falan.
- Extension olan bir class'ı bir başka class extend edebilir.
- Böyle bir durumda super kimi çağırıyor? Nereye gitmesi gerekiyorsa oraya gidiyor. Eğer bir üstünde varsa oraya gider. Yoksa onun da bir üstüne.
- Birden fazla classtan aynı anda **extend** alınamaz. Hem oradan, hem buradan alayım olmuyor.
- Bunu yapamamasının sebebi süper deyince nereye gidecek gibi problemler oluyor.
- Fakat kalıtımın kalıtımının kalıtımının gibi bir yapı yapılabiliyor.
- Bir classı extend eden classlar var mı diye bakmak için 'Open Type Hierarchy' yapıyoruz. F4 kısayolu.
- Yazdığınız her class esasında Object classından gelir. Her classın başıdır.
- Bu bilgi bize gösteriyor ki object classından gelen methodların hepsini Override edebiliriz. Mesela toString() metodunu override ettik.
## Override
- Metot ezme. Extend edilen classtan aynı isimli metodu alıyoruz ama içini **farklılaştırıyoruz**.
- Bugün çalıştıklarımızı ezbere bilmek zorundasınız.
## final
- Override'a izin vermek istemiyoruz diyelim. Eğer superclassta tanımlarken 'final' dersek, metod değiştirilemez.
- Bu tasarımlar bizim hükmümüze kalmış, şu kesin final olmalı diye bir kaide yok.
- Peki bir değişkeni superclassta final yapsam ve onu superclassın constructor metoduyla değişken alıp ilk değerini versem?
  - Bunu yapınca subclasslar hata veriyor. Çünkü onlar superclassın constructırına riayet etmiyor. Riayet etmek zorundalar.
  - Final değişken superclassta olduğundan onun altında extend eden subclasslar üst tarafa o değişkeni vermek zorunda. Onu vermenin yolu da constructor metod.
  - Final değişkene ilk değerini verebilmek için superclassta constructor yazıyoruz. Bunu yazdığımız için subclasslar bu constructor'a kendi içinden istediği değişkeni vermek zorunda.
  - Bunu verebilmek için subclass constructır çalıştırıyor, bu constructor "super" keywordü ile superclassa istediği değişkeni veriyor. Super ilk çalışan metod olmak zorunda bu durumda.

## Protected erişim belirleyici
- Protected yaparsak dışarıdan, globalden erişim yapılamaz.
- class, package ve subclass tarafından erişilebilir.

## Soyut Class
- Super classımı abstract yapsam
- Abstract cclass içine concrete metod yazılabilir.
- Abstract metod da yazılabilir fakat bu extension classta override edilmek zorunda yoksa hata verir.
- Abstract sınıflar new yapılamazlar.
- O yüzden sınıfı oluştururken new yapılacak mı düşünmek gerek. Ona göre karar verilecek.
- Anonymous class, anonymous implementation
- Bu dersten öğrenecekler extends, override, super constructor.
- Gerçek Hayatta bir yapıyı alıp class olarak düzenleyip diğer classlara kalıtım ile extend etmek ve kurudğun sistemi açıklamak. Önemli olan açıklamak. Sistem muhteşem olmasına gerek yok.
- 

# 8. Java Dersi (15.10.2022)
- Inh sonrası insanların kafası karışabiiyor. Aksiyonları aktarmak zor olabiliyor.
- Soyut şeyleri aktarmak zor olabiliyor inh ile.
- Biz hep extend kullandık ama implement de kullanacağız.
## Polymorphism:
- Poly. "is a" ilişkisi kuruyor.
- List var altında arraylist, linkedlist var. Hepsi eleman tutuyor. Fakat arkada tuttuğu yapı esasında farklı çalışıyor. Burada list 'interface' oluyor.
- insan interface'i açalım. Bu insan direk özellikleri barındırmaz ama olması gereken özellikleri tutar.
- Extends uzatmak idi. Interfacede implement ediyoruz. Yani bir şeyi hayata geçiriyoruz.
- Interface de abstract classlar gibi içindeki metodların tekrar yazılıp tanımlanmasını istiyor.
- Abstract class ve interface farkına bakacağız.
- Implement mantığı extendsten farklı. Implement ile ne olduğundan değil ne yaptığından daha çok bahsedeceğiz.
- **Interface interface'den extend alabilir.** bunu araştırabilirsin.
- Interface ve abstract farkı:
  - biyolojide bildiğimiz kalıtım esasında burada polymorphism.
  - **Birden fazla interface implement edilebilir. Esas fark bu. Bir class sadece 1 classı extend ile alabiliyor ama bir class birden fazla infa implement edebilir.**
  -  Çoğunlukla, genelde, evvela interfaceler tanımlanır. Oradan implementasyonlar yapılır.
  - Infa ile çalışınca artık her şey soyut. Üstte bir class yok, super diye bir şey yok.
- "instanceof":
  - is **this** an instance of **this** şeklinde çalışan yapı.
  - Bize sorduğumuz class bunu implement ediyor mu ya da extend ediyor mu diyen yapı.
- able classlar diye bir tanım var. 

  