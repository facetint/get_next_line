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


## STACK - HEAP FARKLARI
| STACK | HEAP|
| :--- | :--- |
| Kullanımı kolaydır. | Kullanımı stack e göre daha karmaşık olabilir. |
| Bilgisayarda RAM’de tutulur. | Bilgisayarda RAM’de tutulur. |
| Oluşturulan değişkenler stack kapsamından çıkınca otomatik olarak yok edilir. | Bir blok içerisinde oluşturulan heap değişkenler, bloğun dışına çıktığında otomatik olarak yok edilemez, bunun manuel olarak yapılması gerekir. |
| Ulaşılması heap‘e göre daha hızlıdır. | Stack ile karşılaştırıldığında oldukça yavaştır. |
| Stack üzerinde kullanım fazla olduğunda alan yeterli olmayabilir.| Doğru kullanılmaması durumunda bellek sorunları yaratır. |
| Oluşturulan değişkenler pointer olmadan kullanılabilir. | Değişkenler pointer ile kullanılır. |
| Derleme zamanında oluşturulur. | Çalışma zamanında oluşturulur. |
| Kullanacağınız yerin boyutunu tam olarak biliyorsanız Stack‘i kullanmak sizin için uygun olacaktır. | İhtiyacınız olan boyutu tam olarak bilmiyorsanız Heap kullanımı daha iyi olacaktır. |




