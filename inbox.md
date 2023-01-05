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


# AnkiFactory

# Tekrar Notları


## Spring Boot Hakkında
- application.properties dosyasında db'ye bağlanmak için gereken bilgileri vermeliyiz. Bu boot kullanmadan evvel web.xml dosyasının içinde verilebiliyordu veya bir @Configuration classı içinde veriliyordu. Bootta application.propertiesde.
### JPA ve Hibernate hakkında
- application properties içerisine hangi veri tabanını kullandığımıza dair hibernate'e bir bilgi vermemiz gerekiyor.Bu bilgiyi verirken **spring.jpa.properties.hibernate.dialect =org.hibernate.dialect.PostgreSQL10Dialect** şeklinde propertiese ekliyoruz.
- **spring.jpa.hibernate.ddl-auto** ayarına create, create-drop, none, update, validate diyerek uygulama her ayağa kaldırıldığında DB'ye nolduğunu ayarlıyoruz.
- Hibernate object relational mapping ile biz modellerin içine başka model sınıflarından bir nesne verdiğimizde aradaki bağı, yani "join"lemeyi kendisi yapıyor. 