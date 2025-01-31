# Film Rehberi Projesi

Film Rehberi, kullanıcıların film önerileri alabileceği ve çeşitli film bilgilerine kolayca erişebileceği bir Python projesidir. Bu proje, kullanıcıların tercihleri doğrultusunda film türleri, puan aralıkları, çıkış yılları, favori filmleri ve daha fazlası hakkında öneriler almasına olanak tanır. Ayrıca, kullanıcılar herhangi bir film hakkında temel bilgilere ulaşabilir.

## Özellikler

Proje, aşağıdaki özellikleri sunar:

1. **Film Türüne Göre Öneri**: Kullanıcı, belirli bir film türünü (örneğin: Drama, Komedi, Aksiyon) girerek bu türdeki rastgele bir film önerisi alır.
2. **Puan Aralığına Göre Öneri**: Kullanıcı, bir puan aralığı girer (1.0 ile 5.0 arasında) ve bu aralığa uygun rastgele bir film önerisi alır.
3. **Film Temel Bilgileri**: Kullanıcı, bir film adı girer ve bu film hakkında temel bilgileri alır (başlık, tür, yıl).
4. **Belirli Yılda Çıkan Filmler**: Kullanıcı, bir yıl girer ve o yıl içinde çıkan filmleri görüntüler (maksimum 20 film).
5. **Sevdiğiniz Filmlerle Öneri**: Kullanıcı, 3 sevdiği filmi girer ve bu filmlerle en iyi eşleşen filmler arasında öneri alır.
6. **Veri Kaynağı**: Bu proje, MovieLens veri setini kullanmaktadır.

## Kullanım Senaryoları

Projenin temel amacı, film arayışı içinde olanlara yönelik önerilerde bulunmaktır. Kullanıcılar aşağıdaki senaryolarda bu sistemden faydalanabilirler:

- **Film Türüne Göre Öneri**: Kullanıcı belirli bir türde film arayışı içindeyse (örn. "Aksiyon" veya "Komedi") bu türdeki rastgele bir film önerisi alabilir.
- **Puan Aralığına Göre Film Arama**: Belirli bir puan aralığında (örneğin 4.0 ile 5.0 arasında) yer alan filmleri arayan kullanıcılar, bu aralığa uyan bir film önerisi alabilirler.
- **Favori Filmlere Göre Öneri**: Kullanıcılar, sevdikleri üç filmi girerek, bu filmlere benzer türde başka bir film önerisi alabilirler.
- **Film Bilgilerini Görüntüleme**: Kullanıcılar, belirli bir film hakkında ayrıntılı bilgi almak için film adı girerek, bu filmle ilgili temel bilgilere ulaşabilirler.

## Kurulum

Projeyi çalıştırabilmeniz için bilgisayarınızda Python 3.x ve bazı kütüphanelerin kurulu olması gerekmektedir. Aşağıdaki adımları takip ederek projeyi kurabilirsiniz.

### 1. Python ve Gerekli Kütüphaneler

Projeyi çalıştırmadan önce gerekli Python kütüphanelerini yüklemeniz gerekecek. Bunun için terminal veya komut satırında aşağıdaki komutları sırasıyla çalıştırın:

```bash
pip install pandas fuzzywuzzy python-Levenshtein
Bu kütüphaneler, verileri işlemek (pandas) ve metin eşleşmesi sağlamak (fuzzywuzzy) için gereklidir.

2. Veri Seti
Proje, MovieLens veri setini kullanmaktadır. Bu veri setini MovieLens sitesinden indirmeniz gerekiyor.

movie.csv: Filmlere ait temel bilgileri içeren veri seti
rating.csv: Kullanıcılar tarafından yapılan film puanlamalarını içeren veri seti
Bu dosyaları indirip, proje dizinine yerleştirin.

3. Projeyi Çalıştırma
Projeyi çalıştırmak için terminal veya komut satırında aşağıdaki komutu yazabilirsiniz:

python film_rehberi.py
Bu komut, projenin ana menüsünü çalıştıracak ve kullanıcıyı yönlendirecektir.

Kullanım
Projeye girdikten sonra kullanıcılar aşağıdaki seçeneklerden birini seçebilirler:

1. Film Türüne Göre Öneri Al
Kullanıcı, belirli bir film türünü (örneğin: "Drama", "Komedi", "Aksiyon") girerek, o türde rastgele bir film önerisi alır.

Örnek:
Lütfen bir film türü girin (örneğin: Drama, Comedy, Action): Drama
Rastgele Drama filmi önerisi: The Shawshank Redemption
2. Puan Aralığına Göre Rastgele Film Önerisi Yap
Kullanıcı, belirli bir puan aralığı girer (örneğin 4.0 ile 5.0 arasında) ve bu aralığa uygun rastgele bir film önerisi alır.

Örnek:

Minimum puanı girin (1.0 ile 5.0 arasında): 4.0
Maksimum puanı girin (1.0 ile 5.0 arasında): 5.0
Rastgele 4.0-5.0 arası puanlanan film önerisi: Inception
3. Filmin Temel Bilgilerini Al
Kullanıcı, bir film adı girer ve o film hakkında temel bilgileri alır.

Örnek:
Lütfen film adını girin: The Matrix
🎬 Film Adı ve Yılı: The Matrix
📌 Tür: Action|Sci-Fi
🗓️ Yıl: 1999
4. Belirtilen Yılda Çıkan Filmleri Göster (max 20)
Kullanıcı, bir yıl girer ve o yıl içinde çıkan filmleri görüntüler. Maksimum 20 film gösterilir.

Örnek:
Lütfen bir yıl girin: 2000
2000 yılında çıkan filmler (max 20):
- Gladiator
- Cast Away
- Memento
...
5. Sevdiğiniz Filmlerle Öneri Al
Kullanıcı, 3 favori film girer ve bu filmlerle en iyi eşleşen filmler arasında öneri alır.

Örnek:
Lütfen tam olarak 3 sevdiğiniz filmi girin.
1. Film: The Shawshank Redemption
2. Film: The Godfather
3. Film: Inception

🎥 Sevdiğiniz filmlere göre önerim:
🔎 Önerilen Filmler:
1. Fight Club
2. The Dark Knight
3. Pulp Fiction
...
6. Çıkış
Programdan çıkmak için bu seçeneği kullanabilirsiniz.


##Verileri şu kaynaktan edindim https://www.kaggle.com/datasets/grouplens/movielens-20m-dataset/code
Ödevi Google Colab üzerinde sorunsuz çalıştırdım.
