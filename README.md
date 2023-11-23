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

**`get_next_line`** fonksiyonu, özellikle büyük veri dosyalarını satır satır okuma veya metin tabanlı protokollerle iletişim kurma gibi senaryolarda oldukça kullanışlıdır. Bu fonksiyon, kullanıcıya belirtilen dosya veya dosya tanımlayıcısından bir satır okuma yeteneği sunar ve bellek sızıntılarına karşı korur.
