<div align="center">
  
![image](https://github.com/facetint/get_next_line/assets/99668549/5d858c2e-acfa-4736-b1e9-7e7e05dfe2e1)

 </div>

# get_next_line
Bu proje, bir dosya veya dosya tanımlayıcısından (file descriptor) sırayla satırlar okumaktır.  Bu fonksiyon, özellikle metin dosyalarını satır satır işlemek veya girdi akışından veriyi satır bazında okumak için kullanılır. get_next_line fonksiyonu, veriyi okurken belleği etkin bir şekilde yönetmek için dinamik bellek tahsisi kullanır.

# AMAÇ

 **Satır Okuma:** Bir dosyadan veya dosya tanımlayıcısından okunan veriyi satır bazında ayırır. Her çağrıda bir satır okunur.
 
 **Bellek Yönetimi:** ** `get_next_line`**, bellek yönetimini otomatik olarak halleder. Bellek tahsisi yapar ve gereksiz belleği serbest bırakır.
 
 **Tekrarlanabilirlik:** ** `get_next_line`**, çağrıldığında bir sonraki satırı okur. Bu sayede bir dosyayı veya veri akışını sırayla işlemek için döngülerde kullanılabilir.
 
 **Hata Kontrolü:** Dosya sonu veya hata durumları kontrol edilir ve uygun şekilde işlenir.

🟥 `get_next_line` fonksiyonu, özellikle büyük veri dosyalarını satır satır okuma veya metin tabanlı protokollerle iletişim kurma gibi senaryolarda oldukça kullanışlıdır. Bu fonksiyon, kullanıcıya belirtilen dosya veya dosya tanımlayıcısından bir satır okuma yeteneği sunar ve bellek sızıntılarına karşı korur.


## KULLANIM ALANLARI

1. **Dosya Okuma Uygulamaları:** Metin dosyalarını satır satır okumak veya işlemek için kullanılır. Örneğin, bir metin belgesi içeriğini işlemek veya bir konfigürasyon dosyasını okumak için kullanılabilir.

2. **Veri Tabanı Yedekleme:** Büyük veri tabanlarını yedeklemek veya verileri başka bir biçime dönüştürmek için kullanılabilir. Verileri satır satır işlemek, büyük veri tabanlarının bellek sınırlarını aşmadan işlemeyi sağlar.

3. **Ağ İşlemleri:** Ağ protokollerini uygularken, gelen verileri satır satır okumak ve işlemek için kullanılabilir. Örneğin, bir HTTP sunucusundan gelen istekleri veya bir POP3 e-posta sunucusundan gelen e-posta mesajlarını işlemek için kullanılabilir.

4. **Log Dosyaları:** Log dosyalarını okumak ve log verilerini analiz etmek için kullanılabilir. Her satırı ayrı bir log girişi olarak ele alabilirsiniz.

5. **Veri Analizi:** Büyük veri setlerini analiz etmek için kullanılabilir. Her satırı işleyerek veri analizi işlemleri gerçekleştirilebilir.

6. **Komut İşleme:** Bir komut satırı uygulamasının girdisini satır satır işlemek için kullanılabilir. Örneğin, kullanıcı tarafından girilen komutları işlemek ve yanıtlamak için kullanılabilir.

7. **Metin Tabanlı Oyunlar:** Metin tabanlı oyunlarda olayları veya komutları işlemek için kullanılabilir. Her oyuncu hareketini veya eylemi bir satır olarak girer ve oyun bu girdilere yanıt verir.

🟥 **`get_next_line`** fonksiyonu, veri akışını veya dosyayı okurken bellek verimliliği ve işlem hızı önemli olduğunda kullanışlıdır. Veriyi satır satır işlemek, büyük veri kümeleriyle çalışırken bellek sınırlarını aşmamak ve işlem hızını artırmak için etkili bir yöntemdir.

## TERİMLER

  **Buffer Size** 
"Buffer size" (tampon boyutu), bir veri depolama alanının, genellikle bayt veya karakterlerin sayısı olarak ifade edilen, içerdiği verinin miktarını belirtir. Bu tamponlar, veri akışını veya veriyi okuma ve yazma işlemlerini daha verimli hale getirmek için kullanılır.Bu, özellikle dosya okuma, ağ iletişimi veya veri analizi gibi senaryolarda önemlidir.

**Read Fonksiyonu**
C programlama dilinde ve Unix benzeri işletim sistemlerinde kullanılan bir sistem çağrısıdır. Bu fonksiyon, dosya veya dosya tanımlayıcısından veri okumak için kullanılır.

<img width="579" alt="Ekran Resmi 2023-11-23 14 48 37" src="https://github.com/facetint/get_next_line/assets/99668549/0ded8caf-2865-410e-aa75-02bf512f516a">

**`read`** fonksiyonunun işlevi şu şekildedir:

1. **`fd`** ile belirtilen dosya veya dosya tanımlayıcısından, **`count`** ile belirtilen kadar veri okur.

2. Okunan veriyi **`buf`** işaretçisinin gösterdiği bellek alanına kopyalar.

3. Okunan verinin boyutunu döndürür. Başarılı bir okuma işlemi gerçekleştirilirse, dönüş değeri okunan bayt sayısını temsil eder. Eğer dosya sonuna ulaşıldıysa, 0 döner. Bir hata meydana geldiyse, -1 döner ve **`errno`** değişkenine hata kodu atanır.

ssize_t :  POSIX standardına (Portable Operating System Interface for Unix) dayalı işletim sistemlerinde kullanılan bir tamsayı (integer) veri türüdür. Bu veri türü, özellikle dosya işleme işlemleri sırasında kullanılır ve işlem sonuçlarını temsil etmek için tasarlanmıştır.

**`ssize_t`** veri türünün temel özellikleri:

1. **Negatif ve Pozitif Değerler:** **`ssize_t`**, hem negatif hem de pozitif tam sayı değerlerini temsil edebilir. Başarılı işlemlerde, pozitif değerler dönerken, hata durumlarında genellikle -1 gibi negatif değerler döner.

2. **Dosya Okuma ve Yazma İşlemleri:** **`ssize_t`**, özellikle **`read`** ve **`write`** işlevleri gibi dosya okuma ve yazma işlemlerinin sonuçlarını döndürmek için kullanılır. Bu işlevler, işlem sırasında okunan veya yazılan bayt sayısını **`ssize_t`** ile ifade eder.

3. **Hata Kontrolü:** Hata durumlarında **`ssize_t`** genellikle -1 değerini alır. Bu, işlemin başarısız olduğunu ve bir hata kodunun ayarlandığını gösterir. Hata kodu, işlemin neden başarısız olduğunu belirtir ve **`errno`** değişkeni üzerinden elde edilebilir.

4. **Taşma ve Bellek Verimliliği:** **`ssize_t`**, işlemler sırasında büyük veri miktarlarını temsil edebilir ve taşma sorunlarına karşı koruma sağlar. Aynı zamanda veri işleme sırasında bellek verimliliğini artırır.

**size_t ile farkı :   `size_t` işaretsiz bir veri türüdür,(unsigned) yani negatif değerleri temsil etmez. Bu nedenle `size_t`'yi negatif değerlerle karşılaştırmak veya negatif değerlerle kullanmak hatalıdır. `ssize_t` ise işaretli bir veri türüdür (signed) ve hem pozitif hem de negatif değerleri temsil edebilir.**

- **`size_t`**: **`size_t`**, özellikle bellek tahsis etme (malloc, calloc vb.) ve bellek boyutlarını temsil etme işlemleri için kullanılır. Pozitif tamsayı değerlerini temsil eder ve genellikle bellek ile ilgili işlemlerde boyutları ifade etmek için kullanılır. Bu tür, dizilerin veya bellek bloklarının boyutlarını ve indislerini saklamak için idealdir.

- **`ssize_t`**: **`ssize_t`**, dosya okuma ve yazma işlemlerinin sonuçlarını temsil etmek için kullanılır. Hem pozitif hem de negatif tamsayı değerlerini temsil edebilir ve genellikle dosya işleme işlemlerinin sonuçlarını saklamak için kullanılır. Bu tür, **`read`** ve **`write`** işlemleri gibi dosya işleme işlemlerinin sonuçlarını döndürmek için idealdir.

## BELLEK YÖNETİMİ

STACK - HEAP

<img width="701" alt="Ekran Resmi 2023-11-23 14 58 41" src="https://github.com/facetint/get_next_line/assets/99668549/d4eba745-73aa-486d-b8f8-ba8484121b3f">

## STACK 

▶︎ Stack Memory, işlemcilerin register bilgilerinin tutulduğu yerdir. Burada programınızla ilgili bilgiler (örneğin; lokal değişkenler, referans değişkenler vs) yer almaktadır. Bu memory, geliştirici tarafından değil, compiler tarafından yönetilir. Stack’teki bilgiler kodunuzun derleme aşamasında, direk bellek içine yerleştirildiği için erişimi oldukça hızlıdır.

▶︎  Biz geliştiriciler için çok önemli olmasa da, programımız işlemci üzerinde çalışabilmek için sürekli stack belleğini arar. Her lokal değişken ve çağrılan her fonksiyon buraya gider. Genellikle istemeden de olsa stack üzerinde birçok hatalarla karşılaşabiliriz. Sıklıkla karşılaştığımız *stack buffer overflow* ve *incorrect memory*’ye erişmeye çalışmak bu hatalardan bazılarıdır.

▶︎ Öncelikle stack bir LIFO (Last In First Out) data structures’dır. Somutlaştırmak adına LIFO’yu şöyle düşünebiliriz:

İçine kitapların yalnızca üst üste yerleşebildiği kapağı açık boş bir kutu düşünün. Örnek olarak, kutuya üst üste 5 kitap koydunuz. Kutudan çıkaracağınız ilk kitap 5. koyduğunuz kitap olacaktır. Yani son giren 5. kitap ilk çıkacak kitaptır. LIFO dediğimiz olay da tam olarak budur. Aşağıdaki görselle de bunu somutlaştırabilirsiniz.

![Untitled](https://github.com/facetint/get_next_line/assets/99668549/39a2d15c-9809-427e-b7a8-ac2449a6acdd)

Bu yapıyı kullanan bellek, iki basit işlem ile süreci yönetmektedir.

**Push & Pop**

▶︎ Bu iki işlem birbirlerinin tam olarak tersidir. Push, programdan gelen bir değeri stack’in üzerine eklerken, pop is en yüksek değeri stack’ten çıkarır, boşaltır.

▶︎ Pointer, fonksiyon döndükten sonra, stack üzerinde herhangi bir kontrole sahip değildir. Bu nedenle compiler, bilgileri stackten boşaltır (pop operasyonu) ve gerektiği gibi kullanır. Fakat fonksiyondan döndükten sonra, dizinin içeriğini doldurmaya çalıştığımızda bellek bozulur (memory corruption) ve mis gibi bir “segfault” yeriz.

<img width="977" alt="Ekran Resmi 2023-11-23 17 06 25" src="https://github.com/facetint/get_next_line/assets/99668549/5a18b55c-6a78-4d66-9ec8-d116763c6d96">

▶︎ Yukarıdaki gibi bir pop-push operasyonunda, belleğe girip çıkacak değerlerin takibini yapabilmek için Stack Pointer adı verilen özel bir işlemci register’ı vardır. Geliştiriciler, lokal bir değişken veya fonksiyonun dönüş adresi gibi belleğe sürekli bişeyler kaydetmeye çalışır. Bu senaryoda stack bir değeri pushlar ve pointer ı yukarı taşır. Program fonksiyondan her çıktığında ya da tanımlanan değişkenler kaybolduğunda, stack memory bu değerleri pop eder. Böylece belleğin daha verimli kullanılmasını sağlar.


## HEAP

▶︎ Heap Memory, bellek üzerinde yer tahsisi yapılan belli bir bölümdür. 

▶︎ Bu yer, bellek üzerinde “malloc” fonksiyonu aracılığıyla tahsis edilir ve heap üzerinde allocate edilen(yer tahsisi yapılan) bellek “free” lenerek tekrar kullanım için serbest bırakılır.

▶︎ Heap’teki bellek kullanımı compiler tarafından değil, geliştiriciler tarafından kontrol edilir. Karmaşık programlar oluştururken, genellikle büyük bir bellek alanına ihtiyaç duyarız. Bu durumda Heap Memory kullanırız.

▶︎ Heap üzerinde allocate ettiğimiz bellek operasyonuna “dynamic memory allocation” adı verilir.


## HEAP BELLEK AVANTAJLARI

▶︎  Heap'in bellek boyutunda herhangi bir sınırı yoktur.

▶︎  Değişkenlere global olarak erişmenizi sağlar.

▶︎  Çöp toplama, nesnenin kullandığı belleği boşaltmak için yığın belleğinde çalışır.

▶︎  Öncelik Kuyruğunda da yığın yöntemi kullanılır.


## HEAP BELLEK DEZAVANTAJLARI

▶︎  Stack ile karşılaştırıldığında yürütülmesi çok fazla zaman alır.

▶︎  Hesaplamak daha fazla zaman alır.

▶︎  Bir işletim sisteminin sağlayabileceği maksimum belleği sağlayabilir.

▶︎  Heap belleğinde bellek yönetimi küresel olarak kullanıldığından daha karmaşıktır.

  
## STACK - HEAP FARKLARI
| PARAMETRE | STACK | HEAP|
| :--- | :--- | :--- |
| Temel | | Bellek bitişik bir blok halinde tahsis edilir. | | Bellek herhangi bir rastgele sırayla tahsis edilir. |
| Bellek Tahsisi | | Derleyici tarafından otomatik olarak yapılır.| | Programcı tarafından yapılır. |
| Maliyet | | az | | daha fazla |
| Uygulama || Kolay. | Daha zor. |
| Erişim süresi || Ulaşılması daha hızlıdır. | | Daha zordur. |
| Ana Konu || Bellek yetersizliği | | Bellek parçalanması |
| Referans yeri | | Harika | | Çalışma zamanında oluşturulur. |
| Güvenlik || Kullanacağınız yerin boyutunu tam olarak biliyorsanız Stack‘i kullanmak sizin için uygun olacaktır.| | İhtiyacınız olan boyutu tam olarak bilmiyorsanız Heap kullanımı daha iyi olacaktır. |
| Esneklik || Derleme zamanında oluşturulur. | | Çalışma zamanında oluşturulur. |
| Veri türü yapısı || Derleme zamanında oluşturulur. | | Çalışma zamanında oluşturulur. |
| Tercih Edilen || Derleme zamanında oluşturulur. | | Çalışma zamanında oluşturulur. |
| Boyut || Derleme zamanında oluşturulur. | | Çalışma zamanında oluşturulur. |



