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

**fd :   Veriyi okuyacağınız dosya veya dosya tanımlayıcısının (file descriptor) numarasıdır. Dosya tanımlayıcısı, dosyaya veya diğer veri kaynaklarına erişim sağlar.**

**buf :  Okunan verinin saklanacağı bellek alanını gösteren bir işaretçidir. `read` fonksiyonu, okunan veriyi bu bellek alanına kopyalar.**

**count :  Okunacak verinin maksimum boyutunu belirten bir tamsayıdır. `count`, `buf` işaretçisinin gösterdiği bellek alanının boyutunu aşmamalıdır.**

**ssize_t :  POSIX standardına (Portable Operating System Interface for Unix) dayalı işletim sistemlerinde kullanılan bir tamsayı (integer) veri türüdür. Bu veri türü, özellikle dosya işleme işlemleri sırasında kullanılır ve işlem sonuçlarını temsil etmek için tasarlanmıştır.**

**`ssize_t`** veri türünün temel özellikleri:

1. **Negatif ve Pozitif Değerler:** **`ssize_t`**, hem negatif hem de pozitif tam sayı değerlerini temsil edebilir. Başarılı işlemlerde, pozitif değerler dönerken, hata durumlarında genellikle -1 gibi negatif değerler döner.

2. **Dosya Okuma ve Yazma İşlemleri:** **`ssize_t`**, özellikle **`read`** ve **`write`** işlevleri gibi dosya okuma ve yazma işlemlerinin sonuçlarını döndürmek için kullanılır. Bu işlevler, işlem sırasında okunan veya yazılan bayt sayısını **`ssize_t`** ile ifade eder.

3. **Hata Kontrolü:** Hata durumlarında **`ssize_t`** genellikle -1 değerini alır. Bu, işlemin başarısız olduğunu ve bir hata kodunun ayarlandığını gösterir. Hata kodu, işlemin neden başarısız olduğunu belirtir ve **`errno`** değişkeni üzerinden elde edilebilir.

4. **Taşma ve Bellek Verimliliği:** **`ssize_t`**, işlemler sırasında büyük veri miktarlarını temsil edebilir ve taşma sorunlarına karşı koruma sağlar. Aynı zamanda veri işleme sırasında bellek verimliliğini artırır.

**size_t ile farkı :   `size_t` işaretsiz bir veri türüdür,(unsigned) yani negatif değerleri temsil etmez. Bu nedenle `size_t`'yi negatif değerlerle karşılaştırmak veya negatif değerlerle kullanmak hatalıdır. `ssize_t` ise işaretli bir veri türüdür (signed) ve hem pozitif hem de negatif değerleri temsil edebilir.**

- **`size_t`**: **`size_t`**, özellikle bellek tahsis etme (malloc, calloc vb.) ve bellek boyutlarını temsil etme işlemleri için kullanılır. Pozitif tamsayı değerlerini temsil eder ve genellikle bellek ile ilgili işlemlerde boyutları ifade etmek için kullanılır. Bu tür, dizilerin veya bellek bloklarının boyutlarını ve indislerini saklamak için idealdir.

- **`ssize_t`**: **`ssize_t`**, dosya okuma ve yazma işlemlerinin sonuçlarını temsil etmek için kullanılır. Hem pozitif hem de negatif tamsayı değerlerini temsil edebilir ve genellikle dosya işleme işlemlerinin sonuçlarını saklamak için kullanılır. Bu tür, **`read`** ve **`write`** işlemleri gibi dosya işleme işlemlerinin sonuçlarını döndürmek için idealdir.

