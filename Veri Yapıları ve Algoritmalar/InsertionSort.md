# Insertion Sort Methodu

Insertion sort methodu, en basit tabiriyle verinin en başından en sonuna kadar kontrol edilip bulunan en küçük terimin,
dizinin en başına taşınması ve bu işlemin son veriye kadar devam ettirilmesidir. 
Mantığı basit olmasına karşın pratikte çok hızlı çalışmayabilir. Gelin bunu size bir örnekle açıklayalım.

> [22,27,16,2,18,6]

Bize sıralanmamış halde verilen bu veri dizisini gelin birlikte sıralayalım.

## *1. Adım*

Başlangıçta  [22,27,16,2,18,6] halinde olan dizimizin en küçük verisi '2'.
Methodumuz bütün diziyi tarayarak '2' ile '22'nin yerlerini değiştirecek ve ilk adımda bize
[2,27,16,22,18,6] dizisini oluşturacaktır. Bu işlem için methodumuz 6 farklı veriyi kontrol etmiştir.

## *2. Adım*

Artık methodumuz '2' verisinin dizinin en küçük verisi olduğunu biliyor. Bu yüzden artık bu veriyi kontrol etmesine gerek yok.
Bu adımda methodumuz artık geriye kalan 5 veriyi kontrol edecek ve '2' den sonraki 
en küçük veri olan '6' yı ikinci sırada bulunan '27' ile değiştirecek. Dizinin son hali ise;
>[2,6,16,22,18,27]

## *3. Adım*
Bu adım da benzer şekilde gerçekleşecek fakat burada tekrardan dikkat etmemiz gereken
konu methodun daha önceden bulup dizinin başına yerleştirdiği elemanları artık tekrardan kontrol
etmiyor oluşu. Bu da bu adımda artık kontrol edilecek 4 verinin kaldığı anlamını taşımakta. Dizinin bu adımdaki hali ise bu şekilde;
>[2,6,16,22,18,27]

Görüldüğü üzere dizide bir değişiklik olmadı çünkü kalan veriler arasında en küçük olan '16' zaten olması gerektiği yerde!

## *4. Adım*

Kalan 3 veri arasındaki '18' , '22' ile yer değiştirecek ve;
>[2,6,16,18,22,27]

 *Voila!* dizimiz artık sıralı halde. Peki.. methodumuz tamamlanmış oldu mu?

## *5 ve SON!*

4.adımda amacımıza ulaşmamıza rağmen methodumuz bunun farkında değil ve sıralama işlemini doğru yaptığından emin olmak için
methodu son adıma kadar yani 5. adıma kadar götürecek ve kalan son iki veriyi de birbiriyle karşılaştırıp sonuca ulaşacaktır.

Anlaşıldığı üzere Insertion methodu sonucu ne zaman aldığına bakmaksızın barındırdığı veri sayısı kadar
(örneğimizde 6 idi) işlem yapmıştır. 
1. işlemde 6
2. işlemde 5
3. işlemde 4
4. işlemde 3
5. işlemde 2

Şeklinde işlemleri alt alta yazdığımızda toplam işlem adedimizin;
> veri adedi * (veri adedi+1) / 2

Bir başka gösterimle

> n * (n+1) / 2

Olduğunu görmemiz çok kolaylaşacaktır. İfademizi sadeleştirdiğimizde ise;

> n<sup>2</sup>

İfadesini elde ediyoruz. Bu da bize Insertion sort ifadesinin karmaşıklık ölçütü
yani **Big-O Notasyonu** *O(n<sup>2</sup>)* verir.


### Pekiii.. NE?!

Şaşırdığınızı duyar gibiyim. Benim hatam. Size önce bilmemiz gereken bazı hususlar hakkında bilgi vereyim

**Time Complexity**
: Verilen veri setinin belirli bir algoritmaya göre analiz edilme zorluğu ya da uzunluğu anlamına gelir. Bu durumları anlatmak üzere üç farklı senaryo mevcuttur.
- *Worst Case*: Verilen seriyi sıralamak için max. eforu harcamak. örn: Küçükten büyüğe sıralanmak için verilmiş verinin büyükten küçüğe sıralı olması.
- *Best Case*: Worst Case in aksine min. eforla işlemi halletmek. örn:Küçükten büyüğe sıralanmak için verilmiş verinin hazır sıralı verilmesi.
- *Average Case*: bu iki durumun arasında kalan bütün durumlar. Gerçek hayat pratiğine en uygun olasılıklar bu durumda karşımıza çıkar.

İşte bu ayrımı yapmamızı sağlayan karmaşıklık ölçütünün adı da **Big-O** Notasyonudur.
Verilen algoritmanın işlem karmaşıklığını diğer algoritmalarla karşılaştırmamıza yarayan
karmaşıklık (compexity) ölçütüdür.

---
Buna göre ilk örneğimize, daha doğrusu sort edildikten sonraki haline bir göz atalım;
>[2,6,16,18,22,27]

Bu ifadeden '18' ifadesini bulmak hangi duruma girer?

Hep bir ağızdan "Averageeeee" diye bağırdığınızı duyar gibiyim. Evet! Verilen dizide '18' i bulmak bizim ne "best"ne de 
"worst" case'imiz olacaktır. Verilen dizide '2' best case, '27 ' worst case, kalan bütün değerler ise average case olacaktır.


# Yazımızı bitirmeden önce..

Sizlere veda etmeden önce yazımızın başlığı olan Insertion sort metodu hakkında son bir örnek daha tamamlamak istiyorum.
Bu örnekte herhangi bşr açıklama yapmadan direkt olarak adımları sıralayacağım. Bakalım siz de ipucu ve ya yönlendirme olmadan
doğru adımlarla sıralama yapabilecek misiniz? Herkese kolay gelsin!  :blush:


- Adım 0:
>[7,3,5,8,2,9,4,15,6]
- Adım 1:
>[2,3,5,8,7,9,4,15,6]
- Adım 2:
>[2,3,5,8,7,9,4,15,6]
- Adım 3:
>[2,3,4,8,7,9,5,15,6]
- Adım 4:
>[2,3,4,5,7,9,8,15,6]
- Adım 5:
>[2,3,4,5,6,9,8,15,7]
- Adım 6:
>[2,3,4,5,6,7,8,15,9]
- Adım 7:
>[2,3,4,5,6,7,8,9,15]


# *Tebrikler!!!* 🎉