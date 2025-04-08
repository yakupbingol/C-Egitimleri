# C# Egitimleri
# c# derslerim

c# dili nedir ve nasil yazilmalidir 

C# (C Sharp), Microsoft tarafından geliştirilen bir programlama dilidir. Genellikle .NET çerçevesi içerisinde kullanılır ve geniş bir uygulama yelpazesi için kullanılabilir, örneğin masaüstü uygulamaları, web uygulamaları ve oyunlar. C# yazmak için, genellikle bir metin düzenleyici ve bir derleyici gereklidir. Kod, belirli bir syntax kullanılarak yazılır ve sonra derlenir ve çalıştırılır.

**boxing** = object türünde ki bir veriyi kutulama demektir.
**unboxing**= kutulama yapıldıktan sonra kutu dışına çıkarmak istersek boxing yaparken veriyi nasıl kaydettiysek öyle çıkarırız. Örnek olarak boxing'e object eleman = "asd";   tarzında veri attık çıkarırken de string a =(string)eleman; tarzında çıkar yani verinin tipiyle çıkar.

**parse=** string bir diziyi   çevirmede kullanılır.
**break ve continue=** sadece döngülerde ve switchde kullanılır. Koşullarda kullanılmaz dikkat !!!!!!
r**eturn=**  return komutu her yerde kullanılır bir sınırı yoktur. Methoddan çıkmak için kullanılır.
**diziler =** dizi oluşturulurken eleman sayisini vermek zorundayiz.
**diziler.lenght=** dizide ki eleman sayisini return eder
**Array.Clear**= Diziideki elemanlarini degerini varsayan yapar (0)
**Array.Copy**= Diziiyi başka bir diziye kopyalar.
**Array.IndexOf** = Dizini icindeki harf ya da kelime aramamiza yardimci olur. Eger harf ya da kelimeyi bulursa buldugu indexi gönderir bulamazsa -1 degerini return eder
**Array.Reverse** = Diziyi ters cevirir.
**Array.Sort** = Dizi elemanlarini siralar

classlar içinde methodlar tanımlanır işlemler methodlarda gerçekleştirilir. class içinde sadece tanımlama yapılır işlem yapılmaz.

**Methodlar**;
[Erişim belirleyici] [geri dönüş tipi] [adi] ()
{
işlemler
}

nesneler her zaman RAM'in Heap kısmında oluşturulur. Değerler ,referanslar ve değişken isimleri Stackte oluşturulur.

**Overload Metodlar** = Metod isimleri aynı olmalıdır. Metodların parametre sayilari farkli olmalidir değilse parametre tipleri farkli olmalidir degilse parametre siralari farkli olmalidir. Overload çoklu yükleme demektir. Aynı isimde ki metotlari birleştirir ve seçmek istediğin metodu seçip işleme aldırırsın.

**Field** = nesnesin özelliklerini(property) için değer saklama alanıdır.Varsayılan durumda private yapılardır.Class içerisindeki tüm metotlardan erişilebilecek bir değerdir.
**Properties**= Nesnenin özellikleridir, kendi içinde metot barındırabilir.  sadece {} karakter kullanılır ve set get metodu vardır
string adi; // field
sınıf içerisindeki fieldları dışarı kontrollu bir şekilde açmamızı sağlayan yapılardır.
**Set Metodu =** Bir property''ye yeni bir değer atamak için kullanılır. Set metodu olmayan property'ler read-only durumundadır.
**Get Metodu=**  Bir property'nin değerini okumak için kullanılır.
**Constructer** = Constructer metod public olmalidir, geri dönüş degeri olmaz ve classın ismi ile aynı olmalidir. Eğer private kullanırsak constructer'i nesne oluşturmayı engelleriz.
**Static Constructer=** Normal constructerdan da önce calisir ve ilgili siniftan yapilan nesne taleplerinden ilkinde tetiklenirken sonrakilerde tetiklenmez. Static constructer bir sınıftan constructerdan da önce bir kere calisir.
**Garbage Collector=**    oluşturulan nesnenin işi bittiginde bellekte ona ayrılan yer boşaltılır. Bellek boşaltma işlemine denir ve nesnelerin bellekten ne zaman silineceğine karar verir.
**This**= sınıf içerisinde o sınıftan oluşturulan nesneleri temsil etmek için kullanılır.
**Arrayler**=  Eleman sayisini belirtmek gerekir, elemanlari atamasan da bellekte yer kaplar, performansi zayiftir, kod maliyeti vardir. Tek tipte deger alinir. Diziler doğrudan bellek erisimi saglar. Sabit boyutlu verilerde kullanışlıdır.
**ArrayList**= birden fazla tipte deger alir. Kullanımıı ArrayList arrayList = new ArrayList(); eleman ekleme için arrayList.Add() deriz. tip güvenligi saglamaz
**List** = Belirledigimiz tipte deger alir.Kullanımı List<int> list = new List<int>(); eleman eklemek icin list.Add() deriz. Dinamik boyutlara sahiptir.Eleman ekleme çıkarma kolaydır ve tip güvenligi sağlar
**Inheritance** = 2 ve ya da fazla farklı sınıfın ortak özelliklerini tek bir sınıf haline getirir. Kalıtım yoluyla diğer sınıflara aktarır
**Protected**= oluşturuldugu sınıfta ve o sınıftan kalıtım alan sınıflarda erişilir kalıtım almadıgı sınıflarda erişim saglayamaz.
kalıtım veren sınıf(base class) , kalıtım alan sınıf(derived class)

**Virtual** = base class içerisinde bir metot derived classlarda kullanılacaksa base classta ki metot virtual olarak tanımlanır.
**Override**= virtual olarak base classta tanımlanan elemanı derived classta yeniden şekillendirmemizi saglayan komuttur.

**Polimorfizm** = Çok bicimliliktir A referansta ki veriye B nesneyi aktarmadır.
**Abstract** = Abstract ile işaretlenen metot ve ya  propertyler bu sınıftan kalıtım alan her classtan uygulanmak , implement edilmek zorundadır. Gövdeleri tanımlandıkları class içinde yazılmazlar, geri dönüş ve isimleri ve erisim belirleyicileri tanımlanır.Private olamazlar.
Abstract classın nesnesi oluşturulmaz. Referans noktasını alınabilir.
İnterface=  aklımıza kalıtım gelmeli ,kendisinden kalıtım alan classlara kendi icerisinde o elemanların imzasını barındırır. Nesne oluşturulmaz ama referans noktasi olusturulabilir. Bir sınıf birden fazla interface ile kalıtım alabilir. İnterfaceler kendisinden kalıtım alan sınıfların içerisinde olması zorunlu olan yapıları tanımlar. Abstract classlara benzer imza özelligine. Sadece imza özelligi bulunur. İmzası bulununa interface kalıtım yoluyla gittigi classa imzasını zorla dayattırır.
