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



# 9. Java Dersi (17.10.2022)  

zafer onan github polymorphism
- extend implement ileride de dönecek Bunları iyi anlamak gerek.
## String ve Equals
- Javada stringler fazla önemli classlar.
- Sarıcı class diyebiliyor.
- Esasında bir byte array.
- Javada özel muamele görür stringler. String pool diye bir yere gider. Aynı stringler aynı yeri göstermeye çalışır(Nasıl???)
- İki değişkene aynı değeri yazarsak d1 == d2 dersek true yazar. İkisine de bir harf eklesek. tekrar eşit eşittir desek false çıkar.
- Çünkü eşit eşittir değerlerini değil hafızadaki yerlerini karşılaştırıyor. Neden?
- Stringler immutable olduklarından buna yeni harf ekleyince hafızada yerleri farklı yeri gösteriyor.
- Bu sebeple string classında "==" override edilmiştir.
- new String dediğimizde hep hafıza yeri farklı stringler gelir.
- Baştan substring alınırsa aynı string geri döndürülüyor. Baştan itibaren alınmazsa new String oluşturuluyor.
- Javada string için eşit eşittire girme.
- Stringleri arka arkaya birleştirme yolu string buffer ya da string builder. Stringbuffer thread safe halidir string bufferın
-     public static void asd()
    {
        StringBuilder temp = new StringBuilder();
        String temp2 = "";
        long milis1 = System.currentTimeMillis();
        for (int i = 0; i < 150000; i++)
        {
            temp.append("a");
//            temp2 += "a";
        }
        long milis2 = System.currentTimeMillis();
        System.err.println(temp.toString().length() + " (" + (milis2 - milis1) + ")");
    }
## Equals
- String için dedik ama sadece stringlerde değil.
- bir person classı üzerinden denedik.
- equals metodu tam da istediğimiz gibi çalışmıyor.
- O zaman override edeceğiz.
- Sağ tık ve source ile generate edebiliyoruz.
- kullanmak istetiğimiz classta bir equals metodu çağırıp eziyoruz. 
- Bu çok mu önemli ki override edip baştan yazacağız?
- önemli çünkü equals görmediğimiz yerlerde de arka planda kullanılıyor.
- mesela arraylistlerin remove metodunda equals ile karşılaştırıyor. Sileceği indexi öyle buluyor.


### Ders biraz erken bitti
- **Çarşambaya hashcode göreceğiz**
- hashcode hashmap ile alakalıdır.
- Çarşamba günü bunlara bakacağız, araştır da gel.
- Bonus Content: Dosya okuma yazma:
  - Javada çok kolaydır.
  - Stringbuilder genelde dosya okumayla kullanılıyor.
  - "ctrl + shift + /" basarak collapse all yapabiliriyoruz.
  - filereader ve bufferedReader var.
  - Buffered satır satır ya da belirli bir karakter sayısı ile okuyor.
  - nonblocking io??
  - file olarak dosyayı alıp, file'ı stream olarak okuyabiliyoruz.
  - InputStreamReader sadeecfile değil her türlü inputu okuyabiliyor çünkü byte olarak okuyor. zaten her şey byte.
  - bufferedWriter çalışması için fileWriter olarak çağırmak gerekiyor. **Kesinlikle close yapmak gerekiyor bufferedwriterı**.
  - StreamReader'a da bir bak.
  - postgreSQL azıcık bakabilirsin şşş sır bu sır.
  

# 10.Java Dersi (19.10.2022)
Ders evveli notlar.
- **Hashcode** javada her obje ile eşleştirilen bir integer değer.
- hashcode() metodu ise objelerin hashcode'unu döndüren, object sınıfına ait bir metod.
- Object sınıfına ait olduğundan her classta oluyor, user defined classlarda bile.
- Değeri equals() metodu ile aynı dönen objelerin **genelde** hashcodeları da aynıdır. Farklı objeler de genelde farklı hashcode döndürür.
- hashcode metodu equals() metodunu kullandığından eğer equals metodu yeniden tanımlanırsa hashcode metodu da yeniden tanımlanmalı.
- hashing nedir peki? dağıtmak, karmaşıklaştırmak anlamında. Hash functionlar verilen key değerini bir algoritmadan geçirir ve hash değeri üretir. Bu tek yönlü bir algoritmadır. Yani aynı key hep aynı hash değerini çıkartır fakat hash değeri geriye çözümlenip verilen key değeri bulunamaz.
- Collision - Farklı değerlerin aynı hash değerine tekabül etmesidir.
- Hash en çok hash table yapmak için kullanılıyor.
- MD5, SHA1, SHA2 password protection için kullanılan hash yöntemlerinden.
- Hash Table --> Burada key için bir hash value üretilir. Üretilen hash Value key için index görevi görür.
- İyi bir hash fonksiyonu tek yönlü olmalı ve collision yapmamalı.
- AMA yine de collision oluşabilir. Bunu nasıl çözebiliriz.
- Linear Probing: Eğer hashcode için bir key varsa, hashtable'da müsait bir sonraki yeri bulut keyi oraya atamak.
- Chaining: hash table linked listlerden oluşmuş bir array olabilir. eğer arrayde dolu bir yere başka bir eleman daha gelirse gelen elemanlar linked list olarak saklanabilir.
- Resizing hashtable: Belirli bir doluluğa erişinde %60 bu genelde, hash table kapasitesi iki katına çıkarılıyor. Bu hafızaya yük bindirir.
- Beni zorlayan konuları tekrar etmek. Mesela String ve StringBuilder, reader konuları. Son hash konuları beni özellikle zorluyor.
- 
## Ders Kısmı
### HashCode()
- Önemli metodlardan. HashMapte kullanılıyor.
- Nesnelerin otomatik bir hashcodu vardır.
- Bir classı instantiate ettiğimizde ona otomatik bir hashcode atanır.
- toString() içine bakalım. İçinde hashCOde metodunu kullanıyor.
- toStringi override ettik.
- HashSet ve HashMap kullanacağız.
- Sadece equalsı override etmek yetmiyor hashsette. hashCode da override edilmeli.
- Bize hashleri, keyleri ve equalsları gerekiyor.
- HashMapte ne yapacaz bakalım.
- Person ve vehicledan hashmap yapacağız. Person için hashcode ve equals evvelden override ettik.
- Vehicle classını oluşturuyoruz. Model marka var içinde. Constructor da var.
- Şimdi person ve vehicle mapleyelim.
- Hashmape eklerken her seferinde new ile instantiate ediyoruz.
### Pop-Quiz
- Javadaki Stack alanının ne işe yaradığını söyleyebilir misin?
- Encapsulation nedir? değişkenler ve get, set. fakat özelleştirilmiş get set.
- 3 Tane primitive değişkenlerin min-max değerlerini ve bit değerleri. Bu beni zorlar. Tek tek bakmak gerek.
- Bir sınıfın birden fazla constructoru olabilir mi? Bu da beni tongaya düşürürdü.
- JDK ve JRE farkı nedir?
- Bir class içinde bir metodu ille de new instance ile mi çağırmak gerekir?
- GC nedir ne yapar?
- Kerem, farkını ortaya koymk için üzerinden geçtiğimiz her şeyi hatırlaman gerekiyor. **Anki** burada elzem oldu.
- Erişim belirleyicilerini say.
- ArrayList ne işe yarar, nasıl çalışır?
- Bir Mapte ikili değerler tutuyoruz. Bu ikili değerlere ne isim veriliyor.
- Scanner classı ne işe yarar?
- Scanner dışarı output veriyor mu?
- Scannerda bu dediğimiz içerisi ve dışarısı nedir? Kara Kutu.
- Hiç class yazmadan java uygulaması yazabilir miyim?
- Polymorphism nedir? Bundan sonra soru kaçırmış olabilirim. Kayıtlara bak.
- Javada dizilerin indeksi kaçtan başlar?
- Dizilerin indeksi kaça gidebilir? n-1
- Dizinin uzunluğunun dışından eleman almak istesek ne hatası verir? ArrayOutOfBounds.
- Dizileri maksimum kaç boyutlu yazabiliriz?
- Enum nedir?
- Static nedir?
- Queue diye bir veri yapısı var. Ne işe yarar?
- Data Structureların bulunduğu package? Collections.
- Bir classın içinde hiç constructor yok ise bu classtan instance oluşturabilir miyim?
- "Map"lemek ne demektir?
- OOP programlamanın temel prensipleri? inheritance, polymorphism, inheritance, abstraction, mutability.
- Abstraction nedir?
- Abstract method var mı, nasıl?
- Abstract bir class new yapılır mı?
- Maplerin key value ikilisine ne isim veriyorduk? Key-Value Pair? Bunu bulamadım
- Constructor metodu olmadan nasıl new yapabiliyoruz?
- Fieldlar, classlar, packagelar ve metodların sıralaması nedir? Hangisi hangisinin içinde?
- Javada variable nerelerde yazılabilir? metod, class, parametre(?)
- this nedir?
- Byte Code nedir?
- Metodun yazılımını ezbere söyleyebilir misin?
- Javada neler static olabilir?
- Final ne demek?
- Class final olursa, metod final olursa, değişken final olursa her birinin özellikleri nedir, olursa nolur?
- 4 tane access modifier vardı neydi?
- Kalıtımın sınırı var mı?
- Birden fazla sınıftan kalıtım alınabilir mi?
- Enumlar nedir?
- Array list içinde neler tutabilir?
- Nasıl her şeyi tutabiliyor? Object dizisi ile.
- Constructor yazmadan nasıl classı çağırabiliriz? Esasında objectten çağırılıyor.
- Stack Overflow hatası nasıl oluşur?
- Bir hashmap içerisinden sadece keylerini ya da sadece valuelarını alabileceğin metodlar nelerdir?
- Kütüphaneler nedir?
- Kütüphanede main method olabilir mi? Olur ama doğasına aykırı. Bir amacı olmaz.
- Overload ve override farkları nedir?
- Stackoverflowdaki stack nedir, nasıl doluyor?
- Javada şu şundan extend alır dediğin 3 class ve superclassları örnek verir misin?
- Javada classlar metodlar değişkenler, hangileri abstract olabilir?
- Stack ileride bizim için çok önemli olacak, iyice bir bak. 

# 11.Java Dersi (22.10.2022)

## Exception Handling
- Konu exception. Beklenenden daha derin bir konu.
- Exception nedir , nasıl yakalanır(handle edilir)?
- Error, bu hatayı yaklayıp devam etmek istemezsin.
- Exception bunu yakaladım ama devam edebilirim, bildirebilirim sadece.
- Error daha ciddi hatalar.
- Throwabledan exception ve errorlar türüyor.
- ex.dan checked ve unchecked ex. türüyor.
- 7 / 0 yaptırdık ve ArithmeticException aldık.
- ctrl + shift + t ile arattık gittik hataya.
- Ex. mesajının altında stack trace yazıyor.
- Java oluşabilecek hata türlerini tanımlamış kendisi.
- Exception handling try-catch yazıp hatayı atlamak değil.
- try catch sabit bir yapı, yazılışı ezber.
- Ex. için metodlar var. printStackTrace(), getMessage(), getLocalizedMessage().
- Bu metodları catch bloğunda kullanarak ex. mesajını yazdırabiliriz.
- Try-Catch Driven development kötü bir uygulama geliştirme stratejisidir.
- Finally bloğu ise her zaman çalışıyor. Yapı esasında try-catch-finally. hata fırlatılsa da çalışıyor yani.
-  Try bloğunda bir şeyleri yaparsak hata fırlatsa bile orada olan değişiklikler yapılmış oluyor. Bir rollback durumu olmuyor.
- Bundan sebep istiyorsak değeri değişen şeyleri catch bloğunda biz yazarak rollback yapabiliriz.
- buradan bir best practice, try bloğunun içini kısa tut.
- Try içine If bloğu yazıp hataları randomize etti ._.
- Şu nu demek için hangi hatanın geleceğini her zaman bilemeyebilirsin.
- buna bir çözüm olarak birden fazla catch bloğu yazılıp değişken olarak farklı ex. çeşitleri yazılır. Fakat düz ex. değişkeni alan bir catch bloğu da tutuyoruz ki ön göremediklerimizi de yakalayalım. Düz ex. bloğu ile yakalamaya "tepeden ex. yakalamak" diyor.
- düz ex. bloğunu üste değil alta yazmamız gerek, çünkü o bütün ex.leri yakalıyor. O yakalarsa aşağıya gidemez catch blokları.
- Multicatch diye bir ifade de var. "or" mantık işlemi ile yapılıyor.
- catch (ArrayIndexOutOfBoundsException | FileNotFoundException e)
- üstteki şekilde yazılıyor.

## Call Stack
hocanın anlatmasından tam analayamadım.
## Checked ve unchecked
- Javada runtimeexceptiondan türeyen classlar uncheckedtir.
- Bu iki kavram ve throws kavramı iç içe geçmiş kavramlar.
- mesela file not found exception checked bir ex. FileReader yazınca filenotfound ex. throw ediyor.
- Throws eğer bir classta yazıyorsa onu try catch bloğu içine yazmak zorundayız. Bu hatayı fırlatabilir demektir.
- Sadece runtimedan türetilmiş olanlar throws ile yazılmıyor. Ondan ona try-catchi yazmaya bizi zorlamıyor.
- Manuel olarak da exception fırlatılabiliyor. "throw new ArithmeticException();" Bunu metodun içine yazabiliriz. O zaman ex. fırlatır.
- Throwable en tepedeki sınıftır.
- Throws fırlatabileceğini söyler.
- Throw manuel olarak hata fırlatmaktır.
- Aradan sonra kendi ex.lerimizi yazacağız.
- Aradan döndük.
- İleride birbirini çağıran metodlar olacak. Katmanlı tasarım.
- Bunun dışında javada sadece kendi ex.leri yok. Biz de ex. yazabiliriz.
- MyBusinessException
- İçinde sadece exception var diye throws ile yazılkabilir diye bir şey yok.
- Classı ex. türünden yazmak gerek.
- "extends" deyip exception almalı. Runtime Exceptiondan aldık örnekte.
- Kendi ex.imiz olduğundan getMessage metodunu override etmeliyiz. Ama edince super'den bir mesaj döndürüyor. Bunu böyle yapmak saçma.
- return ettiği şeyleri değiştirebiliriz. Biz bakiye yetersiz yaptık.
- Exception driven bir dizayn değil fakat bizim sistemimizde mantıklı olan exceptionları yazıp kullanmamız gerekir.
- İsmi uzun exceptionları seversiniz, size çok bilgi verir.
- Son bir saat kala sıkıştım, gidip geldim. O kısma bir daha bak.
- Olan bir exceptiondan kendi ex.imizi fırlatmak istersek rethrow diye bir şey yapıyoruz. O da var olan exception için catch yazıyoruz, onun içine throw ile kendi ex.imizi fırlattırıyoruz.
- Kerem iki
- Bir sonraki dersimizde annotationlar, reflectionlar ve genericler. 12.sunumda yazanlar. Bunları tek tek evvelden araştır.
- Bu üç konu çok önemli çünkü bu üçüyle tüm spring frameworkü yazabilirsin.
- Eski bilgiler üst üste bindi ve artık buralarda eski dersleri tamamen bilmen gerekiyor.
- Buraya kadar gördüklerimiz Java 101 idi. Bir sonraki dersler bir tık daha advanced.
- ALERT: Önceki dersleri tamamen bir tekrar et Kerem.
- Önümüzdeki 3 konudan sonra design patternlar, maven ve sonra spring geçiyor.
- ÖDEV: Dosya okumayla ilgili küçük bir ödev. Ödev 6. 
- Bir reader extension 'ı yazılması gerekiyor
kelime kelime okuma yapabilmesi gerekiyor
istediğim satır numarasını okuyabilmesi gerekiyor
String 'lerin Split fonksiyonu kullanılmayacak
ArrayList<String> kelimeler = myReader.readWords("C:/dosya.txt");
String satir = myReader.readLineAt(4);
Bir de soyada kaç satır var söyleyen bir metod yazabilirsiniz.



# 12.Java Dersi (24.10.2022)
Geçtiğimiz ödevi buffered reader extensionu olarak bir daha yaz.
Ulan ilk seferinde öyle yazacaktım.
## Generics
- Hayati önemi yok ama güzel konu.
- Esasında az az gördük. Küçüktür büyüktür arası yazdığımız ifadeler mesela. Mesela arraylist tanımlarken <>
- Javanın içindeler.
- Eğer generic type verilmezse mesela arraylist için, o zaman object tutan bir array list olur. Böyle bir array list de pek işe yaramaz.
- documentationa bakarsak arraylistte falan <E> yazar. E nedir? böyle bir class yok. E'nin manası generic typetır işte.
- Ne verirsen "E"linle, o gider seninle.
- Genericler hepsinin yerine geçebiliyor. Sadece temsili bir tip. Bunu neresi için tanımladıysak oradan kullanabiliriz. Class için başta tanımladıysak o class ile kullanabiliriz, o metodun başında kodladıysak o metod ile kullanabiliriz.
- Bu generic tipleri tanımlayıp ne yapacağız desek?
  - Sadece collectionlar böyle yazılır genelde.
  - Custon classlarda böyle generic type yazılmasına pek başvurulmaz.
- Elimde iki class var, person ve vehicle. Bu iki class arası bir ilişki kurmak istiyorum ama iki yönlü istiyorum. Yani bir aranın personı olabiir ama bir personın da arabası olabilir.
- Bu ikisini eşleştirmek ve ortak bir yere koymak istediğimde, Matcher diye bir class yaptık. O classa iki generic type verdik P, V. Bu iki type için dedik ki P extends Person, V extends Vehicle. 
- Onda bir işlem tanımladık ve persondan get name alıp vehicleden git metodu aldık.
-  class Matcher<P extends Person, V extends Vehicle>(){
-  P Person;
-  V Vehicle;
-  public islem(){}
}
- Dışarıdan bakınca bu OOP için çok elzem değil. Ama collection sınıflarında ne oldu kullanmadan belli olmayan, temsili tip kullanan yapılar için kullanılıyor.
- Java type safe olduğu için custom classlarda bunu değişken almak için kullanmak anlamsız olabiliyor.
- Concurrentlarda olabilir. Concurrent nedir ama ben bilmiyorum
- Kendi tiplerini tanımlayan bir classın extensionları da yukarıdaki tiplere saygı duymak zorunda ve onların verdiği tip şeklini almak zorunda.
- class MatcherExtension<P extends Person, V extends Vehicle> extends Matcher<P,V>
- **Alt class üst classtan daha geniş yazılabilir.**
- Eğer generic type sevdiyeniz androidde "asynctask"a bakabilirsiniz.
- why does futuretasks have generic type in java?
- Threadleri anlayamazsınız dedi, anlamaya çalış . 

# 13.Java Dersi (26.10.2022)

## Annotations

