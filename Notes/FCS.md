# FCS

- Frame Check Sequence hata sezme tekniğidir. İletim esnasında verinin bozulup bozulmadığını anlamaya yarar. Destination Address, Sender Address, Type, Veri Alanı alanlarındaki kombinasyonlardan 4 bitlik bir kod üretilir ve FCS kısmına yazılır. Kaynak ve alıcı FCS bilgilerini karşılaştırır. Aynı değilse veri bozulmuş demektir.
- Hedef veriyi aldığında aldığı iletime göre tekrar hesap yapıp FCS üzerine kaynak tarafından yazılan veriyi karşılaştırır.

