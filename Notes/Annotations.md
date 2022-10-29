# Annotations

Java'nın derleme veya çalışma zamanında ihtiyaç duyabileceği bilgileri sağlar. Bu tanım önemli.

Özellikle kendi başına bir komut vermez veya işlem yapmaz.

@Annotation şeklinde yazılırlar. Sonlarında parantez alıp içlerine elemenetler alabilirler. @Annotations(value = "element")

Java'da predefined annotationlar var. Bunun yanında biz de kendi annotationlarımızı tanımlayabiliyoruz.

Yazılırken declarationların başına yazılıyor. Classlar, methodlar, fieldlar ve diğer yerlere de yazılabiliyor. Bunun yanında Type annotationlar typeların olduğu yerlerde de kullanılabilir. Bu tip annotationlar type checkingi kuvvetlendirmek için kullanılabilir.

java.lang tarafından kullanılan predefined annotationlar @Deprecated, @Override, ve @SuppressWarnings. Bunun yanında @SafeVarargs (Warning Suppressionla ilgili bir başka annotation) ve @FunctionalInterface annotationları da vardır.

Diğer annotationları etkileyen predefined annotationlar. Nâm-ı diğer meta-annotationlar. @Retention, @Documented, @Target, @Inherited, @Repeatable.

[[Java]]
[[Declaration]]
[[Class]]
[[Method]]
[[@Deprecated]]
[[@Override]]
[[@SuppressWarning]]
[[@SafeVarargs]]
[[FunctionalInterface]]
[[Retention]]
[[@Repeatable]]
[[@Documented]]
[[@Target]]
[[Inherited]]
[[Reflections]]