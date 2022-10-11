# Encapsulation
Sınıflar içindeki değişkenlere erişimin kontrolünü aynı sınıf içinde yazılan methodlarla sağlamaya encapsulation diyebiliriz. Encapsulation için bir object'e erişim bir mekanizma üzerinden kısıtlanmalı ve kontrol edilmelidir.  

Bir başka tanıma göreyse encapsulation datanın, değişkenlerin, o data üzerinde çalışan methodlarla bir araya getirilmesidir. Bana göre bu iki tanım birleşebilir. Yani encapsulation için data ve o datalara erişim için yazılmış methodlar bir class yapısıyla toparlanmalı, dışarıya erişimleri kontrol edilmelidir. Bu sayede sistemin karmaşıklığı azalır ve "Robustness" yani sağlamlığı artar.

Bu prensibe binaen bir class yazılacağı zaman değişkenler mutlaka **private** olarak tanımlanır ve **getter-setter** metodlarıyla dışarıya açılır.

[[Method]]
[[Class]]
[[Private]]
[[Getter]]
[[Setter]]
[[Abstraction]]
[[Information Hiding]]

